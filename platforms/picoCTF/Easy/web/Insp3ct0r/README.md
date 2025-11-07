# Insp3ct0r
> Kishor Balan tipped us off that the following code may need

> inspection:

> https://jupiter.challenges.picoctf.org/problem/9670/ (link) or

> http://jupiter.challenges.picoctf.org:9670

## About the Challenge
A website with a table titled *Inspect Me* that has two clickable column named **What** and **How**.

![Screenshot of the web for the challenge](https://github.com/FikuriKuri/Writeups/blob/b7c6a04ab30747d07855b28cc6789c66a02cb3d3/platforms/picoCTF/Easy/web/Insp3ct0r/images/web-Insp3ct0r.png)

**What** column header responds when clicked, a merged column below it will change into the name of the column header and an *answer*, in this case it says *I made a website*.

![Screenshot of the what column for the challenge](https://github.com/FikuriKuri/Writeups/blob/c4baec3f3e7e1e825fd7274cacac9008d1ceadf1/platforms/picoCTF/Easy/web/Insp3ct0r/images/what-Insp3ct0r.png)

**How** column header also responds when clicked, a merged column below it will change into the name of the column header and an *answer*, in this case it says 
*I used these to make this site:*
*HTML*
*CSS*
*JS (JavaScript)*.

![Screenshot of the what column for the challenge](https://github.com/FikuriKuri/Writeups/blob/c4baec3f3e7e1e825fd7274cacac9008d1ceadf1/platforms/picoCTF/Easy/web/Insp3ct0r/images/how-Insp3ct0r.png)

## How to Solve
Right before going to the web, on the challenge description there are two given hints, the first one says:

> How do you inspect web code on a browser?

While the second one says:

> There's 3 parts

![Screenshot of the web for the challenge](https://github.com/FikuriKuri/Writeups/blob/b7c6a04ab30747d07855b28cc6789c66a02cb3d3/platforms/picoCTF/Easy/web/Insp3ct0r/images/challenge-Insp3ct0r.png)

Based on the name of the challenge, with my assumption that the flag is inside the web's source code, I tried to look inside with inspect tool.

![Screenshot of the inspect tool](https://github.com/FikuriKuri/Writeups/blob/b7c6a04ab30747d07855b28cc6789c66a02cb3d3/platforms/picoCTF/Easy/web/Insp3ct0r/images/inspect-Insp3ct0r.png)

After a brief dive, I found the first part of the flag on the HTML file, right at the end of the file.

```
<!-- Html is neat. Anyways have 1/3 of the flag: picoCTF{tru3_d3 -->
```

![Screenshot of the first part of the flag](https://github.com/FikuriKuri/Writeups/blob/b7c6a04ab30747d07855b28cc6789c66a02cb3d3/platforms/picoCTF/Easy/web/Insp3ct0r/images/first-flag-Insp3ct0r.png)

Then while proceeding, one thing to keep in mind is that the web was made from HTML, CSS, and JS. I look into the *Sources* and.. Bingo.

![Screenshot of the Source in inspect tool](https://github.com/FikuriKuri/Writeups/blob/b7c6a04ab30747d07855b28cc6789c66a02cb3d3/platforms/picoCTF/Easy/web/Insp3ct0r/images/sources-Insp3ct0r.png)

I checked on two of the other files, and Bazinga! two parts of the flag, each one on those files.

on ***myjs.js***:

```
/* Javascript sure is neat. Anyways part 3/3 of the flag: _lucky?2e7b23e3} */
```
![Screenshot of the third part of the flag](https://github.com/FikuriKuri/Writeups/blob/b7c6a04ab30747d07855b28cc6789c66a02cb3d3/platforms/picoCTF/Easy/web/Insp3ct0r/images/third-flag-Insp3ct0r.png)

on ***mycss.css***:

```
/* You need CSS to make pretty pages. Here's part 2/3 of the flag: t3ct1ve_0r_ju5t */
```
![Screenshot of the second part of the flag](https://github.com/FikuriKuri/Writeups/blob/b7c6a04ab30747d07855b28cc6789c66a02cb3d3/platforms/picoCTF/Easy/web/Insp3ct0r/images/second-flag-Insp3ct0r.png)

From all three parts, when arranged we got a flag:
```
picoCTF{tru3_d3t3ct1ve_0r_ju5t_lucky?2e7b23e3}
```