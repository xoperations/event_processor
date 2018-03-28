# Event Processor

Provides basic functionality to insert new problem alerts to elasticsearch (live_alert_index) and update existing problem alerts.
If a recovery alert is received for an existing problem alert, problem alert is removed from live_alert_index and will be reindexed 
in historical_alert_index.

## Running application
python event_processor.py

## Docker commands 
docker build -t eventlistener . 
docker run -it eventlistener 

## upload docker conainer to GCP 
gcloud container builds submit --tag gcr.io/xops-poc/eventlistener:1.0 .

