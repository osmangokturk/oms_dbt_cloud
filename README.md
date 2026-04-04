# Quick About
A demo for E2E dbt Cloud project  with snowflake, GittHub & PowerBI 

# 1-dbt Cloud  account creation & connection to the snowflake account and GitHub account

- visit dbt cloude web site and create an account with your email and password. 
Then create a connectionw that will use the  credentials of snowflake database, warehouse, database, warehose.... 

- introduce your github repo  to dbt cloude. This process may invoke several  authenticaiton   processes
 to make connection between dbt and github. 

## 1.b) initialization of the first dbt project

- on dbt cloud GUI, on the left presse "initialize new dbt project" button to create the dbt project. 
This will create a project folder structure similar to what we have on dbt core (CLI).

-When you commit and sync the dbt, it will be in syncrony with the main branch of the repo, 
that is to say, if any model is modified in the repo, or a new project folder is introduced it will be able to run it.

## 1.c)  example models
- with initialization of a dbt project folder, an two example model for creation of two models 
 and a schema config  for descriptions and  testing. 
- dbt cloude provide bunch of new menus and features to use  dbt. Like buil +test+Upstream (or Dwonstream). 
 These are equivalent to commands with various options and flages in CLI

- these commands or features will created tables or run tests .
You will be able to see the result either on the dbt or on the snowflake, 
While dbt Core shows results via CLI logs and artifacts (target/artifact run_sresult.json) and documentation site (dbt docs generate).

-first model to create a table of two rows that is created with two SELECT statements with UNION ALL. 
-one row is on purpose populated with NULL value in id. 
-it is materialized as table. 

- second model has no materialized statement, hence by default it is view. 
- as this refer to the table  from first model, this will be visible from lineage map. 

## 1.d) schema config file:

- The schema type config file contains two tests for the id column of the table,
These tests are built-in tests unique an not-null.

## 1.e) Build, test and  run  options  & Upstream or Downstream 

-Downstream measn  from firstmodel then do the second model so on, while Upstream means  if you are starting from second, dbt should  build previous models as well. 
-with build+model (Downstream), the first model is built, but  if any test for the first model is failed, the second model is not built. 
However, this is true only for build, which runs  models + test. if "run" is selected, all the models will be created regardless of the test results. 

-with test model (Downstream), models are not built but tests are run.  

# 2 - GITHUB:  Commiting to or Syncing with  the repo 

- dbt cloude provide  buttons to commit or to create new branches for the new features.
 Once the work is committed to the main or the feature branch, then  on the github we can
  merge the branche to the main via pull requests. 
-

# 3- Importing tables from Snowflake into PowerBI 
- we choose PowerBI as the tool to  for BI. 
- in the get data menu on PoserBI, we select Snowflake and we use credentials as server and warehouse. An authentication method like Single Sign-On will provide the connection beween snowflake and PowerBI. 
- Once the connection is established you can choose any table or  view fro msnowflake to import/DirectQuery into PowerBI.  
- these are type of importing data  into PowerBI. 
- once data is  in PowerBI then we can create the charts or dashboards. 


