# Risk-assessment
# Name :Mohamed Aathil M 
# Reg no. : 212225040246

## EXPERIMENT 5
## AUDITING CLOUD ACTIVITY USING AWS CLOUDTRAIL
### Aim 
To audit and monitor cloud activity in AWS using AWS CloudTrail by viewing and analyzing recorded AWS events and identifying important audit information such as user identity, event name, event time, AWS service, region, and operation status.
1. Requirements
•	AWS Account 
•	Web Browser 
•	Internet Connection 
•	Amazon S3 access 
•	AWS CloudTrail 

## PART A — ACCESS AWS CLOUDTRAIL
# Step 1: Login to AWS
1.	Open the AWS Management Console. 
2.	Sign in using your AWS account. 
3.	In the AWS search bar, type CloudTrail. 
4.	Select AWS CloudTrail. 

<img width="1677" height="476" alt="Screenshot 2026-09-06 184749" src="https://github.com/user-attachments/assets/b6a71d5d-856e-4c5d-9c66-4c1339f2c3c7" />


# Step 2: Open Event History
1.	In the CloudTrail navigation menu, select Event history. 
2.	CloudTrail displays recent AWS activity. 
3.	Review the available events. 
The Event History page may display information such as:
•	Event time 
•	Username 
•	Event name 
•	Event source 
•	Resource type 
•	Resource name 

<img width="835" height="450" alt="Screenshot 2026-09-06 184800" src="https://github.com/user-attachments/assets/e7496ab5-e76a-456f-867d-643ed7ad60f2" />

## PART B — ANALYZE A CLOUDTRAIL EVENT
# Step 3: Select an Event
1.	From the Event History list, select an S3-related event. 
2.	Click the event to open its details. 
3.	Examine the event information and the event record/JSON. 
For this experiment, a CreateBucket event can be used.

<img width="838" height="447" alt="Screenshot 2026-09-06 184812" src="https://github.com/user-attachments/assets/eb149411-22da-4600-ad40-0141596510c2" />

# Step 4: Analyze the CreateBucket Event
The CreateBucket event indicates that an Amazon S3 bucket creation operation occurred.
Record the following information:
| Parameter | Observation |
|---|---|
| Event Time | August 04, 2026, 08:59:49 (UTC+05:30) |
| User Name | root |
| Event Name | CreateBucket |
| Event Source | s3.amazonaws.com |
| AWS Region | ap-south-1 |
| Read-only | false |
| Error Code | - |
| Activity | S3 bucket creation |

Meaning of Important Fields
Field	Meaning
Event Time	Time at which the activity occurred
User Name	User/identity associated with the activity
Event Name	AWS operation that was performed
Event Source	AWS service that generated the event
AWS Region	Region where the activity occurred
Read-only	Indicates whether the event was only a read operation or involved a change
Error Code	Indicates whether an error occurred

## PART C — IDENTIFY ANOTHER CLOUDTRAIL EVENT
# Step 5: Select Another Event
1.	Return to CloudTrail → Event history. 
2.	Select another event. 
3.	Open its details. 
4.	Record the important fields. 
For example, an event such as:
AutomatedDefaultVpcCreation may be present.
This event is associated with Amazon EC2.

<img width="1775" height="886" alt="image" src="https://github.com/user-attachments/assets/6b4a2b72-e185-4c3e-9d7c-f2b42da89f6b" />

# Step 6: Analyze the Second Event
Record:
| Parameter | Observation |
|---|---|
| Event Time | August 04, 2026, 09:12:25 (UTC+05:30) |
| User Name | - |
| Event Name | AutomatedDefaultVpcCreation |
| Event Source | ec2.amazonaws.com |
| AWS Region | ap-south-1 |
| Read-only | false |
| Error Code | - |
| Activity | Automated default VPC creation |



## PART D — COMPARE THE EVENTS
# Step 7: Prepare the Audit Comparison
Compare the two CloudTrail events.
| Parameter | Event 1 | Event 2 |
|---|---|---|
| Event Time | August 04, 2026, 08:59:49 (UTC+05:30) | August 04, 2026, 09:12:25 (UTC+05:30) |
| User Name | root | - |
| Event Name | CreateBucket | AutomatedDefaultVpcCreation |
| Event Source | s3.amazonaws.com | ec2.amazonaws.com |
| AWS Region | ap-south-1 | ap-south-1 |
| Read-only | false | false |
| Error Code | - | - |
| Activity | S3 bucket creation | Automated VPC creation |

## PART E — SECURITY AUDIT ANALYSIS
# Step 8: Identify Who, What, When and Where
For each event, identify: WHO?
Who or which identity performed/generated the activity? WHAT?
What AWS operation was performed? WHEN?
At what date and time did the activity occur? WHERE?
In which AWS Region did the activity occur? RESULT?
Was the operation successful or did it generate an error?
# Step 9: Prepare the Final Audit Table
Students should prepare a final table similar to the following:
| Event Time | User | Event Name | Service | Region | Read-only | Result | Activity |
|---|---|---|---|---|---|---|---|
| August 04, 2026, 08:59:49 (UTC+05:30) | root | CreateBucket | Amazon S3 | ap-south-1 | false | Successful | S3 bucket creation |
| August 04, 2026, 09:12:25 (UTC+05:30) | - | AutomatedDefaultVpcCreation | Amazon EC2 | ap-south-1 | false | Successful | Automated VPC creation |

## PART F — SCREENSHOTS TO SUBMIT
Students should capture the following screenshots:
1.	AWS CloudTrail Dashboard 
2.	CloudTrail Event History 
3.	CreateBucket Event Details 
4.	Second CloudTrail Event Details 
5.	Final Audit/Observation Table

## RESULT
The cloud activities in AWS were successfully audited using AWS CloudTrail Event History. Different AWS events were examined based on event time, user identity, event name, event source, AWS Region, read-only status, and error status. The experiment demonstrated how AWS CloudTrail provides an audit trail for monitoring, accountability, and investigation of cloud activities.
