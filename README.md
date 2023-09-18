
# django_allauth - Social Authentication with Django

**django_allauth** is a Django project that demonstrates the use of the `django-allauth` library for handling social authentication, registration, and account management in Django applications.

## Features

**django_allauth** leverages the power of `django-allauth` to provide the following features for your Django project:

1. **Authentication:**
   - User login via username and password.
   - User logout.
   - Password change functionality.
   - Password reset via email.
   - Password reset with a reset key.

2. **Registration:**
   - User registration with email confirmation.
   - Social authentication using popular platforms like Google, Facebook, Twitter, and more.
   - Registration with social authentication providers.
   - Resending confirmation emails for unconfirmed accounts.
   
3. **Account Management:**
   - User account settings page.
   - Ability to manage email addresses associated with the user's account.
   - Management of social account connections (if social authentication is enabled).
   - Disconnecting social accounts from the user's profile.
   - Handling inactive users.

4. **Social Authentication:**
   - User registration and login via social authentication providers.
   - Seamless integration with OAuth2 and OpenID Connect.
   - Social account connection management.
   - Disconnecting social accounts.

## Requirements

To use **django_allauth** and leverage the features provided by `django-allauth`, make sure you have the following requirements installed:

- Python 3.x
- Django 3.x (or the version compatible with your project)
- `django-allauth` package: You can install it using pip.
- Database (e.g., SQLite, PostgreSQL, MySQL) for storing user data.
- Web server (e.g., Gunicorn, uWSGI) for hosting your Django application.

## Installation and Setup

1. Clone or download the **django_allauth** project repository to your local machine.

2. Create a virtual environment and activate it:

   ```shell
   python -m venv venv
   source venv/bin/activate
   ```
---

Here are the steps to create credentials (Secret ID and Secret Key) for different social authentication providers such as Google, GitHub, Facebook, and Twitter when using the `django-allauth` library:

### Google

1. Go to the [Google Developers Console](https://console.developers.google.com/).

2. Create a new project if you don't have one already.

3. In the dashboard, click on "Create credentials" and select "OAuth client ID."

4. Choose "Web application" as the application type.

5. Enter a name for your OAuth client ID.

6. Under "Authorized redirect URIs," add the redirect URL for your Django project. For local development, it might be something like `http://localhost:8000/accounts/google/login/callback/`.

7. Click "Create" to generate your OAuth client ID and secret.

8. Copy the client ID and secret, and add them to your Django project's settings. In your `settings.py` file, add:

   ```python
   SOCIALACCOUNT_PROVIDERS = {
       'google': {
           'APP': {
               'client_id': 'YOUR_CLIENT_ID',
               'secret': 'YOUR_CLIENT_SECRET',
           }
       }
   }
   ```

### GitHub

1. Go to [GitHub Developer Settings](https://github.com/settings/developers).

2. Click on "New OAuth App."

3. Fill in the required information:
   - Application name
   - Homepage URL (your Django project's URL)
   - Authorization callback URL (e.g., `http://localhost:8000/accounts/github/login/callback/` for local development)

4. Click "Register application."

5. You will be provided with a "Client ID" and "Client Secret." Copy these.

6. In your Django project's settings (`settings.py`), add:

   ```python
   SOCIALACCOUNT_PROVIDERS = {
       'github': {
           'APP': {
               'client_id': 'YOUR_CLIENT_ID',
               'secret': 'YOUR_CLIENT_SECRET',
           }
       }
   }
   ```

### Facebook

1. Go to the [Facebook Developers](https://developers.facebook.com/) website.

2. Create a new app and choose "For Everything Else."

3. Complete the setup wizard by providing a display name, email, and other requested information.

4. In the app dashboard, go to "Settings" > "Basic."

5. Find the "App ID" and "App Secret" fields, and click on "Show" to reveal the secret.

6. Add your website's URL under "App Domains" and "Website URL."

7. Under "Facebook Login," add the valid OAuth redirect URIs. For local development, it might be something like `http://localhost:8000/accounts/facebook/login/callback/`.

8. In your Django project's settings (`settings.py`), add:

   ```python
   SOCIALACCOUNT_PROVIDERS = {
       'facebook': {
           'APP': {
               'client_id': 'YOUR_APP_ID',
               'secret': 'YOUR_APP_SECRET',
           }
       }
   }
   ```

### Twitter

1. Go to the [Twitter Developer Dashboard](https://developer.twitter.com/en/apps).

2. Click on "Create App."

3. Fill out the required fields, including the "App name," "Application description," and "Website URL."

4. Under "Authentication settings," add the callback URL. For local development, it might be something like `http://localhost:8000/accounts/twitter/login/callback/`.

5. Read and accept the Developer Agreement, then click "Create."

6. In your app's dashboard, navigate to "Keys and Tokens."

7. Copy the "API Key" and "API Secret Key."

8. In your Django project's settings (`settings.py`), add:

   ```python
   SOCIALACCOUNT_PROVIDERS = {
       'twitter': {
           'APP': {
               'client_id': 'YOUR_API_KEY',
               'secret': 'YOUR_API_SECRET_KEY',
               'key': '',
           }
       }
   }
   ```

Remember to keep your credentials secret and do not share them publicly. These steps should help you set up social authentication for your Django project using the `django-allauth` library.

---

So on for more provider....................

---

3. Install the project dependencies using pip:

   ```shell
   pip install -r requirements.txt
   ```

4. Configure your Django project's settings to include `allauth` in your `INSTALLED_APPS` and set up authentication backends.

5. Configure `AUTHENTICATION_BACKENDS` in your settings to include `allauth` backends.

6. Run migrations to create the necessary database tables:

   ```shell
   python manage.py migrate
   ```

7. Customize the `allauth` templates and views as needed to fit your project's design and user experience.

8. Start your Django development server:

   ```shell
   python manage.py runserver
   ```

9. Access the **django_allauth** project in your web browser, and you can start using the social authentication, registration, and account management features.

## Customization

You can customize the behavior and appearance of `django-allauth` in your Django project by modifying templates, views, and settings. Refer to the official `django-allauth` documentation for detailed customization options.


## Author

- RAKESH KUMAR

---


