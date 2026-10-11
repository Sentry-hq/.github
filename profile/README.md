# Sentry

All my life I separated my life into modules. Finance, Work, Uni, Health etc. It's nothing ground breaking or special, it's just the way I viewed my life. But it was never simply the sum of all these modules. There was always a connection between them missing and I spent years searching for something to connect them. I did the whole "second brain" thing in Notion and it worked for a bit but then I found more overhead to make sure everything was configured perfectly. It was too brittle to handle the ever-changing nature of these modules. 

Despite leaving it, I still couldn't help but constantly come up with new ideas for the things I would be able to do if I just had all my data in one place. How I could deeply integrate my life in software with my actual life and how I can control all of it. It only got more exciting when I would consider the possibilities of how I can integrate this control with things like my HA (HomeAssistant), or home server and how I can control everything from my phone and mac. So Sentry is the culmination of all this daydreaming and its work will never really end. There's always more to add. 

### So what does Sentry do? 

Sentry gives me insights but also gives me control over the things I've connected it to.

- `ScreenTime` - Shows me how badly I need to touch grass. It aggregates all the screen time usage across all my devices (cheats a bit by getting this data from my mac's internal DB rather than just through the Apple API so I can actually store this information in my own server rather than get sandboxed by iOS and blocked from saving my own data)
- `Finance` - Finally one place to see my financial life. With so many accounts across so many banks, it's so easy to get lost in subscriptions and random payments and just not now where I stand financially. Now it's all in one and I can track it all and not have to worry about random payments (In Australia, there's no consumer developer API for your own data so you need to use a third-party service accredited with ACCC)
- `Work` - A way to track my work hours (pretty self explanatory)
- `Calendar`
- `Home Assistant` - The HA API was a lifesaver because it allowed me to get all my smart devices (including my car) to be part of this making Sentry truly the only place I need to go to control anything
- `Password Manager` - Something I can genuinely trust because I own it all. It definitely beats a random excel password book and I can actually have one place across my devices to go to for saved passwords
- `Email` - One place for all my emails
- `Health` - I don't aim on reinventing the wheel here. Apple's Health already does quite well so I just build on that

There's still so many more ideas that I have for sentry and I don't think I'll ever be able to call this project truly finished

The thing is. All of these things on their own are fine, but as I said, my life isn't the sum of all of them. It's the things in between. So I try to bridge that gap. For instance, `Email` can inform `Finance` to confirm a subscription reminder. `Work` informs the `Calendar` for days worked and days projected. `Work` also informs `Finance` for projected income. My goal with sentry is to aggregate everything and deeply connect what is relevant.

### So what is Sentry made of?

| Repo | What it is |
|---|---|
| [sentry-api](https://github.com/Sentry-hq/sentry-api) | The backend. Bun, Hono and Postgres. Every number the apps show is computed here. |
| [sentry-app](https://github.com/Sentry-hq/sentry-app) | The Mac app. A native shell around the web dashboard, React and Vite inside WKWebView. |
| [sentry-ios](https://github.com/Sentry-hq/sentry-ios) | The iPhone app. SwiftUI, same backend. |
| [sentry-capture](https://github.com/Sentry-hq/sentry-capture) | My own Mac app that replaces and extends upon the basic screenshot functionality. |
| [sentry-finder](https://github.com/Sentry-hq/sentry-finder) | A file browser for the Mac. |
| [sentry-launcher](https://github.com/Sentry-hq/sentry-launcher) | A wonderful app which fully replaces mac's horrible spotlight search and provides a myriad of fancy features |
