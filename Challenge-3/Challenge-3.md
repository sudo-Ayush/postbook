# Insecure Direct Object References [IDOR] in Input Form

* **Postbook Challenge 3**

## What are insecure direct object references (IDOR)?

Insecure direct object references (IDOR) are a type of access control vulnerability that arises when an application uses user-supplied input to access objects directly. The term IDOR was popularized by its appearance in the OWASP 2007 Top Ten.

## Steps to Reproduce:

* Click on "Write a new post".
* Fill "Title" and "Post" contents.
* Before clicking on "Create Post", right click on the button and select **inspect**.
* Locate the following element
```html
<input type="hidden" name="user_id" value="2">
```
* Change the value to '1'.
```html
<input type="hidden" name="user_id" value="1">
```
* That's all.

## Impact:

- The attacker will able to create any post as **Admin**.

## POC:

![1](https://github.com/sudo-Ayush/postbook/blob/main/Challenge-3/poc/1.PNG)
<br>

![2](https://github.com/sudo-Ayush/postbook/blob/main/Challenge-3/poc/2.PNG)
<br>

![3](https://github.com/sudo-Ayush/postbook/blob/main/Challenge-3/poc/3.PNG)
<br>

![4](https://github.com/sudo-Ayush/postbook/blob/main/Challenge-3/poc/4.PNG)
