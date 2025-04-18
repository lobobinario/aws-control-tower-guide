# AWS Control Tower User Guide

-----
*****Copyright &copy; Amazon Web Services, Inc. and/or its affiliates. All rights reserved.*****

-----
Amazon's trademarks and trade dress may not be used in 
     connection with any product or service that is not Amazon's, 
     in any manner that is likely to cause confusion among customers, 
     or in any manner that disparages or discredits Amazon. All other 
     trademarks not owned by Amazon are the property of their respective
     owners, who may or may not be affiliated with, connected to, or 
     sponsored by Amazon.

-----
## Contents
+ [What Is AWS Control Tower?](what-is-control-tower.md)
   + [How AWS Control Tower Works](how-control-tower-works.md)
   + [Plan your AWS Control Tower landing zone](planning-your-deployment.md)
+ [Terminology](terminology.md)
+ [Pricing](pricing.md)
+ [Setting up](setting-up.md)
+ [Getting started with AWS Control Tower](getting-started-with-control-tower.md)
+ [Limitations and quotas in AWS Control Tower](limits.md)
+ [Best practices for AWS Control Tower administrators](best-practices.md)
   + [Administrative tips for landing zone setup](tips-for-admin-setup.md)
   + [Administrative tips for landing zone maintenance](tips-for-admin-maint.md)
   + [Sign in as a Root User](root-login.md)
   + [Recommendations for setting up groups, roles, and policies](roles-recommendations.md)
   + [AWS Control Tower and VPCs](vpc-concepts.md)
      + [CIDR and Peering for VPC and AWS Control Tower](vpc-ct-cidr.md)
   + [Configuration update management in AWS Control Tower](configuration-updates.md)
   + [AWS multi-account strategy for your AWS Control Tower landing zone](aws-multi-account-landing-zone.md)
   + [Using AWS CloudShell to work with AWS Control Tower](using-aws-with-cloudshell.md)
+ [Automating tasks in AWS Control Tower](automating-tasks.md)
+ [How AWS Control Tower works with roles to create and manage accounts](roles-how.md)
+ [How AWS Regions Work With AWS Control Tower](region-how.md)
   + [Configure the Region deny guardrail](region-deny.md)
+ [Provision and manage accounts in AWS Control Tower](provision-and-manage-accounts.md)
   + [About AWS accounts in AWS Control Tower](accounts.md)
   + [Provision and manage accounts with Account Factory](account-factory.md)
      + [Create or Enroll An Individual Account](quick-account-provisioning.md)
      + [Provisioning Account Factory Accounts With AWS Service Catalog](provision-as-end-user.md)
      + [Updating and moving account factory accounts with AWS Service Catalog](updating-account-factory-accounts.md)
      + [Configuring Account Factory with Amazon Virtual Private Cloud Settings](configuring-account-factory-with-VPC-settings.md)
      + [Unmanaging a Member Account](unmanage-account.md)
      + [Closing an Account Created in Account Factory](delete-account.md)
      + [Resource Considerations for Account Factory](account-factory-considerations.md)
   + [Provision accounts with AWS Control Tower Account Factory for Terraform](taf-account-provisioning.md)
      + [Deploy AWS Control Tower Account Factory for Terraform (AFT)](aft-getting-started.md)
         + [Post-deployment steps](aft-post-deployment.md)
      + [Overview of AWS Control Tower Account Factory for Terraform](aft-overview.md)
         + [AFT Architecture](aft-architecture.md)
         + [Pricing](aft-pricing.md)
      + [Terraform version supported](version-supported.md)
      + [Enable feature options](aft-feature-options.md)
      + [Resource considerations for AWS Control Tower Account Factory for Terraform](aft-resources.md)
      + [Required roles](aft-required-roles.md)
      + [Component services](aft-components.md)
      + [AFT account provisioning pipeline](aft-provisioning-framework.md)
      + [Account customizations](aft-account-customization-options.md)
      + [Alternatives for version control of source code in AFT](aft-alternative-vcs.md)
      + [Data protection](aft-data-protection.md)
      + [Remove an account from AFT](aft-remove-account.md)
+ [Detect and resolve drift in AWS Control Tower](drift.md)
   + [Manage resources outside of AWS Control Tower](external-resources.md)
