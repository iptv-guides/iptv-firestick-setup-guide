# Xtream Codes vs M3U: Which IPTV Login Type Should You Use? (2026)

> **Disclosure:** Written by the Ark IPTV support team. Back to the [main setup guide](README.md).
>
> *Last updated: October 2026*

## The short answer

Use **Xtream Codes** when your provider gives you one. It's a username, password and server address that loads the live channels, movies, series and TV guide together, and keeps them up to date. Use an **M3U playlist link** when your app or device only accepts a playlist, such as VLC or some Smart TV players. Both give you the same channels; the difference is how well the app can organise them.

## What each login looks like

**Xtream Codes** comes as three separate details:

```
Server URL:  http://example-server.com:8080
Username:    your-username
Password:    your-password
```

**M3U** comes as a single link (the username and password are inside it):

```
http://example-server.com:8080/get.php?username=...&password=...&type=m3u_plus&output=ts
```

If you only have the M3U link, you can usually read the server, username and password out of it: everything before `/get.php` is the server URL, and the username and password follow `username=` and `password=`.

## Side-by-side comparison

| | Xtream Codes | M3U playlist |
|---|---|---|
| What you enter | Server URL, username, password | One playlist URL |
| TV guide (EPG) | Usually loaded automatically | Often needs a separate EPG link |
| Movies and series | Organised into their own sections, with posters | Often mixed into one long list |
| Updates | App refreshes channels automatically | Reload the playlist when channels change |
| Catch-up / replay | Supported in many apps | Limited |
| Loading a large list | Faster, loads by category | Slower, downloads the whole file |
| Compatibility | Most dedicated IPTV apps | Almost every player, including VLC |

## Which one to use in each app

| App or device | Use |
|---|---|
| TiviMate | Xtream Codes (choose *Xtream Codes* when adding a playlist) |
| IPTV Smarters Pro | Xtream Codes (*Login with Xtream Codes API*) |
| VLC (computer or phone) | M3U |
| Smart TV players that ask for a MAC address | Whatever the app's website accepts, often M3U |
| MAG boxes | Portal (Stalker) URL from your provider, not M3U or Xtream |

## How to enter each one

**Xtream Codes in TiviMate:** Add playlist > Xtream Codes > type the server URL, username and password > Next > name the playlist > Done.

**M3U in TiviMate:** Add playlist > M3U playlist > type the URL > Next. If the guide is empty, add the provider's EPG link in the playlist settings (see [EPG not working](https://iptvhelpdesk.wordpress.com/2026/10/09/iptv-epg-not-working/)).

**Xtream Codes in IPTV Smarters:** Login with Xtream Codes API > any name > username > password > server URL > Add user.

## Common login errors and fixes

- **"Failed to authorize" or "login failed":** check for typos and extra spaces, retype the password, and make sure the server URL includes `http://` and the port number (for example `:8080`). Also check that the subscription is still active.
- **"Invalid playlist" with M3U:** the link was cut off when copying. Copy the whole link again, including everything after the `?`.
- **Empty channel list:** wait for the first download to finish, then refresh. Very large playlists can take a couple of minutes on older devices.
- **Channels but no TV guide:** with M3U, add the EPG link; with Xtream Codes, force an EPG update in the app's settings.
- **Works on one device, not another:** some plans limit how many devices can stream at once. Close the stream on the other device.

## Is one more secure than the other?

Both send your login to the server, so treat both like a password: don't post them online or share screenshots that show them. An M3U link contains your username and password in plain view, so be extra careful where you paste it.

## Frequently asked questions

**Is Xtream Codes better than M3U?**
For dedicated apps like TiviMate and IPTV Smarters, usually yes: the TV guide, movies and series load automatically and stay organised. M3U is better only when your app doesn't support Xtream Codes.

**Can I convert an M3U link into Xtream Codes?**
Often yes. Everything before /get.php is the server URL, and the username and password are in the link after username= and password=.

**Why does my M3U playlist have no TV guide?**
M3U often loads only the channels. Add the separate EPG link from your provider in the app's playlist settings, then update the guide.

**Do Xtream Codes and M3U give different channels?**
No. They are two ways of logging in to the same subscription. The difference is how the app organises and updates what you get.

## About Ark IPTV
Ark IPTV emails your Xtream Codes login automatically after payment, and it works with Xtream Codes and M3U players. Try it with the 24-hour free trial at [arkiptv.com](https://arkiptv.com/?utm_source=github&utm_medium=readme&utm_campaign=xtream-m3u).

See also: [buffering fix](iptv-buffering-fix.md) · [Smart TV setup](iptv-smart-tv-setup.md)
