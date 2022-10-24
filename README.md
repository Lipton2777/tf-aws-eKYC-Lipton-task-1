
------------
<h1 align="center">Task 1</h1>
<b>Answer:</b> Here, A monolithic ekyc system (NID validation with real time image processing) has to be migrated into the cloud. The solution has a global user base mainly from Southeast Asia and North America (can be deployed in multiple geographical locations or CDN). I have create a Terraform script to infrastructure deploy on AWS platform. Please visit the below mentioned GIT:
###  1. Micro service definition for the application.
<b>Monolithic Architecture:</b> Monolithic architecture is like a big container in which all the software components of an application are clubbed inside a single package.

<b>Microservices Architecture: </b> Microservices Architecture is an architectural development style which builds an application as a collection of small autonomous services developed for a business domain.

*Main differences between Microservices and Monolithic Architecture has been below shown:*


<p align="center"><img src="https://raw.githubusercontent.com/Lipton2777/tf-aws-eKYC-Lipton-task-1/main/Screenshot%20from%202022-10-24%2010-50-08.png" /></p>

*In the mentioned application, I think, It’s best way to be develop a monolithic tightly coupled architecture.*

###   2. What type of database solution would be feasible for the application.
<b>Answer:</b>At a glance, We are usually use the NoSQL database for data storing & management and AWS S3 using for object storage to develop this applications.

###   3. What if the solution is a hybrid architecture where some country enforces that their user data has to be stored in a local database.

<b>Answer:</b>To protect against a loss of connectivity in case our customer gateway device becomes unavailable, we can set up a second Site-to-Site VPN connection to our VPC and virtual private gateway by using a second customer gateway device. By using redundant Site-to-Site VPN connections and customer gateway devices, we can perform maintenance on one of our devices while traffic continues to flow over the second customer gateway's Site-to-Site VPN connection.
The following diagram shows the two tunnels of each Site-to-Site VPN connection and two customer gateways.

<p align="center"><img src="https://raw.githubusercontent.com/Lipton2777/tf-aws-eKYC-Lipton-task-1/main/Flow-chart.png" /></p>


<p align="center">For this scenario, do the following:</p>

**a)** Set up a second Site-to-Site VPN connection by using the same virtual private gateway and creating a new customer gateway. The customer gateway IP address for the second Site-to-Site VPN connection must be publicly accessible.

**b)** Configure a second customer gateway device. Both devices should advertise the same IP ranges to the virtual private gateway. We use BGP routing to determine the path for traffic. If one customer gateway device fails, the virtual private gateway directs all traffic to the working customer gateway device. Dynamically routed Site-to-Site VPN connections use the Border Gateway Protocol (BGP) to exchange routing information between our customer gateways and the virtual private gateways. Statically routed Site-to-Site VPN connections require we to enter static routes for the remote network on our side of the customer gateway. BGP-advertised and statically entered route information allow gateways on both sides to determine which tunnels are available and reroute traffic if a failure occurs. We recommend that our configure to network to use the routing information provided by BGP (if available) to select an available path. The exact configuration depends on the architecture of our network.

###   4. If hybrid then what would be the connection medium between cloud and on-prem?
**Answer:** If deploy the hybrid architecture, Site-to-Site VPN connection configuring to interconnection between Cloud and On-premises network.

###   5. How will fault tolerance and global scalability be made sure?

**Answer:** Load balancing solutions allow an application to run on multiple network nodes, removing the concern about a single point of failure. For example, a system containing two production servers can use a load balancer to automatically shift workloads in the event of an individual server failure.

Fail-over solutions, on the other hand are used during the most extreme scenarios that result in a complete network failure. When these occur, a fail-over system is charged with auto-activating a secondary (Stand-by) platform to keep a web application running while the IT team brings the primary network back online.

###   6. Discuss about the application/infrastructure security measures and cost optimization strategies.

<b>Answer:</b> AWS provides several security capabilities and services to increase privacy and control network access.

These includes are:

<b>a) </b>Network firewalls built into Amazon VPC let you create private networks and control access to your instances or applications. Customers can control encryption in transit with TLS across AWS services.

<b>b) </b> Connectivity options that enable private, or dedicated, connections from your office or on-premises environment.

<b>c) </b> DDoS mitigation technologies that apply at layer 3 or 4 as well as layer 7. These can be applied as part of application and content delivery strategies.

<b>d) </b> Automatic encryption of all traffic on the AWS global and regional networks between AWS secured facilities.

<b>Cost optimization strategies:</b> The best way to start an IT cost optimization initiative is to focus on the activities with the best and quickest return on investment. Be careful about setting our time horizon for payoff too far out. IT and the business will change too fast to be looking much more than a year or two into the future. Technology is constantly changing, businesses reorganize and merge with other organizations and competitive forces and business strategies change.


###### 5 Key Strategies for IT Cost Optimization:


<b>a) Align initiatives with business priorities:</b>Rightsizing, auto-scaling, just-in-time provisioning and increased cost awareness are all activities that have a positive impact on the companies results.

<b>b) Gain visibility across your hybrid IT:</b>Optimizing the cost of IT services requires visibility of all the different components involved in the service delivery. But it’s actually pretty common for organizations to lack this visibility. Hybrid IT, involving both public cloud service and traditional on-premises data center operations is the new normal for almost every organization.

<b>c) Define cost structures: </b> To properly quantify cost savings, we need to define the cost structure for our operating environment. Breaking down the cost into individual components allows we to quickly valuate different alternatives and make sure that financial impact gets top priority. Optimization programs without continuous calculation of financial impact risk becoming simply a technical exercise and losing sight of the overarching goal to reduce the cost.

<b>d) Safely identify inefficiencies:  </b>The right-sizing efforts will have a direct impact on our overall cloud expenditure. An automated right-sizing process should be part of our continuous management process and could considerably reduce cloud cost.


<b>f) Allocate cost based on activity: </b>For public cloud resources this is straight forward. Charging for exactly what we are using is a fundamental mechanism of the framework, and not relaying that cost to the business units means missing a great opportunity to increase cost awareness.
