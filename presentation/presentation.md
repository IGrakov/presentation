# Presentation of Microservices
## created by Ivan Grakov
[Link to Reveal presentation deploy](https://5fec79c6d3088e0007840c9a--igrakov-presentation.netlify.app/)

[Link to YouTube video](https://youtu.be/o3PiXGqMX9M)

## Introduction
Hello, my dear friends. My name is Ivan Grakov and today I would like to talk about microservices. However, to understand advantages of microservices we first should talk about some preliminary things.

## What do we need software for
And we start with the point how software is developed. If we are talking about industrial software, that is software for real world use, not software as a classroom exercise or something developed for training purposes, in many cases it requires effort of thousands of people and years of development. Even small mobile applications often surprisingly require a big team for their creation. So software development in the great majority of cases is not an individual work, it is a teamwork of business analysts, developers, testers, support specialists, project managers and many other people.

## Software development cycle
Now, it is time to say a few words about software development cycle and in broader sense software lifecycle. No matter which methodology is used, waterfall or agile, this cycle is followed explicitly or implicitly when developing any piece of software.

Some people think that software development relates only to development or coding part. Those with deeper understanding add business analysis or planning stage as well as testing to the cycle. However, when software coding is completed and the software passes all tests, it is still far from the end. Purpose of any industrial software is not development of the software itself. Definitely, there can be exception, but in general, software does not exist per se. It must meet certain purpose. And this purpose can be met only when software is deployed and can be used by end users.

In fact, this is not the end, as a need to fix bugs, improve performance, add new functionality makes us to go again to planning stage and repeat everything in cycles till we make decision to stop using and abandon the software.

## Monolith architecture features
Now we almost got to microservices. As opposed to microservices architecture the traditional one is the monolith or monolithic architecture. What are the main features of such architecture?

Monolith application is a single application that performs all required functionality. It uses one database. It is organized around technology layers, which means that the application is divided into several layers, for instance user interface layer responsible for interaction with users, business logic layer where application logic resides, persistence layer responsible for long-term storage of data.

What is important from software development cycle point of view is that we must deploy the entire application in one go.

Also one technology stack is used for the entire application. It influences how quickly we can scale our development capacity. This means that if a company needs to make a modification to an application for whatever reason and there is no free team with competencies in relevant technologies, such modification has to be put in a development queue. Free teams with competencies in other technologies cannot be added to the project. In addition, teams need long time to get to know significant part of the application to be able to produce working result and become productive.

## Microservces architecture features
Finally, we can describe features of microservices architecture. Basically, with microservicies we split our application into a set of small applications interacting with each other, each performing minimal number of functions, ideally just one. Such functions are organized around business capabilities. Here is an example of microservices at well known company Uber. However, granularity of microservices can be much finer. For example, at Netflix. And even finer, for example at Amazon. Each microservice is independent of others and stores its data in an independent database. Each microservice is deployed separately, which greatly simplifies deployment process. If we re-deploy a microservice, we do not have to stop the entire application and re-deployment process significantly accelerates. Microservices can be also deployed in multiple copies, so when re-deploying copies of a microservice one by one we can achieve zero downtime of our application. Such deployments may be made very frequently, many times a day. One of the trendsetters Amazon even in 2011 claimed software deployment nearly every 12 seconds. Nowadays it is made even more frequently. It means that even smallest change in functionality is being almost in no time thoroughly tested and available to end users.

## Microservices pros
Another advantage of microservices approach is that for each microservice we can choose different stack of technologies independently on what other parts of application are based on. A microservice can be imagined as a black box for which we know only external behavior or its interfaces and do not care what is going on inside. In this case microservices can be developed by independent teams with different technical competences. Development teams become productive much faster as in order to produce working result they need to know just a small part of an application.

## Microservices cons
Definitely, microservices architecture as any other one has its own downsides. Developers must deal with additional complexity of creating a distributed system. Any requests than span across multiple microservices provide additional complexity to coordination between teams. If there are many microservices there is significant overhead of communication between them. Though deployment can be made much faster and more frequently complexity of the deployment if higher. There is also additional operational complexity once application is deployed. There are additional issues that must be dealt with like partial or full service unavailability, which can be addressed via creation of additional instances of microservices.

## Conclusion
So based on the above, there is no one fits all recipe. Monolithic architecture is good for small applications, for startups with small teams and homogeneous technical expertise, for projects with small resource base. However, for development of complex large-scale systems and for companies with multiple teams with heterogeneous skills microservices architecture is a better choice.
