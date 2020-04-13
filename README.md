**Bank Holiday Temperatures**

###### virtualenv

It is recommended to run the scripts below within a python virtualenv.

To install and use virtualenv:

`$ python3 -m pip install --user --upgrade virtualenv`

`$ mkdir exercises`

`$ cd exercises`

`$ source env/bin/activate`

`$ git clone https://github.com/williamhargrove/assessment.git`

`$ cd assessment`

###### Dependancies

To install required dependancies

`pip install -r requirements.txt`

###### Exercise 1

usage:

`./exercise1.py <place> "<bank holiday>" <year>`

eg

`./exercise1.py Liverpool "Christmas Day" 2019`

returns

`The highest temperature in Liverpool on Christmas Day 2019 was 8.56 Celsius`

`The lowest temperature in Liverpool on Christmas Day 2019 was 1.71 Celsius`


###### Exercise 2

usage:

`./exercise2.py <place> "Bank Holiday"`

eg

`./exercise2.py Liverpool "Good Friday"`

returns

`2020 recorded the highest temperature for Good Friday in Liverpool`

######Improvements and known issues

Known issues
1. When looking up the date of a bank holiday, the first date match is taken from the list of regions returned from the gov.uk portal,
usually giving the england-and-wales data. This would be an issue if a commonly named bankholiday had different dates
per region. To correct for this, when looking up WOEID, this also needs to be mapped to a region, so we would know that
Glasgow is in Scotland and parse this json section.

Improvements
1. Add logging to the script with `logging` module.
2. Separate out URLs into a properties file parsed with `configparser` module.
