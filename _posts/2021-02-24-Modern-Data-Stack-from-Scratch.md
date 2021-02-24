# Objective

Ever since I did Data Science (DS) analytics for an AI start-up and put in charge of winning Instacart over, I wanted to dig 
deeper into the data I was given. I realzied as I was presenting metrics to stakeholders at Instacart, I was not 100%
confident with what I was giving them. And it had to do with not really understanding where all the numbers were coming
from. So I made sure that in my next data project, I would figure out more Data Engineering (DE)!

One set back was that I knew of the common platforms used in order to build data infrastructure-- Fivetran, Stitch, Snowflake.
They were perfect for enterprise scale and budget, but not for someone who just wanted to run something local to get a foundation
for DE. Enter PostgreSQL, Meltano (Singer + DBT) and Superset. They are free to use, can be run on a local machine and are used at 
the Enterprise scale as well. 

# Data Source

Given that the data stack chosen to be built was meant to perform just like Enterprise level data stack, had to go after data
that was similar to what big companies deal with. So thought about continuous data that was dynamic and relevant. Hence, chose
election data that gets updated continuously. This simulates closely user data that would stream into warehouses continuously/
regularly scheduled workflows that would collect records of users' fluctuating behaviors, which is similar to people's voting 
choices. So there is the longitudinal aspect with the exception that the data is not in real-time. 

Data collected was from [MIT Election Data + Science Lab](https://electionlab.mit.edu/data). Specifically, got historical US
elections results for the House of Representatives, the Senate and the Presidential Candidates in the Electoral College.

# Applications

1. [PostgreSQL](https://www.postgresql.org/download/) - SQL client
2. [TablePlus](https://tableplus.com/) - GUI for SQL client
3. [Python3](https://www.python.org/) - most components in the stack depend on this
4. [Sublime](https://www.sublimetext.com/) - Scripts editor

# Extraction and Load (Meltano)

Started a vitual environment.

  mkdir ds4fnp
  cd ds4fnp                   
  python3 -m venv .venv       # create your virtual environment
  source .venv/bin/activate   # activate your virtual environment

# Transformation 

# Visualization

In the end, was able to build a data warehouse (PostgreSQL), extract and load data in to the warehouse (Meltano) and create
visualizations to present insights as a dashboard (Superset). 
