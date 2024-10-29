# About

This repository holds a helm chart for mviewer and mviewerstudio. This README file aims to present
some of the features and/or implementation choices.

# Maintainers

## How to create a new chart release
1. Change and push the version in the Chart.yaml
2. Write a changelog in the CHANGELOG.md

# Usage

## Install

WARNING: Change `0.7.0` by the latest version of the helm chart found in https://github.com/mviewer/helm-charts/blob/main/mviewer/Chart.yaml#L18

### Quick start

1. Execute this command for installing the mviewer chart:  
   ```
   helm install mviewer oci://ghcr.io/mviewer/helm-charts/mviewer --version 0.7.0
   ```
   
4. Go to [https://YOURDOMAIN](https://YOURDOMAIN) OR [https://YOURDOMAIN/mviewerstudio](https://YOURDOMAIN/mviewerstudio)

### Customized installation
1. Create a new separate 'values' file (or edit the existing one, not recommended).  

3. Execute this command for installing the mviewer chart:  
   ```
   helm repo add mviewer https://charts.mviewer.com
   helm repo update
   helm install -f your-values.yaml mviewer oci://ghcr.io/mviewer/helm-charts/mviewer --version 0.7.0
   ```

4. Go to [https://YOURDOMAIN](https://YOURDOMAIN) OR [https://YOURDOMAIN/mviewerstudio](https://YOURDOMAIN/mviewerstudio)

## Upgrade

Apply only for a customized installation.

```
helm upgrade -f your-values.yaml mviewer oci://ghcr.io/mviewer/helm-charts/mviewer --version 0.7.0
```