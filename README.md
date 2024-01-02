# EPB static start pages

The service start pages moved from our codebase to GOV.UK's main content managed by GDS.
We use the pages to test the full journey in pre-production environments.

We currently have two static start pages:
- Find an energy certificate
- Getting a new energy certificate

## Contributing

This application uses a `staticfile_buildpack` and therefore the environment variables set in CloudFoundry cannot be read within the HTML.
For this reason it is necessary to review and if necessary update the links in the HTML files before deploying to a relevant environment/space, so they correspond to the correct environment.

Suggested developer workflow:

1. Make relevant changes
2. Test your changes locally
3. Deploy the app to integration following the instructions below
4. Test your changes in integration
5. Push your changes to GitHub
6. Replace all instances of `integration` with `staging` in the project (except for in the README)
7. Deploy the app to staging
8. Test your changes in staging
9. Discard your changes of swapping `integration` with `staging`


There are [integration](https://github.com/communitiesuk/epb-static-start-pages/tree/aws-integration) and [staging](https://github.com/communitiesuk/epb-static-start-pages/tree/aws-staging) branches that should be used for deploying these start pages to the AWS infrastructure 