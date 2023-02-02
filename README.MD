## Installation ##

```
cd /opt/tljh/hub/lib/python3.6/site-packages
git clone https://github.coma/revotechuet/dummyauthenticator
```

Should install it. It has no additional dependencies beyond JupyterHub.

You can then use this as your authenticator by adding the following line to
your `jupyterhub_config.py`:

```
vim /opt/tljh/hub/lib/python3.6/site-packages/tljh/jupyterhub_config.py
c.JupyterHub.authenticator_class = 'dummyauthenticator.DummyAuthenticator'
```

