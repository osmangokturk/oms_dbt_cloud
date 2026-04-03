# Quick About
A demo for E2E dbt Cloud project  with snowflake, GittHUB & Power bit_and(

# dbt Cloud  account creation, connection to the snowflake.cortex.complete(

visit dbt cloude web site and create an account with your email and password. Then create a connectionw that will use the  credentials of snowflake database, warehouse, database, warehose.... 
Once the connection is saved. 
- introduce your github repo  to dbt cloude. This process may invoke several  authenticaiton   processes to make connection between dbt and githbu. 

## creation of the first dbt project

- on dbt cloud GUI, on the left presse "initialize new dbt project" button. 
this will create a project folder structure similar to what we have on dbt core (CLI). 

- you can create some models for just testing the dbt cloude. 
- dbt cloude provide bunch of new menus, features to use  dbt as gui. Like buil +test+Upstream (or Dwonstream).  These are equivalent to commands with various options and flages in CLI

- these commands or features will created tables or run tests . you will be able to see the result either on the dbt or on the snowflake 

## Commiting to the repo 

- dbt cloude provide  buttons to commit or to create new branches for the new features. Once the work is committed to the ain or the feature branch, then  on the github we can merge the branche to the main via pull requests. 

# Using created table or view for BI 
- we choose PowerBI as the tool to  for BI. 
- in the get data menu on PoserBI, we select Snowflake and we use credentials as server and warehouse. An authentication method like Single Sign-On will provide the connection beween snowflake and PowerBI. 
- Once the connection is established you can choose any table or  view fro msnowflake to import/DirectQuery into PowerBI.  
- these are type of importing data  into PowerBI. 
- once data is  in PowerBI then we can create the charts or dashboards. 


### Using the starter project

Try running the following commands:
- dbt run
- dbt test


### Resources:
- Learn more about dbt [in the docs](https://docs.getdbt.com/docs/introduction)
- Check out [Discourse](https://discourse.getdbt.com/) for commonly asked questions and answers
- Join the [dbt community](https://getdbt.com/community) to learn from other analytics engineers
- Find [dbt events](https://events.getdbt.com) near you
- Check out [the blog](https://blog.getdbt.com/) for the latest news on dbt's development and best practices
