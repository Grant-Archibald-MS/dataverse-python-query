# Overview

Example of how to query Dataverse from a Python script using Azure Active Directory Application registration

## Getting Started

To use this sample the following is assumed:

1. [Walkthrough registering App-Azure-Active-Directory](https://docs.microsoft.com/en-us/power-apps/developer/data-platform/walkthrough-register-app-azure-active-directory) with Dataverse API

2. [Create An Application User](https://docs.microsoft.com/en-us/power-platform/admin/manage-application-users#create-an-application-user) in the power platform environment and assigned a security role has access to teh table that you want to query

3. Update the [sample.config](./sample.config) with your values for

   - **authority** with your Azure Active Directory tenant id
   - **client_id** your client id from the Azure App Registration created above
   - **secret** the secret created in the step above
   - **scope** and **account** replace insert-your-org-here with your dataverse environment name

4. Python dependencies are installed

```bash
pip install -r requirements.txt
```

5. Run the sample

```bash
python sample.py sample.config
```

## Resources

This sample is based on [Python Confidential Client Secret](https://github.com/AzureAD/microsoft-authentication-library-for-python/blob/dev/sample/confidential_client_secret_sample.py).

If you need an overview on Dataverse Security Roles review the [Security concepts in Microsoft Dataverse](https://docs.microsoft.com/en-us/power-platform/admin/wp-security-cds).

Read more on query of Dataverse using REST API [Query Data Web Api](https://docs.microsoft.com/en-us/power-apps/developer/data-platform/webapi/query-data-web-api).
