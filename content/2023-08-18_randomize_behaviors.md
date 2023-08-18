+++
title = "Randomize Your Non-Guarantees"
date = "2023-08-18"

[taxonomies]
tags = [ "shorts" ]
+++

Save yourself a world of hurt: randomize.

Hyrum's Law guarantees that _all_ observable traits of a system will come to be relied upon. Even those traits that are not documented or guaranteed.

- What time does that critical cron job run?
- What is the default sort you use when the user doesn't specify?
- How do you form the URL for user-uploaded files?

Even when we promise nothing about these kinds of behaviors, Hyrum's Law tells us that changing these things can cause downstream breakage of our consumers.

- The cron job is 10min late, and your customer has a time-sensitive business process that relies on it happening at the same time each day
- You change the default sort from being by creation time to being by name alphabetically, breaking integrations across the spectrum of maturity
- You switch from replacing spaces in filenames with underscores to dashes, breaking your customer's assumptions about how to predict the filename.

Being aware of what guarantees you actually provide, and taking steps to prevent unintentional patterns or behavior from forming can prevent breakage.

- Add as much jitter to your cron job's runtime as you can allow. If it only matters if it runs once a day, allow it to run during any hour of the day. If it needs to happen once an hour, allow it to run at any minute of the hour
- If the user doesn't specify a sort and you don't guarantee a default sort direction, try randomizing the order of data as you return it. Users will learn to specify a sort order.
- Instead of deriving the URL from the uploaded file's name, use a randomly generated name or a UUID to foil attempts to predict URL paths.

The name of the game here is "managing expectations". Don't provide behavior that you don't plan on guaranteeing!
