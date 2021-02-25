# Objective

Ever since I did Data Science (DS) analytics for an AI start-up and put in charge of winning Instacart over, I wanted to dig 
deeper into the data I was given. I realzied as I was presenting metrics to stakeholders at Instacart, I was not 100%
confident with what I was giving them. And it had to do with not really understanding where all the numbers were coming
from. So I made sure that in my next data project, I would figure out more Data Engineering (DE)!

One set back was that I knew of the common platforms used in order to build data infrastructure-- Fivetran, Stitch, Snowflake.
They were perfect for enterprise scale and budget, but not for someone who just wanted to run something local to get a foundation
for DE. Enter PostgreSQL, Meltano (Singer), DBT and Superset. They are free to use, can be run on a local machine and are used at 
the Enterprise scale as well. 

# Data Source

Given that the data stack chosen to be built was meant to perform just like Enterprise level data stack, had to go after data
that was similar to what big companies deal with. So thought about continuous data that was dynamic and relevant. Hence, chose
election data that gets updated continuously. This simulates closely user data that would stream into warehouses continuously/
regularly scheduled workflows that would collect records of users' fluctuating behaviors, which is similar to people's voting 
choices. So there is the longitudinal aspect with the exception that the data is not in real-time. 

Data collected was from [MIT Election Data + Science Lab](https://electionlab.mit.edu/data). Specifically, got historical US
elections results for the House of Representatives, the Senate and the Presidential Candidates in the Electoral College.

# Applications Needed:

1. [PostgreSQL](https://www.postgresql.org/download/) - SQL client
2. [TablePlus](https://tableplus.com/) - GUI for SQL client
3. [Python3](https://www.python.org/) - most components in the stack depend on this
4. [Sublime](https://www.sublimetext.com/) - Scripts editor

# Extraction and Load (Meltano)

Created local project folder and starting a virtual environment.

```
mkdir ds4fnp
cd ds4fnp                   
python3 -m venv .venv       # create your virtual environment
source .venv/bin/activate   # activate your virtual environment
```
Meltano helps extract away all the custom python code needed when doing tradional ETL. What it does is pulls from data sources (taps) and puts into data load destinations (targets). 

Installed Meltano and created a new project by:

```
pip3 install meltano
meltano init ./meltano
cd ./meltano
```

After initiating Meltano, there were several subdirectories created along with a meltano.yml file. This is where most of the Extraction and Loading work was done along with working with Meltano's CLI. For more information, this is [Meltano's documentation](https://meltano.com/docs/project.html#projects) to understand how configuration files work. 

## Configuring Sources for Extraction

We will be using plugin called [tap-spreadsheets-anywhere](https://meltano.com/plugins/extractors/spreadsheets-anywhere.html#getting-started). It is able to pull data from CSV files and Excel spreadsheets on cloud and local storage. Ran the following command in meltano CLI to add extractor to my meltano project:

```
meltano add extractor tap-spreadsheets-anywhere
```
When this was completed, config section was added to meltano.yml. Then added manually into the [file](https://github.com/mindyng/2021-Projects/blob/main/modern_data_stack/meltano/meltano.yml) nested items under tables. URL's were added to 3 different datasets from the MIT site:

* https://dataverse.harvard.edu/api/access/datafile/4202836
* https://dataverse.harvard.edu/api/access/datafile/4300300
* https://dataverse.harvard.edu/api/access/datafile/4299753

## Configuring Targets for Loading

Singer target/destination was specified for CSV files to be loaded into PostgreSQL database. 

PostgreSQL database and persmissions created using psql (CLI):

```
#via initial user login as postgres with pw 'postgres' using command: sudo -u postgres psql

create database ds4fnp;
\connect ds4fnp;
create role ds4fnp with login password 'ds4fnp';
grant all privileges on database ds4fnp to ds4fnp;
```
Once this is complete, made sure that meltano.yml script changed under config:

config:
      user: ds4fnp
      password: "ds4fnp"
      host: 127.0.0.1
      port: 5432
      dbname: ds4fnp
      
then ran to add loader as PostgreSQL database: 

```
meltano add loader target-postgres --variant meltano
```

# Transformation 

# Visualization

In the end, was able to build a data warehouse (PostgreSQL), extract and load data in to the warehouse (Meltano) and create
visualizations to present insights as a dashboard (Superset). 
