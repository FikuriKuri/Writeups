# Username enumeration via subtly different responses
> This lab is subtly vulnerable to username enumeration and password brute-force attacks. It
> has an account with a predictable username and password, which can be found in the 
> following wordlists:

> Candidate usernames
> Candidate passwords
> To solve the lab, enumerate a valid username, brute-force this user's password, then 
> access their account page.

## About the Challenge
A website with a UI of a blog. There is a menu titled *Home* and *My Account* on the upper right side.

![Screenshot of the web for the challenge]()

## How to Solve
The lab session tells us directly that brute-force is necessary in order to login with a user's credentials. So in Burp Suite I went to the *Intruder* tool. There I configure the attack settings for the username, sniper attack with the wordlist provided. Then I started it.

For a while the result may look zero, but after further inspection, the correct username does not have a point symbol at the end of the *wrong username* warning. The username was `vagrant`. Therefore, I took that data and proceed with the password.

![Screenshot of the correct username]()

And then, after a while, I found the correcct password, which was `thunder`

![Screenshot of the correct password]()

Then, I inserted those correct credentials, and finished the lab.

![Screenshot of the finished lab session]()