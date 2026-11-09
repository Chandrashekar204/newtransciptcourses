# 28.7 — Wrap Up

> Section 28: Security

This is it for this module, the two most important attack patterns or vulnerabilities I want you to take away from it are these two - security details in your code which you expose accidentally and cross site scripting attacks. These are the Javascript specific attack patterns whereas the CSRF pattern works with any language on the backend and with no Javascript code in the frontend and causes a general security concept but two leftmost holes, security holes are the important ones you might have in your application.

If you expose code there, all your Javascript code is always readable by anyone, that's something you have to keep in mind, exposing important information in your Javascript code allows anyone to read and abuse it and cross site scripting attacks allows users to prepare data or prepare links which all visitors of your page might then see and if that data, this prepared data, contains scripts that executes, then for all visitors of your page, these scripts will execute and can do dangerous stuff, like read personal data, send malicious requests with user data to some malicious servers and so on, so you definitely need to protect against these two security holes, for example by sanitizing output by using text content instead of innerHTML and by not leaving any important data in your Javascript code.

----------------------------------------
