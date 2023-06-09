# ImmoEliza API
This repository hosts an API to build on Docker. It is ready for render, with which you can directly host this repository.
This API is a simple implementation of a linear-regression price-prediction model for houses and apartments in Belgium.
Providing at the very least a living area and a zipcode, and possibly information about a garden, a swimming pool, or a building condition for instance, a post request to the /predict/ endpoint returns a price prediction.
# API:
The API answers to two endpoints:
## /
To a get request, answers "alive" if the server is running.
## /predict/
To a get request, answers with a message detailing how to properly post data to get a price prediction.
To a post request, providing data with the following format:  
- with OPTIONAL denoting an optional input (area and zip_code are required)  
- - several strings meaning you have to pick one out of them:    
     
{  

 "area": int,    
 "zip_code": int,  
   
 "property_type": OPTIONAL "APARTMENT", "HOUSE", "OTHERS",  
 "rooms_number": OPTIONAL int,  
 "land_area": OPTIONAL int,  
 "garden": OPTIONAL false, true  
 "garden_area": OPTIONAL int,  
 "equipped_kitchen": OPTIONAL true, false  
 "full_address": OPTIONAL "string",  
 "swimming_pool": OPTIONAL false, true  
 "furnished": OPTIONAL false, true  
 "open_fire": OPTIONAL false, true  
 "terrace": OPTIONAL false, true  
 "terrace_area": OPTIONAL int,  
 "facades_number": OPTIONAL int,  
 "building_state": OPTIONAL "NEW", "GOOD", "TO RENOVATE", "JUST RENOVATED","TO REBUILD"  
}  
    
    The API gives an output such as:  
    {"prediction" : prediction}  

    
