# EPB static start pages

The service start pages moved from our codebase to GOV.UK's main content managed by GDS.
We use the pages to test the full journey in pre-production environments.

We currently have two static start pages:
- Find an energy certificate
- Getting a new energy certificate

The integration & staging versions of the start pages are stored in different branches in this repository:
- [aws-integration](https://github.com/communitiesuk/epb-static-start-pages/tree/aws-integration)
- [aws-staging](https://github.com/communitiesuk/epb-static-start-pages/tree/aws-staging)

These are deployed as static hosted websites in S3 in the Dev AWS account.

## Contributing

Suggested developer workflow:

1. Pull the relevant branch (integration or staging)
2. Make relevant changes
3. Test your changes locally
4. Upload files to the relevant S3 bucket in the AWS dev account 
