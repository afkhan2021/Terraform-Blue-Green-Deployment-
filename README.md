# Terraform-Blue-Green-Deployment-
 Terraform Blue Green Deployment &amp; Terraform Canary Deployment 🔵🐣🟢 AWS | ALB | EC2 

### Overview
+You will implement a deployment strategy using AWS-Services that allows routing traffic from one server to another without any downtime.
+The routing should be controllable via script. Servers can simply be `NGINX`s responding with different versions or names, e.g:

+
+```
+$ ./deploy-infrastructure # optional if it is not already setup.
+$
+$ for i in `seq 1 5`; do curl $DESTINATION; done
+Hi, I am Frank
+Hi, I am Frank
+Hi, I am Frank
+Hi, I am Frank
+Hi, I am Frank
+```
+When we run your script we should get a different/new version as a response without much delay.
+```
+$ ./your_script
+$
+$ for i in `seq 1 10`; do curl $DESTINATION; done
+Hi, I am Frank
+Hi, I am Frank
+Hi, I am Frank
+Hi, I am Frank
+Hi, I am Carol
+Hi, I am Carol
+Hi, I am Carol
+Hi, I am Carol
+Hi, I am Carol
+Hi, I am Carol
+```
+
However we should also be able to rollback to the earlier setup.
+
+#### Evaluation criteria
+ - [ ] The infrastructure setup is automated using terraform or cloudformation and the code is checked into a version control system.
+ - [ ] The project contains a `README.md` with documentation on how to run the project.
+
+#### Deliverable
+- [ ] The source is accessible on a Github repository.
+- [ ] The infrastructure is publicly available and can be tested similar to the scripts above.
+- [ ] Provide us IAM credentials to login to the AWS account. If you have other resources in it make sure we can only access what is related to this test.
+

+#### Bonus
+We know time is precious, we won't mark you down for not doing the extra credits, but if you want to give them a go.
+
+- [ ] We can manage traffic distribution with finer grained controls e.g. percent wise distribution like 20% `Frank` and 80% `Carol`
+- [ ] The project has a CI/CD Pipeline with manual approval.
+

+#### Remarks
+We kept the challenge fairly open to let you be creative.
+It's important to note that it's by no means a test, we just want to get a sense for how you write code and solve problems.

+Don't hesitate to write down your assumption to help us understand the decisions you made.  Its also important for us to see that you can make the right trade-offs knowing that this code is not going to production. For example you shouldn't care about security for this challenge but you should indicate in the `README` or in the code when you purposely didn't implement something that you would have implemented if this code would be pushed to production. We encourage to reduce dependencies as much as possible. If you decide to use a framework or library, please explain why in the `README`.

+
