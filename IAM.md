## IAM 101

IAM is universal in all regions

### Terms

- Users
- Groups
- Roles
- Policies
  * a document that defines permissions
  * JSON
  * key-value pairs

### Features

- manage users and their level of access
- centralised control
- shared access to account
- granular permissions
- identity federation (AD, Facebook, Linkedin)
- MFA
- temporary access for users/devices/services
- password rotation policy
- PCI DSS compliance
- integrates with different AWS services


## Active Directory Federation

- User -> ADFS
- ADFS -> AD
- ADFS -> SAML assertion -> User
- User -> SAML assertion -> AWS sign-in endpoint -> AssumeRoleWithSAML
- Access to console granted

## Web Identity Federation

Access using facebook, google, etc

- login to facebook
- get access token
- get temp security creds with AssumeRoleWithWebIdentity request (assumes some role)
- access resources using assumed role

## Role types

- AWS Service Role
- AWS service-linked roles
  * Lex bots and channels
- Role for cross-account access
- Role for identity provider access
  * access for idP users to AWS account

  #todo

  - https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_iam-condition-keys.html
  - PermissionsBoundaries