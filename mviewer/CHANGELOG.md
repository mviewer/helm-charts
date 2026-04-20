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
