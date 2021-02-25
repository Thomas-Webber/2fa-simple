# 2fa-simple 
Go Simple implementation of two-factor login flow using a local configuration for users.
- Verification is done using a verification code sent by email
- Act as an http server for Login to any Single Page Application
- Supports i18n
- TailwindCss is used for the Web-UI

# Configuration
```
# config.yml
base_url: http://localhost:3000
language: fr
spa_directory: web-spa              # directory of your single page app
spa_fallback: index.html            # requests will fallback once logged-in
sqlite_database: data/fiber.sqlite3 # sqlite ddb for session storage

# Email sender
website: example.com            # Used in templates/layout.html and in the mail templates
service_email: service@ecorp.co # Used to send an email
support_email: service@ecorp.co # Shown in the footer
company_name: E-corp

# Users
users:
  - email: test@example.com
    password: $2a$14$mPFZutVj5fBIEr7rjEqH0u7hm/PD3XmlM.cLZjc3Hle664Rz4mJ.K
```


# Dev requirements
- go 1.14+
- Environment:
    - `export SENDGRID_API_KEY='7OL816snJH6yjECp4eO_DT8'`
- node/npm for building tailwind css


# TODO:
- docker
- deutsche Übersetzung

Tests:
- api end to end tests


Optimizations:
- error page template
- compression
- caching
- cors/xss security