## Deploying to Azure

Our application is now ready to be deployed to Azure!

We'll use [Azure Static Web Apps](https://docs.microsoft.com/azure/static-web-apps/overview) to deploy the frontend, and [Azure Container Instances](https://docs.microsoft.com/azure/container-instances/) to deploy the backend.

Run these commands to build and deploy the application:

```bash
azd deploy backend
azd deploy frontend
```

This process should take a few minutes. Once it's done, you should see the URL of the deployed frontend application in the output of the command.

![Output of the azd command](./assets/azd-deploy-output.png)

You can now open this URL in a browser and test the deployed application.

![Screenshot of the deployed application](./assets/deployed-app.png)

<div class="tip" data-title="Tip">

> You can also build and deploy all the services at once by running `azd deploy`. This command will build and deploy the backend, frontend and indexer services.
>
> Even better! If you're starting from scratch and have a completed code, you can use the `azd up` command. This command combines both `azd provision` and `azd deploy` to provision the Azure resources and deploy the application in one command.

</div>