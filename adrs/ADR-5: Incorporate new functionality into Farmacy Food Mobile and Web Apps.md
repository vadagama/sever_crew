## ADR-5: Incorporate new functionality into Farmacy Food Mobile and Web Apps

### Date:
2021-10-28

### Status:
Proposed

### Context:
Based on the requirements provided by Product Owner we need to incorporate new functionality (profile, blogs, webinars, etc) into Family Food mobile and web applications. 

### Decision:
Based on our assumptions about technological stack (see ASM-6 and ASM-7), we propose to refactor existing iOS and Android App and append such Farmacy Family functionality as p2p and group chats, user profile, community spaces and forums, dietitian feeds. We offer you to add only necessary functions for the mobile version and full functionality for the web version.

We don't recommend to use web oriented approaches like Cordova for such mobile applications because of the following considerations:

* **Native Apps Have The Best Performance**: with native mobile app development, the app is created and optimized for a specific platform. As a result, the app demonstrates an extremely high level of performance. Native apps are very fast and responsive because they are built for that specific platform and are compiled using platforms core programming language and APIs. 

* **Native Apps Are More Secure**: web apps rely on different browsers and underlying technologies such as JavaScript, HTML5, and CSS. Developing a native mobile app is a great way to guarantee your users reliable data protection.

* **Native Apps Are More Interactive And Intuitive**: native mobile apps run much smoother regarding user input and output. These types of apps inherit their devices’ OS interfaces, making them look and feel like an integrated part of the device.

According to the QA-6 we should provide architectural solutions with the ability to create flexible mobile solutions with a lot of different functionality (Including location data using GPS, camera, microphone, security options, etc). Native mobile development could provide such capability.

### Consequences:
The cost may be higher with native mobile app development approach