# MySQL connection in Python
This project basically showcase how to make a connection to MySQL database in Python and answered some basic questions.

## Getting Started

Follow these instructions to setup your local environment and test the project. 

### Prerequisites

You have to install the following software to get started:
- MySQL workbench from here: https://dev.mysql.com/downloads/workbench/
- Juputer notebook as part of the anaconda distribution: https://www.anaconda.com/download

## Running the tests

Once you are done setting up MySQL workbench and Jupyter notebook. Fire up Jupyter notebook follow the steps:

#### Install pymysql to be able to establish connection with MySQL database.
```
pip install pymysql
```

#### Import all the needed libraries
```
import pandas as pd
from sqlalchemy import create_engine
import pymysql
```

#### Create connection to your database
```
#create engine
engine = create_engine('mysql+pymysql://root:password@localhost/vgsales2016')
# connection string
conn = engine.connect()
```

#### Load data
Now that you have created a connection, you can proceed to querying the table of your choice like so.
```
df = pd.read_sql("SELECT * FROM `vgsales-2016`", conn)
print(df.shape)
# display data columns
df.head(2)
```

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
