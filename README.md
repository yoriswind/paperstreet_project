# paperstreet_project

PaperStreet

A paper trading website where users practice stock trading with fake money. It is a safe place for beginners to learn how the market works without any real risk.

This is a class project. The front end is kept plain on purpose so the team can focus on the database layer, which is the harder and more important part of the project.

What it does

Users sign up and get a starting balance of $10,000 in paper money. They can search for stocks, buy and sell shares, and track their holdings, total value, and a watchlist over time.

Current status

This is an early prototype. The five pages are built in plain HTML with no styling, and the database is not connected yet.

Right now every button shows a popup that explains what it would do once the database is connected, including the MySQL or MongoDB query it would run. After the popup it carries out the front-end step it can do without a backend, like moving to the next page. This lets the team walk through the full flow before the database work begins.

The sample user shown throughout is called "User" and the numbers on the dashboard and portfolio are placeholder values.

Pages


index.html - Home page with Log In and Sign Up buttons
auth.html - Create an account or log in
dashboard.html - Cash balance, holdings, and total value
search.html - Look up a stock, buy shares, add to watchlist
portfolio.html - Holdings, trade history, and watchlist


Tech stack

HTML for page structure and plain JavaScript for form checks, popups, and navigation. CSS will be added later and kept simple. MySQL and MongoDB are planned for the database layer, with Node.js and Express for the server.

How the two databases are split

Each database has its own job so they never need to stay in sync with each other.

MySQL holds the structured data where accuracy matters: a users table for account info, an accounts table for each user's cash balance, and a trades table that records every buy and sell.

MongoDB holds the flexible data that does not need to be perfectly precise: a watchlist collection for stocks each user follows, a price_history collection for past prices used in charts, and a notes collection for news or comments.

Cash balance and holdings come from MySQL. Watchlist and price charts come from MongoDB. Stock prices use sample data built into the project rather than a live feed, since the focus is the databases.

Running the prototype

No setup is needed for the current version. Clone the repo and open index.html in a web browser. The Live Server extension in VS Code also works.

git clone https://github.com/YOUR_USERNAME/paperstreet.git

Roadmap

Week 2: Five pages and basic layout built. One test record reading and writing from each database to prove both connections work.

Week 3: Login plus buying and selling works, with MySQL connected first and MongoDB added second.

Week 4: Charts and final styling done and everything tested.

Team

One person handles the front-end pages and styling, one handles the JavaScript and stock price logic, and one handles the MySQL and MongoDB setup. Everyone helps with testing at the end.

License

Student project for coursework. Not intended for production use.
