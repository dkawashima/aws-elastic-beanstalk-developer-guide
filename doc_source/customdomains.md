# Your Elastic Beanstalk Environment's Domain Name<a name="customdomains"></a>

By default, your environment is available to users at a subdomain of `elasticbeanstalk.com`\. When you [create an environment](using-features.environments.md), you can choose a hostname for your application\. The subdomain and domain are autopopulated to `region.elasticbeanstalk.com`\.

To route users to your environment, Elastic Beanstalk registers a CNAME record that points to your environment's load balancer\. You can see the current value of the CNAME in the [environment dashboard](environments-console.md#environments-dashboard), as shown\.

![\[Environment URL with CNAME showing on the Elastic Beanstalk console's environment dashboard\]](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/images/environment-management-dashboard-url.png)

You can change the CNAME on your environment by swapping it with the CNAME of another environment\. For instructions, see [Blue/Green Deployments with Elastic Beanstalk](using-features.CNAMESwap.md)\.

If you own a domain name, you can use Amazon Route 53 to resolve it to your environment\. You can purchase a domain name with Amazon Route 53, or use one that you purchase from another provider\. 

To purchase a domain name with Route 53, see [Registering a New Domain](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/domain-register.html) in the *Amazon Route 53 Developer Guide*\.

To learn more about using a custom domain, see [Routing Traffic to an AWS Elastic Beanstalk Environment](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-to-beanstalk-environment.html) in the *Amazon Route 53 Developer Guide*\.

**Important**  
If you terminate an environment, you must also delete any CNAME mappings you created, as other customers can reuse an available hostname\.