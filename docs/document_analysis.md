# Document Analysis

## Scope

Telles is a microblogging application with the same principles as Twitter. The heart of its operation are the _tells_: small posts written by users, possible and referential within the platform itself.

## Macro Flow of Activities (BMPN)

## Actors

- <ins>Teller</ins>: the user of Telles.

- <ins>System</ins>: the application itself.

## Glossary

- Tell: micro-post made by a Teller. It can contain text only, image only, or both.
- Retell: analogous to retweet, may contain other texts and images.

## Requirements

### Functional

#### The <ins>Tellers</ins> can:

- __FR1__: create a account on the <ins>System</ins>.
- __FR2__: login.
- __FR3__: create a _tell_.
    - __FR3.1__: insert a image when creating a _tell_.
    - __FR3.2__: answer to other's _tells_.
    - __FR3.3__: _retell_ another _tell_.
- __FR4__: edit the profile attributes like name, nickname, profile picture and the contents of a specific _tell_.
- __FR5__: delete his account.

### Non-functional

#### About security, the <ins>System</ins> must:

- __NFR1__: be designed to handle [SQLInjection's](https://owasp.org/www-community/attacks/SQL_Injection) and [Bruteforcing](https://owasp.org/www-community/controls/Blocking_Brute_Force_Attacks) attacks.
- __NFR2__: accept __only__ `.jpg` and `.png` file formats.
- __NFR3__: be built with the following technologies:
    - ExpressJS (>= 4.0);
    - SQLite (>= 3.4);
    - Bootstrap (>= 5.0);

#### About technical restrictions, the <ins>System</ins> must ensure that:
- __NFR4__: each email have only one account.
- __NFR5__: each _tell_ has only one image embedded.
- __NFR6__: all the passwords are stored with bcrypt hashing.
- __NFR7__: all the communications are made through HTTPS.
