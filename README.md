# spoiless
Remove reddit spoilers API
To test out using Docker:

$ git clone "https://github.com/luciencd/spoiless/"

//May not be necessary on all git versions
$ git submodule update --init --recursive
//

$ docker-compose build

$ docker-compose up

visit localhost:5000 in browser.

Try out commands like: /getShows or /createUser

This component of the spoiless project is in charge of maintaining a REST API that can respond to numerous calls from the front end.

Most requests will be of simple user changes.

For example, adding/removing/hiding/showing a show to their list of spoilers. Other uses will be to request the list of shows from the database for the user to choose from.

Other requests will be in the realm of collecting data for the machine learning model.

For example, if you find a reddit comment that spoils the ending of game of thrones season 7, you can click on the button at the bottom of a reddit comment which says "spoiler" and that will send the comment with all its features to the database so that the machine learning model can do analysis on it.

Alone, these requests are simple, and we make sure the queries are parametrized to avoid injection attacks.

So far, the requests are accpted by a set of flask functions, and it will probably stay that way because the user backend should be very simple.

This backend is not going to be in charge of intercepting actual requests to classify a comment as being a spoiler or not for a given show. That is the purpose of the machine learning repository
