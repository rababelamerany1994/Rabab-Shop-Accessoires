# rabab-ecommerce-microservice - Ecommerce Progressive Web Apps

rabab-ecommerce-microservice is React and Node.js based eCommerce platform. Allows creating a Progressive Web Apps.

Built with:
* Node.js v8.9
* React v16
* Redux
* Express
* Babel
* WebPack 4
* MongoDB

### Requirements
* Node.js >= 8
* MongoDB >= 3.2

## Application Structure

```
.
├── config                   # Project and build configurations
├── dist                     # Distribution folder
├── locales                  # Text files
├── logs                     # Log files
├── public                   # Static public assets and uploads
│   ├── admin                # Dashboard index.html
│   ├── admin-assets         # Dashboard assets
│   └── content              # Store root folder
|
├── scripts                  # Shell scripts for theme install/export
├── src                      # Application source code
│   ├── admin                # Dashboard application
│   │   └── client           # Client side code
│   ├── api                  # REST API
│   │   └── server           # Server side code
│   ├── store                # Store application
│   |   ├── client             # Client side code
│   |   ├── server             # Server side code
│   |   └── shared             # Universal code
│   └── index.js             # Server application start point
├── theme                    # Theme as a local package
└── process.json             # pm2 process file
```

Getting Started
Installation
Run Application
Configuration
Preparing Database

1. Installation
Requirements
Node.js >= 8
MongoDB >= 3.2
git clone https://github.com/rabab-ecommerce-microservice
cd rabab-ecommerce-microservice
npm install
npm run build
2. Run Application
npm start
Also, you can run application with PM2 and watch for modifications.

Install PM2 globally
npm install pm2 -g
Run application
pm2 start process.json
Open http://localhost:3000 to see your store.
Dashboard - http://localhost:3000/admin
API - http://localhost:3001

3. Configuration
By default MongoDB connection string is mongodb://127.0.0.1:27017/shop

Change it with environment variables

DB_HOST=255.255.255.255 \
DB_PORT=27017 \
DB_NAME=shop \
DB_USER=user \
DB_PASS=password \
#or SET a DB_URL with mongodb connection string(https://docs.mongodb.com/manual/reference/connection-string/)
DB_URL=mongodb://db1.example.net:27017,db2.example.net:2500/?replicaSet=test
npm start

4. Preparing Database
This script will:

test MongoDB connection
add default data
create basic indexes
npm run setup
