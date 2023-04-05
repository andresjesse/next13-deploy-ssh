# SSH Deploy Config

Configure your project build to `output: "standalone"` in `next.config.js`.

Setup github permissions for workflow: From your repository Settings >> Actions >> General, scroll down to Workflow permissions >> enable Read and Write permissions.

## Add SSH Key as a SECRET

Open your repository Settings >> Secrets and Variables >> Actions >> Tab Secrets.

Add the following secrets:

`SSH_PRIVATE_KEY`: A valid SSH key from your deployer user. The public key should be added to host authorized_keys (add his own key).

## Add additional environment variables

Open your repository Settings >> Secrets and Variables >> Actions >> Tab Variables. Add the following variables:

`REMOTE_HOST`: your host domain (e.g. myvps.example.com)

`REMOTE_USER`: your host deployer username (e.g. deployer)

`REMOTE_TARGET`: destination folder in host (e.g. /home/deployer/apps/myapp)

## Example config for nginx

There's an example nginx file in `.deploy` folder. Make sure to update servername, then add it to nginx sites-enabled:

`sudo nano /etc/nginx/sites-enabled/your_servername.conf`

`sudo nginx -t` to check your config;

`sudo service nginx reload`
