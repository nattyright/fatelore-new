---
title: Deadline Tracker for S5
weight: 50
---

A basic thread tracker has been implemented to support the deadline system of Season 5. To ensure smooth operation of the bot, please make sure to take the below requirements into account when configuring channels for Season 5.

## Channel Category

*Naming*

Please name the Channel Category as `Season 5` (capitalization does not matter).

## RP Channels - Thread Locking/Unlocking

*Introduction*

The thread pausing feature has been implemented to help tide players over short-term emergencies. Should most, or all players in a thread run into difficulties IRP and thus need to leave the thread on hold for a while, they can elect to pause the thread for `up to 7 days` at a time. Pausing a thread will put a stop to the deadline timer, effectively granting players extra time to finish the thread without exceeding the 3-week deadline.

*Usage* 👈👈👈

- To pause a thread, please use the `/pause` command within the thread itself. Doing so will lock the thread.

*Ruling*

- A paused thread can safely remain paused for up to 7 days, or 168 hours. After the 7 days are up, if no player has requested the thread be unpaused (unlocked), the 3-week deadline timer will start ticking again.
- After a thread has been unpaused, it cannot be paused again for 7 more days.

*Channel Permissions & Mod Duties*

- The Bot keeps tracks of paused thread via a `thread locking trigger`. **Please make sure that no one aside from mods can lock/unlock threads.** Furthermore, please inform mods to `never lock threads`, as that can interfere with how the Bot tracks paused threads.

- On the other hand, mods should by all means `assist users in unlocking` locked threads, as the act of unlocking a thread will reset the pause timer.

## Archive Requests

*Ruling*

- Whenever a player submits an archive request using the `template` provided in the same channel, the Bot will timestamp all mentioned threads and mark them as finished. It will then calculate whether those threads have exceeded the 3-week deadline while factoring in any pauses and unpauses.

- Players can mention multiple threads in the same archive request. The Bot will add 1 emoji for each thread that has exceeded the 3-week deadline.


*Channel Permissions & Mod Duties*

- Please `turn off ‘Add Reactions’` for the channel. The bot will use reactions to track the number of overdue threads in each Archive Request submission.
