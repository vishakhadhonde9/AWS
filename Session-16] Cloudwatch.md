# Cloudwatch -
- Amazon CloudWatch is a web service that enables you to monitor and manage various metrics and configure alarm actions based on data from those metrics.
- Sends notification if anything goes wrong.
- CloudWatch uses metrics to represent the data points for your resources. AWS services send metrics to CloudWatch.
- CloudWatch then uses these metrics to create graphs automatically that show how performance has changed over time.

## Cloudwatch Dashboard-
- CloudWatch dashboards are customizable home pages in the CloudWatch console that you can use to monitor your resources in a single view, even those resources that are spread across different Regions.
- You can use CloudWatch dashboards to create customized views of the metrics and alarms for your AWS resources.

## CloudWatch alarms -
- With CloudWatch, you can create alarms that automatically perform actions if the value of your metric has gone above or below a predefined threshold.
- What are the 3 states of the CloudWatch metric alarm:
    - OK—The metric or expression is within the defined threshold.
    - ALARM—The metric or expression is outside of the defined threshold.
    - INSUFFICIENT_DATA—The alarm has just started, the metric is not available, or not enough data is available for the metric to determine the alarm state.

  ![image](https://github.com/user-attachments/assets/93bade2a-c808-48e5-95ce-934e4c93a93e)

## Cloudwatch Logs -
- CloudWatch Logs enables you to centralize the logs from all of your systems, applications, and AWS services that you use, in a single, highly scalable service.
- It allows you to monitor, store, and access log files from various AWS services.


## Cloudwatch Events-
- CloudWatch Events delivers a near real-time stream of system events that describe changes in AWS resources.
- CloudWatch Events becomes aware of operational changes as they occur.
- CloudWatch Events responds to these operational changes and takes corrective action.

# Simple Notification Service (SNS)-
- SNS is a managed service that provides message delivery from publishers to subscribers (also known as producers and consumers).
- An SNS topic is a communication channel that allows you to group multiple recipients (subscribers) under a single entity.
