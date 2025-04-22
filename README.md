## ❄️ Snowflake Streamlit App with Snowpark Python

This project demonstrates how to build and share a data application using **Snowpark for Python**, and **Streamlit** within **Snowflake** — enabling secure user access and streamlined app sharing.

---

### 🚀 Objective

To gain hands-on experience with:

- Snowflake database and user management
- Snowpark for Python (data processing in Snowflake)
- Building and deploying Streamlit apps within Snowflake
- Sharing the app securely with a new Snowflake user

---

### 🧠 Prerequisites

- A **Snowflake Trial Account** (Student version via Azure - East US 2)
  - [Sign up here](https://signup.snowflake.com/)
- Basic SQL and Python knowledge

---

### 🛠️ Project Steps

#### 🔹 Part 1: Setup and Quickstart

1. **Followed Snowflake Quickstart Guide:**\
   [Getting Started with Snowpark for Python and Streamlit](https://quickstarts.snowflake.com/guide/getting_started_with_snowpark_for_python_streamlit/#0)

2. **Dataset Access:**
   
   - Get the dataset from [Snowflake Marketplace](https://app.snowflake.com/marketplace/listing/GZTSZAS2KF7/snowflake-data-finance-economics?_fsi=QrmINNI3)
   - The dataset has been renamed from\
   `FINANCIAL__ECONOMIC_ESSENTIALS` to\
   `FINANCE__ECONOMICS`
  
4. **Completed Steps 1–9 of the Guide:**

   - Setup database and warehouse
   - Develop Snowpark code using Python
       - Import required libraries, setup page config and gain access to current session
       - Load and transform stock price data using several Snowpark DataFrame functions
       - Create interactive visualizations
       - Create a sidebar to select either Daily Stock Performance or Exchange (FX) Rates option
   - Run application

5. **Validated the Streamlit App Runs in Snowsight**

---

#### 🔹 Part 2: User Management – Creating a New User

1. **Logged into Snowsight** using the `ACCOUNTADMIN` role
2. **Executed SQL to Create New User **``**:**

```sql
USE ROLE ACCOUNTADMIN;
CREATE USER RASHMI
    PASSWORD = 'abcde'
    LOGIN_NAME = 'John'
    DISPLAY_NAME = 'John';
```

> ⚠️ Note: This is an example insecure password used only for demonstration. Always use secure credentials in production.

---

#### 🔹 Part 3: Sharing the Streamlit App

1. **Granted Role to New User **:**

```sql
GRANT ROLE ACCOUNTADMIN TO USER John;
```

2. **Shared the Streamlit App** by generating a public URL

3. **Streamlit App URL:**\
   [🔗 View Streamlit App](https://app.snowflake.com/east-us-2.azure/rya46516/#/streamlit-apps/STOCKPRICEFXRATEDATA.PUBLIC.OZU1YFZL2JZO7JGG?ref=snowsight_shared)

---

#### 🔹 Part 4: Verification 

- Logged out of original user session
- Logged in as user `John`
- Successfully accessed the Streamlit app via shared URL

---

### 📌 Learnings

- Leveraged Snowflake’s integrated data science features
- Gained experience in Snowpark-based data processing
- Understood secure app sharing and role-based access control

### Screenshots 


