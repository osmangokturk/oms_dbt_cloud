# Quick About
A demo for E2E dbt Cloud project  with Snowflake, GitHub & PowerBI

![Alt text for the image](picture1.jpg)

# dbt Cloud  account creation, connection to Snowflake

Visit dbt cloude web site and create an account with your email and password. Then create a connection that will use the  credentials of snowflake database, warehouse, database, warehouse.... 
Once the connection is saved. 
- Introduce your GitHub repo  to DBT Cloud. This process may invoke several  authentication   processes to make a connection between dbt and GitHub. 

## creation of the first dbt project

- on dbt cloud GUI, on the left, press the "Initialize new DBT project" button. 
This will create a project folder structure similar to what we have on dbt core (CLI). 

- You can create some models for just testing the dbt Cloud. 
- dbt cloude provide bunch of new menus, features to use  dbt as gui. Like build +test+Upstream (or Downstream).  These are equivalent to commands with various options and flags in CLI

- These commands or features will create tables or run tests. You will be able to see the result either on the dbt or on the snowflake 

## Committing to the repo 

- dbt cloude provide  buttons to commit or to create new branches for the new features. Once the work is committed to the ain or the feature branch, then  on the github we can merge the branche to the main via pull requests. 

# Using the created table or view for BI 
- We choose Power BI as the tool to  for BI. 
- In the get data menu on PoserBI, we select Snowflake, and we use credentials as server and warehouse. An authentication method like Single Sign-On will provide the connection between Snowflake and Power BI. 
- Once the connection is established, you can choose any table or  view from Snowflake to import/DirectQuery into Power BI.  
- These are types of importing data  into Power BI. 
- Once the data is  in PowerBI then we can create the charts or dashboards. 

