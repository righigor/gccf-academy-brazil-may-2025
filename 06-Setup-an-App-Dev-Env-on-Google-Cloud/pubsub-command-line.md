# Pub/Sub: Qwik Start - Command Line

1. Create a Pub/Sub topic:
   ```bash
   gcloud pubsub topics create myTopic
   ```
2. Create a Pub/Sub subscription:
   ```bash
   gcloud  pubsub subscriptions create --topic myTopic mySubscription
   ```
3. Publish a message to the topic:
   ```bash
   gcloud pubsub topics publish myTopic --message "Hello"
   ```
