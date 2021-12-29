---
title: Google Apps Script
categories:
  - web
  - gas
tags:
  - null
toc: true
date: 2021-02-27 10:35:04
---

[Apps Script | Google Developers](https://developers.google.com/apps-script/)  
[Overview of Google Apps Script | Google Developers](https://developers.google.com/apps-script/overview)

[Standalone Scripts | Apps Script | Google Developers](https://developers.google.com/apps-script/guides/standalone)
Back in the old days, GAS had to be attached to a Spreadsheet or Document. Now we can create scripts in standalone Code project.

[Apps Script](https://script.google.com/home) console
[Apps Script Quota](https://docs.google.com/macros/dashboard)
[Quotas for Google Services | Apps Script | Google Developers](https://developers.google.com/apps-script/guides/services/quotas)

Simple way to interact with other Google services, enable (per project) in **Resources > Advanced Google Services**.

You can also deploy your GAS as _web service_, note access _MUST_ be granted to anyone (so that they can execute your script). And remember to create a new project version following each update and redeploy, just like commit and redeploy in backend.

[Reference Overview | Apps Script | Google Developers](https://developers.google.com/apps-script/reference/)
[Apps Script API | Google Developers](https://developers.google.com/apps-script/api)
[Built-in Google Services | Apps Script | Google Developers](https://developers.google.com/apps-script/guides/services)
[Class ContentService | Apps Script | Google Developers](https://developers.google.com/apps-script/reference/content/content-service)
[Properties Service | Apps Script | Google Developers](https://developers.google.com/apps-script/guides/properties)

[G Suite Developers Blog: Apps Script](https://gsuite-developers.googleblog.com/search/label/Apps%20Script)
[Google Apps Script - YouTube](https://www.youtube.com/playlist?list=PL68F511F6E3C122EB)

[Google Apps Script snippets - Desktop Liberation](https://ramblings.mcpher.com/gassnippets2/)
[Apps Script - Desktop Liberation](https://ramblings.mcpher.com/apps-script/)

[Structure and simplify your Google Apps Script | by Jasper Duizendstra | JavaScript in Plain English](https://javascript.plainenglish.io/create-javascript-objects-in-google-apps-script-91472378ab55)
[How to Learn Google Apps Script](http://ctrlq.org/code/19803-learn-google-apps-script)
[Google Apps Script for Developers - Digital Inspiration](https://www.labnol.org/internet/google-apps-script-developers/32305/)
[google-apps-script - Getting started with google-apps-script | google-apps-script Tutorial](https://riptutorial.com/google-apps-script)
[Automating Google Forms & Sheets using Apps Script | by Varun Joshi | codeburst](https://codeburst.io/automating-google-forms-sheets-using-apps-script-2c59db97966f)

## Dev setup/examples

Since HTMLService fails silently and there's always a "TransportError: There was an error during the transport or processing of this request. Error code = 10, Path = /wardeninit" error (even if script working properly), it is recommended to use local environment to validate HTML and code before pushing to GAS to test.

[Script Projects | Apps Script | Google Developers](https://developers.google.com/apps-script/guides/projects)
[google/clasp: 🔗 Command Line Apps Script Projects](https://github.com/google/clasp)
[clasp - The Apps Script CLI](https://codelabs.developers.google.com/codelabs/clasp/#0)
[Create and manage deployments | Apps Script | Google Developers](https://developers.google.com/apps-script/concepts/deployments)
[Develop Apps Script using TypeScript | Google Developers](https://developers.google.com/apps-script/guides/typescript)

```sh
clasp clone <project_id>
clasp open # online script editor

clasp pull
clasp push
clasp push --watch

clasp version "First version"
clasp deploy 1 "First deployment"
```

[leonhartX/gas-github: sync gas code to github](https://github.com/leonhartX/gas-github)
[LEARN BY EXAMPLE - Google Apps Script Examples](https://sites.google.com/site/scriptsexamples/learn-by-example)
[jasonjurotich/JJ-GAS: A collection of Google Apps Script code (GAS) for Google Apps and Classroom](https://github.com/jasonjurotich/JJ-GAS)

[googleworkspace/apps-script-samples: Apps Script samples for Google Workspace products.](https://github.com/googleworkspace/apps-script-samples)
[noel-yap/science-test-grading: Google Sheets functions to aid with grading science tests including metrics unit conversions and significant figures.](https://github.com/noel-yap/science-test-grading)
[Google Apps Scripts Collection - The Best Google Scripts](https://www.labnol.org/internet/google-scripts/28281/)

[How to create an automated calendar with Google Apps Script with open source on top | Opensource.com](https://opensource.com/article/19/1/automate-calendar)
[Create PDF files from templates with Python and Google Scripts | Codementor](https://www.codementor.io/garethdwyer/create-pdf-files-from-templates-with-python-and-google-scripts-p63kal1vb)
[Amazon Price Tracker Made With Google Docs](http://www.labnol.org/internet/amazon-price-tracker/28156/)

## Verifying apps

[My Google Apps Script app isn’t verified: Understanding why and how to fix – MASHe](https://hawksey.info/blog/2017/08/my-google-apps-script-app-isnt-verified-understanding-why-and-how-to-fix/)
[Unverified apps - Google Cloud Platform Console Help](https://support.google.com/cloud/answer/7454865?hl=en)
[Google Sheets Script - Authorization Required/This app isn't verified - Explained - YouTube](https://www.youtube.com/watch?v=Sxu-4VULQ10)
[Why does my apps script deployed as API executable return Permission Denied? - Stack Overflow](https://stackoverflow.com/questions/32920443/why-does-my-apps-script-deployed-as-api-executable-return-permission-denied/33008218#33008218)

[Google Cloud Platform Projects | Apps Script | Google Developers](https://developers.google.com/apps-script/guides/cloud-platform-projects) some API can only be accessed as GCP standard project; add-on or an API executable need GCP standard project

## Add ons

[Libraries | Apps Script | Google Developers](https://developers.google.com/apps-script/guides/libraries)
[Extending G Suite with Add-ons | G Suite Add-ons | Google Developers](https://developers.google.com/gsuite/add-ons/overview)
[Use add-ons & Apps Script - Computer - Docs Editors Help](https://support.google.com/docs/answer/2942256?co=GENIE.Platform%3DDesktop&hl=en)

[50 Google Sheets Add-Ons to Supercharge Your Spreadsheets - The Ultimate Guide to Google Sheets | Zapier](https://zapier.com/learn/google-sheets/best-google-sheets-addons/)
[15 Best Google Sheets Add Ons & Power Tools to Supercharge Your Data - Automate.io Blog](https://automate.io/blog/google-sheets-add-ons/)

## Fetch

[Class UrlFetchApp | Apps Script | Google Developers](https://developers.google.com/apps-script/reference/url-fetch/url-fetch-app)

[Apps Script Navigator: UrlFetchApp Empowered With Cookie Management, Re-Login, and Much More! - DZone Performance](https://dzone.com/articles/apps-script-navigator-urlfetchapp-empowered-with-c)
[Navigator - Project Editor - Apps Script](https://script.google.com/home/projects/1IWpJgWcUgNg1wbIh4WlP_Qz0rWF6ssyyWHmrow2HFE402v_JWHPpwtmM/edit)

## HTML UI

> use [alpinejs/alpine](https://github.com/alpinejs/alpine), [Lit](https://lit.dev/) or other light-weight frameworks

[HTML Service: Create and Serve HTML | Apps Script | Google Developers](https://developers.google.com/apps-script/guides/html)
[Class HtmlService | Apps Script | Google Developers](https://developers.google.com/apps-script/reference/html/html-service)

[HTML Service: Communicate with Server Functions | Apps Script](https://developers.google.com/apps-script/guides/html/communication) "Server" is the App script
[Class google.script.run (Client-side API) | Apps Script](https://developers.google.com/apps-script/guides/html/reference/run)

## Sending Email

[dwyl/learn-to-send-email-via-google-script-html-no-server: An Example of using an HTML form (e.g: "Contact Us" on a website) to send Email without a Backend Server (using a Google Script) perfect for static websites that need to collect data.](https://github.com/dwyl/learn-to-send-email-via-google-script-html-no-server)
[Contact Form Example](https://dwyl.github.io/learn-to-send-email-via-google-script-html-no-server/)

[Adding a Script to a Google Form to Email Responses - FormEmailer - YouTube](https://www.youtube.com/watch?v=-o6JCQcLsBo)
[FormEmailer](https://sites.google.com/site/formemailer/form-emailer)

## Google Sheets

[Spreadsheet Service | Apps Script | Google Developers](https://developers.google.com/apps-script/reference/spreadsheet)

[Google Sheets… Your Next Database? - YouTube](https://www.youtube.com/watch?v=K6Vcfm7TA5U) Google Sheet + Next.js

[Google Sheet 自製股票監察表教學 一表自動監察股價上落 - ezone.hk - 教學評測 - 應用秘技 - D190329](https://ezone.ulifestyle.com.hk/article/2309466)

### Form -> Sheet

[Google Sheets API - HTML Form Data to Google Sheet - YouTube](https://www.youtube.com/watch?v=BxqfwfQi0jk)

[Creating an Editable Webpage With Google Spreadsheets and Tabletop.js | CSS-Tricks](https://css-tricks.com/creating-an-editable-webpage-with-google-spreadsheets-and-tabletop-js/) use Papa Parse instead
[jsoma/tabletop: Tabletop.js gives spreadsheets legs](https://github.com/jsoma/tabletop)
[Papa Parse - Powerful CSV Parser for JavaScript](https://www.papaparse.com/)

[jamiewilson/form-to-google-sheets: Store HTML form submissions in Google Sheets.](https://github.com/jamiewilson/form-to-google-sheets)
[How to Submit an HTML Form to Google Sheets…without Google Forms](https://medium.com/@dmccoy/how-to-submit-an-html-form-to-google-sheets-without-google-forms-b833952cc175)
[Google Spreadsheets as a Database – INSERT with Apps Script form POST/GET submit method – MASHe](https://mashe.hawksey.info/2011/10/google-spreadsheets-as-a-database-insert-with-apps-script-form-postget-submit-method/)

### Sheet -> Form

[Forms Service | Apps Script | Google Developers](https://developers.google.com/apps-script/reference/forms)

[Google I/O 2013 - Use Apps Script to Create Dynamic Google Forms - YouTube](https://www.youtube.com/watch?v=38H7WpsTD0M)
[Google Forms - Drop Down List from Spreadsheet Using Apps Script - YouTube](https://www.youtube.com/watch?v=o3AL7ASI_cA)
[Apps Script: Dynamic Forms Multiple Choice - YouTube](https://www.youtube.com/watch?v=MPlT_sIwL6k)
[Create Dynamic Questions on a Google Form - Stack Overflow](https://stackoverflow.com/questions/47586640/create-dynamic-questions-on-a-google-form)
[Creating form with a script : Page Break and go to page issue - Stack Overflow](https://stackoverflow.com/questions/17083500/creating-form-with-a-script-page-break-and-go-to-page-issue)
[Google Forms - Drop Down List from Spreadsheet Using Apps Script - YouTube](https://www.youtube.com/watch?v=o3AL7ASI_cA) using Forms Service

[NEW GAS TO CREATE FORMS FROM SHEETS WITH TEMPLATE - YouTube](https://www.youtube.com/watch?v=tXxkyxmWzEg&t=0s)
[JJ-GAS/formFromSheetComplete.gs at master · jasonjurotich/JJ-GAS](https://github.com/jasonjurotich/JJ-GAS/blob/master/formFromSheetComplete.gs)

[Google Forms Quiz functionality for Google Apps Script FormApp Class TextItem [117437423] - Visible to Public - Issue Tracker](https://issuetracker.google.com/issues/117437423) cannot set correct answer to text item (only choices)
[Google Forms - Inserting an image in a multiple choice field using Apps Script - Stack Overflow](https://stackoverflow.com/questions/49022122/google-forms-inserting-an-image-in-a-multiple-choice-field-using-apps-script)
[Get and set images to checkbox and multiple choice items. [36765518] - Visible to Public - Issue Tracker](https://issuetracker.google.com/issues/36765518) cannot add image to choice item choices
