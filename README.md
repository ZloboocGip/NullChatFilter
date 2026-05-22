# NullChatFilter

Simple chat filter plugin for Bukkit/Spigot/Paper servers.

## Features

- Anti spam cooldown
- Anti repeat messages
- Anti caps
- Bad words filter
- Similar letters detection
- Latin/Cyrillic bypass protection
- Symbol bypass protection
- Configurable messages
- Bypass permission

## Installation

1. Put `NullChatFilter.jar` into `/plugins`
2. Start the server
3. Configure `plugins/NullChatFilter/config.yml`
4. Restart the server

## Permission

nullchatfilter.bypass

Players with this permission ignore all chat filter checks.

## Config

Main settings:

settings:
  chat-delay-seconds: 2
  block-repeat-messages: true
  block-words: true
  block-caps: true
  caps-min-length: 8
  caps-max-percent: 70
  lowercase-message: false
  use-similar-letters: true
  remove-symbols: true

## Blocked Words

blocked-words:
  - badword
  - spamword
  - admin

## Similar Letters

The plugin can detect bypasses using similar-looking symbols.

Examples:

admin
аdmin
@dmin
4dmin
a.d.m.i.n
a-d-m-i-n

All these variants will be detected as:

admin

Config example e.g: 

similar-letters:
  a:
    - "а"
    - "@"
    - "4"

  e:
    - "е"
    - "ё"
    - "3"


## Messages

messages:
  cooldown: "&cDo not spam. Wait before sending another message."
  repeat: "&cYou cannot send the same message twice."
  blocked-word: "&cYour message contains a blocked word."
  caps: "&cDo not use too much caps."

## License

MIT
