# Overview
As a penetration tester, I assessed the search functionality of the application for client-side vulnerabilities and identified a DOM-based Cross-Site Scripting (DOM XSS) issue within an AngularJS expression. By injecting malicious payloads into the search input, it was possible to execute arbitrary JavaScript in the user’s browser, leading to potential session hijacking, credential theft, and unauthorized actions. This project demonstrates how improper handling of AngularJS expressions can expose high-severity client-side risks.

# Steps Undertaken

Step 1: Analyzed client-side scripts and DOM behavior using browser developer tools.

Step 2: Reviewed the search feature to identify AngularJS directives and expressions handling user input.

Step 3: Crafted AngularJS payloads to test for XSS within ng-app and {{ }} expressions.

Step 4: Injected the payload {{$on.constructor('alert(1)')()}} into the search input and verified execution via an alert box.

Step 5: Confirmed that arbitrary JavaScript could run in the user’s browser, validating the vulnerability.

# Conclusion

This assessment confirmed a high-severity DOM XSS vulnerability in the AngularJS-based search feature. Implementing proper input sanitization, escaping user data, and using AngularJS strict contextual escaping (SCE) are critical to securing front-end frameworks against such client-side attacks.
