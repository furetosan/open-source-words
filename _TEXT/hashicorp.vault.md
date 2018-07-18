vault please note we take vaults security and our users trust very seriously if you believe you have found a security issue in vault please responsibly disclose by contacting us at security hashicorp com website https www vaultproject io irc vault tool on freenode announcement list google groups discussion list google groups vault is a tool for securely accessing secrets a secret is anything that you want to tightly control access to such as api keys passwords certificates and more vault provides a unified interface to any secret while providing tight access control and recording a detailed audit log a modern system requires access to a multitude of secrets database credentials api keys for external services credentials for service oriented architecture communication etc understanding who is accessing what secrets is already very difficult and platform specific adding on key rolling secure storage and detailed audit logs is almost impossible without a custom solution this is where vault steps in the key features of vault are secure secret storage arbitrary key value secrets can be stored in vault vault encrypts these secrets prior to writing them to persistent storage so gaining access to the raw storage isnt enough to access your secrets vault can write to disk consul and more dynamic secrets vault can generate secrets on demand for some systems such as aws or sql databases for example when an application needs to access an s3 bucket it asks vault for credentials and vault will generate an aws keypair with valid permissions on demand after creating these dynamic secrets vault will also automatically revoke them after the lease is up data encryption vault can encrypt and decrypt data without storing it this allows security teams to define encryption parameters and developers to store encrypted data in a location such as sql without having to design their own encryption methods leasing and renewal all secrets in vault have a lease associated with it at the end of the lease vault will automatically revoke that secret clients are able to renew leases via built in renew apis revocation vault has built in support for secret revocation vault can revoke not only single secrets but a tree of secrets for example all secrets read by a specific user or all secrets of a particular type revocation assists in key rolling as well as locking down systems in the case of an intrusion for more information see the introduction section of the vault website getting started documentation all documentation is available on the vault website developing vault if you wish to work on vault itself or any of its built in systems youll first need go installed on your machine version 1 10 1 is required for local dev first make sure go is properly installed including setting up a gopath next clone this repository into gopath src github com hashicorp vault you can then download any required build tools by bootstrapping your environment sh make bootstrap to compile a development version of vault run make or make dev this will put the vault binary in the bin and gopath bin folders sh make dev bin vault to run tests type make test note this requires docker to be installed if this exits with exit status 0 then everything is working sh make test if youre developing a specific package you can run tests for just that package by specifying the test variable for example below only vault package tests will be run sh make test test vault acceptance tests vault has comprehensive acceptance tests covering most of the features of the secret and auth methods if youre working on a feature of a secret or auth method and want to verify it is functioning and also hasnt broken anything else we recommend running the acceptance tests warning the acceptance tests create destroy modify real resources which may incur real costs in some cases in the presence of a bug it is technically possible that broken backends could leave dangling data behind therefore please run the acceptance tests at your own risk at the very least we recommend running them in their own private account for whatever backend youre testing to run the acceptance tests invoke make testacc sh make testacc test builtin logical consul the test variable is required and you should specify the folder where the backend is the testargs variable is recommended to filter down to a specific resource to test since testing all of them at once can sometimes take a very long time acceptance tests typically require other environment variables to be set for things such as access keys the test itself should error early and tell you what to set so it is not documented here for more information on vault enterprise features visit the vault enterprise site