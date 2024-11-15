* ![[Pasted image 20240920110944.png]]
* ![[Pasted image 20240920111004.png]]

## Types of Load Balancer
### Classic Load Balancer:
* 1st gen. LB
* Doesn't support multiple ssl certificates thus load balancing multiple apps. is not possible,
* ![[Pasted image 20240920111731.png]]
### Application Load Balancer:
* Works with web apps.
* ![[Pasted image 20240920111920.png]]
* SSL certs are configured at ALB level. Traffic is forwarded from ALB to EC2 over HTTP by default.
* It's possible to forward traffic from ALB to EC2 over HTTPS but the SSL certs. needs to be installed & managed by the user.![[Pasted image 20240920112054.png]]
### Network Load Balancer:
* ![[Pasted image 20240920112755.png]]
* ![[Pasted image 20240920112852.png]]
* ![[Pasted image 20240920113120.png]]
* By default LB node can only split load with in an AZ ![[Pasted image 20240920114110.png]]
* ![[Pasted image 20240920114134.png]]
* ![[Pasted image 20240920114401.png]]
* ![[Pasted image 20240920114643.png]]
* Listeners are rules to match specific request
* Target Groups are the destination to which the request needs to be sent.![[Pasted image 20240920114924.png]]

## Summary
* ![[Pasted image 20240920115155.png]]
* ![[Pasted image 20240920115317.png]]
* ![[Pasted image 20240920115340.png]]
* 