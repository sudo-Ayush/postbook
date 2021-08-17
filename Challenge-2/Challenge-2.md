# Insecure Direct Object References [IDOR] in URL

* **Postbook Challenge 2**

## What are insecure direct object references (IDOR)?

Insecure direct object references (IDOR) are a type of access control vulnerability that arises when an application uses user-supplied input to access objects directly. The term IDOR was popularized by its appearance in the OWASP 2007 Top Ten.

## Steps to Reproduce:

* Look the URL
```
http://34.94.3.143/6ebb71d6f6/index.php?page=view.php&id=3
```
* Try to change the ID in the URL
```
http://34.94.3.143/6ebb71d6f6/index.php?page=view.php&id=2
```

## Impact:

- The attacker will able to see the information of different users by simply changing the '**id**' in the **'url'**.

## POC:

![1](https://github.com/sudo-Ayush/postbook/blob/main/Challenge-2/poc/1.PNG)
<br>

![2](https://github.com/sudo-Ayush/postbook/blob/main/Challenge-2/poc/2.PNG)
