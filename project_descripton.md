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
Name:XYZ
PICKUP:HKT
DROP:CNX 
FROM:2026-03-01 10:00 
TO:2026-03-05 14:00 
`

And the moment you make a typo/error, the entire booking will either fail or be wrong.

I have thought of a way to work around this and I could technically setup an automation via n8n platform (a platform that connects web-hooks/AI/scripts) where we send info (message/email), this triggers n8n webhook, the platform then passes the information to a bot (AI), the bot reads the information, parses it and creates the booking. There are costs for this but they aren't overly high, my estimate is 50-55 euro a month (though note that bulk of this price is n8n subscription and the platform can be used for more than just this project)

^ this should in theory/technically work even on vik-rent-car, the issue is that the AI (LLM) models we have now are nowhere close to being perfect or unfaultable, they can make mistakes so you will still need a person who checks over the bookings once in a while.  



**My evaluation:** Personally this is doable project for me on a 5 month deadline, 6 months would be preferable. Would obviously need to talk about expectations/feature set if there is anything unclear/missing from what I outlined. This is also a basis (V1) that can be further expanded on in the future. 
