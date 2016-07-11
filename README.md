# Models and migrations

## Introduction

> ***Note:*** _This can be a pair programming activity or done independently._

You and the people at Tunr want to add some functionality to your talent management application.  Specifically, they also want to be able to keep track of their managers and the songs their artists put out. Use Google and the [ActiveRecord Official Docs](http://edgeguides.rubyonrails.org/active_record_migrations.html) if you need help and incorporate the requirements below to build on what you did in the previous lesson.  Be sure to do these in order and keep an eye on your ```schema.rb``` file to see that your migrations are working properly!  Also, think about the most appropriate datatype for each migration and use your discretion as you write them.  The views and controllers are set up for you.

## Exercise

### Requirements

#### Part 1
  You can use `rails g scaffold` to generate the model, view and controller files in one go in this part.

  - Create a manager class that inherits from ActiveRecord

    - For this class, create a table in your database and the corresponding forms that collect and display information about the manager's name, email, and office number.

  - Create a song class that inherits from ActiveRecord

    - For this class, create a table in your database and the corresponding forms that collect and display information about the song title, duration, year of release, and album title.

  - Remember to do `rake db:migrate`

#### Part 2
  Since the model files have been generated already so you can no longer use `rails g scaffold` in this part of the lab. Instead, you can try to generate the migration scripts using `rails g migration` manually and then make the changes to the model, view and controller files by hand.

  - Add a phone number column to the manager table as an integer
  - Change the phone number column to a string
  - Add a downloads column to the song table
  - Rename the phone number column to "cell phone number" in the managers table
  - Remove the downloads column from the song table
  - Add a column to the song table called artist last name

#### Testing

  - In order to make sure all is working well, Add one record for artist, manager, and song that has this information:

  - **Artist**:

    - Name: Kevin Rox
    - Photo URL: "http://png.clipart.me/graphics/thumbs/144/anime-manga-rock-star-guitar-player_144647441.jpg"
    - Nationality: Italian
    - Instrument: Guitar
    - Home Address: 100 Rocks Lane

  - **Manager**:

    - Name: Ricky Bobby
    - Email: rbobby@gmail.com
    - Office Number: 516-877-0304
    - Cell Phone Number: 718-989-1231

  - **Song**:

    - Title: The Best Song Ever
    - Duration: 3:31
    - Date of Release: 7/13/2015
    - Album Title: Best Album Ever
    - Artist Last Name: Rox

#### Bonus
  1. Try to update the `*.erb.html` view files so that the changes to the DB columns in Part 2 can be reflected in the application? `erb` is just similar to `ejs` so you should have no trouble using it!!
  1. If you still have time and you don't like the look-and-feel of the scaffold, feel free to update the HTML/CSS!!


#### Starter code

Fork and Clone this repo and start working

#### Deliverable

A whole bunch of migrations, and your ```schema.rb``` file should look like this:

![](http://s29.postimg.org/4sw62q90n/Screen_Shot_2015_07_13_at_12_00_36_PM.png)

## Additional Resources

- [ActiveRecord Official Docs](http://edgeguides.rubyonrails.org/active_record_migrations.html)
