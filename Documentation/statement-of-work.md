## Project Description

This project aims at upgrading and enhancing OpenMainframeProject/ade, by implementing support for Spark logs. The ADE project was started in early 2016, with the purpose of making prevalent Linux systems more stable by implementing a framework to help in quick traceablility of the source of an unusual occurrence by predicting anomalous logs from Linux Syslogs. Analysis of the anomalous logs can be a good indication of the root of the problem, thus helping in eradicating such issues. This is specially important when working in an environment where every second is important, and fatal system crashes can mean the loss of tens of thousands of dollars. Such systems, for example stock markets, can be hugely benefited by a system that identifies the origin of the anomaly, which can be the cause of a fatal crash.
However, ADE supports only Linux Syslogs at the moment. With this project, I aim to enhance ADE by expanding it to support middleware areas, such as nginx/spark logs. I hope this project is a solid move towards more robust anomaly detection. It should also help in showcasing the ability of ADE to deliver results in the case of comparatively more complicated logs.

## Current State

[ade](https://github.com/openmainframeproject/ade) has proved to be very useful when applied to linux syslogs. However, it doesn't
support any other log structure at the moment. This project is a first step towards adding support for more complicated (middleware) logs. 

## Value

There are a lot of areas where anomaly detection can have tremendous value. Robust anomaly detection can help us identify the source
of the system crash and reach the root of the problem efficiently. While ade has shown to be very effective, there still remain a 
number of avenues where such a system can have more generalized usage. Web servers, for instance, handle a lot of traffic and fatal
crashes here can lead to huge downtime. Identifying the source of the issue is another cumbersome process within itself.

## Business Requirements

- Add option to introduce spark logs in ade.
- Implement parsers for ade logs
- Create and upload the data to a derby database.
- Verify, train, analyze and repeat until we get reasonable results to prove the effective of ade under such settings.
