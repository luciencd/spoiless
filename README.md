# spoiless
Remove reddit spoilers API
To test out using Docker:

$ git clone "https://github.com/luciencd/spoiless/"

$ git submodule update --init --recursive

$ docker-compose build

$ docker-compose up

Enter localhost:5000 in browser.

Try out commands like: localhost:5000/getShows or localhost:5000/createUser

This repository is just acting as the parent directory for 3 smaller submodules which each have their own purpose.
