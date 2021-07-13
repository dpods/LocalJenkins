# LocalJenkins
Run a Jenkins CI server locally

## Getting Started
Create a `.env` file
```bash
cp .env.example .env
```

Create local directories for Jenkins data. These are excluded in the .gitignore but necessary to persist data
```bash
mkdir jenkins_data
mkdir jenkins_certs
```

Start the Jenkins Server
```bash
docker-compose up
```

Initial setup may take a few minutes. Look for output similar to this in your docker-compose logs:
```bash
jenkins    | *************************************************************
jenkins    | *************************************************************
jenkins    | *************************************************************
jenkins    | 
jenkins    | Jenkins initial setup is required. An admin user has been created and a password generated.
jenkins    | Please use the following password to proceed to installation:
jenkins    | 
jenkins    | 1fdb93012ece40e0d3922c2b5cd94246
jenkins    | 
jenkins    | This may also be found at: /var/jenkins_home/secrets/initialAdminPassword
jenkins    | 
jenkins    | *************************************************************
jenkins    | *************************************************************
jenkins    | *************************************************************
```

Copy the password, go to [http://localhost:8080](http://localhost:8080), and enter the admin password.

Proceed with the rest of the setup steps in the Getting Started wizard.

