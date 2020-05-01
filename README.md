
# Barterbook - Jack Perry & Joe Gelay

Barterbook is our Flatiron School's Mod 2 Project. We came up with the idea to create a website that gives people the ability to connect and barter their services for other's services.
This website is built with JavaScript, Ruby on Rails, HTML, CSS, Bootstrap, and a tiny amount of JQuery. 

### Required Versions

- Rails 6.0+
- Lite-Server

### Before You Start Using

Navigate to the Backend folder and run the following commands in order:<br />
- `bundle-install`
- `rails db:create`
- `rails db:migrate`
- `rails db:seed`

### Starting the Frontend and Backend

To start the servers you will need to:<br />
- Backend:
    - Go into the backend folder and run the following command: `rails s -p 4000`<br />
- Frontend:
    - Go into the frontend folder and run the following command: `lite-server`

### Navigating to the Website

After you have started running the Frontend and the Backend, then you will navigate to `http://localhost:3000/landingPage.html`.

### Website Pages

- `http://localhost:3000/landingPage.html`
    - This page shows a brief description of Barterbox and gives the user the ability to navigate to the Sign In page.
    - This page will pop up with a Toast message if the parameter `?reason=deleted_profile` is added
        - This parameter is added when a user deletes their profile

- `http://localhost:3000/signInPage.html`
    - The user will sign in here
        - Authentication is not working currently, so any username/password works
        - Navigates to the index page
            - Excludes the signed in user from the card list
        - Using a valid email will give you access to My Profile page from the index page
    - The user can also sign up here by entering a username and a password and checking the checkbox
        - They will be navigated to the My Profile page where they can edit their new profile 

- `http://localhost:3000/index.html?email={EMAIL}`
    - The user will be able to see everyones cards besides their own
        - The cards show basic information on the front and more information when you hover over them and flip them
    - Search Bar
        - Can search by the following: Name, Skill, Desired Skill
            - Does a `LIKE %SEARCH_TERM%` search so that anything that contains the search will show
    - Barterbook - Click to navigate back to the Landing page
    - Home - Click to show all of the cards besides your own (resetting after searching)
    - My Profile - Click to go to the signed in user's profile

- `http://localhost:3000/myProfile.html?email={EMAIL}`
    - The user can update their name, profile image, bio, skills, and desired skills here.
    - The user can delete their profile as well
        - Redirected to Landing page with a Toast message if the user deletes their profile

### Video Demo

[![Barterbook Walk-through Video](https://img.youtube.com/vi/258CrIi6kJg/0.jpg)](https://www.youtube.com/watch?v=258CrIi6kJg)

### Authors

* **Jack Perry**  - [Jack Perry's Github](https://github.com/japerry911)
* **Joe Gelay** - [Joe Gelay's Github](https://github.com/joegelay)

### License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
