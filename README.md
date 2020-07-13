## Unchecked Growth - An introduction to serverless databases

The growth of cloud computing has been comprised of many, separate trends. A set of relatively new cloud services has formed via the intersection of two such trends: cloud databases and serverless computing. [Gartner](https://www.gartner.com/en/newsroom/press-releases/2019-07-01-gartner-says-the-future-of-the-database-market-is-the) has said that in two years, 3 out of every 4 databases will run on a cloud. Flexera's State of the Cloud ranked serverless computing as the fastest growing cloud service in [2018](https://www.suse.com/media/report/rightscale_2018_state_of_the_cloud_report.pdf) and the fourth highest in [2020](https://info.flexera.com/SLO-CM-REPORT-State-of-the-Cloud-2020), already being more widely used than popular workloads such as IoT and Machine Learning (it is also worth noting that Relational Databases as a Service were the highest used cloud services in both reports). Together, these make up the world of serverless databases, this article will introduce both serverless computing and serverless databasing concepts, and let you know how you can get started with your own instance!

|![299769BD-38FB-491C-AC9D-82F93F00D1C7.jpeg](https://github.com/PubChimps/Timescale/blob/master/images/299769BD-38FB-491C-AC9D-82F93F00D1C7.jpeg?raw=true) |  
|:--:| 
| *Flexera's State of the Cloud in both 2018 (left) and 2020 show the wide adoption of cloud databases and the growth of serverless technologies* |

### Serverless Computing

Serverless platforms allow for the dynamic deployment of production code, and are automatically scaled, managed, and maintained by cloud service providers on a pool of infrastucture. Utilizing these services can allow developers to focus on building the best code possible without having to worry about administration, and can provide cost saving as well, as charges only occur when the code is run and is often billed by the second or milliseconds. Infrastucture is deployed and charges are incured often by code written as *functions*, so many clouds (Azure Functions, Google Cloud Functions) offer their serverless platform with that name. The most popular, however, is provided by Amazon and called AWS Lambda. [Here](https://blog.timescale.com/blog/using-aws-lambda-with-timescale-cloud-for-iot-data/) is an example AWS Lambda can be used with TimescaleDB to ingest and store IoT data.

|![78231136-1E62-444A-8B72-3779D1D1F752.png](https://github.com/PubChimps/Timescale/blob/master/images/78231136-1E62-444A-8B72-3779D1D1F752.png?raw=true) |  
|:--:| 
| *[Taken from GCP](https://medium.com/google-cloud/serverless-on-google-cloud-platform-an-introduction-with-serverless-store-demo-41992dec085), less time spent on managing deployments and more can be spent on builind applications* |

### Serverless Databases

Many cloud database providers are taking advantage of the benefits described above, especially automatic scaling, by offering their databases in a serverless environment. Serverless databases are particularly helpful in use cases with dynamic data needs and unpredictable envirmonments. For instance, a retailer building out a new application and/or performing capacity planning for a holiday season may be unaware of the size of vm instance or number of containers necessary to accomodate a workload, and could offload these decisions to the autoscaling of a fully managed database by just setting the maximum number of computing resources an instance is allowed to grow to and having the service take care of the rest. Popular examples of serverless relational databases include [Amazon Aurora](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&ved=2ahUKEwiepaSLycnqAhUCWqwKHb1KCiwQFjABegQIAhAB&url=https%3A%2F%2Faws.amazon.com%2Frds%2Faurora%2Fserverless%2F&usg=AOvVaw17Gf02EzB4ixJGGYhdrF0U), [Google BigQuery](https://cloud.google.com/bigquery), and [Azure SQL Database Serverless](https://techcommunity.microsoft.com/t5/azure-sql-database/optimize-price-performance-with-compute-auto-scaling-in-azure/ba-p/966149).

### How to get started

The serverless databases mentioned above have many migration options and [documention](https://cloud.google.com/bigquery-transfer/docs) to get started in their serverless enivronment. If you are questioning whether or not your data environment could benefit from a move to serverless, ask us on [Slack](https://slack.timescale.com). Just like other cloud services, these databases will need to be monitored when they are deployed and used. For more information check out the Timescale Tutorial [Monitoring ang Logging AWS Serverless Applications with CloudWatch, Prometheus, and TimescaleDB](https://github.com/PubChimps/Timescale/edit/master/README.md).

|![87364E64-A0F7-4154-B6DB-6535F83138B0.png](https://github.com/PubChimps/Timescale/blob/master/images/87364E64-A0F7-4154-B6DB-6535F83138B0.png?raw=true) |  
|:--:| 
| *The path from AWS Serverless applications to Prometheus is through AWS CloudWatch, as [sysdig](https://sysdig.com/blog/monitor-aws-fargate-prometheus/#the-rise-of-serverless) demonstrate* |

### Summary

Serverless computing allows all the deployment tasks of an application to be performed by a cloud serivce provider, saving developers time and money as costs for idle time can often be eliminated. These benefits can be extended to databases, and many clouds have serverless offerings. These serverless databases can be monitored with Prometheus and TimescaleDB.
