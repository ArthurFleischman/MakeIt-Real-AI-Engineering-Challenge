# MakeIt Real – AI Engineering Challenge

## TASK 1 Airflow Pipeline

1. Implement an Airflow DAG that performs the following operations:

2. Load a CSV file into the PostgreSQL database.

3. Create an aggregated table called user_outfit_profile containing:
    + user_id
    + preferred_upper_garment
    + preferred_lower_garment
    + garment_style
    + garment_color


## TASK 2 – FastAPI Service + GenAI

1. Fastapi python api

### Routes

1. **GET /user/{user_id}**
    
    example:
    ```json
    {
     "user_id": 42
    }
    ```
    expected behavior:
    + Returns the user profile from the user_outfit_profile table 
    
    ---
2. **POST /generate-image**
    
    example:
    ```json
    {
     "user_id": 42
    }
    ```
    expected behavior:
    + Retrieve the user profile from the database
    + Build a prompt using the garments in the profile
    + Generate an image using the generative model
    + Return the image or the URL of the generated image
    
    ---
## Technologies included

+ python/fastapi
+ docker
+ airflow(container)
+ postgresql(container)
