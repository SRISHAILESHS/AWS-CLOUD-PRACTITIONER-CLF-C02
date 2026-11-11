# 134. Why Global Applications?

## Simple meaning

A global application serves users in different parts of the world. AWS provides infrastructure and networking services that help make applications faster, more available and easier to reach worldwide.

## Example

Imagine an online shopping application hosted in Mumbai. Customers in India may get a good response time, but customers in the USA may experience more delay because their requests travel a longer distance.

You can improve the experience by using services such as:

- **Amazon Route 53:** directs users to suitable application endpoints using DNS.
- **Amazon CloudFront:** caches and delivers content from edge locations closer to users.
- **AWS Global Accelerator:** routes traffic through the AWS global network to healthy application endpoints.
- **Multiple Regions:** can support geographic distribution and disaster recovery when the application is designed for it.

## Key terms

- **Latency:** time taken for data to travel between a user and a service.
- **High availability:** designing a system to remain accessible despite failures.
- **Fault tolerance:** ability to continue operating when a component fails.
- **Disaster recovery:** restoring service after a major disruption.
- **Global reach:** making an application available to users in multiple geographic areas.

## Important exam point

Using more AWS Regions does not automatically make an application globally available. The application, data, DNS, networking, security and failover processes must also be designed for multiple locations.
