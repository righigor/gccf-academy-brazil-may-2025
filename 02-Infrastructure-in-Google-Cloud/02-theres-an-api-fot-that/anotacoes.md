Aplication programming Inteface (API)
  A clean, well-defined interface;
  Underlying implementation can change;
  Changes to the API are made with versions;

What is a REST API?
  Representational State Transfer;
  A set of constraints a service must comply with;
  An API that uses HTTP requests to GET, PUT, POST and DELETE data;
  Designed to set up a format for applications to communicate;
  Great for cloud applications beacaus they are stateless;
  Authentication via OAuth and security by leveraging tokens.

Apigee API Management
  Specific focus on business problems, like rate limiting, quotas and analytics;
  Many Apigee API Management users provide a software service to other companies;
  Backend services for Apigee API Management don't need to be in Google Cloud;

Challenges to data ingestion
  1 - Data can be streamed from many diffrent methods and devices;
  2 - It can be hard to distribute event messages to the right subscribers;
  3 - Data can arrive quickly and at high volumes;
  4 - Ensuring services are reliable, secure, and perform as expected;

Pub/Sub features
  Ensures at-least-once delivery;
  No provisioning is required;
  APIs are open;
  Global by default;
  Offers end-to-end encryption;

LABS
  Pub/Sub: Qwik Start - Python:
    Learn the basics of Pub/Sub;
    Create and list a Pub/Sub topic;
    Create and list a Pub/Sub subscription;
    Publish messages to a topic;
    Use a pull subscriber to output individual topic messages;
