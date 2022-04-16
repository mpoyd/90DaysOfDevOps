---
title: '#90DaysOfDevOps - Plan > Code > Build > Testing > Release > Deploy > Operate > Monitor > - Day 5'
published: false
description: 90DaysOfDevOps - Plan > Code > Build > Testing > Release > Deploy > Operate > Monitor >
tags: "devops, 90daysofdevops, learning"
cover_image: null
canonical_url: null
id: 1048830
---
## Plan > Code > Build > Testing > Release > Deploy > Operate > Monitor > 

Today we are going to focus on the individual steps from start to finish and the continous cycle of an Application in a DevOps world. 

![DevOps](Images/Day5_DevOps8.png)

### Plan:

It all starts with the planning process, this is where the development team gets together and figures out what types of features and bug fixes they're going to roll out in their next sprint. This is an opportunity for you as a DevOps Engineer to get involved with that and learn the sort of things that are coming your way that you need to be involved with, and also an opportunity to influence their decisions or their path, and help them work with the infrastructure that you've built, or in case they're not on that path, you can steer them towards something that's going to work better for them.
One key thing to point out here is that developers or the software engineering team are your customers as a DevOps engineer, so this is your opportunity to work with your customers before they go down a bad path.

### Code:

Now once that planning session's done they're going to start writing code, you may or may not be involved a whole lot with this process, but one of the ways you may get involved is, whenever they're writing code, you can help them better understand the infrastructure, so that they know what services are available and how to best talk with those services, once they're done they'll merge that code into the repository.

### Build:

This is where we'll kick off the first of our automation processes because we're going to take their code and we're going to build it depending on what language they're using it may be transpiling it or compiling it or it might be creating a docker image from that code either way we're going to go through that process using our ci cd pipeline 

## Testing:

Once we've built it we're going to run some tests on it, now the development team usually writes the test but you may have some input in what tests get written.
We need to run those tests as a way for us to try and minimise introducing problems out into production, testing doesn't guarantee that, but we want to get as close to a guarantee as we can that we're not introducing new bugs, and that we're not breaking things that used to work.

## Release:

Once those tests pass we're going to do the release process and depending again on what type of application you're working on this may be a non-step. The code may just live in the GitHub repo or the git repository or wherever it lives but it may be the process of taking your compiled code or the docker image that you've built and putting it into a registry or a repository where it's accessible by your production servers for the deployment process 

## Deploy:

Deployement is the next step, and the end game of this whole thing.
We put the code into production, and it's not until this point that our business actually realizes the value from all the time effort and hard work that you and the software engineering team have put into this product up to this point. 

## Operate:

Once it's deployed we are going to operate it, and operating it may involve something like, you start getting calls from your customers that they're all annoyed that the site's running slow or their application is running slow, so you need to figure out why that is and then possibly build auto-scaling you know to handle increase the number of servers available during peak periods and decrease the number of servers during off-peak periods, either way that's all operational type metrics, another operational thing that you do is include a feedback loop from production back to your ops team letting you know about key events that happened in production such as a deployment, this may or may not get automated depending on your environment the goal is to always automate it when possible there are some environments where you possibly need to do a few steps before you're ready to do that but ideally you want to deploy automatically as part of your automation process but if you're doing that it might be a good idea to include in your operational steps some type of notification so that your ops team knows that a deployment has happened 

## Monitor:

All of the above parts lead to the final step: monitoring.
It is especially needed for operational issues, auto-scaling and troubleshooting.
You simply don't know if there's a problem when you don't have monitoring in place to tell you that there's a problem.
Some of the things you might build monitoring for are memory utilization CPU utilization disk space, api endpoint,  response time,  how quickly that endpoint is responding and a big part of that as well is logs. Logs give developers the ability to see what is happening without having to access production systems. 

## Rince & Repeat: 

Once that's in place you go right back to the beginning to the planning stage and go through the whole thing again

## Continuous:

Many tools help us achieve the above continuous process, all this code and the ultimate goal of being completely automated, cloud infrastructure or any environment is often described as Continuous Integration/ Continuous Delivery/Continous Deployment or “CI/CD” for short. We will spend a whole week on CI/CD later on in the 90 Days with some examples and walkthroughs to grasp the fundamentals. 

### Continuous Delivery:

Continuous Delivery = Plan > Code > Build > Test 

### Continuous Integration:

This is effectively the outcome of the Continuous Delivery phases above plus the outcome of the Release phase. This is the case for both failure and success but this is fed back into continuous delivery or moved to Continuous Deployment. 

Continuous Integration = Plan > Code > Build > Test > Release 

### Continuous Deployment: 

If you have a successful release from your continuous integration then move to Continuous Deployment which brings in the following phases 

CI Release is Success = Continuous Deployment = Deploy > Operate > Monitor 

You can see these three Continuous notions above as the simple collection of phases of the DevOps Lifecycle. 


### Resources:

- [DevOps for Developers – Software or DevOps Engineer?](https://www.youtube.com/watch?v=a0-uE3rOyeU)
- [Techworld with Nana -DevOps Roadmap 2022 - How to become a DevOps Engineer? What is DevOps? ](https://www.youtube.com/watch?v=9pZ2xmsSDdo&t=125s)
- [How to become a DevOps Engineer in 2021 - DevOps Roadmap](https://www.youtube.com/watch?v=5pxbp6FyTfk)
