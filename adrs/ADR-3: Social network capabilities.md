## ADR-3: Social network capabilities

### Date:
2021-10-28

### Status:
Proposed

### Context:
Based on the requirements provided by Product Owner we need to develop new social functionality such as groups, profiles, blogs, messages, etc. 

### Decision:
We have analyzed several approaches durings our research:
* Develop all functionality on a low level using popular frameworks like Django, Spring, Ruby on Rails or Laravel.
* Integrate several different open source social tools in one holistic solution - social network platform.
* Choose a high quality open source prepared for production social network platform with good quality, documentation, modern stack and ability to make changes.

We propose a third one because there are no reasons to build such a system from scratch: it is a tedious process with a lot of risks. The way of integration is quite risky too because we need really close integration between components and researching appropriate components  may take a long time.

According to functional requirements and assumptions (see ASM-9 and ASM-10) we don’t need a global social network with millions of users. Owner requests are much more modest. According to our constraints (see CON-3 and CON-4) we have some limitations in budget, time for development.


We analyzed several social network engines:
* [SocialEngine](https://www.socialengine.com/)
* [Ning](https://www.ebool.com/alternatives/ning)
* [Zoho Connect](https://www.ebool.com/alternatives/zoho-connect)
* [Elgg](https://www.ebool.com/alternatives/elgg)
* [HumHub](https://www.ebool.com/alternatives/humhub)
* [JomSocial](https://www.ebool.com/alternatives/jomsocial)
* [Oxwall](https://www.oxwall.com/)
* [Jcow](https://www.jcow.net/)
* [Bitrix24](https://www.bitrix24.com/)

We propose the [HumHub](https://www.humhub.com/en) platform because of the benefits listed below.
* All necessary functionality for Farmacy Family out of the box - it’s an open-source social network kit that offers the tools to make communication, interaction and collaboration.
* Provides a powerful modular platform based on the Yii2 Framework (which is organized according to the MVC architectural pattern). 
* Free to use (but with ability to use vendor support)
* Self hosted (could be easily hosted on AWS EC2 instances)
* Headless installation and maintenance
* Highly customizable
    * Custom theme support
    * Custom module development support
    * Many configuration and fine tuning options
    * Possibilities for changing core modules
    * Well documented REST API
* Open source
    * Transparent development process
    * Community support and contribution
    * Direct contact to the core development team
    * Many eyes principle
* Translated into more than 40 languages
* Marketplace for modules and themes (most of them are free for use)
* User-friendly interface

### Consequences:
Could be not enough flexible for our purposes