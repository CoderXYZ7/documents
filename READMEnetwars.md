
# NETWars
## Design philosophy
NETWars is a strategy game inspired by battleship, a game based on luck and pattern prevision.
### Design Rules
1. The player should be always able to win, independently from the state of play.
2. Randomness is emphasized.
3. The artistic direction is Pixel-art.
## Involved Technologies
- Docker
- Html
- Maria DB
- SQL
- JavaScript
- CSS
- PHP
- Python
## How it will work on the technical side of things

| Name | Docker | Scope | Techs |
| ------------ | ------------ | ------------ | ------------ |
| Backend | nw-backend | managing the game logic | Python(?) SQL |
| Frontend | nw-frontend | displaying the interface to the user | Html CSS PHP JS |
| Database | nw-db | storing the data of the players an game | Maria DB SQL |

### Docker
The game will be running on a system called Docker.
Docker is a platform that enables developers to automate the deployment of applications within lightweight, portable containers. These containers package the application code along with its dependencies, ensuring consistent behavior across various environments, from development to production.
This will enable us to build the one of the parts of the game at a time without the need of having the other two already in development.

As said before we will have 3 containers:

### Backend
It will be an API container that will manage the communications between the Frontend and the DB.
It will be written in Python (probably) using a network library like Flask, that makes possible to interrogate the DB trough a secure connection between the Frontend and the Backend, without exposing the DB credentials.

### Frontend
It will be a simple Html page with all the required languages to make it pretty an working.
This will be the interface between the user and the game.

### Batabase
The DB will store all the data in tables for the game and the users.

## Gameplay
The gameplay will be turn based, at the start of the game the player will have a cache of fishes from random pool, the fishes are used as ammo to sink the enemy boats.
The fish-trowing system works on a First in-First out.
The fishes will be a limited resource that must be replenished by fishing a card (this wordplay works better in Italian).
There are fishes that have special abilities of disabilities.
Those include but are not limited to:
- Exploding Fish
- Poison Fish
- Dumb Fish
- Flying Fish
- Instant use
- Heat seaking fish
- Hit in strange patterns Fish
- Long Fish
- Average Fish
- F.I.S.H.

In his turn the player will have to chose between trowing a fish and fishing a fish.

# Interface
The interface will be divided in tree pages, a login page, a game selection page and a game page.
The login page is a simple page where one can register (simply inserting a username and password that will be added to the datab
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjEyNzcyNDAxOCwtMTgwOTcyOTY3NF19
-->