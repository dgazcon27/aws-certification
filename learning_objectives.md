# Introduction to EC2

In this video, we are going to talk at a high level about a service called Amazon Elastic Compute Cloud or EC2. If you remember from our coffee shop, the employees are a metaphor for the client/server model where a client sends a request to the server; the server does some work, and then sends a response. That example is for the coffee shop. But the same idea applies to other businesses. Your business, whether it be in healthcare, manufacturing, insurance, or delivering video content to millions of users all around the world, are also using this model to deliver products, resources, or data to your end users. And you're going to need servers to power your business and your applications. You need raw compute capacity to host your applications and provide the compute power that your business needs. When you're working with AWS, those servers are virtual. And the service you use to gain access to virtual servers is called EC2. 


Using EC2 for compute is highly flexible, cost effective, and quick when you compare it to running your own servers on premises in a data center that you own. The time and money it takes to get up and running with on-premises resources is fairly high. When you own your own fleet of physical servers, you first have to do a bunch of research to see what type of servers you want to buy and how many you'll need. Then you purchase that hardware up front. You'll wait for multiple weeks or months for a vendor to deliver those servers to you. You then take them to a data center that you own or rent to install them, rack and stack them, and wire them all up. Then you make sure that they are secure and powered up and then they're ready to be used. Only then can you begin to host your applications on top of these servers. The worst part is, once you buy these servers you are stuck with them whether you use them or not. 


With EC2, it's much easier to get started. AWS took care of the hard part for you already. AWS already built and secured the data centers. AWS has already bought the servers, racked and stacked them, and they are already online ready to be used. AWS is constantly operating a massive amount of compute capacity. And you can use whatever portion of that capacity when you need it. All you have to do is request the EC2 instances you want and they will launch and boot up, ready to be used within a few minutes. Once you're done, you can easily stop or terminate the EC2 instances. You're not locked in or stuck with servers that you don't need or want. Your usage of EC2 instances can vary greatly over time. And you only pay for what you use. Because with EC2, you only pay for running instances, not stopped or terminated instances. 


EC2 runs on top of physical host machines managed by AWS using virtualization technology. When you spin up an EC2 instance, you aren't necessarily taking an entire host to yourself. Instead, you are sharing the host with multiple other instances, otherwise known as virtual machines. And a hypervisor running on the host machine is responsible for sharing the underlying physical resources between the virtual machines. This idea of sharing underlying hardware is called multitenancy. The hypervisor is responsible for coordinating this multitenancy and it is managed by AWS. The hypervisor is responsible for isolating the virtual machines from each other as they share resources from the host. This means EC2 instances are secure. Even though they may be sharing resources, one EC2 instance is not aware of any other EC2 instances also on that host. They are secure and separate from each other. 


Luckily, this is not something you, yourself, need to set up. But it's important to know the idea of multitenancy and have a high level understanding of how this works. EC2 gives you a great deal of flexibility and control. Not only can you spin up new servers or take them offline at will, but you also have the flexibility and control over the configuration of those instances. 


When you provision an EC2 instance, you can choose the operating system based on either Windows or Linux. You can provision thousands of EC2 instances on demand. With a blend of operating systems and configurations to power your business' different applications. 


Beyond the OS, you also configure what software you want running on the instance. Whether it's your own internal business applications, simple web apps, or complex web apps, databases or third party software like enterprise software packages, you have complete control over what happens on that instance. EC2 instances are also resizable. You might start with a small instance, realize the application you are running is starting to max out that server, and then you can give that instance more memory and more CPU. Which is what we call vertically scaling an instance. 


In essence, you can make instances bigger or smaller whenever you need to. You also control the networking aspect of EC2. So what type of requests make it to your server and if they are publicly or privately accessible is something you decide. 


