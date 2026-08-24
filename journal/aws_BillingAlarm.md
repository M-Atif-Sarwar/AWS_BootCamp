# Biling Alarm

## step 1 set Sns ##

## SNS simple notification service 

## create sns topic
aws sns create --name Billing alarm

## we need  suscribe sns sevcie ## 
aws sns subscribe \
   --topic-arn topic name
   --protocol email \
   --notification-endpoint your email


## step 3 create a Alarm ##
aws cloudwatch put-metric-alarm \
    --region us-east-1 \
    --cli-input-json file://billing-alarm-config.json