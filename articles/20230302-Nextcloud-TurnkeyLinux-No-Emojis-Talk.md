|   |   |
|---|---|
|Date| 2023/03/02|
|Tags| #Nextcloud, #TurnkeyLinux, #MySQL|

# Activate Emojis in Nextcloud Talk with [Turnkeylinux V16.1](https://www.turnkeylinux.org/nextcloud)

I was having hard time to get emojis working in Nextcloud Talk on the Turnkeylinux Nextcloud V16.1 image.
Emojis need propper UTF8 support to work. Almost all google hits went into the direction to check database collation to support UTF8.

Solution to get this running was to set the database connection in `/etc/myssql/` to use UTF8 because this was "misconfigured".

# [Startpage](/)