We will touch more on this later in the course in detail. Virtual machines are not a new thing. But the ease of provisioning EC2 instances allows for programmers and businesses to innovate more quickly. AWS has just made it much, much easier and more cost effective for you to acquire servers through this Compute as a Service model. There's a lot more to learn about EC2. We talked about virtualization and the types of software you can run on an EC2 instance. But there is more you can configure with EC2 as well.

# How Amazon EC2 works

## Launch

First, you launch an instance. Begin by selecting a template with basic configurations for your instance. These configurations include the operating system, application server, or applications. You also select the instance type, which is the specific hardware configuration of your instance. 


As you are preparing to launch an instance, you specify security settings to control the network traffic that can flow into and out of your instance. Later in this course, we will explore Amazon EC2 security features in greater detail.

## Connect

Next, connect to the instance. You can connect to the instance in several ways. Your programs and applications have multiple different methods to connect directly to the instance and exchange data. Users can also connect to the instance by logging in and accessing the computer desktop.


## Use

After you have connected to the instance, you can begin using it. You can run commands to install software, add storage, copy and organize files, and more.

# Types of EC2

Now that we've learned about EC2 instances and the crucial role they play in AWS, let's talk about the different types of EC2 instances that are available. Thinking back to our coffee shop analogy, you'll remember that EC2 instances are like our employees and that they serve client requests. If we want to have a cafe that can serve a lot of customers, then we're probably going to need multiple employees, right? And they all can't just be cashiers. We also need someone to make the drinks, someone to handle the food, and maybe someone to do that cool latte art that our customers love so much. Like any business, there are a variety of tasks that need to be done, and they often require different skillsets. 


If we want our business to operate as efficiently as possible, it's important to make sure that an employee's skillset suits their role. In the same way that our coffee shop has different kinds of employees, AWS has different types of EC2 instances that you can spin up and deploy into your AWS environment. 


Each instance type is grouped under an instance family and are optimized for certain types of tasks. Instance types offer varying combinations of CPU, memory, storage, and networking capacity, and give you the flexibility to choose the appropriate mix of resources for your applications. The different instance families in EC2 are general purpose, compute optimized, memory optimized, accelerated computing, and storage optimized. 


### General purpose instances 
provide a balance of compute, memory, and networking resources. You can use them for a variety of workloads, such as:

    - application servers
    - gaming servers
    - backend servers for enterprise applications
    - small and medium databases

Suppose that you have an application in which the resource needs for compute, memory, and networking are roughly equivalent. You might consider running it on a general purpose instance because the application does not require optimization in any single resource area.

### Compute optimized instances 
are ideal for compute-bound applications that benefit from high-performance processors. Like general purpose instances, you can use compute optimized instances for workloads such as web, application, and gaming servers.

However, the difference is compute optimized applications are ideal for high-performance web servers, compute-intensive applications servers, and dedicated gaming servers. You can also use compute optimized instances for batch processing workloads that require processing many transactions in a single group.

### Memory optimized instances 
are designed to deliver fast performance for workloads that process large datasets in memory. In computing, memory is a temporary storage area. It holds all the data and instructions that a central processing unit (CPU) needs to be able to complete actions. Before a computer program or application is able to run, it is loaded from storage into memory. This preloading process gives the CPU direct access to the computer program.

Suppose that you have a workload that requires large amounts of data to be preloaded before running an application. This scenario might be a high-performance database or a workload that involves performing real-time processing of a large amount of unstructured data. In these types of use cases, consider using a memory optimized instance. Memory optimized instances enable you to run workloads with high memory needs and receive great performance.

### Accelerated computing instances 
use hardware accelerators, or coprocessors, to perform some functions more efficiently than is possible in software running on CPUs. Examples of these functions include floating-point number calculations, graphics processing, and data pattern matching.

In computing, a hardware accelerator is a component that can expedite data processing. Accelerated computing instances are ideal for workloads such as graphics applications, game streaming, and application streaming.

### Storage optimized instances 
are designed for workloads that require high, sequential read and write access to large datasets on local storage. Examples of workloads suitable for storage optimized instances include distributed file systems, data warehousing applications, and high-frequency online transaction processing (OLTP) systems.

