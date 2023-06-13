---
title: "BRO. Business Reviewer & Organizer"
seoTitle: "BRO. Business Reviewer & Organiser (My 1st flutter project)"
datePublished: Mon May 16 2022 16:56:11 GMT+0000 (Coordinated Universal Time)
cuid: cl38yx1uc01eerxnv2teg3cbj
slug: bro-business-reviewer-and-organizer
cover: https://cdn.hashnode.com/res/hashnode/image/unsplash/g5jpH62pwes/upload/v1652719676406/YAgf197hf.jpeg
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1653723611648/vPjFxAAxX.png
tags: firebase, flutter, stream, frontend-development, vscode

---

### ***WHAT EXACTLY IS BRO?***



“A virtual business analyst and manager” - BRO. Unified platform for small and medium-size scale business owners to manage their business. It can be broadly divided into two aspects the normal execution part and the other part is Implementing statistics in the form of Algorithms and code to process the data and then display it to the user. The system will be implemented as an app we. Intend to contribute to “Make in India”.
Various services offered by BRO-
Accounting
Management
The available software's are extremely professional and might be difficult for individuals to use hence with easy to use and pre-calculated data we intend to make accounting extremely trivial even for Non-professionals.
1. Our App (software) provides enhanced communication with the team.
2. Planning and scheduling meets and deadlines.
3. Exploring nearby places to find possible vendors or local stores for help.
4. Storing of sales data on Firebase hance keeping it secure.
5. Analysing the sales and processing data


***PATHWAY DISCOVERED AFTER INTENSIVE RESEARCH***

When a user comes in, he or she is greeted by a gorgeous splash screen that displays our logo, after which the user is taken to the login screen. If this is the user's first time using the bro platform, he or she must register. After logging in, the user may navigate between the main page and the profile page. On the home page, there are many button widgets that link the visitor to the project's other five parts. The user data from the database is displayed on the profile page ( Firebase). It may be amended in the future to include an update area where the deadlines and imp meets will be presented.


In a flutter, we use them on a pressed feature to traverse between pages. As a result, when we hit the Accounts button, we are routed to a new page where the user submits data in the form of a CSV file, which is subsequently transformed into JASON data and posted to Firebase for the relevant user. And the user data is now protected on the cloud. The CSV to JASON conversion code was obtained from the internet.

We are transported to a new website that displays monthly events on a calendar when we click on the calendar button. This capability is not linked to a database; instead, user data is saved on the user's device. We utilised the sync fusion widget, which is a very interactive widget, to present data to the user. To incorporate fully functioning calendars in flutter applications, use sync fusion for the flutter framework.

When we click the Teams button, we are taken to a screen that manages chat capability in our app using the stream API. It's a very scalable API with fantastic user interface functionality. When a user registers for the app using Firebase, they are given a token, which they may use in the stream API. Users can communicate with one another using this token.

The Explore section describes how our user may explore and engage with other businesses in order to identify suitable suppliers for his company. This page essentially integrates the Google Maps API with our app.

The Sales Analysis Section analyses data and makes recommendations. Visualization of data We are still working on the data analysis portion, however for visual data representation, we are utilising the sync fusion Widget, which aids in the effective display of data.


![Screenshot 2022-05-16 at 10.16.08 PM.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1652719585246/L99w1ZUkS.png align="left")

