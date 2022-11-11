## Idea

OP Crypto, a Web 3 venture capital fund, has suggested that we build them a tool to manage internal workflow and automate various processes between different communication tools and workforce management software they use. Currently, the fund uses Telegram as an internal communication tool and has a "Deals" groupchat where all team members send in decks and fundraising details for projects they have sourced. This information is then mannually uploaded onto Monday.com to compile information of different deals during due diligence.

We want to create an solution that sends daily updates to the deal groupchat (with a telegram bot) about how many new deals were added to the pipeline, total number of deals in the pipeline, number of deals per person, number of deals have been there longer than 48 hours, number of deals older than 48 hours per person.

## Implementation
For this exercise, we will require an addition of two APIs minimum. The first is the monday.com API, which will allow us to retrieve and edit data from the monday.com work OS. This way, we will be able to sync data between monday.com and telegram, as well as any other tools we decide to add. The API is built on GraphQL, which is different from the schematic of REST APIs, overall we think it will be easier to query objects and fields using this API. Using this API, we will have to use only JSON-formatted bodies, however with file uploads, we can use multipart requests. 

Our second API will be the telegram bot API, in addition to his, we will be using a librarythat provides a pure python interface for the telegram bot API. This library - .python-telegram-bot-module - will provide a bunch of high level classes that we believe will make easier to make out bot. 

The rest of the program should come straightforward, with us using the monday.com API to recognize late/updated work events, and transmit the information to the right groups via the telegram bot API.


## Schedule
We plan to initailize our API's with the respective keys and working nature by the end of 11/13 - on the weekend. This will ensure any last minute problems due to API issues be reduced/avoided. 

Our next plan of action is make sure that we make steady progress, working on a bit of code every couple of days. Our main goal is to not email the professor the day before submission explaining how we're confused. 

Another step we aim to include is adding features and other cool additions to our program. If we make good progress with our program, we can add features such as text updates, reminders, and even terms for transmitting updates. 


## Learning Goals
We see big potential room for learning with what we're creating. Especially within the information space as we use live data to improve efficiency within organizations. 


## Collaboration Plans
Hrishi will work at ensuring we have the best APIs for what we are trying to accomplish, this may include swithcing APIs in the future. Mads will be in charge of sound logic for the bulk of our program, ensuring that we can save time and characters where we can.