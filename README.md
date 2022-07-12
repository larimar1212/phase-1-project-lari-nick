## Project goal: create a 'lite' version of reddit with content displayed from the reddit API

The content will show in two places: a block of posts across the top of the page that display on page load, consisting of something like top posts from r/all, and a main content section that is only populated when a user submits a form. The minimum requirement for form submission is a subreddit title, but the user should be able to select (by dropdown) search options such as sort method, number of posts to display, unit of time, and length of time. Default values for the search options should be top posts from the past 24 hours.

Specifications:

The top container will be a div. On page load, this div will be populated with child divs that have
- a background image
- a heading/div element with a subreddit name
- a heading/div element a thread title
- a heading/div element with a number of upvotes

Each of these should come straight from the database.

The user will submit info through a form to display content in the main container. This container will be a div that, upon form submission, will display child divs for different posts, each with
- a thumbnail
- a heading/div element with a subreddit name
- a heading/div element a thread title
- a heading/div element with a number of upvotes
- a paragraph/div element with the post text (if applicable)

The number of threads displayed will be 10 by default, but the form should allow the user to select 10-25-50 posts to display

STRETCH FEATURES:

- Dark mode
- Allow media playback
- Allow user to expand images to larger size
- Allow user to expand text from a thread if it exceeds a number of characters

NOTES ON THE DATABASE:

1) NOT ALL POSTS HAVE IMAGES
2) SOME POSTS ARE VIDEOS
3) NOT ALL POSTS HAVE SELFTEXT
4) NOT ALL DATA HAS A POST HINT

For ease of displaying things to the page, we should maintain an array of objects for both containers. When we fetch data, we should update an array with objects that contain the fetched data. These objects should populate the top div on page load.

When the user fills out the form and hits submit, we should fetch data again and simply push to a new array with a new set of objects. Or an array inside an array. Who knows?

## Summary for getting started 7-12-2022

FINAL PROJECT GOALS:

- Finish div at top of screen (display text from object over background)
- Complete the form/improve form functionality and appearance
- Include a box in lower 1/2 of screen that will show a preview of posts based on values input into the form

ADDITIONAL POSSIBILITIES:

- Option to load more posts at the top (get the next set of 4 from the database, for instance, or a side scroller or carousel)
- Option to toggle types of content (e.g. only images/videos)
- Option to remove the top bar
- Option to replace the top bar with "favorites"





