## Installation ##
Install python requests module
```
/opt/tljh/hub/bin/pip3 install requests
```
```
cd /opt/tljh/hub/lib/python3.6/site-packages
git clone https://github.com/revotechuet/dummyauthenticator
```

Should install it. It has no additional dependencies beyond JupyterHub.

You can then use this as your authenticator by adding the following line to
your `jupyterhub_config.py`:

```
vim /opt/tljh/hub/lib/python3.6/site-packages/tljh/jupyterhub_config.py
c.JupyterHub.authenticator_class = 'dummyauthenticator.DummyAuthenticator'
c.DummyAuthenticator.password = "11111111"
```

Restart Service
```
systemctl restart jupyterhub.service
```
Custom spawner default url
```
vim /opt/tljh/config/app.py
c.Spawner.default_url = "/lab"
```
