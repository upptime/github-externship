---
name: Nirmit Jatana
email: nirmitjatana38@gmail.com
institution: Vellore Institute of Technology, Vellore
linkedIn: https://www.linkedin.com/in/nirmit-jatana/ 
applicationNumber: 26-05_Nir465_tfa_260
---

## Table of Contents

* [Contact information](#contact-info)
* [About the project](#about-the-project)
* [Progress](#progress-so-far)
* [Ideas](#ideas)
* [Execution plan](#execution-plan)
* [Timeline & deliverables](#timeline-and-deliverables)
* [Post externship period](#post-externship-period)
* [Working schedule and Commitment](#working-schedule-and-commitment)
* [Related work & past experience](#related-work-and-past-experience)
* [Why choose me](#why-choose-me)


## Contact info

**Nirmit Jatana**
- Phone: +91 83604 07845
- College: Vellore Institute of Technology (VIT)
- Email: [nirmitjatana38@gmail.com](mailto:nirmitjatana38@gmail.com)
- Github: [https://github.com/Nirmitjatana](https://github.com/Nirmitjatana)
- LinkedIn: [https://www.linkedin.com/in/nirmit-jatana/](https://www.linkedin.com/in/nirmit-jatana/)
- Medium: [https://medium.com/@nirmitjatana38](https://medium.com/@nirmitjatana38)
- Resume: [https://bit.ly/2Tcn2ZH](https://bit.ly/2Tcn2ZH)

Application Number: **26-05_Nir465_tfa_260**

My name is Nirmit, and I am an undergraduate at Vellore Institute of Technology. I am an Open-source enthusiast. The motivation for me to apply for this opportunity is because the areas of my interest are aligned with Upptime. I am always looking to contribute to real-world projects which are used by thousands of people, and Upptime as a product impressed me a lot.

## About the project

Upptime is an open source uptime monitor and status page powered entirely by Github actions, issues and pages.
Upptime uses cron jobs to run specific workflows and make sure websites are up. It uses Issues to report incidents and github pages to host a personalized status page for you.

## Progress so far

- I started with setting up the project for myself. 
[https://nirmitjatana.github.io/uptime/](https://nirmitjatana.github.io/uptime/) 
Repo: [https://github.com/Nirmitjatana/uptime](https://github.com/Nirmitjatana/uptime).

![](https://lh6.googleusercontent.com/b-YF2_GmnBHVKL-WkdTnBHH4LaxrLSpIPqymrmNtHNBYMDBC5FIaEJKFPzURmXQF-AnjHbpJhAU02lCWEDNvY07YZ-gDl7CE4gXJ1uszwyTKCHoRYz4xRwpJcxgN5rRyyNutoV6Y)

- I went through the documentation, and gave time in understanding different features of the project. 
- My next step was to go through the codebase. I went through Upptime template [repo](https://github.com/upptime/upptime) , following with other supporting repos [status-page](https://github.com/upptime/status-page), [graphs](https://github.com/upptime/graphs), [updates](https://github.com/upptime/updates), [uptime-monitor](https://github.com/upptime/uptime-monitor), and [Upptime.js.org](https://github.com/upptime/upptime.js.org).

- After getting a fair idea of the codebase and how things are working, I was fascinated by the code quality and maintenance. I started diving into the open issues and participated in conversations related to the project.
	- [#256](https://github.com/upptime/upptime/issues/256) 
	- [#344](https://github.com/upptime/upptime/issues/344) 
	- [#148](https://github.com/upptime/upptime/discussions/148) 
	- [#185](https://github.com/upptime/upptime/issues/185) 
	- [#264](https://github.com/upptime/upptime/issues/264). 
> PRs opened by me:
>**[#271(merged)](https://github.com/upptime/status-page/pull/271).** - Moving of assets to gh-pages branch
>**[#275](https://github.com/upptime/status-page/pull/275)** - Open graph support
 
There are various issues which I would like to work on and contribute my set of code to the project. (details discussed in next section).

## Ideas

After going through the discussions and issues, I realised that some popular requested features are websockets support, twitter feed integration, and RSS feed. Following that some small features like custom discord notifications, theme configuration on status page and more metric info on graphs.

## Execution plan

I am listing a detailed execution plan along with illustrations on the features that according to me should be implemented. 
>Note: 
>I would love to implement all sorts of new ideas which are not mentioned here.

### Websockets support


We can expand Upptime as a **websocket echo testing tool**. Similar to websites, Upptime will run a workflow which will invoke the websocket url(provided by the user) and get the response time of the socket. And for that we can create a graph as well.

**Specifically for sockets the connection will be as follows:**
```
Websocket.open() //to open connection with with websocket
websocket.send() //to send message
websocket.onmessage() //to receive message
websocket.onerror() //to detect error
```
In case error is detected, websocket will be marked as “down”, and an issue will be created on the user’s template repo.

**.upptimerc.yml**

![](https://lh3.googleusercontent.com/7xx1ZPf5a1jKeRx-f14nEEaXwqBRHCN5JtjRaIBmfYN24JCf1VV6iZtY7YDdmV6GA2n7h2SXapW5GhPSjW28LeqeDFljqicbuRWscNQ-YfY_Cxkg6sgQ3x3rv4bupuNj4GWVSgI4)

I went through the code present in [update.ts](https://github.com/upptime/uptime-monitor/blob/master/src/update.ts) in [upptime-monitor](https://github.com/upptime/uptime-monitor) repo.

Similar to this we can setup the connection to websocket and perform operations accordingly.

![](https://lh6.googleusercontent.com/8vS5_BXKWwwWlXfM5SGzPg61Wxu0k45odH0i05Hpjx02l20qA7FdBJ6cvIMIxQ0GeDQf3wFIUUGterLfPDy2hvT_DUD8kcdIpBGaLFqiQqe3LAkFPysAWI8F1a_bSss92u0EGx6w)

### Twitter feed integration
Many organizations have separate twitter accounts to share maintenance, down-times and incidents. We can use uptime to automate that process of tweeting regular updates using twitter API.

**.upptimerc.yml**
```
notifications:
	twitter:
		downtimeTweet:
		investigatingTweet:
		fixCommitedTweet:
		fixDeployedTweet:
		resolved:
```

**Using twitter api:**

Twitter api provides certain end points which can be used by Upptime.
Post tweet endpoint: [https://developer.twitter.com/en/docs/twitter-api/v1/tweets/post-and-engage/api-reference/post-statuses-update](https://developer.twitter.com/en/docs/twitter-api/v1/tweets/post-and-engage/api-reference/post-statuses-update)

**Flow:**

-   Incase of an outage, the issue is opened. At this point **twitter API** will be called to post a tweet on behalf of the user.
    
-   When the issue is assigned, tweet can be posted about the status.
    
-   As all kinds of updates will be posted on the twitter handle. So, when an issue is resolved the tweet about the details of the issue can be posted which would ease out the process of notifying users.

![](https://lh5.googleusercontent.com/SkJCNppdb8FDPUE-QRn_wz0HA9A38Sy6DgtTi4oWTRLpV2sKc4lxZR7U_tK7Lmwfz5QOhHtJblgnXQseaMT1bxZKhtRnIi7Wf39kr7oONHn3Zz-g34_9x7PzaFBX2R1CRi2rM_5G)

**Authentication:**

-   User logs in on [developer.twitter.com](https://developer.twitter.com/en)
    
-   Setup a new app
    
-   After creating a new app, user will be provided with **API key** and **API secret key**.
    
-   We will use this API key and API secret key to post tweets on behalf of the user.

### RSS feed

RSS feed can let the customers subscribe for updates. Checking each site one by one will take forever.  RSS will provide them updates on outage and reason of outage. We can add a hyperlink to RSS feed on the status page. We can also integrate RSS feed with twitter, according to the user’s will.
RSS feed will be a great addition to Upptime, as it will allow customers to subscribe for updates. Notifications will them skip the tiring process of checking the status page regularly.

![](https://lh4.googleusercontent.com/2KeUiqOW5zfZ6-xzcJfooUECY423uRNhteJ_SmmmSpfRsZ_cdVbj5pV_OF5RDkK4U0kf3oBjqtRj6YYZUo0Qoj4OhUhm_G-pgjMSeMac4BtSEy22my2QY_m8JOof2uI_iIVgU4GQ)



### Custom discord notifications:

There are open issues and discussions about this feature, and this will be a great addition to Upptime. This will enable us to make notifications look better and functional as well. We can add link to the issue, custom colors etc.

I went through the discord webhooks guide. I found that *Embeds* can be used to customize these notifications.
https://birdie0.github.io/discord-webhooks-guide/structure/embeds.html

If we send the following code in body of the request:
```
{
  "embeds": [
    {
      "title": "Meow!",
      "color": 1127128
    },
    {
      "title": "Meow-meow!",
      "color": 14177041
    }
  ]
}
```
we get output something like this:

![embeds example](https://birdie0.github.io/discord-webhooks-guide/img/structure/embeds_2.png)

Majorly, modifications will be required in this file:
https://github.com/upptime/uptime-monitor/blob/a1aa9a442b1a9a0e33e9c0445e1cf46d96f33fb6/src/helpers/notifme.ts


By this finding, we can make discord notifications more effective in terms of functionality and better looking for a delightful experience.

### Other issues:
	
- **TCP support and gRPC health checks:**
	- If we add TCP support to Upptime it will open gates to support **SMTP** servers, **IMAP**, **FTP** and **SSH**. This will open horizons for Upptime and expand it as a full fledged outage monitor for services as well as websites. A **gRPC** service is used as the health checking mechanism for both simple client-to-server scenario and other control systems such as load-balancing.
Kubernetes does not support gRPC health checks natively. To address this, we can use an open source project called **grpc-health-probe**.

- **UI tweens:**
	- There are some UI bugs in the documentation website, specifically related to responsiveness. 
	- I felt like we can add pictures to the **get started** page for an easier setup. personally I made a little mistake of adding the wrong `baseUrl:` which lead to wrong README.md file.
	- Since we are storing history of the websites, we can add a separate history page as well.
	- If we look at the graph, it is only generated for *7days* period, we can add option for *30 days* and *1y* as well.

## Timeline and deliverables:

**21 June 2021 - 30 June 2021:**

I’ve been spending time in understanding the codebase and solving major issues. During this period, I’ll try to solve more tasks, along with that I’ll carry on my experiments and demos with various technologies being used to gain a deeper understanding of the same. At the same time, I would be listing down my areas of concern and discuss it with my mentor for a better understanding.

**1 July 2021 - 22 July 2021 (3 weeks)**

In this period I’ll work on the **websocket support** feature. My approach will be to constantly make active PRs and try to complete the basic functionalities in this period. By the end of 2 weeks I’ll start working on making the code better and simultaneously resolve bugs if any.

**23 July 2021 - 30 July 2021 (1 week)**

During this time, feature will be ready to deploy and I will make a complete report of the work done. It is necessary to update the documentation with the new feature added by me. This period will also be used to fix last minute bugs.

**31 July 2021 - 22 August 2021 (3 weeks)**

By this time I will be upto speed and in this period I’ll work on twitter API support feature. The main task during this period will be to get the authentication with twitter working and using their API to post tweets on behalf of the user. By the end, I will also write a report of the complete development process regarding new feature. Once everything is approved I will update the documentation as well.

**23 August 2021 - 6 September 2021 (2 weeks)**

In this phase, I will find a suitable way to auto generate a RSS feed for user’s customers. My plan is to link that RSS feed to the status page of the user. RSS feed will allow customer to subscribe for latest updates and outages.

**7 September 2021 - 21 September 2021 (2 weeks)**

Meanwhile, I will solve open issues and implement some minor features such as UI tweens on the documentation website and custom discord notifications. This period will also be utilized to compensate backlogs(if any). Ultimately, will give my best to contribute more and more to Upptime.

**22 September 2021 - 27 September 2021**

In the last week of the externship, I will submit a well versed complete report of all the contributions made so far. All the features will be debugged and deployed with complete documentation. All the promised features will be delivered by this point working like a charm.

## Post externship period:

I am very fascinated by Upptime as a product. It impressed me a lot as a user and also a open source project, and post this externship I plan to keep contributing to Upptime. In future, I would like to work on extra features I mentioned like TCP and FTP support etc. I will keep on providing minor patches and bug fixes.

## Working schedule and commitment:

I’ll be mostly working full-time on the code on weekdays (Monday to Friday). On weekends, I’ll be focusing on documentation, testing and bug fixing. My awake hours would usually be between 10 AM IST (4:30 AM UTC) to 2 AM IST the next day (8:30 PM UTC) and I’m comfortable working anytime during this period.

I’m very flexible with my schedule and already have the habit of working at night and hence timezone variation (with my mentor) won’t be an issue. I’m comfortable with any form of communication that suits my mentor.

## Related work and past experience:

My zest to learn new technologies and willingness to contribute to the community is what pushes me every day. My tech journey started from the day-1 of my university, and since then I have never looked back. I am part of many college clubs and chapters. Contributing and building new products is what excites me. I have been mentoring my juniors within student communities and helping them build projects. I have also been invited as a mentor in many international hackathons, sponsored by MLH. I love to work with React and Javascript. I always try to contribute to projects that create an impact.

**Some popular projects:**

| Project                   | Description                                                                                                                                                                                                                        | Link                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| SocioCredz                | SocioCredz will help you to provide education, and food, etc to the people in need without you even spending a single penny from your pocket!                                                                                      | [repo](https://github.com/Nirmitjatana/SocioCredz) |
| Akina (500+ active users) | A one-stop web app to request anything that you need and let the community help you.                                                                                                                                               | [link](https://akina.dscvit.com/)                  |
| IRIS                      | Iris is used by 100s of web hoppers to skip on the long hours of surfing the web and hopping between web pages to find between links or paths between two Wikipedia pages.                                                         | [link](https://iris.dscvit.com/)                   |
| Covid Tracker             | Covid tracker is all in one portal to stay updated about the pandemic, made it personalized for each user, where user can see all the data related to helpline numbers, beds available, active cases all based on user’s location. | [link](https://rekursion-vithack2020.netlify.app/) |


> Note:
I would like to document my github externship journey on medium/dev.to and will be releasing blogs each month.


## Why choose me:

I have good experience with Javascript and React. Upptime aligns with my interests and is a product I would like to carry in future as well. As soon as I was introduced to the project I started contributing to it. I like to be professional about my work ethics and solving problems drives me everyday. I also have a little exposure to competitive programming and secured 1577 AIR in Google Hashcode. I have worked on 20+ open source projects, checkout my [github](https://github.com/Nirmitjatana) . I have been part of open source organizations and have a fair understanding about the importance of a friendly work environment. I believe sharing knowledge and working together in a team helps everyone. I am glad to have mentoring experience in hackathons, and I like to discuss tech a lot. I see this externship as an opportunity to expand my network and become a humble open-source citizen.

