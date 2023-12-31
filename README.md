# sea-cinema

## About The Project
This project was created as a requirement for enrolling in COMPFEST's Software Engineering Academy. It is a movie ticket booking app that allows users to explore through a wide selection of movies and book tickets. The app includes features in the mandatory phase and the challenge phase.

### Built with
The technologies used in this app are:
- HTML
- CSS
- Javascript
- PHP 
- MySQL

This project utilizes XAMPP as the local development environment, including the MySQL database server.

This project also uses icons from [Font Awesome](https://fontawesome.com).


### File structure
- fonts: The fonts used in this project.
- images: The images used in this project.
- index.php: The main page where users can see listed movies.
- login: The pages for user registration, login, and logout.
- movie-info: Loads the description for a movie that the user clicked.
- profile: The users' profile page. They can view their personal info, modify their balance, and change their password here.
- purchase: The pages for purchasing a ticket. They include a page for selecting date and time, a page for selecting seats, a confirmation page, and a success page for when a user completes a transaction.
- tickets: Users can view and refund their tickets here.

### Setting up the server
1. Make sure Apache is installed.
2. Place the files in this repository to Apache's 'htdocs' folder (depends on the document root directory, for Windows it's typically 'C:\xampp\htdocs').
3. Start the Apache service.

### Setting up the database
1. Make sure to have MySQL installed and start the service.
2. Create a new database named movie_booker.
3. Import movie_booker.sql to the database.

## Features

### User registration / login / logout
Users register by entering their username, password, and age (the page asks for their birth date so their age can be constantly updated). Each input components are validated before being saved to the database. The user is then redirected to the main page. Registered users can login by entering their username and password. Users can log out once they're done with their session. Unregistered users can still view movies and their description but they can't buy tickets or access user-only features (viewing tickets, changing their balance).

### Movie booking process
Users view movies from the main page, then they can click on the movie they want to watch. A new page with the description of the movie and a button to buy a ticket will be loaded. If the users are old enough, they will be redirected to select the date (has to be in the future), time (users can choose between 13:00, 16:30, and 20:00 for each movie), and their seats. Users can only book 6 seats at a time.Then, they will be asked to confirm the booking by entering their password. After entering the correct password, users can see their ticket history in the "Tickets" page. They can also refund their tickets.

Note: The default timezone for the booking process is set to Asia/Jakarta.

### User balance
Users can top up or withdraw their balance in the "My Profile" page. The amount is validated first. Users cannot enter anything other than digits and the most they can withdraw is min(500000, current_balance).

### Extra features
Users who want to change their password can do so by going to the "My Profile" page and clicking on the "Change password" button.
