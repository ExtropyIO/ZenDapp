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
