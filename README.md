# Chat API

<a href="https://jonazwetsloot.nl/chat/timeline">Chat </a> is a social media platform where you can post messages, share images, send DMs and much more! This repository contains the documentation for the free <a href="https://jonazwetsloot.nl/chat/api/welcome">Chat API</a>.

<br>

## Table of contents

- Chat API documentation
  - Scope accounts
    - [Sending the user to the authorization URL](authorize.md#-get-apiv1authorize)
    - [Fetching the user access token](token.md#-get-apiv1token)
    - [Create new account](profile.md#-post-apiv1profile)
  - Scope public
    - [Retrieving a client access token](token.md#-get-apiv1token)
    - [Refreshing an access token](token.md#-get-apiv1token)
    - [Timeline](timeline.md#-get-apiv1timeline)
    - [Get message](message.md#-get-apiv1message)
    - [Profile](profile.md#-get-apiv1profile)
    - [Username availability](status-username.md#-get-apiv1status-username)
    - [Email address availability](status-mail.md#-get-apiv1status-mail)
    - [Email verification status](status-mail-verified.md#-get-apiv1status-mail-verified)
    - [Upload image](image.md#-post-apiv1image)
    - [View image](image.md#-get-apiv1image)
    - [Get amount of likes](like.md#-get-apiv1like)
  - Scope messages
    - [Send message/reaction](message.md#-post-apiv1message)
    - [Like message/reaction](like.md#-post-apiv1like)
  - Scope contacts
    - [Contact list](contact.md#-get-apiv1contact)
    - [Follow user](contact.md#-post-apiv1contact)
    - [Direct messages](direct-message.md#-get-apiv1direct-message)
    - [Send DM](direct-message.md#-post-apiv1direct-message)
  - Scope profile
    - [Adjust profile](profile.md#-put-apiv1profile)
  - Scope delete
    - [Delete message/reaction](message.md#-delete-apiv1message)
    - [Delete DM](direct-message.md#-delete-apiv1direct-message)
    - [Unfollow user](contact.md#-delete-apiv1contact)
    - [Delete account](profile.md#-delete-apiv1profile)

<br>

## How to start?

First, determine your needs. If you want to perform actions on behalf of others, you'll need to use a user access code. On the other hand, if you only need to retrieve the timeline or someones profile, you should use a client access code. This is simpler as it only requires one step.

<details><summary>Get user access token</summary>
  
  1. [Sending the user to the authorization URL](authorize.md#-get-apiv1authorize)
  2. [Fetching the user access token](token.md#-get-apiv1token)
  
</details>

<details><summary>Get client access token</summary>
  
  1. [Fetching the client access token](token.md#-get-apiv1token)

</details>

After you have an access token (which is valid for one hour), you can make API requests. After the access token expires, you can [refresh it with the refresh token](token.md#-get-apiv1token).

<br>

## Contributing

You can always edit the documentation for yourself. If you improved something, you can submit a pull request. Please be clear about what your pull request changes/adds.