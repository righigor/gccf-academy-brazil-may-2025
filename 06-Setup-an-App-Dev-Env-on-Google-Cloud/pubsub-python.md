# Pub/Sub: Qwik Start - Python

1. Create a virtual environment:
   ```bash
   sudo apt-get install -y virtualenv
   ```
  Build a virtual environment:
   ```bash
   virtualenv venv
   ```
   Activate the virtual environment:
   ```bash
   source venv/bin/activate
   ```
2. Install the Pub/Sub client library:
   ```bash
   pip install --upgrade google-cloud-pubsub
   ```
  Get the sample code:
   ```bash
   git clone https://github.com/googleapis/python-pubsub.git
   ```
3.  Run the publisher script to create Pub/Sub topic:
    ```bash
    python publisher.py $GOOGLE_CLOUD_PROJECT create MyTopic
    ```
  List the topics:
    ```bash
    python publisher.py $GOOGLE_CLOUD_PROJECT list
    ```
4. Run the subscriber script to create Pub/Sub subscription:
    ```bash
    python subscriber.py $GOOGLE_CLOUD_PROJECT create MyTopic MySub
    ```
5. Publish a message to the topic:
    ```bash
    gcloud pubsub topics publish MyTopic --message "Hello"
    ```
6. Run the subscriber script to receive messages:
    ```bash
    python subscriber.py $GOOGLE_CLOUD_PROJECT receive MySub
    ```