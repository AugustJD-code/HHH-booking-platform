Description: home-brew car booking, WP-based plugin.

**Features for V1:**

- Front end booking wizard (step-by-step booking process from date/location selection, car selection to paying)
- Fleet/car based view and availability
- Clean WP dashboard that offers:
	- car type + unit 
	- drop-off/pick-up locations
	- order list
	- calendar view of the orders
	- A 'basic' pricing model
		- flat fee based on days booked
		- a fee attached to each drop/pick location
		- tax
		- ability to % increase prices for specific seasons
	- Automatic sending of document (email/pdf/invoice) to clients that book
	- Ability to extend booked days for orders
	- A one way sync to google calendar
	- A notificaiton to Line/What's app
- A bot that helps/guides customer through the booking process
- payment via stripe and paypal (possibly bank transfer)


**Problematic features:**
- two-way sync (creating bookings based on google calendar entry or a message from line/what's app)
^ this feature will have the same issue as it has with VIK. It's technically possible but highly impractical, the issue is that if this is script-based you will always have to follow a strict format like:
`
CAR:YARIS
PICKUP:HKT
DROP:CNX 
FROM:2026-03-01 10:00 
TO:2026-03-05 14:00 
`

And the moment you make a typo/error, the entire booking will either fail or be wrong.

I have thought of a way to maybe work around this 
