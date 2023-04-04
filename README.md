# SSH Deploy Config

## Add SSH Key as a SECRET

Open your repository Settings >> Secrets and Variables >> Actions >> Tab Secrets. Add a "New repository secret" named `SSH_PRIVATE_KEY` with a valid SSH key from your deployer user.

## Add additional environment variables

Open your repository Settings >> Secrets and Variables >> Actions >> Tab Variables. Add the following variables:

`REMOTE_HOST`: your host domain (e.g. myvps.example.com)

`REMOTE_USER`: your host deployer username (e.g. deployer)

`REMOTE_TARGET`: destination folder in host (e.g. /home/deployer/apps/myapp)
