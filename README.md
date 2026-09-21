# Weather Alert Bot (n8n)

An automated workflow built with [n8n](https://n8n.io) that checks the weather every morning and sends an email alert only when specific conditions are met - rain, thunderstorms, drizzle, or extreme heat.

## What it does

1. **Triggers daily** at 6:00 AM via a Schedule Trigger
2. **Fetches live weather data** for a specified city using the OpenWeatherMap API
3. **Evaluates conditions** using an IF node with OR logic - checks for Rain, Thunderstorm, Drizzle, or other configured weather types
4. **Sends an email alert** via Gmail only if one of the conditions is true - no notification on clear days


## Nodes used

- **Schedule Trigger** - runs the workflow daily at a set time
- **HTTP Request** - calls the OpenWeatherMap API and retrieves current weather data
- **IF** - evaluates multiple weather conditions using OR logic
- **Gmail** - sends a formatted email alert when conditions match

## Setup

1. Get a free API key from [OpenWeatherMap](https://openweathermap.org/api)
2. Import 'Weather_Alert_bot.json' into your n8n instance
3. Replace 'YOUR_OPENWEATHERMAP_API_KEY' in the HTTP Request node with your own key
4. Update the 'sendTo' field in the Gmail node with your email address
5. Connect your own Gmail account via OAuth2 credentials in n8n
6. Activate the workflow

## What I learned

This was my first n8n project, built to get hands-on with:
- Scheduled automation triggers
- Making authenticated API calls and parsing nested JSON
- Conditional branching logic (IF nodes, AND/OR combinators)
- OAuth-based integrations (Gmail)
- Debugging workflows using n8n's execution/output panels

