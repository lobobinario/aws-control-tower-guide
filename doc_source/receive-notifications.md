# Guardrail compliance notifications<a name="receive-notifications"></a>

To receive compliance change notifications in email sent to your audit account, subscribe to this Amazon SNS topic:

`arn:aws:sns:AWSRegion:AuditAccount:aws-controltower-AggregateSecurityNotifications` 

When subscribing, substitute your actual AWS Control Tower home Region and audit account information into the topic name shown\. You can subscribe to SNS topics that receive notifications about each supported AWS Region in which you run AWS Control Tower\.

**SNS topics and notifications you can receive**
+ `aws-controltower-SecurityNotifications`: One of these topics exists for each supported AWS Region\. It receives compliance, noncompliance, and change notifications from AWS Config in that Region\. It forwards all incoming notifications to `aws-controltower-AggregateSecurityNotifications`
+ `aws-controltower-AggregateSecurityNotifications`: This topic exists in each supported AWS Region\. It receives noncompliance notifications from the region\-specific `aws-controltower-SecurityNotifications` topics\. Additionally, in the home Region, it also receives drift notifications\.
+ `aws-controltower-AllConfigNotifications`: It receives notifications from AWS Config regarding compliance, noncompliance, and change\.

**Other considerations about SNS topics:**
+ All of these topics exist and receive notifications in the audit account\.
+  By default, the audit account email address is subscribed to the `aws-controltower-AggregateSecurityNotifications` SNS topic\.
+ SNS topics in AWS Control Tower are extremely noisy, by design\. For example, AWS Config sends a notification every time AWS Config discovers a new resource\.
+ Administrators who wish to filter out specific types of notifications from an SNS topic can create an AWS Lambda function and subscribe it to the SNS topic\. Alternatively, you can set up an EventBridge rule to filter notifications, as described in this support article, [How can I be notified when an AWS resource is non\-compliant using AWS Config?](http://aws.amazon.com/premiumsupport/knowledge-center/config-resource-non-compliant/)
+ AWS Config notifications contain a JSON object\.
+ AWS Control Tower drift notifications appear in plain text\.