# What is Akto? 
Open source API Security platform

# How to install Akto on your laptop?
1. Create a directory named `owasp-akto`
2. Copy these 2 files in your directory
  - You can get `docker-compose.yml` file from here - https://github.com/akto-api-security/akto/blob/master/docker-compose.yml
  - You will also need a `docker.env` file from here - https://github.com/akto-api-security/akto/blob/master/docker.env
3. Run `docker-compose up -d`
4. Open http://localhost:9090 on your browser

# Sign up
1. Click on the "sign-up" button on the screen if you are running it for the first time else simply login.
2. Enter an email / password and signup 
3. Login with the same credentials
4. If an onboarding popup comes, you can skip it. We are going to be ninjas on Akto by end of workshop any way :) 
   
# Get API Inventory - Juiceshop
1. You should already see a Juiceshop inventory with ~19 APIs or so.
2. But lets just create our own. Go to `Quick start` > `Connect traffic data` > `Burpsuite` and follow the steps
3. Download AktoBurp extension from the link on the dashboard
4. In case the link doesn't work, download from here - https://github.com/akto-api-security/akto/blob/master/apps/dashboard/src/main/resources/Akto.jar
5. Go to Akto plugin > Options and check all the details. If you have downloaded it from the github link, then you will have to enter the IP, collection name and API key manually too.
6. Go to Proxy and click on `Open browser` button.
7. Hit *https://juiceshop.akto.io* (or any other juiceshop hosting)
8. Do a signup > login > add a review > edit review > add to basket > checkout > add quantity > add credit card > add address > pay > add a complaint > add a feedback etc. etc. etc.
9. You should see 70+ APIs in your inventory now.

# Add your own data type

# Explore ChatGPT cases

# Add test cases