In computing, the term input/output operations per second (IOPS) is a metric that measures the performance of a storage device. It indicates how many different input or output operations a device can perform in one second. Storage optimized instances are designed to deliver tens of thousands of low-latency, random IOPS to applications. 

You can think of input operations as data put into a system, such as records entered into a database. An output operation is data generated by a server. An example of output might be the analytics performed on the records in a database. If you have an application that has a high IOPS requirement, a storage optimized instance can provide better performance over other instance types not optimized for this kind of use case.

### Pricing

We talked about EC2 instance types, but you're all probably wondering how much is this gonna cost me? Well, don't fret. For EC2, we have multiple billing options available. 


The first one and the one that most people are familiar with is called On-Demand. What that means is that you only pay for the duration that your instance runs for. This can be per hour or per second, depending on the instance type and operating system you choose to run. Plus, no long-term commitments or upfront payments are needed. This type of pricing is usually for when you get started and want to spin up servers to test out workloads and play around. You don't need any prior contracts or communication with AWS to use On-Demand pricing. You can also use them to get a baseline for your average usage, which leads us to our next pricing option, Savings Plan. 


Savings Plan offers low prices on EC2 usage in exchange for a commitment to a consistent amount of usage measured in dollars per hour for a one or three-year term. This flexible pricing model can therefore provide savings of up to 72% on your AWS compute usage. This can lower prices on your EC2 usage, regardless of instance family, size, OS, tenancy, or AWS region. This also applies to AWS Fargate and AWS Lambda usage, which are serverless compute options that we will cover later in this course. 


Another option is Reserved Instances. These are suited for steady-state workloads or ones with predictable usage and offer you up to a 75% discount versus On-Demand pricing. You qualify for a discount once you commit to a one or three-year term and can pay for them with three payment options: all upfront, where you pay for them in full when you commit; partial upfront, where you pay for a portion when you commit; and no upfront, where you don't pay anything at the beginning. 


The next option is Spot Instances, and they allow you to request spare Amazon EC2 computing capacity for up to 90% off of the On-Demand price. The catch here is that AWS can reclaim the instance at any time they need it, giving you a two-minute warning to finish up work and save state. You can always resume later if needed. So when choosing Spot Instances, make sure your workloads can tolerate being interrupted. A good example of those are batch workloads. 

And finally, we have Dedicated Hosts, which are physical hosts dedicated for your use for EC2. These are usually for meeting certain compliance requirements and nobody else will share tenancy of that host.

## On-Demand Instances 
are ideal for short-term, irregular workloads that cannot be interrupted. No upfront costs or minimum contracts apply. The instances run continuously until you stop them, and you pay for only the compute time you use.

Sample use cases for On-Demand Instances include developing and testing applications and running applications that have unpredictable usage patterns. On-Demand Instances are not recommended for workloads that last a year or longer because these workloads can experience greater cost savings using Reserved Instances.

### Reserved Instances 
are a billing discount applied to the use of On-Demand Instances in your account. There are two available types of Reserved Instances:

    Standard Reserved Instances
    Convertible Reserved Instances

You can purchase Standard Reserved and Convertible Reserved Instances for a 1-year or 3-year term. You realize greater cost savings with the 3-year option. 


#### Standard Reserved Instances: 
This option is a good fit if you know the EC2 instance type and size you need for your steady-state applications and in which AWS Region you plan to run them. Reserved Instances require you to state the following qualifications:

    Instance type and size: For example, m5.xlarge
    Platform description (operating system): For example, Microsoft Windows Server or Red Hat Enterprise Linux
    Tenancy: Default tenancy or dedicated tenancy

You have the option to specify an Availability Zone for your EC2 Reserved Instances. If you make this specification, you get EC2 capacity reservation. This ensures that your desired amount of EC2 instances will be available when you need them. 


