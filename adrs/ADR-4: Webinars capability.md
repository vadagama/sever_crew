## ADR-4: Webinars capability

### Date:
2021-10-29

### Status:
Proposed

### Context:
We are convinced that developing webinars capability from scratch is not the best idea, because it is quite difficult, risky and expensive. Therefore, we offer a seamless connection of a ready-made solution to the Farmacy Family system.

Choosing a proper online webinar platform is difficult sometimes as things can go wrong anytime during the webinar. Weak network, download issue, unclear audio, non-HD video, and whatnot. While selecting a webinar hosting platform, we need to make sure to consider the several aspects: 
* Is it fulfilling our requirements? 
* Does it have necessary APIs for full integration with the Farmacy Family system?
* How many participants can join our webinar?
* How cranky downloads and extensions are?
* What is the price? Is it reasonable?

We have reviewed several popular platforms and prepared a comparison table.
<table>
  <tr>
   <td><strong>Name</strong>
   </td>
   <td><strong>Pros</strong>
   </td>
   <td><strong>Cons</strong>
   </td>
   <td><strong>Price</strong>
   </td>
   <td><strong>Rating</strong>
   </td>
  </tr>
  <tr>
   <td><a href="https://webinarcare.com/recommends/demio">Demio</a>
   </td>
   <td>
<ul>

<li>Automatic, cloud-based events and recordings

<li>Chats, handouts, and polls with enjoyable waiting room experience

<li>Built-in robust analytics and insights

<li>Easy-to-integrate marketing tools

<li>Email automation plus event reminders
</li>
</ul>
   </td>
   <td>
<ul>

<li>Price is on the higher end for more than 50 live participants.

<li>No registration page conversion analytics, so it cannot be determined how many did not register, for instance.
</li>
</ul>
   </td>
   <td>Starter Plan costs $34/month for a 50-person room
   </td>
   <td>8 of 10
   </td>
  </tr>
  <tr>
   <td><a href="https://webinarcare.com/recommends/WebinarJam">WebinarJam</a>
   </td>
   <td>
<ul>

<li>Automatic recording

<li>Excellent customer support

<li>Social media integrations like Facebook

<li>Handle multiple attendees easily

<li>Compatible with various browsers and OS

<li>Incorporate polls and surveys with webinar
</li>
</ul>
   </td>
   <td>
<ul>

<li>Needs purchase of EverWebinar for automated on-demand webinars

<li>Occasionally video and sound delay up to a couple of seconds

<li>Lacking integration with third-party AV tools
</li>
</ul>
   </td>
   <td>Basic Plan costs $499/year or $41.58/month for up to 500 participants per webinar and 3 presenters.
   </td>
   <td>8 of 10
   </td>
  </tr>
  <tr>
   <td><a href="https://webinarcare.com/recommends/EverWebinar">EverWebinar</a>
   </td>
   <td>
<ul>

<li>Switch between WebinarJam and EverWebinar in one click

<li>Fake your audience count

<li>Show performance stats in real-time

<li>Convert previous live events to evergreen events

<li>Just-in-time online events start right upon registration

<li>An advanced scheduling system that blocks out unavailable dates

<li>Auto-detection of time zone

<li>Unlimited free hosting through cloud-based servers
</li>
</ul>
   </td>
   <td>
<ul>

<li>A few complaints about streaming on mobile
</li>
</ul>
   </td>
   <td>Monthly Plan $99/mo
   </td>
   <td>7 of 10
   </td>
  </tr>
  <tr>
   <td><a href="https://webinarcare.com/recommends/livestorm">Livestorm</a>
   </td>
   <td>
<ul>

<li>Access easy to set-up adaptable webinar themes

<li>Interactive experience with chats, polls, questions, and more

<li>Integration and analysis of meetings

<li>High-level automation and webinar sequences

<li>Comprehensive, multi-language customer support.

<li>Detailed attendance analytics, source tracking, replay analytics, and participation report

<li>Unlimited storage of recording
</li>
</ul>
   </td>
   <td>
<ul>

<li>The host’s internet connection influences video and audio performance

<li>Occasional blurry and pixelated display

<li>Spotty customer support at times

<li>No offers on replay; offers done on live are lost on replay

<li>There’s not way to re-open pop-ups

<li>Email reminder is uncustomizable
</li>
</ul>
   </td>
   <td>Webinar Premium costs $99/host/month with a 4-hour limit per webinar
   </td>
   <td>5 of 10
   </td>
  </tr>
  <tr>
   <td><a href="https://webinarcare.com/recommends/crowdcast">Crowdcast</a>
   </td>
   <td>
<ul>

<li>Easy to get started

<li>Go live or attend on any device

<li>Has a separate tab for public chat and for asking questions.

