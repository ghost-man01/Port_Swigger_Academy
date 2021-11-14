# What is XSS
Cross site scripting allows an attacker to compromise the interaction that users have vulnerable application. It allows an attacker to circumvent **same origin policy**, which is designed to segregate different websites from each other.
Cross site scripting vulnerability normally allow an attacker to masquerade as a victim user, to carry out actions that user an is able to perform and to access any other user's data.
If victim user has privileged access to  within the application then the attacker might able to gain full access over the data.

# How does XSS works
Cross site scripting works by manipulating a vulnerable web site so that it returns malicious JavaScript to users. When the malicious code executes inside a victim's browser, the attacker can fully compromise their interaction with the application. 

![[Pasted image 20211114182132.png]]

# XSS PoC
By injecting a payload that cause your own browser to execute some arbitrary JavaScript. 
alert() is common in practice but print() also recommended.

# Type of XSS attacks ?
There are three main types of XSS attacks.  These are:<br>
**[[Reflected XSS]]** Where the malicious script comes from the current HTTP request.<br>
**[[Stored XSS]]** Where the malicious script comes from the website's database.<br>
**[[DOM-Based XSS]]** Where the vulnerability exists in client side code rather than server side code. <br>
