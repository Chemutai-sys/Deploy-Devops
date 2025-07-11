# Deploy-Devops
name: Frontend CI
on:
  push:
    paths:
      - "client/**"

jobs:
  build:
    runs-on: ubuntu-latest
    defaults:
      run:
        working-directory: client
    steps:
      - uses: actions/checkout@v3
      - run: npm install
      - run: npm run build
name: Backend CI
on:
  push:
    paths:
      - "server/**"

jobs:
  test:
    runs-on: ubuntu-latest
    defaults:
      run:
        working-directory: server
    steps:
      - uses: actions/checkout@v3
      - run: npm install
      - run: npm test
## Deployment URLs
- Frontend: [your-frontend-url](https://yourapp-frontend.vercel.app)
- Backend: [your-backend-url](https://yourapp-backend.onrender.com)

## CI/CD
- Frontend CI: 
- Backend CI: 
- CD Webhooks: 

## Monitoring
- Uptime monitoring via BetterStack
- Error tracking with Sentry

## Screenshots
- ![Frontend CI success](./screenshots/frontend-ci.png)
- ![Backend CI passing](./screenshots/backend-ci.png)