+ [Enable AWS Control Tower on organizations and accounts](existing-orgs.md)
   + [Nested OUs in AWS Control Tower](nested-ous.md)
   + [Register an existing organizational unit with AWS Control Tower](importing-existing.md)
      + [Register an existing OU](how-to-register-existing-ou.md)
      + [Create a new OU](create-new-ou.md)
      + [Update existing OUs and accounts](update-existing-accounts.md)
   + [Enroll an existing AWS account](enroll-account.md)
      + [Enroll an account](enrollment-steps.md)
      + [Manually add the required IAM role to an existing AWS account and enroll it](enroll-manually.md)
   + [Enroll accounts that have existing AWS Config resources](existing-config-resources.md)
+ [Guardrails in AWS Control Tower](guardrails.md)
   + [View guardrail details](guardrail-details.md)
   + [Enable guardrails](enable-guardrails.md)
   + [Optional guardrails](optional-guardrails.md)
   + [Guardrails and compliance](compliance.md)
      + [Drift prevention and notification](prevention-and-notification.md)
      + [Guardrail compliance notifications](receive-notifications.md)
   + [Guardrail reference](guardrails-reference.md)
      + [Mandatory guardrails](mandatory-guardrails.md)
      + [Strongly recommended guardrails](strongly-recommended-guardrails.md)
      + [Elective guardrails](elective-guardrails.md)
         + [Guardrails that enhance data residency protection](data-residency-guardrails.md)
+ [Integrated services](integrated-services.md)
   + [Scripting Environments with AWS CloudFormation](cloudformation.md)
   + [Monitoring Events with CloudTrail](cloudtrail.md)
   + [Monitoring Resources and Services with CloudWatch](cloudwatch.md)
   + [Govern Resource Configurations with AWS Config](config.md)
   + [Manage Permissions for Entities with IAM](iam.md)
   + [Run Serverless Compute Functions with Lambda](lambda.md)
   + [Manage Accounts Through AWS Organizations](organizations.md)
   + [Store Objects with Amazon S3](s3.md)
   + [Provisioning Accounts Through AWS Service Catalog](service-catalog.md)
   + [Managing Users and Access Through AWS Single Sign-On](sso.md)
   + [Tracking Alerts Through Amazon Simple Notification Service](sns.md)
   + [Build Distributed Applications with AWS Step Functions](step-functions.md)
+ [Security in AWS Control Tower](security.md)
   + [Data Protection in AWS Control Tower](controltower-console-encryption.md)
   + [Identity and Access Management in AWS Control Tower](auth-access.md)
      + [Overview of Managing Access Permissions to Your AWS Control Tower Resources](access-control-overview.md)
      + [Prevent cross-service impersonation](prevent-confused-deputy.md)
      + [Using Identity-Based Policies (IAM Policies) for AWS Control Tower](access-control-managing-permissions.md)
   + [Compliance Validation for AWS Control Tower](compliance-program-info.md)
   + [Resilience in AWS Control Tower](disaster-recovery-resiliency.md)
   + [Infrastructure Security in AWS Control Tower](infrastructure-security.md)
+ [Logging and monitoring in AWS Control Tower](logging-and-monitoring.md)
   + [Monitoring](monitoring-overview.md)
   + [Logging AWS Control Tower Actions with AWS CloudTrail](logging-using-cloudtrail.md)
   + [Lifecycle Events in AWS Control Tower](lifecycle-events.md)
+ [Walkthroughs](walkthroughs.md)
   + [Walkthrough: Cleaning up AWS Control Tower Managed Resources](walkthrough-delete.md)
   + [Walkthrough: Configuring AWS Control Tower Without a VPC](configure-without-vpc.md)
   + [Walkthrough: Customize Your AWS Control Tower Landing Zone](customize-landing-zone.md)
   + [Walkthrough: Automated Account Provisioning in AWS Control Tower](automated-provisioning-walkthrough.md)
   + [Walkthrough: Setting Up Security Groups in AWS Control Tower With AWS Firewall Manager](firewall-setup-walkthrough.md)
   + [Walkthrough: Decommission a landing zone](decommission-landing-zone.md)
      + [Overview of the decommissioning process](decommissioning-process-overview.md)
      + [Resources not removed during decommissioning](resources-not-removed.md)
      + [How to decommission a landing zone](how-to-decommission.md)
      + [Setup after decommissioning a landing zone](known-issues-decommissioning.md)
+ [Troubleshooting](troubleshooting.md)
+ [Related information](related-information.md)
+ [AWS Control Tower release notes](release-notes.md)
   + [January 2021 - Present](2021-all.md)
   + [January - December 2020](January-June-2020.md)
   + [January - December 2019](January-December-2019.md)
+ [Document history](doc-history.md)
+ [AWS glossary](glossary.md)