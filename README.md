# Stardew Valley Pterodactyl Server 

This repository contains the files needed to spin up a Stardew Valley multiplayer server for pterodactyl.

Use the egg file and set the Steam varialbes. The scripts will remotely grab necessary files. The nexus API for mods doesn't allow downloading without a premium account, so the necessary mods here in this repository and will be pulled into the server on installation.

## GitHub Workflow for CI/CD

This repository includes a GitHub workflow to automate the setup and testing of the Stardew Valley server. The workflow is defined in the `.github/workflows/ci.yml` file.

### How to Use the GitHub Workflow

1. **Triggering the Workflow**: The workflow is triggered on every push to the `main` branch and on every pull request to the `main` branch.

2. **Workflow Steps**:
   - **Checkout repository**: The workflow checks out the repository.
   - **Set up environment**: The workflow installs necessary dependencies.
   - **Install dependencies and set up server**: The workflow runs the `install_script.sh` to set up the Stardew Valley server.
   - **Run tests**: The workflow runs tests to ensure the server is functioning correctly.

3. **Viewing Workflow Results**: You can view the results of the workflow runs in the "Actions" tab of your GitHub repository.

4. **Modifying the Workflow**: If you need to modify the workflow, you can edit the `.github/workflows/ci.yml` file.

For more details on GitHub Actions and workflows, refer to the [GitHub Actions documentation](https://docs.github.com/en/actions).
