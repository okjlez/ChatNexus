# ChatNexus
<p align="center">
  <a href="https://app.codacy.com/gh/chomnr/ChatNexus/dashboard?utm_source=gh&utm_medium=referral&utm_content=&utm_campaign=Badge_grade"><img src="https://app.codacy.com/project/badge/Grade/2fa43e5859d34135b08ed7132c3cadf4"/></a>
  <img src="https://img.shields.io/github/commit-activity/m/chomnr/chatnexus?color=ff69b4"/>
  <img src="https://img.shields.io/github/repo-size/chomnr/chatnexus"/>
</p>

Video Preview<br>
https://www.youtube.com/watch?v=gq852Cxr980

Just another centralized chat system.
<br>
<br>
Authentication is done through Discord's OAuth2 API. The chat messages are transmitted through google's inhouse remote procedure call framework (gRPC). The status of everything is kept up to date with Redis.
<br>
<br>
Nice and simple. I think.

## Getting started
The only external dependency you need is Redis. 
<br>
1. Install [Redis](https://redis.io/download/)

### Configuring env
```
REDIS_HOST = ""
REDIS_USERNAME = ""
REDIS_PASSWORD = ""
REDIS_PORT = ""
REDIS_DATABASE = ""

OAUTH2_ENDPOINT = ""
OAUTH2_AUTHORIZE = ""
OAUTH2_TOKEN = ""
OAUTH2_SCOPES = ""
OAUTH2_CLIENT_ID = ""
OAUTH2_CLIENT_SECRET = ""
OAUTH2_REDIRECT_URI = ""


WEB_SECRET_KEY = "RANDOM VALUE HERE."
```
### Running the servers and client
```bash
git clone https://github.com/chomnr/ChatNexus.git
cd chatnexus
cargo build

# Running the chat server.
cd chatnexus-chat
cargo run

# Running the web server.
cd chatnexus-web
cargo run

# Running the client.
cd chatnexus-client
cargo run
```
