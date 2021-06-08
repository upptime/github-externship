---
name: Jayant Katia
email: jayantkatia65@gmail.com
institution: Thapar Institute of Engineering & Technology
application-id: 23-04_Jay996_tfa_260
linkedin: https://www.linkedin.com/in/jayant-katia
---

# :arrow_up: Jayant's application for the Upptime GitHub Externship
Hello! This is Jayant Katia, a student pursuing B.E. in Computer Science and Engineering at Thapar Institute of Engineering, Patiala. I love to learn new things and am experienced in HTML/CSS, Javascript, NodeJs, Flutter and GoLang.
 
## Contents
- [Ideas](#ideas)
- [Issues](#issues)
- [Deliverables](#deliverables)
- [Related Work](#related-work)

##  Ideas
### :sparkles::sparkles: Add more components and functionality to Static website
<p align='right'>(@upptime/status-page, @upptime/uptime-monitor, @upptime/graphs)</p>

Adding more components and functionality will better the user experience and provide more insights. Some of the functionality/components can be,
- Add options to view 24h, 30d, 1y, all-time graphs and details in the *history page*. Currently, 7-day graph and all-time details are shown.
- Add filters to filter out *degraded performance* or *downtime incidents* from incidents in the *homepage* and *history page*.
- Add pagination for past incidents.
- Search incidents based on time.
- Add a section to show scheduled maintenances in the *history page*.

Issues and discussions in this context,<br>
[#264 History always shows "7-day response time" chart and never 30d or 1y](https://github.com/upptime/upptime/issues/264)<br>
[#372 Add pagination for "past incidents" in site](https://github.com/upptime/upptime/discussions/372)<br>

### :books::books: Developer Guides and Better Docs
<p align='right'>(upptime/upptime.js.org)</p>

While customizing Uptime-Monitor, I came across various roadblocks. I realized the need for a developer guide. It would encourage developers to contribute better to the project. Some topics that can be included are,
- Setting up the environment. Must emphasize the Node version. I, on the first try, used Node v14 that led to some errors :sweat_smile:.
- Testing customized actions and the need to commit the Node modules.
- Using a mix of upptime's action and customized actions by replicating scripts and configuring ```.upptimerc.yml``` . Checkout [Related Work Section](#related-work).

Issues and discussions in this context,<br>
[#344 Need for better docs](https://github.com/upptime/upptime/issues/344#issuecomment-846603577)<br>

### :sparkles::sparkles: Enable notifications customization
<p align='right'>(@upptime/uptime-monitor, upptime/upptime)</p>

Going through the issues and discussions, I noticed that the feature which enables notification customizations is very much in-demand, especially for more popular social platforms like Twitter, Discord, Telegram, etc. We can have users add their customized template configurations either in the ```.upptimerc.yml``` or in a separate "templates" folder. Upptime-Monitor will parse the template files and send out the notifications accordingly.

Issues and discussions in this context,<br>
[#357 Discord message customization](https://github.com/upptime/upptime/issues/357)<br>
[#368 Custom notification text](https://github.com/upptime/upptime/discussions/368)<br>

### :sparkles::sparkles: Add RSS feed  
<p align='right'>(@upptime/uptime-monitor, upptime/upptime)</p>

Adding RSS feed support will allow clients/customers to subscribe to status updates without being part of the mainstream groups(Discord/Telegram/others).
Reference: [#148 Allow for subscribing by customers](https://github.com/upptime/upptime/discussions/148)

Issues and discussions in this context,<br>
[#275 Add rss feed](https://github.com/upptime/upptime/discussions/275)<br>
[#198 Add rss feed link](https://github.com/upptime/upptime/discussions/198)

### Other Ideas
- :recycle::recycle: Sapper to SvelteKit
- :sparkles::sparkles: Websockets and gRPC checks

## Issues
I am open to work on existing issues and bugs. I have already gone through them once. Some of the issues which are higher on my priority list are,
- [#225 Secret urls are sent to notifications](https://github.com/upptime/upptime/issues/225)
- [#352 Telegram notifications aren't working with underscores in the URL](https://github.com/upptime/upptime/issues/352)
- [#186 Process notification services even if the GitHub API is giving an error](https://github.com/upptime/upptime/issues/186)
- [#344 owner name does not update in README.md](https://github.com/upptime/upptime/issues/344)
- [#328 tcp-ping does not produce outage](https://github.com/upptime/upptime/issues/328)

## Deliverables
I will be able to devote at least 35 hours/week, which can be incremented according to the project needs.  
### :calendar::clock2: Timeline
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Time&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|Objectives|
|-------------------|-------------|
| Week 1 | Get acquainted with the team + understand codebase in-depth + know the conventions used throughout the project + prepare drafts for the features/ideas |
| Week 1-5 | Implement features + resolve issues + write documentation |
| Week 5-6 | Mid-Externship review + analyze pace and completion percentage of feature implementations + make plans for latter part of the Externship  |
| Week 6-10 | Improvise the existing tasks on the basis of reviews + work on new features if planned + add i18n support to newly added features if applicable|
| Week 10-11 | Document the features implemented thoroughly + test the features|
| Week 12 | Reserve week to handle delays + finalize |

## Related Work
Coming from a Javascript and Flutter(type and null safety) background, I was able to understand the codebase(and TypeScript) very comfortably to a great extent. I have previously worked with Vue, AngularJs, ReactJs. I am confident that I will be able to pick up Svelte pretty fast.
### :arrow_up::bug: Upptime Issues
I have already gone through the issues once and contributed to some of them,
- :green_circle: [#356 Workflow schedule not setting properly](https://github.com/upptime/upptime/issues/356)
- :yellow_circle: [#226 HTTP 403 is reported, CLI curl returns 200](https://github.com/upptime/upptime/issues/226)
- :yellow_circle: [#340 Custom User-Agent when checking sites](https://github.com/upptime/upptime/issues/340)
- :yellow_circle: [#344 owner name does not update in README.md](https://github.com/upptime/upptime/issues/344)
### :arrow_up::chart_with_upwards_trend: My Upptimes
<table>
    <tr>
        <td>My Personal Upptime Status Page</td>
      <td>https://jayantkatia.github.io/status &nbsp; <i>(uses customized Upptime monitor)</i></td>
    </tr>
    <tr>
        <td>My Customized Uptime-Monitor</td>
        <td>https://github.com/jayantkatia/uptime-monitor/tree/scripts-enabled</td>
    </tr>
</table>
<br>
<br>
<details open>
  <summary><b>Read more about my Customized Uptime-Monitor (Scripts enabled)</b></summary>
  <blockquote>Partially implemented (graphs action is not customized yet)</blockquote>
  <b>What inspired the changes?</b>
  <p>
    I came across some discussions on <b>location-based checking</b> of the status of the page.
  </p>
  <b>Solution (not the best one)</b>
  <p>
    It led me to think if we could run scripts just before pinging and just after pinging( to save bandwidth by not using it to commit and perform other bandwidth-consuming actions), we can allow the users to do anything they want. Users can connect to a VPN via CLI tools. Luckily, I came across <a href="https://windscribe.com/">Windscribe VPN service</a> (proprietary :disappointed: ) which provides a CLI tool and free 10GB/month which is enough for 5-6 websites pinged every 5 minutes.
  </p>
  <b>Pros</b>
  <ul>
    <li>Users do not need to customize uptime-monitor, they simply need to commit scripts to their upptime templates and mention the path in .upptimerc.yml</li>
    <li>Users can run site-specific scripts</li>
    <li>Users can specify tags for each site. <a href="https://github.com/jayantkatia/status/blob/master/.upptimerc.yml#L16">Check out</a> my configuration's site-specific tags(windscribe's location abbreviations)</li>
  </ul>
</details>