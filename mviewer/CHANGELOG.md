# 1.3.0
- Fix mviewerstudio `config.json` being ignored since mviewerstudio v4.3: the ConfigMap is now mounted at `/home/mvuser/src/static/config.json`, the path read by the new image layout. The ConfigMap is now always the source of truth for `config.json`.
- The pod restarts automatically when `mviewerstudio.configMap.configJson` changes.
- Remove the `copy-starter-configmap` init container and the `keepConfigFromKubernetes` value.
- The `mviewerstudio-static-apps` PVC is kept and still mounted, but is no longer used by mviewerstudio v4.3+.

# 1.2.0
- Switch user id back from 1000 to 999 for mviewer, mviewerstudio and elasticsearch, as per https://github.com/mviewer/mviewerstudio/pull/437. **Make sure to change the permission of your existing volume**:
```
chown 999:999 * -R
```

# 1.1.0
- Update to mviewer v4.1 & mviewerstudio v4.3
- Switch user id from 999 to 1000. **Make sure to change the permission of your existing volume**:
```
chown 1000:1000 * -R
```

# 1.0.1

Bug fix for https://github.com/mviewer/mviewerstudio/issues/327

# 1.0.0

Stable release.
Update to mviewer v3.12

# 0.8.0

Let the default environment variables for Mviewer studio. It was causing some issues with mviewer.

# 0.7.1
Add automatic copy of default.xml if not found.

Update ingress so that / is default to mviewer

# 0.7.0

Initial version of the helm chart
