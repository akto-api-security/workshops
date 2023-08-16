# API Security testing Workshop

## What do we need?
1. Create an Akto account
2. Create an API Collection to be tested
3. Start writing test cases

### Step 1: Create an account
Login here - app.akto.io
   
### Step 2: Create an API Collection to be tested
1. You should already see a Juiceshop inventory with ~19 APIs or so.
2. But lets just create our own. Go to `Quick start` > `Connect traffic data` > `Burpsuite` and follow the steps
3. Download AktoBurp extension from the link on the dashboard
4. In case the link doesn't work, download from here - https://github.com/akto-api-security/akto/blob/master/apps/dashboard/src/main/resources/Akto.jar
5. Go to Akto plugin > Options and check all the details. If you have downloaded it from the github link, then you will have to enter the IP, collection name and API key manually too.
6. Go to Proxy and click on `Open browser` button.
7. Hit *https://juiceshop.akto.io* (or any other juiceshop hosting)
8. Do a signup > login > add a review > edit review > add to basket > checkout > add quantity > add credit card > add address > pay > add a complaint > add a feedback etc. etc. etc.
9. You should see 70+ APIs in your inventory now.


### Step 3: Start writing test cases
Documentation for reference - https://docs.akto.io/test-editor/overview

#### 1. Broken Authentication test by deleting auth token entirely!
1. Write a YAML file to remove the Authorization header
2. Try it on GET reviews endpoint, PUT reviews endpoint. 
3. What are the implications?
4. How about PATCH reviews endpoint? 

#### 2. Broken Authentication test by JWT None algo
1. Write a YAML file to hardcode "Authorization" header with a None-token. Alternatively, use Akto's `${auth_context.none_algo_token}`
2. What are the implications?

#### 3. Exposed Prometheus tracking endpoint to public?
1. Try hitting /metrics endpoint?

#### 4. Give a 0-star rating
1. Modify request payload to set the rating to 0

#### 5. Broken Authorization by a diff user
1. Modify the auth token to a diff user and try editing a review? (PATCH review) 

#### 6. Get a list of all feedbacks
1. Given an endpoint to submit a feedback, how do you try and get a list of all feedbacks?

#### 7. Open redirect
1. Why is it a problem?
2. Modify a query parameter this time!

#### 8. XSS 
1. Track-orders endpoint - write data on the screen that was never intended!
2. Modify query-param
3. Validate using regex
