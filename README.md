Multi-player Poker Games

By Herman Chui, Manny Inwang and Leslie Shaw in May 2020
 - Manny Inwang: poker hand scoring engine
 - Leslie Shaw: card table front-end first pass
 - Herman Chui: back-end/DB, other front-end, integration

Features:
 - 5-card stud, 5-card draw, 7-card stud multi-player games
 - Configurable to add variants with arbitrary number of rounds, betting parameters, face up/down cards and number of players
 - In-game messaging to augment game play
 - Players can monitor all active games from the "Card Room" and join any of interest
 - Leaderboard shows best win-loss records and best betting performance

Required virtual environment:
 - Python 3
 - Flask
 - SQLalchemy
 - Flask-socketio

Program files:
 - app.py -- startup file, use "python app.py" to run
 - routes.py -- URL routes, calls controller.py
 - controller.py -- primary routines for each route; redirects/renders pages; uses socketio to trigger other clients
 - utilities.py -- detailed functions called by controller.py; interfaces with database
 - score.py -- poker scoring engine called by utilities.py
 - models.py -- SQLalchemy ORM class definitions
 - config.py -- configuration routines called by app.py upon startup
 - card-room1.db -- SQLalchemy database, can open with SQL Lite
 - templates/... -- html files for all pages
 - migrations/... -- SQLalchemy generated files


