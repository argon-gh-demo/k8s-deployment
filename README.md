# k8s-deployment

This repository is designed to showcase how Aqua can block insecure configurations from progressing through the SDLC.

## Overview

The repository contains a deployment.yaml file, which has an instruction to run as a certain user (uid 100; line 13)

The repository has 3 branches:
- main
- deploy-dev
- deploy-prod

## Demo Flow
- In the deploy-dev branch, change the UID to 0 to set the deployment to run as root and open a PR to main.
-- This simulates a more lenient branch to which there are less strict security controls in place
- In the deploy-prod branch, change the UID to 0 to set the deployment to run as root and open a PR to main.
-- This simulates a strict approach that is meant to stop risky misconfigurations from affecting prod environments
