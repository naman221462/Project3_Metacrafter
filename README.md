# Voting_System

## Overview
The `Voting System` is a Solidity smart contract designed for managing elections. It demonstrates the use of `require()`, `assert()`, and `revert()` statements to handle errors and ensure the contract operates as expected.

## Features
- **require()**: Validates conditions before executing specific functions.
- **assert()**: Ensures the integrity of the contract's internal state.
- **revert()**: Reverts transactions if certain conditions are not met.

## Functions

### constructor
- Initializes the contract and sets the contract deployer as the admin.

### addCandidate
- Adds a new candidate to the system.
- Uses `require()` to ensure the candidate does not already exist and the candidate name is not empty.

### vote
- Allows a voter to cast a vote for a candidate.
- Uses `require()` to verify that the candidate exists.
- Uses `assert()` to ensure that the vote count remains non-negative.
- Uses `revert()` (illustrative) to revert the transaction if the vote count becomes negative, although this should not normally occur due to the use of `assert()`.

### getCandidate
- Retrieves details of a specific candidate based on their address.
- Uses `require()` to ensure that the candidate exists before returning their details.

## How to Use
1. Deploy the contract. The deployer is assigned as the admin.
2. Call `addCandidate()` with a candidate’s address and name to add a new candidate.
3. Call `vote()` with a candidate’s address to cast a vote for that candidate. Ensure you have not voted before using the `hasNotVoted` modifier.
4. Call `getCandidate()` with a candidate’s address to retrieve their name and vote count.

## License
This project is licensed under the MIT License.
