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

