# 2FA broken logic
> This lab's two-factor authentication is vulnerable due to its flawed logic. To solve the 
> lab, access Carlos's account page.

> Your credentials: wiener:peter
> Victim's username: carlos
> You also have access to the email server to receive your 2FA verification code.

## About the Challenge
A website with a UI of a blog. There is a menu titled *Home* and *My Account* on the upper right side.

## How to Solve
The lab session tells us directly that we have to login as `carlos`. In this case however, we are in control of an account by the name `wiener`.

I attempted to go ahead and logged into the account by the name `wiener`. And two things to note are, the login uses two-factor authentication, also in this session we got an email page.

While checking for the HTTP history, there are two requests that caught my eyes. the first one is `GET login2` and the second one is `POST login2`.

Now both of these have different functions on their own, but these are keys to enter the web as `carlos`. I took the `GET login2` request and move it to the *Repeater* tool. From there I ran it, in order to get the 2FA code.

![Screenshot of the repeater]()

Now for the `POST login2`, I entered a wrong code for the authentication before taking the request from HTTP history. After that, I moved the `POST login2` to the *Intruder* tool. Here comes the hard part, I use brute-forcer to the OTP numbers that I get from my previous login attempt, four numbers in any position. Then, I ran it. Not long after luckily, I got the OTP numbers.

![Screenshot of the intruder tool]()

Then, I opened the web page for the correct response, and finished the lab.

![Screenshot of the finished lab session]()