# FulfillFlow – Fulfillment Control Tower

A simple internal web app for a small e-commerce fulfillment team.
Built for the XYZ take-home assignment (Fulfillment Hub).

**Live demo:** [https://shipflow-bhagya.netlify.app](https://shipflow-bhagya.netlify.app/)

## Run locally
Download **index.html** and open it in any browser. No install needed.

## What it does
- Dashboard: priority orders, overdue or at-risk orders, open exceptions
- Orders: search, filters, one clear next action per order
- Inventory: recorded vs physically verified stock, main and secondary warehouse
- Transfers: Requested → In transit → Received (main stock updates only after counting)
- Exceptions: log, assign an owner and next action, keep visible until resolved

## Business rules
- At risk: time left to the deadline is less than the time the remaining steps normally need
- Picking is blocked if verified main-warehouse stock is too low
- Packing is blocked if the picked variant doesn't match the order
- Staging requires a location
- Orders move one step forward at a time, so nothing ships before courier handover is confirmed
- Couriers whose pickup is after the deadline can't be selected

## Demo limits
- All data is fake: 10 sample orders (real volume is about 200–300 a day)
- No real courier or marketplace connections
- Data is saved in the browser only
- Stage time estimates are assumptions

Built with HTML, CSS and JavaScript, with AI assistance.
