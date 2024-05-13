# uptycs-ci-github-workflow
An example of how to run an Uptycs image scan inside a GitHub Workflow. 

# Setup
1. Get Uptycs Tenant Values: Uptycs Secret & TLS Hostname
   - Login to your Uptycs tenant and go to 'Integrations and Downloads'
     
     ![image](https://github.com/uptycslabs/uptycs-ci-github-workflow/assets/49769928/e264b6d8-9c1b-4af4-a835-3911e7e9aa1f)
   - Copy the values for Uptycs Secret & TLS Hostname and save them
     ![image](https://github.com/uptycslabs/uptycs-ci-github-workflow/assets/49769928/511641d8-b03b-4ac1-9f7b-1b6929bb1381)
2. Create an Uptycs API key
   - Go to 'Configurations' - 'Users' then click Edit on your user
   - Then go to 'User API key' and click 'CREATE', then 'Download' the API key file
     ![image](https://github.com/uptycslabs/uptycs-ci-github-workflow/assets/49769928/3211594a-7c65-4736-b135-7b6024b69c84)
3. Create the GitHub Action Repository Secrets
   
   Go to the GitHub Repository 'Settings' - 'Secrets and variables' - 'Actions' then click 'New repository secret' then add 
   - UPTYCS_CI_HOSTNAME (Value from the Integrations and Downloads screen)
   - UPTYCS_CI_SECRET (Value from the Integrations and Downloads screen)
   - UPTYCS_API_KEY (Value from the API key file)
   - UPTYCS_API_SECRET (Value from the API key file)
   - UPTYCS_CUSTOMER_ID (Value from the API key file)
4. Run the Workflow
   
   There is a workflow that can be run for testing, it is located at: .github/workflows/build-scan-repo-dockerfile.yml 