<li>Easy invite feature

<li>Presenters can multi-stream on Facebook and Youtube.

<li>Very interactive (Polls, Analytics, Question & Answer)

<li>A good option for people who are new in marketing or live streaming.

<li>The audience can chat and ask questions even before the live starts.
</li>
</ul>
   </td>
   <td>
<ul>

<li>The landing page for the audience is not very customizable

<li>Sessions have a limit of 2 hours for starter plans

<li>No multi-user access

<li>Some features are locked on expensive plans.
</li>
</ul>
   </td>
   <td>Pro $89/mo
   </td>
   <td>6 of 10
   </td>
  </tr>
  <tr>
   <td><a href="https://livestream.com/">Livestream</a>
   </td>
   <td>
<ul>

<li>Unlimited storage and attendees

<li>Excellent customer support

<li>Privatization of events

<li>Private sharing of link

<li>Extensive in-built robust analytics

<li>Facebook Live or YouTube streaming

<li>Embed webinar to website
</li>
</ul>
   </td>
   <td>
<ul>

<li>No audience engagement features such as surveys or polls
</li>
</ul>
   </td>
   <td>At $42/month, there’s no limit to participants
   </td>
   <td>8 of 10
   </td>
  </tr>
  <tr>
   <td><a href="https://www.webinarsonair.com/">WebinarsOnAir</a>
   </td>
   <td>
<ul>

<li>Schedule webinar for up to 50,000 attendees in under a minute

<li>Use “Tracking Pixels” to create “laser-targeted audiences for retargeting”

<li>Live Q&A with live-chats

<li>Allows 10 moderators or speakers at once

<li>Easy webinar registration

<li>in-built opt-in forms

<li>Cloud-based hosting

<li>strong customer service
</li>
</ul>
   </td>
   <td>
<ul>

<li>Dependent on Hangouts and may become inaccessible due to changes in Google software
</li>
</ul>
   </td>
   <td>$99/month for unlimited participants
   </td>
   <td>5 of 10
   </td>
  </tr>
  <tr>
   <td><a href="https://www.dacast.com/">DaCast</a>
   </td>
   <td>
<ul>

<li>No viewer limit

<li>Real-time robust analytics

<li>Allows FTP access

<li>Live stream on social media platforms like Facebook

<li>An interactive video on demand (VOD) solution

<li>Easy to set up

<li>User-friendly web conferencing interface

<li>strong customer service
</li>
</ul>
   </td>
   <td>
<ul>

<li>$0.15 charge per GB beyond the bandwidth amount or streams will shut off
</li>
</ul>
   </td>
   <td>The monthly plan starts at $19/month and includes prepaid bandwidth, viewer hours, storage, and support
   </td>
   <td>7 of 10
   </td>
  </tr>
  <tr>
   <td><a href="https://zoom.us/">Zoom</a>
   </td>
   <td>
<ul>

<li>HD video and audio plus screens sharing

<li>Desktop and app sharing options

<li>Backup meetings in the cloud

<li>Private and public chats, allowing participants to communicate during webinar interruption

<li>Free access to up to 100 participants with 40 mins limit on group meetings

<li>Host controls and virtual whiteboards

<li>Easily navigable dashboard.

<li>No one-time fees
</li>
</ul>
   </td>
   <td>
<ul>

<li>The navigating interface can be quite confusing

<li>There are complaints of calls being disconnected
</li>
</ul>
   </td>
   <td>The business package is $19.99/month and is ideal for small and medium-sized businesses
   </td>
   <td>10 of 10
   </td>
  </tr>
  <tr>
   <td><a href="https://www.adobe.com/products/adobeconnect/meetings.html">Adobe Connect</a>
   </td>
   <td>
<ul>

<li>Various templates to customize for virtual environments.

<li>Create unique registration pages

<li>Reach out to target audience using videos, blogs, surveys, and polls.

<li>Detailed adobe analytics for better insights

<li>Integrates with CRM software such as Eloqua and Salesforce.
</li>
</ul>
   </td>
   <td>
<ul>

<li>There are reports of some video and audio disturbances on mobile.
</li>
</ul>
   </td>
   <td>Meeting Plan starts at $50/month for 25 participants and up to 200 participants for the Learning plan.
   </td>
   <td>6 of 10
   </td>
  </tr>
</table>


### Decision:
We suppose to integrate Farmacy Family with Zoom for several reasons:
1. Very stable on all kind of devices
2. Could integrate this several popular learning management systems (LMS) and makes it easy to schedule a meeting with any course activity and invite the right students from LMS
3. Well documented API with a lot of capabilities for better integration
4. Reasonable price

### Consequences:
For new users it could be quite confusing to use Zoom for the first time