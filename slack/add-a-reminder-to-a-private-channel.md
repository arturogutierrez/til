# Add a reminder to a private channel in Slack

It's too easy to add a reminder to a public channel simply following the hint of
the `/remind` command but there is no info (or I didn't find it) about how to
add it to a private channel. It can be done with the following command from
your private channel:

```
/remind @channel "Weekly time!!" at 11 am every Monday
```

Please, note that `@channel` is not your private channel name. You can use
either `@channel` for all channel members or `@here` to remind only online
members.
