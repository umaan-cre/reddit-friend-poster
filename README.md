# Reddit Private Posting Tool

A small private and non commercial tool for manually submitting Reddit posts and comments through an authorized Reddit account.

## Purpose

This project is intended for personal use by one Reddit account and one trusted user.

The goal is to provide a simple interface through n8n that allows the authorized account owner to give a trusted user limited access to create and manually submit Reddit posts and comments without sharing the Reddit account password.

## How It Works

```text
Trusted user
     ↓
Private interface / n8n
     ↓
Reddit OAuth
     ↓
Authorized Reddit account
     ↓
Reddit API
```

The Reddit account owner explicitly authorizes the application through Reddit OAuth.

The trusted user does not receive the Reddit account password, OAuth client secret, refresh token, or other authentication credentials.

## Intended Functionality

The application will provide:

- Manual Reddit post submission
- Manual Reddit comment submission
- OAuth authorization
- Low volume API usage
- Access only through a private interface
- Actions initiated explicitly by the user

Every post or comment will require an explicit user action before it is submitted.

## What This Tool Does Not Do

This project will not:

- Scrape Reddit
- Manipulate votes
- Automate voting
- Send spam
- Perform bulk posting
- Automatically generate and publish content
- Automatically comment on posts
- Circumvent Reddit restrictions
- Collect or redistribute Reddit user data
- Share Reddit OAuth credentials with other users

## Intended Usage

This is a private, non commercial project intended for one Reddit account and one trusted user.

Expected API usage is very low volume and limited to manually submitted posts and comments.

The application will only perform actions that the authorized Reddit account is permitted to perform normally.

## Authentication

The application is intended to use Reddit OAuth for authentication.

Credentials such as:

- Client Secret
- Refresh Token
- Access Token

will never be committed to this repository.

Secrets will be stored securely in the deployment environment or n8n credentials system.

## n8n

The planned implementation uses n8n to handle the workflow and Reddit API requests.

The n8n workflow will:

1. Receive a manually submitted post or comment.
2. Validate the requested action.
3. Authenticate using Reddit OAuth.
4. Submit the requested action through the Reddit API.
5. Return the result to the private interface.

No automated background posting is intended.

## Privacy

This project is private and does not intend to sell, redistribute, or publicly expose Reddit data.

Only the minimum information required to submit the requested post or comment will be processed.

## Project Status

This project is currently in development.

Reddit API access is being requested before production use.

## License

This project is intended for personal use.
