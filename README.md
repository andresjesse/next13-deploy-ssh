# SSH Deploy Config

Configure your project build to `output: "standalone"` in `next.config.js`.

## Add SSH Key as a SECRET

Open your repository Settings >> Secrets and Variables >> Actions >> Tab Secrets.

Add the following secrets:

`SSH_PRIVATE_KEY`: A valid SSH key from your deployer user. The public key should be added to host authorized_keys (add his own key).

## Add additional environment variables

Open your repository Settings >> Secrets and Variables >> Actions >> Tab Variables. Add the following variables:

`REMOTE_HOST`: your host domain (e.g. myvps.example.com)

`REMOTE_USER`: your host deployer username (e.g. deployer)

`REMOTE_TARGET`: destination folder in host (e.g. /home/deployer/apps/myapp)
