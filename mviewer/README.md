# About

This repository holds a helm chart for mviewer and mviewerstudio. This README file aims to present
some of the features and/or implementation choices.

# Maintainers

## How to create a new chart release
1. Change and push the version in the Chart.yaml
2. Write a changelog in the CHANGELOG.md
3. Execute `git tag 0.X.X` (with the same version as the chart)
4. Execute `git push --tags`

# Usage

## Install

### Quick start

   ````
1. Execute these commands for installing the mviewer chart:  
   ```
   helm repo add mviewer https://charts.mviewer.com
   helm repo update
   helm install mviewer mviewer/mviewer
   ```
   
4. Go to [https://YOURDOMAIN](https://YOURDOMAIN)

### Customized installation
1. Create a new separate 'values' file (or edit the existing one, not recommended).  

3. Execute these commands for installing the mviewer chart:  
   ```
   helm repo add mviewer https://charts.mviewer.com
   helm repo update
   helm install -f your-values.yaml mviewer mviewer/mviewer
   ```

4. Go to [https://YOURDOMAIN](https://YOURDOMAIN)

## Upgrade

Apply only for a customized installation.

```
helm upgrade -f your-values.yaml mviewer mviewer/mviewer
```