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

- CURRENT_DIR
- DEPLOY_DIR
- RELEASES_DIR
- TMP_DIR
- SHARED_DIR
- SSH_PRIVATE_KEY
- SERVER_HOST
- SERVER_USER

Enjoy and happy coding!