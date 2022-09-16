A description of the problem you wish to solve or the application you wish to develop, and, more specifically, what you plan to demonstrate at the end of this project.

Our plan is to undertake an almost standard project, creating a website that allows users to explore information about the hobby of board gaming, with a specific focus on those who are newer to the hobby. By the end of the project we want to have developed a robust backend with efficient data storage solutions, an API layer to expose this backend to the public, and a user friendly front end that allows users to easily obtain and analyze the data they are presented with.

How it is important, interesting, and/or useful; and how it involves data management.

Board games have expanded far beyond the scale of family Monopoly night and simple card games in recent times. As an example of just how large this hobby has grown we need not look further than GenCon: the worlds largest board game convention. GenCon had almost 70,000 attendees in 2019, a number that other conventions such as UK Games Expo in the UK, Essen Spiel in Germany, and Games Market in Japan are inching towards in their own right. This explosion in popularity has of course been mirrored by an explosion of new board games. There are hundreds of new games that come out each year, each with designers, publishers, and artists who make them happen. Not only that, board games often utilize core mechanics seen in other games prior, such as worker placement or hand management to name a couple. All of this information lend board games to be a perfect topic for our databases project. 

Initial thoughts on how to approach the problem or build the application, including the preliminary system architecture and the platform you plan to use.

While at least two of our group have experience working with various web technologies, we at this point are planning on following the architecture proposed by the standard project. If at some point in the future we find that our project would benefit from a tweak in said architecture, we will discuss the merits of both be for making the change or not. Regardless, at the moment we plan to use Python, Flask, and PostgreSQL for our project.

Survey of previous and/or related work and systems, including discussions of how they relate to your problem as well as their limitations and/or flaws.

https://boardgamegeek.com/ (BGG) is the place to go for information about board games. The amount of information on the site, however, could be overwhelming or unintuitive to someone new to the hobby. We want to emulate BGG in some ways such as keeping info on rankings and mechanics, but present it in such a way that new board gamers have an easier time processing the info. Something we would also like to add is what a good pathing might look like in regards to what games would on ramp new gamers into the hobby most effectively, which could lend itself to some cool visualizations. BGG has a lot of data that we will probably be pulling from in order to populate our site as well.

Current Specs

## Users
- A new user can register for a new account; an existing user can log in using email and password.
- Each user account has a system-assigned id. Other account information includes email, username, and password. Users can update all information except the id. Ensure that email is unique among all users.
- Users can add games to their collections, which will have an associated date 
- Users can browse their history of additions to various collections, sorted in reverse chronological order by default. For each game in this list, show a summary and link to the detailed game page.
- Provide a public view for a user. It will show the account number and name as well as any other summary information you deem necessary. If the user also acts as a designer/artist/etc, show also email, address, and include a section with all reviews for this position.

## Games
- There is a list of predefined game mechanics, and each product belongs to one or more categories.
- At the minimum, a game should have a name, a description, an image, player count, complexity, length, and rating.
- Users can browse and search/filter all games. For each game in the result list, show a summary (e.g., image, name, average review rating, etc.) and link to the detailed game page. At the minimum, support browsing by category, searching by keywords in name/description, and sorting by rating.
- A detailed game page will show all details for the game, together with a list of contributors (designers, publishers, artists). The page should also include a section showing all reviews for this product (see Feedback / Messaging).
- Users can log plays of games

## Collections
- Each user can make collections. Games can be added to collections from their detailed pages. Each item in a collection refers to a specific version of a game by some designer/publisher. Collections' pages should summarize information about the games present such as the different mechanics present, range of complexities etc. It should also provide ways to edit the collection by remove and reordering games, as well as adding collections to other collections.
- Collections can be made public after which the collection can no longer be edited by its creator (tho it can still be removed). A published collection should be able to receive comments from other users as well as be duplicated by any into a copy of said collection. 
- Games with logged plays are automatically collected into a collection for the user

## Commendations and Recommendations
- Users can give a commendation to a published collection. These commendations are given based on the list being especially well tuned to whatever the list sought out to be. 
- Recommendations will have two forms, 
 - low complexity games for each type of mechanics
  - These will be there to onramp new players with easy games
 - Recommendations that are auto generated based upon the current contents of a collection
  - More games like these
  - Make this collection more well rounded
  - What type of group is this collection best suited for currently
  - etc

## Libraries
- Similar to collections, but angled towards actual physical collections
- Keep track of what games and how many of them are in the collection
- take note of what games are in storage, and which are checked out and with whom
- when a game is checked out it should be subtracted from the games that are left in the library

## Feedback / Messaging
- A user can submit a single rating/review for a game. The submission link will be incorporated in the detailed product page (see Products). The user cannot submit multiple ratings/reviews for the same product, but can edit/remove any existing ratings/reviews by this user.
- A user can submit a single rating/review for a publisher, provided that the user has played something from the publisher. Incorporate the submission link in appropriate places in the website, e.g., and the public view of a publisher. Again, the user cannot submit multiple ratings/reviews for the same seller, but an existing rating/review can be edited or removed.
- Each user should be able to list all ratings/reviews authored by this user, sorted in reverse chronological order by default. From this interface the user should be able then select ratings/reviews to update. Incorporate the link to this interface in user account view (see Account / Purchases).
- Produce summary ratings for games and publishers; pages or sections showing lists of reviews for games and publishers. At the very least, the summary needs include the average and number of ratings; the reviews lists should be sorted by rating or date.


Further Ideas
## Rulesbooks and the learning experience
- No one really has any data on how easy or hard a game is to learn or get into as a result of its manuals and rulebooks. We could integrate this into the review section but specify some reviews only for rule books and new players.
- Certain people could designate themselves as reviewers, up lift their reviews but allow others to review the reviewer?