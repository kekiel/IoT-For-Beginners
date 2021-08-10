# IoT for Beginners - A Curriculum

Forked 10.08.2021 from https://github.com/microsoft/IoT-For-Beginners

Azure Cloud Advocates at Microsoft are pleased to offer a 12-week, 24-lesson curriculum all about IoT basics. Each lesson includes pre- and post-lesson quizzes, written instructions to complete the lesson, a solution, an assignment and more. Our project-based pedagogy allows you to learn while building, a proven way for new skills to 'stick'.

The projects cover the journey of food from farm to table. This includes farming, logistics, manufacturing, retail and consumer - all popular industry areas for IoT devices.

![A road map for the course showing 24 lessons covering intro, farming, transport, processing, retail and cooking](sketchnotes/Roadmap.jpg)

> Sketchnote by [Nitya Narasimhan](https://github.com/nitya). Click the image for a larger version.

> **Teachers**, we have [included some suggestions](for-teachers.md) on how to use this curriculum. If you would like to create your own lessons, we have also included a [lesson template](lesson-template/README.md).

> **Students**, to use this curriculum on your own, fork the entire repo and complete the exercises on your own, starting with a pre-lecture quiz, then reading the lecture and completing the rest of the activities. Try to create the projects by comprehending the lessons rather than copying the solution code; however that code is available in the /solutions folders in each project-oriented lesson. Another idea would be to form a study group with friends and go through the content together. For further study, we recommend [Microsoft Learn](https://docs.microsoft.com/users/jimbobbennett/collections/ke2ehd351jopwr?WT.mc_id=academic-17441-jabenn).

For a video overview of this course, check out this video:

[![Promo video](https://img.youtube.com/vi/bccEMm8gRuc/0.jpg)](https://youtube.com/watch?v=bccEMm8gRuc "Promo video")

> 🎥 Click the image above for a video about the project!

## Hardware

The [hardware page](./hardware.md), including links to buy complete kits from our friends at Seeed Studio.

## Each lesson includes:

- sketchnote
- optional supplemental video
- pre-lesson warmup quiz
- written lesson
- for project-based lessons, step-by-step guides on how to build the project
- knowledge checks
- a challenge
- supplemental reading
- assignment
- post-lesson quiz

> **A note about quizzes**: All quizzes are contained [in this app](https://brave-island-0b7c7f50f.azurestaticapps.net), for 48 total quizzes of three questions each. They are linked from within the lessons but the quiz app can be run locally; follow the instruction in the `quiz-app` folder. They are gradually being localized.

## Lessons

|     | Project Name | Concepts Taught | Learning Objectives | Linked Lesson |
| :-: | :----------: | :-------------: | ------------------- | :-----------: |
| 01 | [Getting started](./1-getting-started) | Introduction to IoT | Learn the basic principles of IoT and the basic building blocks of IoT solutions such as sensors and cloud services whilst you are setting up your first IoT device | [Introduction to IoT](./1-getting-started/lessons/1-introduction-to-iot/README.md) |
| 02 | [Getting started](./1-getting-started) | A deeper dive into IoT | Learn more about the components of an IoT system, as well as microcontrollers and single-board computers | [A deeper dive into IoT](./1-getting-started/lessons/2-deeper-dive/README.md) |
| 03 | [Getting started](./1-getting-started) | Interact with the physical world with sensors and actuators | Learn about sensors to gather data from the physical world, and actuators to send feedback, whilst you build a nightlight | [Interact with the physical world with sensors and actuators](./1-getting-started/lessons/3-sensors-and-actuators/README.md) |
| 04 | [Getting started](./1-getting-started) | Connect your device to the Internet | Learn about how to connect an IoT device to the Internet to send and receive messages by connecting your nightlight to an MQTT broker | [Connect your device to the Internet](./1-getting-started/lessons/4-connect-internet/README.md) |
| 05 | [Farm](./2-farm) | Predict plant growth | Learn how to predict plant growth using temperature data captured by an IoT device | [Predict plant growth](./2-farm/lessons/1-predict-plant-growth/README.md) |
| 06 | [Farm](./2-farm) | Detect soil moisture | Learn how to detect soil moisture and calibrate a soil moisture sensor | [Detect soil moisture](./2-farm/lessons/2-detect-soil-moisture/README.md) |
| 07 | [Farm](./2-farm) | Automated plant watering | Learn how to automate and time watering using a relay and MQTT | [Automated plant watering](./2-farm/lessons/3-automated-plant-watering/README.md) |
| 08 | [Farm](./2-farm) | Migrate your plant to the cloud | Learn about the cloud and cloud-hosted IoT services and how to connect your plant to one of these instead of a public MQTT broker | [Migrate your plant to the cloud](./2-farm/lessons/4-migrate-your-plant-to-the-cloud/README.md) |
| 09 | [Farm](./2-farm) | Migrate your application logic to the cloud | Learn about how you can write application logic in the cloud that responds to IoT messages | [Migrate your application logic to the cloud](./2-farm/lessons/5-migrate-application-to-the-cloud/README.md) |
| 10 | [Farm](./2-farm) | Keep your plant secure | Learn about security with IoT and how to keep your plant secure with keys and certificates | [Keep your plant secure](./2-farm/lessons/6-keep-your-plant-secure/README.md) |
| 11 | [Transport](./3-transport) | Location tracking | Learn about GPS location tracking for IoT devices | [Location tracking](./3-transport/lessons/1-location-tracking/README.md) |
| 12 | [Transport](./3-transport) | Store location data | Learn how to store IoT data to be visualized or analysed later | [Store location data](./3-transport/lessons/2-store-location-data/README.md) |
| 13 | [Transport](./3-transport) | Visualize location data | Learn about visualizing location data on a map, and how maps represent the real 3d world in 2 dimensions | [Visualize location data](./3-transport/lessons/3-visualize-location-data/README.md) |
| 14 | [Transport](./3-transport) | Geofences | Learn about geofences, and how they can be used to alert when vehicles in the supply chain are close to their destination | [Geofences](./3-transport/lessons/4-geofences/README.md) |
| 15 | [Manufacturing](./4-manufacturing) | Train a fruit quality detector | Learn about training an image classifier in the cloud to detect fruit quality | [Train a fruit quality detector](./4-manufacturing/lessons/1-train-fruit-detector/README.md) |
| 16 | [Manufacturing](./4-manufacturing) | Check fruit quality from an IoT device | Learn about using your fruit quality detector from an IoT device | [Check fruit quality from an IoT device](./4-manufacturing/lessons/2-check-fruit-from-device/README.md) |
| 17 | [Manufacturing](./4-manufacturing) | Run your fruit detector on the edge | Learn about running your fruit detector on an IoT device on the edge | [Run your fruit detector on the edge](./4-manufacturing/lessons/3-run-fruit-detector-edge/README.md) |
| 18 | [Manufacturing](./4-manufacturing) | Trigger fruit quality detection from a sensor | Learn about triggering fruit quality detection from a sensor | [Trigger fruit quality detection from a sensor](./4-manufacturing/lessons/4-trigger-fruit-detector/README.md) |
| 19 | [Retail](./5-retail) | Train a stock detector | Learn how to use object detection to train a stock detector to count stock in a shop | [Train a stock detector](./5-retail/lessons/1-train-stock-detector/README.md) |
| 20 | [Retail](./5-retail) | Check stock from an IoT device | Learn how to check stock from an IoT device using an object detection model | [Check stock from an IoT device](./5-retail/lessons/2-check-stock-device/README.md)  |
| 21 | [Consumer](./6-consumer) | Recognize speech with an IoT device | Learn how to recognize speech from an IoT device to build a smart timer | [Recognize speech with an IoT device](./6-consumer/lessons/1-speech-recognition/README.md) |
| 22 | [Consumer](./6-consumer) | Understand language | Learn how to understand sentences spoken to an IoT device | [Understand language](./6-consumer/lessons/2-language-understanding/README.md) |
| 23 | [Consumer](./6-consumer) | Set a timer and provide spoken feedback | Learn how to set a timer on an IoT device and give spoken feedback on when the timer is set and when it finishes | [Set a timer and provide spoken feedback](./6-consumer/lessons/3-spoken-feedback/README.md) |
| 24 | [Consumer](./6-consumer) | Support multiple languages | Learn how to support multiple languages, both being spoken to and the responses from your smart timer | [Support multiple languages](./6-consumer/lessons/4-multiple-language-support/README.md) |

### Slides

There are slide decks for some of the lessons in the [slides](./slides) folder.
