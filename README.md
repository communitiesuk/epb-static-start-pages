# EPB static pages

This is the repo for the various static pages we use. These include the static start pages for testing the full journey pre-prod, and the static error pages that the site points to when the service is unavailable.

## EPB static start pages

The service start pages moved from our codebase to GOV.UK's main content managed by GDS.
We use the pages to test the full journey in pre-production environments.

We currently have two static start pages:
- Find an energy certificate
- Getting a new energy certificate

The integration & staging versions of the start pages are stored in different branches in this repository:
- [aws-integration](https://github.com/communitiesuk/epb-static-start-pages/tree/aws-integration)
- [aws-staging](https://github.com/communitiesuk/epb-static-start-pages/tree/aws-staging)

These are deployed as static hosted websites in S3 in the Dev AWS account.

### Contributing

Suggested developer workflow:

1. Pull the relevant branch (integration or staging)
2. Make relevant changes
3. Test your changes locally
4. Upload files to the relevant S3 bucket in the AWS dev account 

## EPB static error pages

When the service goes down, we can intercept the errors in cloudfront and point to our own static error pages hosted in S3, rather than serving the generic AWS error pages.

These provide some information on how to contact us, and keeps the branding consistent.

The error pages are the same across environments, so all variants are tracked in the main branch of this repo.

If you make changes, you will need to upload the directories and their files to the error pages es3 buckets in each AWS account either via the console or the cli.