#### Convertible Reserved Instances: 
If you need to run your EC2 instances in different Availability Zones or different instance types, then Convertible Reserved Instances might be right for you. Note: You trade in a deeper discount when you require flexibility to run your EC2 instances.


At the end of a Reserved Instance term, you can continue using the Amazon EC2 instance without interruption. However, you are charged On-Demand rates until you do one of the following:

    Terminate the instance.
    Purchase a new Reserved Instance that matches the instance attributes (instance family and size, Region, platform, and tenancy).

AWS offers Savings Plans for a few compute services, including Amazon EC2. EC2 Instance Savings Plans reduce your EC2 instance costs when you make an hourly spend commitment to an instance family and Region for a 1-year or 3-year term. This term commitment results in savings of up to 72 percent compared to On-Demand rates. Any usage up to the commitment is charged at the discounted Savings Plans rate (for example, $10 per hour). Any usage beyond the commitment is charged at regular On-Demand rates.


## The EC2 Instance Savings Plans 

are a good option if you need flexibility in your Amazon EC2 usage over the duration of the commitment term. You have the benefit of saving costs on running any EC2 instance within an EC2 instance family in a chosen Region (for example, M5 usage in N. Virginia) regardless of Availability Zone, instance size, OS, or tenancy. The savings with EC2 Instance Savings Plans are similar to the savings provided by Standard Reserved Instances.


Unlike Reserved Instances, however, you don't need to specify up front what EC2 instance type and size (for example, m5.xlarge), OS, and tenancy to get a discount. Further, you don't need to commit to a certain number of EC2 instances over a 1-year or 3-year term. Additionally, the EC2 Instance Savings Plans don't include an EC2 capacity reservation option.


Later in this course, you'll review AWS Cost Explorer, which you can use to visualize, understand, and manage your AWS costs and usage over time. If you're considering your options for Savings Plans, you can use AWS Cost Explorer to analyze your Amazon EC2 usage over the past 7, 30, or 60 days. AWS Cost Explorer also provides customized recommendations for Savings Plans. These recommendations estimate how much you could save on your monthly Amazon EC2 costs, based on previous Amazon EC2 usage and the hourly commitment amount in a 1-year or 3-year Savings Plan.


### Spot Instances 
are ideal for workloads with flexible start and end times, or that can withstand interruptions. Spot Instances use unused Amazon EC2 computing capacity and offer you cost savings at up to 90% off of On-Demand prices.

Suppose that you have a background processing job that can start and stop as needed (such as the data processing job for a customer survey). You want to start and stop the processing job without affecting the overall operations of your business. If you make a Spot request and Amazon EC2 capacity is available, your Spot Instance launches. However, if you make a Spot request and Amazon EC2 capacity is unavailable, the request is not successful until capacity becomes available. The unavailable capacity might delay the launch of your background processing job.

After you have launched a Spot Instance, if capacity is no longer available or demand for Spot Instances increases, your instance may be interrupted. This might not pose any issues for your background processing job. However, in the earlier example of developing and testing applications, you would most likely want to avoid unexpected interruptions. Therefore, choose a different EC2 instance type that is ideal for those tasks.

### Dedicated Hosts 
are physical servers with Amazon EC2 instance capacity that is fully dedicated to your use. 

You can use your existing per-socket, per-core, or per-VM software licenses to help maintain license compliance. You can purchase On-Demand Dedicated Hosts and Dedicated Hosts Reservations. Of all the Amazon EC2 options that were covered, Dedicated Hosts are the most expensive.

## Scaling EC2 instaces

So we have a good idea now on the basics of EC2 and how it can help with any compute needs, like making coffee. Well, like metaphorically making coffee. The coffee represents the, whatever your instance is producing. The next thing we want to talk about is another major benefit of AWS, scalability and elasticity, or how capacity can grow and shrink, based on business needs.

