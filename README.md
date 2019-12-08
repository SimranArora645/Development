Readme-


Instructions on how to run locally:
To run our site locally, download our files (src, public, package.json) and unzip each one individually. Then, navigate into the folder containing all of these files and run “npm install” in order to get the node-modules. Then, run “npm start” and the site will open in your browser.


Design Principles and Considerations:
Our interface relates some of the design principles. One of the key concepts we kept in mind while designing the webpage is affordances. Our interface has a well-defined navigation bar with clear options. Moreover, the dropdown buttons with their downward arrows make it intuitive for the user to know that these buttons have to be clicked to see other options and filter based on them. The user can conveniently see that the 2 main categories of items served at Jeff’s cafe are Beverages and Baked Goods, with the ability to further sort items based on Popularity and view favorited items only. All of these clearly defined and labeled features as well as options make our interface intuitive in terms of usability, learnability and memorability, all of which are key design components. The menu has pictures of items to make it more visually appealing in addition to the name of the items. The price of each item is mentioned directly under it to avoid any sort of confusion and to help users get an idea of what the price range of dining at the cafe would look like. We also have a grey bar that shows the Item Type, Sorting Method and Favorites labels to further make the process more intuitive and help the user distinguish what filter/option they are searching under.


Passing Data:
Our site is composed of 5 components: Search, Navigation, FilteredList, List, and Labels. In addition to FilteredList, we have 2 additional components to facilitate smooth user interaction. These components are Search and Labels.
Search is the parent class of Navigation and FilteredList. FilteredList is the parent class of List and Labels. Search passes (via props) a boolean to Navigation that indicates if the current page is the home page or not. Navigation uses this to update its state and determine what page to display and what url to navigate to. (Our navigation bar is not one of our additional two components and does not actually work but it does work as a reset button. It’s there mostly for style.) Search updates its state to the searched item and passes to FilteredList (via props) the inputted search query, the list of menu items, and the onSearch function that tells the site what is being searched for. Our “Display All” button (which functions as a reset on the filters - except sorting) is designed in such a way that it does not remove the input to search. Therefore, clicking the “Display All” button while simultaneously searching for an item will reset the filters, but will still only show the items that match the search.
FilteredList uses the props passed to it from Search to perform searching and to filter on the menu items, as well as handling favorites. It updates its state whenever a filter is changed or an item is favorited. FilteredList passes to Labels (via props) the filters that are currently being applied. Labels uses these props to update its state and display the state (aka display what the currently active filters are). FilteredList also passes to List (via props) the list of items (with the filter and search applied) and a helper function used for displaying the items.


User Interactions and State Changes:
The user triggers state changes every time they search for an item, apply a filter, favorite an item, press the “Display All” button, or press any of the Navigation bar buttons.


Overall high level goal of the Website:
The website allows users to look at the menu of Jeff’s cafe and find items as per their preferences and dietary restrictions by following a few simple steps. The labels are clear and straightforward and thus, allow users to filter and narrow down the scope of all the items offered, helping them manage their time more efficiently instead of looking at a long, confusing menu to find the item of their choice. Each item has an image and its price next to it to make it the interface more user friendly and help customers get a sense of the cafe’s offerings.


Purpose of our Website:
This website is particularly useful for people who are coffee lovers, for college students who enjoy working in cafes and getting away from college campus as well as for the working population that does not have a lot of time to look at huge menus and would highly prefer sorting through all the items to find bakery items/beverages that best fit their taste and dietary restrictions. It also provides users with the option to mark items as favorites and go back to them later instead of having to repeatedly look through the menu each time they want to place an order.
