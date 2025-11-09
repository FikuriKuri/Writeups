# IntroToBurp
> Try here to find the flag

## About the Challenge
A website with a simplistic register page. It expects user information in order to complete the registration.

![Screenshot of the web for the challenge](https://github.com/FikuriKuri/Writeups/blob/0e9e5f7dab3c8eae1373e0f16279b0d11ade25ab/platforms/picoCTF/Easy/web/IntroToBurp/images/web-IntroToBurp.png)

## How to Solve
Right before going to the web, on the challenge description there are two given hints which says:

> Try using burpsuite to intercept request to capture the flag.

> Try mangling the request, maybe their server-side code doesn't handle malformed requests very well.

![Screenshot of the challenge hint](https://github.com/FikuriKuri/Writeups/blob/0e9e5f7dab3c8eae1373e0f16279b0d11ade25ab/platforms/picoCTF/Easy/web/IntroToBurp/images/challenge-IntroToBurp.png)

Based on the challenge name and the hint, Burp Suite will be sufficient to solve the flag.

So I tried using the Burp Suite on the website.

After registering, the website asked for a 2FA Authentication code, which I did not get. So, I entered random word into it, and it returns *Invalid* page

![Screenshot of the invalid page](https://github.com/FikuriKuri/Writeups/blob/0e9e5f7dab3c8eae1373e0f16279b0d11ade25ab/platforms/picoCTF/Easy/web/IntroToBurp/images/invalid-IntroToBurp.png)

From the second hint, there must be something interesting so I looked on the request and response through the use of *intercept* tool. While sending the second 2FA code, I intercepted the request and erased the OTP.

![Screenshot of the intercept page](https://github.com/FikuriKuri/Writeups/blob/0e9e5f7dab3c8eae1373e0f16279b0d11ade25ab/platforms/picoCTF/Easy/web/IntroToBurp/images/2fa-IntroToBurp.png)

And , VOILA! I got the flag

![Screenshot of the flag(1)](https://github.com/FikuriKuri/Writeups/blob/0e9e5f7dab3c8eae1373e0f16279b0d11ade25ab/platforms/picoCTF/Easy/web/IntroToBurp/images/flag-IntroToBurp.png)

![Screenshot of the flag(2)](https://github.com/FikuriKuri/Writeups/blob/0e9e5f7dab3c8eae1373e0f16279b0d11ade25ab/platforms/picoCTF/Easy/web/IntroToBurp/images/flag2-IntroToBurp.png)

```
picoCTF{#0TP_Bypvss_SuCc3$S_e1eb16ed}
```