Here is the on-prem data center dilemma. If your business is like 99% of all businesses out in the world, your customer workloads vary over time: perhaps over a simple 24 hour period, or you might have seasons where you're busy, and weeks that are not in demand. If you're building out a data center, the question is, what is the right amount of hardware to purchase? If you buy for the average amount, the average usage, you won't be wasting money on average. But when the peak loads come in, you won't have the hardware to service the customers, especially during the critical moments to expect to be making all your results.


Now, if you buy for the top max load, you might have happy customers, but for most of the year, you'll have idle resources. Which means your average utilization is very low. And I've seen data centers with average utilization under 10%, just out of fear of missing peak demand. So how do you solve the problem on-premises? Well the truth is, you can't. And here's where AWS changes the conversation entirely. 


What if you could provision your workload to exactly the demand, every hour, every day? Well, now you have happy customers, because they can always get the services they want. And you have a happy financial officer because they get the ROI your company needs. 


And here's how it works. Morgan is behind the counter. She's taking orders and we have a decoupled system. Morgan isn't doing all of the work here, so we need somebody making the drinks. It looks like Rudy's up. Now, the first problem I wanna solve, is the idea that we plan for a disaster. There's a great quote by Werner Vogels that says, "Everything fails all the time, so plan for failure and nothing fails." Or in other words, we ask ourselves what would happen if we lost our order taking instance? Well, we'd be out of business until we'd get another person to work the line, sorry, another instance up and running. 


So here is where AWS makes it really simple. Using the same programmatic method we used to create the original Morgan, we can create a second Morgan. So if one fails, we have another one already on the front line and taking orders. The customers never lose service. Well, don't forget about the backend. Let's make our processing instances redundant as well. So that gets our regular operating capacity. We now have a highly available system, with no single point of failure. And as long as the number of customers in line stays the same, we're good. But you know that's gonna change, right? So let's take a look at what's going to happen when we have a rush of customers, an increase in demand.

## Amazon EC2 Auto Scaling

If you’ve tried to access a website that wouldn’t load and frequently timed out, the website might have received more requests than it was able to handle. This situation is similar to waiting in a long line at a coffee shop, when there is only one barista present to take orders from customers.

Amazon EC2 Auto Scaling enables you to automatically add or remove Amazon EC2 instances in response to changing application demand. By automatically scaling your instances in and out as needed, you can maintain a greater sense of application availability.

Within Amazon EC2 Auto Scaling, you can use two approaches: dynamic scaling and predictive scaling.

Dynamic scaling responds to changing demand. Predictive scaling automatically schedules the right number of Amazon EC2 instances based on predicted demand.

## Example: Amazon EC2 Auto Scaling

In the cloud, computing power is a programmatic resource, so you can take a more flexible approach to the issue of scaling. By adding Amazon EC2 Auto Scaling to an application, you can add new instances to the application when necessary and terminate them when no longer needed.

Suppose that you are preparing to launch an application on Amazon EC2 instances. When configuring the size of your Auto Scaling group, you might set the minimum number of Amazon EC2 instances at one. This means that at all times, there must be at least one Amazon EC2 instance running.
Amazon EC2 instances scaling in and out as part of an Auto Scaling group.

When you create an Auto Scaling group, you can set the minimum number of Amazon EC2 instances. The minimum capacity is the number of Amazon EC2 instances that launch immediately after you have created the Auto Scaling group. In this example, the Auto Scaling group has a minimum capacity of one Amazon EC2 instance.


Next, you can set the desired capacity at two Amazon EC2 instances even though your application needs a minimum of a single Amazon EC2 instance to run.

If you do not specify the desired number of Amazon EC2 instances in an Auto Scaling group, the desired capacity defaults to your minimum capacity.

The third configuration that you can set in an Auto Scaling group is the maximum capacity. For example, you might configure the Auto Scaling group to scale out in response to increased demand, but only to a maximum of four Amazon EC2 instances.

Because Amazon EC2 Auto Scaling uses Amazon EC2 instances, you pay for only the instances you use, when you use them. You now have a cost-effective architecture that provides the best customer experience while reducing expenses.