I have been wanting to explore streamed events post-ingestion. Tracking a customer's user behavior in real-time is extremely valuable because it allows you to see 
instant reponse to a new product feature or even intervene immediately when you see a customer possibly churn.

![sitemap](/assets/images/sitemap.png)

Though this is the standard data that comes into a company's system, testing a data pipeline's transformation and BI layer does not need code committed to 
Production. This is where mock event data comes in. In order to create some, I knew I had to find some online or create some on my own. And I ended up bumping into
this wonderful [post](https://towardsdatascience.com/simulating-web-events-7199bf8afcfd). 

The differentiator in this data was that random event data was created that simulated more real-life behavior probabilities. For example, the likelihood that a customer clicks on the Cart page, will not be the same likelihood that a customer click on Home page. A library called fake_web_events was used to generate the mock web events. Within the library, the Simulation function has user_pool_size and sessions_per_day arguments to define a certain population. Also, Simulation's run method allows you to define event time duration in seconds.

Here is a sample event:

![event](/assets/images/fake_event.png)

And in order to load the data into my local Postgres database, sqlalchemy library was called. What it did was help
create the structure in order to load and store the mock data. It helped create the table, column and data types. Script is [here](https://github.com/mindyng/2021-Projects/blob/main/events_to_postgres%20copy.py). From here, after connecting to database and creating mock data, events were loaded into postgres database.

From here, I wanted to see if I could create different business logic models using dbt. So I created my virtual env, created my dbt folder, initiated by dbt project, wrote my SQL queries and built the tables out to do business intelligence on. The follow is: 

my projects.yml file: 

![profiles](/assets/images/profiles.png)

dbt_project.yml file:

![dbt_project](/assets/images/dbt_project.png)

and my DAG/Lineage Graph from running:

``` 
dbt run docs
dbt docs serve
```
![DAG](/assets/images/DAG.png)

Finally, I was able to use the metadata to Tableau and create a dashboard showing hourly pageviews as well as the most hits per page. 

![tableau](/assets/images/tableau.png)


And as expected, there is an hourly cyclical trend as well as huge hits concentrated in home, product A and product B pages. Thus, being able to track customer behavior allows us to closely monitor whether or not business is successful at providing solution to customers at a granular level. 
