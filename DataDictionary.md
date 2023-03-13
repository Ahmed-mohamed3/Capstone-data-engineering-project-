# DEND Capstone

# **Data Dictionary Dimension Tables**
## US Demographics Dimension Table
 * id: record id 
 * state_code: US state code
 * city: name of the city
 * state: US State where city is located
 * median Age: Median age of the population
 * male population: Count of male population
 * Female Population: Count of female population 
 * Total Population: Count of total population
 * Number of veterans: count of total veterans
 * foreign born: Count of residents of the city that were not born in the city
 * Average house size: Average city household size
 * Race: Respondent race
 * count: Count of city's individual per race
 
 
## Immigration Calendar Dimension Table
 * id: primary key
 * arrdate: arrival date into US
 * arrival_year: arrival year into US
 * arrival_month: arrival Month
 * arrival_day: arrival Day 
 * arrival_week: arrival Week
 * arrival_weekday: arrival Weekday
 
## Visa Type Dimension Table
 * visa_type_key: Unique id for each visa issued
 * visa_type: Name of Visa 
 

## Countries dimension table
 * country_code: long (nullable = true) - Country code
 * country_name: string (nullable = true) - Country name
 * average_temp: Average temperature of country
 


# Fact Table (Inmigration Registry)
    * record_id: Unique record ID
    * country_residence_code: 3 digit code for immigrant country of residence
    * visa_type_key: A numerical key that links to the visa_type dimension table
    * state_code: US state of arrival
    * i94yr: 4 digit year
    * i94mon: Numeric month
    * i94port: Port of admission
    * arrdate: Arrival Date in the USA
    * i94mode: Mode of transportation (1 = Air; 2 = Sea; 3 = Land; 9 = Not reported)
    * i94addr: USA State of arrival
    * depdate: Departure Date from the USA
    * i94bir: Age of Respondent in Years
    * i94visa: Visa codes collapsed into three categories
    * count: Field used for summary statistics
    * dtadfile: Character Date Field - Date added to I-94 Files
    * visapost: Department of State where where Visa was issued
    * occup: Occupation that will be performed in U.S
    * entdepa: Arrival Flag - admitted or paroled into the U.S.
    * entdepd: Departure Flag - Departed, lost I-94 or is deceased
    * entdepu: Update Flag - Either apprehended, overstayed, adjusted to perm residence
    * matflag: Match flag - Match of arrival and departure records
    * biryear: 4 digit year of birth
    * dtaddto: Character Date Field - Date to which admitted to U.S. (allowed to stay until)
    * gender: Non-immigrant sex