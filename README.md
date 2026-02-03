<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>

<body>

# Tutorial

## Prerequisites
Before starting, ensure you have a Facebook Page. If you don't have one, create a Facebook Page first.

## Installation
Ensure you have Node.js installed, then run:

```bash
npm install express body-parser fs axios
```

## Step 1: Go to Facebook Developers
1. **Navigate to Facebook Developers:**
   - Open your web browser and go to [developers.facebook.com](https://developers.facebook.com).

2. **Create a Developer Account (if you don’t have one):**
   - Log in with your Facebook credentials and follow the prompts to set up a developer account.

## Step 2: Create an App
1. **Create an App:**
   - Click on "My Apps" in the top-right corner.
   - Select "Create App".
   - Choose "Business" as the app type.
   - Fill out the required details such as the app display name and contact email, then click "Create App ID".

## Step 3: Add the Messenger Product
1. **Set Up Messenger:**
   - In the left sidebar of your app's dashboard, click on "Add Product".
   - Locate "Messenger" and click the "Set Up" button.

## Step 4: Connect Your Facebook Page
1. **Generate a Page Access Token:**
   - Scroll to the "Access Tokens" section.
   - Click on "Add or Remove Pages".
   - Follow the prompts to connect your Facebook Page.
   - Once connected, click "Generate Token" and copy the token for later use.

## Step 5: Set Up Webhooks
1. **Configure Webhooks:**
   - Scroll down to the "Webhooks" section in Messenger settings.
   - Click "Setup Webhooks".
   - Enter the following details:
     - **Callback URL:** `https://your_hosting.site/webhook`
     - **Verify Token:** `pagebot-v3`
   - Subscribe to the following fields:
     - `messages`
     - `messaging_optins`
     - `messaging_postbacks`
   - Click "Verify and Save".

## Step 6: Add Page Subscriptions
1. **Subscribe to Page Events:**
   - Under "Webhooks", navigate to "Page Subscriptions".
   - Select the page you connected earlier.
   - Ensure that `messages`, `messaging_optins`, and `messaging_postbacks` are selected.

## Step 7: Retrieve Your Page Access Token
1. **Copy the Token:**
   - Go back to "Access Tokens".
   - Copy the generated Page Access Token.

## Step 8: Configure the Bot with the Token
1. **Enter the Token:**
   - Paste the Page Access Token into `configure.json`.

## Step 9: Test Your Messenger Bot
1. **Test Bot Functionality:**
   - Open your Facebook Page.
   - Send a message (e.g., "help") to verify if the bot responds correctly.
   - Ensure that the account used for testing has a role in the app.

**Note:** The bot will only respond to accounts assigned specific roles within the app.

## Step 10: Deploy Your Bot
1. **Deployment Instructions:**
   - Ensure your server is set up with Node.js.
   - Deploy the app to your server or cloud platform (e.g., Heroku, Render, Vercel).

2. **Run Your App:**
   - Navigate to your project directory and install any additional dependencies:
     ```bash
     npm install
     ```
   - Start your server:
     ```bash
     node index.js
     ```
   - To ensure your server restarts when code changes, consider using `nodemon` (optional):
     ```bash
     npm install -g nodemon
     nodemon index.js
     ```

## Adding Roles
1. **Navigate to [developers.facebook.com](https://developers.facebook.com):**
   - Go to [developers.facebook.com](https://developers.facebook.com).

2. **Access Your App:**
   - Log in and navigate to "My Apps".

3. **Select "App Roles":**
   - Find the "App Roles" section in your app's dashboard.

4. **Add Roles:**
   - Click on "Add Role" to start the process.

5. **Define Role Details:**
   - Specify role name and permissions as needed.

6. **Assign Roles to Users:**
   - Assign the role to specific users by providing their name or user ID.

## Credits
- This guide was created by Clarence, Kyle, Christel, and Akira.


**Note:** Feel free to modify this file as needed.

## Contact Information
Feel free to contact **French Clarence Mangigo** if you have any concerns: [https://www.facebook.com/frenchclarence.mangigo.9](https://www.facebook.com/frenchclarence.mangigo.9)

</body>
</html>
