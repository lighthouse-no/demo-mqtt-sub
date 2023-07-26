# MQTT Subscriber Example App

A simple Rust-based app that publishes messages to the public MQTT server at `tcp://broker.emqx.io:1883`

This app works with in conjunction with a corresponding subscriber app.

![MQTT Demo Pub/Sub App](https://github.com/lighthouse-no/demo-mqtt-pub/blob/main/img/architecture.png)

## Usage

1. Push this app to Cloud Found<br>`cf push`
1. Watch the CF logs `cf logs mqtt-demo-sub`

When the corresponding publisher app runs, you will see log messages similar to the following

```log
2023-07-26T15:27:39.36+0100 [APP/PROC/WEB/0] OUT rust/mqtt: Hello world! 0
2023-07-26T15:27:39.45+0100 [APP/PROC/WEB/0] OUT rust/test: Hello world! 1
2023-07-26T15:27:39.54+0100 [APP/PROC/WEB/0] OUT rust/mqtt: Hello world! 2
2023-07-26T15:27:39.63+0100 [APP/PROC/WEB/0] OUT rust/test: Hello world! 3
2023-07-26T15:27:39.73+0100 [APP/PROC/WEB/0] OUT rust/mqtt: Hello world! 4
```

To terminate the subscriber, deleted the deployed app in Cloud Foundry