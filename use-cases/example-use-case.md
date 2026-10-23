# Example Use Case: Register New User

## ID
UC-IDENTITY-001

## Title
Register New User

## Description
A user signs up to the platform.

## Actors
- New User

## Preconditions
- User is not yet registered.

## Postconditions
- User has an init role until verified
- User gets a verification email

## Main Flow
1. User opens registration page.
2. User fills in email and password.
3. User submits the form.
4. System hashes password and stores user.

## Linked Requirements
- REQ-IDENTITY-001
- REQ-IDENTITY-002

