# Github Workflow Demo

This is a simple Github workflow that deploys code to a server. It is configured to automatically run when the `main` branch is updated. It's free to use and you can customize it to your needs.

## Deploys

Simple. Just push your code.

Alternatively, you can trigger the workflow manually using the Github CLI:

```bash
gh workflow run deploy.yml
```

## Rollbacks

Rolling back to a previous deploy can be done directly from the Github Actions UI where you will be prompted to enter the commit SHA or tag of the previous deploy.

Alternatively, you can trigger the workflow manually using the Github CLI:

```bash
gh workflow run deploy.yml --input rollback=[insert commmit sha here]
```

## Github Secrets

You will need to create the following Github secrets:

- CURRENT_DIR - path of the symlink that is created Ex. /home/john/somesite.com/current
- DEPLOY_DIR - path for the root folder where your files live Ex. /home/john/somesite.com 
- RELEASES_DIR - path to the releases directory Ex. /home/john/somesite.com/releases
- TMP_DIR - path to temp folder where the repo is uploaded to on the server Ex. /home/john/deploy
- SHARED_DIR - path to shared assets that need to survive deploys Ex. /home/john/somesite.com/shared
- SSH_PRIVATE_KEY - private key that you use for SSH access
- SERVER_HOST - usually an IP address
- SERVER_USER - username

Enjoy and happy coding!