# Splith App Planning

## Primary App Features
The main function of Splith is scanning receipts and splitting the cost amongst multiple people based on which items they are responsible for. The primary example is as following: a group of friends goes out to eat dinner, where they order their own items as well as a few items to share. At the end, a single bill comes out and one person pays it, but everyone else needs to pay that person what they ordered. Splith lets you select who ordered what, who shared what, and proportionally split tax and tip according to how much they paid. 

The tertiary function of Splith uses the main scanning function, but specifically is utilized for trips where a group accumulates multiple expenses together. This trip creation function should allow multiple receipts to accumulate.

### Comprehensive Feature List
- Sign in and Authentication
    - Sign in/Sign up with email/password, google, or apple
    - Add venmo information in onboarding flow
    - Choose user tag in onboarding flow
    - Persistent database to retain receipt and trip history

- Homepage
    - Show current trip
    - Show main button to scan receipt
    - View incomplete pipelines where receipt was scanned but not fully split (? maybe not necessary)
    - Show tabs of trips (trip history), receipts (receipt history), and user (user page)
    - Show recent receipts
    - Display receipt upload limit

- Single and batch receipt upload
    - Stage 1: Take photo or choose from album
    - Stage 2: Confirm information - AI autofills information but needs to be confirmed
        - When certain fields are altered, should add a checkbox that asks if this change wants to be remembered (e.g. Name field of CPT -> Chipotle)
    - Stage 3: Split bill
        - Add people (This doesn't need to be done if the receipt is done within a trip where group members are designated)
        - Designate who got what
        - Add item share option, where two people split the cost of one item
            - Defaults to even split, have option to designate an uneven split
            - Add an "everyone" option for item share that splits evenly amongst everyone for family style items (could be this or add a group member named 'everyone')
    - Stage 4: Bill summary
        - Show simplified summary of how much each person owes
            - Should be easy to copy or screenshot to send to a groupchat
        - Option to show exact itemized breakdown of one person's cost
        - Option to generate venmo requests if a user has their venmo information set up
    - Uncertain where these functions should be in the flow:
        - Assign who paid for the bill (probably in stage 4)
        - Add receipt to trip

- Trips for groups
    - Create trip
    - Delete trip (needs confirmation)
    - Add receipt to trip from receipt history
    - Add new receipt to trip (Does same flow as normal receipt upload but uses persistent group members)
    - 

- User Page
    - View usage limit details
    - Show dashboard of uploads
    - Change password
    - Delete account (needs confirmation)
    - Update venmo

## Product Phases

### V1 - MVP
- Master single file receipt upload functionality
    - Maximize scanning accuracy


### V2


### V3 - Build out paid/free tier



## Stack
Splith is meant to primarily serve as a mobile platform, both as a web app and as a mobile app. The web app should be reactive so that UI/UX still makes sense on larger screens such as ipads and computers. I believe React native and React native web will accomplish this best, though if you have a strong opinion for an alternative, I am open to such opinions. I plan to use Expo to maintain a monorepo. I would like to use Typescript on the backend. 

## App Flow

### Remaining app flow decisions to be made
- When a trip is active, should receipts generated apply to that trip by default?
- 