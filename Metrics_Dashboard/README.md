**Note:** For the screenshots, you can store all of your answer images in the `answer-img` directory.

## Verify the monitoring installation

 run `kubectl` command to show the running pods and services for all components. Take a screenshot of the output and include it here to verify the installation

![Alt text](./answer-img/podsandservices.png?raw=true "Pods-Services")

## Setup the Jaeger and Prometheus source
Expose Grafana to the internet and then setup Prometheus as a data source. Provide a screenshot of the home page after logging into Grafana.

![Alt text](./answer-img/grafana.png?raw=true "grafana")

![Alt text](./answer-img/prometheuskubernetes.png?raw=true "Kubernetes")

## Create a Basic Dashboard
Create a dashboard in Grafana that shows Prometheus as a source. Take a screenshot and include it here.
![Alt text](./answer-img/prometheusdatasource.png?raw=true "Data Source")

## Describe SLO/SLI
Describe, in your own words, what the SLIs are, based on an SLO of *monthly uptime* and *request response time*.

Service-Level Objectives (SLOs)are a clear objective or goal.  Service-level indicators (SLIs) . Once we have a clear definition and objective for the is a measure the performance to the goal.  An SLI for montly uptime would be a measurement for montly uptime, say 99.9% (three 9s). Latency SLI could be the time between request and response.  The time measured should be within 95% of the required latency (this is an example). 

The percentages above are ratio - of a measurement to a given amount of time (the measured uptime per year). 

## Creating SLI metrics.
It is important to know why we want to measure certain metrics for our customer. Describe in detail 5 metrics to measure these SLIs. 

| SLO           | SLI           |
| ------------- | ------------- |
| Uptime        | Time service is active  |
| Latency       | Time of response after request  |
| Failure Rate  | # of failures in a time period  |
| CPU Usage     | Percent of CPU used in a time period  |
| Network Bandwidth | Network bandwidth in a time period  |

## Create a Dashboard to measure our SLIs
Create a dashboard to measure the uptime of the frontend and backend services We will also want to measure to measure 40x and 50x errors. Create a dashboard that show these values over a 24 hour period and take a screenshot.

![Alt text](./answer-img/custommetrics.png?raw=true "My dashboard")

## Tracing our Flask App
 We will create a Jaeger span to measure the processes on the backend. Once you fill in the span, provide a screenshot of it here.

## Jaeger in Dashboards
Now that the trace is running, let's add the metric to our current Grafana dashboard. Once this is completed, provide a screenshot of it here.
![Alt text](./answer-img/backendjaeger.png?raw=true "Mapplication")

## Report Error
Using the template below, write a trouble ticket for the developers, to explain the errors that you are seeing (400, 500, latency) and to let them know the file that is causing the issue.

TROUBLE TICKET

Name: HTTP Error 500

Date: 11/12/21

Subject: Unknown server error

Affected Area: Backend star api endpoint

Severity: HIGH

Description: Unknown error - internal server error


## Creating SLIs and SLOs
We want to create an SLO guaranteeing that our application has a 99.95% uptime per month. Name three SLIs that you would use to measure the success of this SLO.

* Uptime - 99.95% service up and running
* Http Error Rate - < 95%
* CPU and Memory - never higher than 70% of capacity
* Network Bandwidth- less than 5B/s

## Building KPIs for our plan
Now that we have our SLIs and SLOs, create KPIs to accurately measure these metrics. We will make a dashboard for this, but first write them down here.
Now that we have our SLIs and SLOs, create KPIs to accurately measure these metrics. We will make a dashboard for this, but first write them down here.

* Services Uptime 
    * Backend uptime + Frontend uptime
* Http Error rate
    * Backend and frontend 
* Network Bandwidth < 5B/s
* Resource capacity < 70% capacity     
    * CPU 
    * Memory 


| SLO           | SLI           |
| ------------- | ------------- |
| Uptime        | Time service is active  |
| Memory Usage  | Percent of Memory used in a time period
| Failure Rate  | # of failures in a time period  |
| CPU Usage     | Percent of CPU used in a time period  |
| Network Bandwidth | Network bandwidth in a time period  |
## Final Dashboard
 Create a Dashboard containing graphs that capture all the metrics of your KPIs and adequately representing your SLIs and SLOs. Include a screenshot of the dashboard here, and write a text description of what graphs are represented in the dashboard.  

![Alt text](./answer-img/KPIspage1.png?raw=true "Mapplication")
![Alt text](./answer-img/KPIspage2.png?raw=true "Mapplication")
![Alt text](./answer-img/KPIspage3.png?raw=true "Mapplication")