# demo-github-actions
Two Github actions to be deployed on repositories for Looker demos

1. [Spectacles](/workflows/spectacles.yml) for validating pull requests using spectacles and notifying of failures / successes in slack
2. [Content Validation](/worflows/content_validate.yml) for validating dashboards in the demo, expoerting LookML dashboards to github and importing LookML dashboards to other instances

Each demo repo needs the following secrets:
- CLIENT_ID: client id for the development instance
- CLIENT_SECRET: client secret for the development instance
- GOOGLEDEMO_CLIENT_ID: client id for the googledemo.looker.com
- GOOGLEDEMO_CLIENT_SECRET: client secret for the googledemo.looker.omc
- PERSONAL_ACCESS_TOKEN: github personal access token

And the following env variables need to be updated in both yaml files:
- DEMO_NAME: Demo name, to be used in slack message (e.g. Ecommerce)
- PROJECT_NAME: LookML project name (e.g. thelook_events)
- HOST: name of the development instance (e.g. demo)
