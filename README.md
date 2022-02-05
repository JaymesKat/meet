# meet

# Objective
To build a serverless, progressive web application (PWA) with React using a test-driven
development (TDD) technique. The application uses the Google Calendar API to fetch
upcoming events.

# Key Features
1. Filter events by city.
2. Show/hide event details.
3. Specify number of events.
4. Use the app when offline.
5. Add an app shortcut to the home screen.
6. View a chart showing the number of upcoming events by city.


# FEATURE 2: SHOW/HIDE AN EVENT'S DETAILS

As a user, 
I should be able to load an event with the details hidden,
So that I can choose if it pertains to me before seeing the details

As a user, 
I should be able to expand an events’ details, 
So that I can see the specifics of this event

As a user, 
I should be able to collapse an events’ details,
So that I can hide the specifics of this event

Given user hasn’t clicked on event details
When the user searches for an event
Then the event details should be collapsed

Given a user has click to show the event details
When the event details are collapsed
Then the event details should expand

Given a user has clicked to hide the event details
When the event details are expanded
Then the event details should collapse

# FEATURE 3: SPECIFY NUMBER OF EVENTS

As a user, 
I should be able to see 32 events by default, 
So that I can see the unfiltered events

As a user, 
I should be able to specify the number of events I want to see, 
So that I can only see the ones that apply to me

Given a user hasn’t specified a number of events
When they search for events
Then 32 events should populate

Given a user specifies a number of events
When they search for events
Then the specified number of events will populate

# FEATURE 4: USE THE APP WHEN OFFLINE

As a user, 
I should be able to see cached data without internet connection, 
So that I can still see an event without being connected to the internet

As a user, 
I should receive an error message when changing settings without internet connection, 
So that I know why the information isn’t loading

Given a user has no internet connection
When they are accessing the app
Then they should see the cached data

Given a user tries to change settings 
When they have no internet connection
Then they should see an error

# FEATURE 5: DATA VISUALIZATION

As a user, 
I should be able to see a chart with upcoming events in each city, 
So that I can easily navigate the information from the app


Given a user has searched for events
When they specified a city
Then they should see a chart with upcoming events


