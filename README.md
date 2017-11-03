## ZenDApp

This will be an archive (on IPFS) and voting system for DApp designs based around ERC20 tokens.

### Registration
All users will need to register, maybe with an email address also.
Any user can submit up to 2 designs every X blocks for a small fee.
The design will need to be checked by an admin for validity, and should be a complete DApp.
Any DApp not implementing the ERC20 standard willbe disqualified, and 90% of the fee returned.
The contracts must work, and be callable from the UI.
Any framework can be used to build the DApp.
We will not be able to run all the DApps on our site (but possibly the winners)


### Voting

Registered users will be allowed to vote on designs (perhaps for a small fee) after X blocks the winning design will be archived and awarded 40% of the accumulated ether. Any design not winning after 5X blocks will be removed.
(where X is say 20K blocks)


# Zen ÐApp
Some other suggestions for how the Zen ÐApp webpage would be designed and work:

## Overview
The [CSS Zen Garden](http://www.csszengarden.com/) website provides people with a skeleton HTML file which is not to be changed and asks the designers to provide a new CSS file that when applied to the HTML will create a unique and beautiful webpage; demonstrating the designer's creativity.  

## Goal 
To get ÐApp developer's to focus on the difficult problem of user experience, specifically:
* Wallets and addresses 
* The role of Ether and gas (the user may not have any Ether, the implication of gas price, setting sensible defaults for gas price etc.)
* Web3 providers (different options for the user connecting to the Ethereum blockchain and interacting with Smart Contracts - sensible fallback options).
* Variable, and long, transaction times (and conveying this to the user to set expectations)  
* Updating the user's view of the ÐApp when the state is changed by another user

## General Concepts
* The most version of the ÐApp that provides the best user experience and is most visually appealing will organically be selected by the audience.
* The entered ÐApps will be hosted as part of the main website and linked to from the landing page.
* The Smart Contract will be a constant; and should not be modified as part of the submission. It will provide quite simple functions and events that are logged when a user performs an action. 
* The could be a static HTML file - that perhaps designers can only modify dynamically
* There could be a base set of JS (a library) that interacts with the contracts and that must be used and not modified, but instead extended / enhanced. 
* The CSS is up to the designer(s) and developer(s).

## Skeleton ÐApp

### Initial idea
A voting contract that captures the audiences preference amongst the available ÐApp designs.
* Users signal their approval by sending Ether to the contract in the form of a vote (it could potentially be up to the user how much they send).
* Designers are responsible for the part of the UI that deals with the user voting for their contract.
* The signalled Ether is then split between the winning submission and the audience that voted for that design.
    * A lot of work is potentially required by the designers, so they should get the lion's share of the Ether.
    * The challenge is getting the users to part with some of their Ether rather than just hodl it.
    * Hopefully, the fact that the both the designers and some of the voters get rewarded will encourage them to spread the word and create a network effect.
* App designers have to be able to register - to get the ID which is used in their interface. This could be achieved on a function of the Smart Contract.  

### Advanced enhancements / considerations
* Can a vote be taken back or switched?
* How do we get people to vote if there is no submission deadline?
* Keeping the most popular design secret until the end - perhaps a Commit-reveal approach that does not rely on the user having to return at a certain date to reveal their vote.
* Whales ability to skew the results / get an economic advantage.
* If there is clearly a winner, how do we convince people it is even worth voting / to make things impartial.

## Landing page
The ÐApp Zen Garden website's landing page should contain the following information:
* Convey the reasons for doing this and the general concept to introduce the project.
* Convey the rules and the reward for submitting a winning design and potentially for voting. 
* Provide links to designs that have been submitted.
* Provide links to the starter kit (a Github repo).
* Provide the address of the Smart Contract that is to be developed against - on the mainnet - so that the designers / developers can register.
* \[optional\] Display an indication of the amount of Ether that has been contributed and the number of votes that there have been.  

## Seasons
We run contests over different contracts / ÐApps that showcase different capabilities and usecases of Ethereum. 
Each new *skeleton* ÐApp is a new season - and a new starting point for the designers. 
A given, current, season ends with a winner and potentially runners-up and honorable mentions. 
It should be possible to view archives of past seasons and the winners (runners-up and honorable mentions). 

## Logistics
As with most applications, a significant challenge is reaching an audience and encouraging participation; engaging people to interact with and create content for the application / website.

Without people submitting designs and an audience of voters picking a winning design the project ultimately fails to make any impact. 

With the correct economic incentives it should be possible to give the application the best possible chance of succeeding.

We need to make it as easy as possible for a designer to submit an entry and to limit the amount of time that they have to spend creating an entry: most of the functionality present, just the UX needs to be completed to. 
 

# truffle-init-webpack
Example webpack project with Truffle. Includes contracts, migrations, tests, user interface and webpack build pipeline.

## Usage

To initialize a project with this example, run `truffle init webpack` inside an empty directory.

## Building and the frontend

1. First run `truffle compile`, then run `truffle migrate` to deploy the contracts onto your network of choice (default "development").
1. Then run `npm run dev` to build the app and serve it on http://localhost:8080

## Possible upgrades

* Use the webpack hotloader to sense when contracts or javascript have been recompiled and rebuild the application. Contributions welcome!

## Common Errors
