# Getting started with Strapi
### `develop`

Start your Strapi application with autoReload enabled.

```
npm run develop
# or
yarn develop
```

### `start`

Start your Strapi application with autoReload disabled.

```
npm run start
# or
yarn start
```

### `build`

Build your admin panel.

```
npm run build
# or
yarn build
```

<img width="948" alt="image" src="https://github.com/satyam19arya/ecommerce_backend/assets/77580311/52bd4966-16a0-465d-ae0f-5dbf19428f5e">


### To deploy in production
```
module.exports = {
  apps: [
    {
      name: 'crazycart', // Your project name
      cwd: '/home/ubuntu/ecommerce_backend', // Path to your project
      script: 'npm', // For this example we're using npm, could also be yarn
      args: 'start', // Script to start the Strapi server, `start` by default
      env: {
        APP_KEYS: '',  // you can find it in your project .env file
        API_TOKEN_SALT: '',
        ADMIN_JWT_SECRET: '',
        JWT_SECRET: '',
        NODE_ENV: 'production',
        DATABASE_HOST: '', // database Endpoint under 'Connectivity & Security' tab
        DATABASE_PORT: '5432',
        DATABASE_NAME: 'strapi', // DB name under 'Configuration' tab
        DATABASE_USERNAME: 'postgres', // default username
        DATABASE_PASSWORD: '',
        AWS_ACCESS_KEY_ID: '',
        AWS_ACCESS_SECRET: '', 
        AWS_REGION: 'us-east-1',
        CLOUDINARY_NAME: '',
        CLOUDINARY_KEY: '',
        CLOUDINARY_SECRET: '',
        STRIPE_SECRET_KEY: '',
        CLIENT_BASE_URL: 'http://crazycart.satyam-arya.click/#',
      },
    },
  ],
};
```

Reference - https://docs.strapi.io/dev-docs/deployment/amazon-aws
