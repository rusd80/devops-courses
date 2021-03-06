## Task 4 - bot displays info about repository's content 

### This bot uses `WebHook` 

### Bot provides this commands:
1. `/start` - greeting and basic info about bot
2. `/help`  - describing of commands
3. `/git`   - returns URL of repository
4. `/tasks` - get full list of your done homeworks directories 
5. `/task#` - get URL to directory of homework number #
6. `/topics` - show list of topics of the repository
7. `/stats` - show number of commits made this week and the previous week

### If you don't have "white" IP, use http tunnel [ngrok](https://ngrok.com/)
```
Session Status                online                                                             
Version                       2.3.40                                                             
Region                        United States (us)                                                 
Web Interface                 http://127.0.0.1:4040                                              
Forwarding                    http://1cd2-176-53-210-50.ngrok.io -> http://localhost:8090        
Forwarding                    https://1cd2-176-53-210-50.ngrok.io -> http://localhost:8090       
```
### or deploy it to cloud or use a PAAS like [heroku](https://heroku.com/)

## To run bot:
1. Clone repo with `git clone` command 
2. Create your own bot using `BotFather` and save `SECRET TOKEN`
3. Create in project directory file `.env` with following data:

`TOKEN="2144052527:AAELCMqXtbt9jKclUW...` - your bot ``SECRET TOKEN``

`PORT="8090"` - port that will be used by your app

`REPO="/rusd80/andersen-devops"` - your repository on GitHub.com

4. Also, you supposed to set `WEBHOOK` to allow telegram send POST requests to your app:
```
curl --location --request POST 'https://api.telegram.org/bot21440#####:AAELCMqXtbt9jKclUWVZj####SECRET####/setWebhook?url=https://1cd2-176-53-210-50.ngrok.io'
```
