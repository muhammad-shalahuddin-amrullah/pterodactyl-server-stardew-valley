# Stardew Valley Pterodactyl Server 

This repository contains the files needed to spin up a Stardew Valley multiplayer server for pterodactyl.

Use the egg file and set the Steam varialbes. The scripts will remotely grab necessary files. The nexus API for mods doesn't allow downloading without a premium account, so the necessary mods here in this repository and will be pulled into the server on installation.

## GitHub Actions Workflow

This repository includes a GitHub Actions workflow to automate the setup and running of the Stardew Valley server. The workflow file is located at `.github/workflows/stardew-valley-server.yml`.

### How to Use the GitHub Actions Workflow

1. Fork this repository to your GitHub account.
2. Go to the `Settings` tab of your forked repository.
3. Click on `Secrets` in the left sidebar.
4. Add a new secret with the name `NGROK_AUTH_TOKEN` and your ngrok authentication token as the value.
5. Push a commit to the `main` branch or create a pull request to trigger the workflow.

The workflow will set up the environment, install dependencies, and run the Stardew Valley server.

## Accessing the Server via ngrok

The GitHub Actions workflow uses ngrok to expose the Stardew Valley server. Follow these steps to access the server:

1. After the workflow completes, go to the `Actions` tab of your repository.
2. Click on the latest workflow run.
3. In the workflow run details, find the `Start ngrok` step.
4. Copy the `Forwarding` URL provided by ngrok. This URL will allow you to access the Stardew Valley server.
