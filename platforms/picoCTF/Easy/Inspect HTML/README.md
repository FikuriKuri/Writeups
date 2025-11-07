# Inspect HTML
> Can you get the flag?

> Go to this website and see what you can discover.

## About the Challenge
A website with only a glimpse of information about <ins>Histiaeus</ins> from *Wikipedia*

![Screenshot of the web for the challenge](Writeups/platforms/picoCTF/Easy/Inspect%20HTML/images/web-inspect-html.png)

## How to Solve
Right before going to the web, on the challenge description there is a given hint which says:

> What is the web inspector in web browsers?

![Screenshot of the challenge hint](Writeups/platforms/picoCTF/Easy/Inspect%20HTML/images/challenge-inspect-html.png)

Based on the challenge name and the hint, it is clear there is a relation between the hints and the flag.

So I tried using the inspect tool on the website.

![Screenshot of the inspect tool](Writeups/platforms/picoCTF/Easy/Inspect%20HTML/images/inspect-inspect-html.png)

After a brief dive, I found the flag in a comment below a '<p>' block.

![Screenshot of the flag](Writeups/platforms/picoCTF/Easy/Inspect%20HTML/images/Screenshot%202025-11-07%20165227.png)

'''
picoCTF{1n5p3t0r_0f_h7ml_fd5d57bd}
'''