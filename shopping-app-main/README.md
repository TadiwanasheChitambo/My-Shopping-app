Built by Tadiwanashe Chitambo
My Shopping App  is a simple but effective shopping list application with offline support. Here's a breakdown of its key features and how it works:
Key Features & Technologies:
	1	Dexie.js for Local Storage
	◦	The app uses Dexie.js, a wrapper around IndexedDB, to store shopping items locally.
	◦	The database (ShoppingApp) has a table items with fields: id, name, price, and isPurchased.
	◦	This allows the app to work offline and persist data even after refreshing the page.
	2	Progressive Web App (PWA) Features
	◦	A service worker (sw.js) is registered to enable caching and offline access.
	◦	A manifest file (manifest.json) defines app icons, colors, and behavior when installed.
	◦	The app is installable on mobile or desktop, mimicking a native experience.
	3	User Interface (index.html)
	◦	Simple form to add item name, quantity, and price.
	◦	A dynamically updated list of added items with checkboxes for marking purchases.
	◦	A total price calculator displaying the combined cost of selected items.
	4	Core Functionality (index.js)
	◦	Adding items: Saves new entries to IndexedDB.
	◦	Displaying items: Populates the UI from the database on page load.
	◦	Marking purchases: Updates isPurchased status when checkbox is clicked.
	◦	Removing items: Deletes an item and refreshes the list.
How the App Works (Flow):
	1	User opens the app → Service Worker ensures assets are cached.
	2	User adds an item → Data is stored in IndexedDB.
	3	User checks an item as purchased → Updates the database.
	4	User deletes an item → Removes it from the database and updates the UI.
	5	User closes & reopens the app → Data persists due to IndexedDB.



