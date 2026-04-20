# FB-Testing

A **Cocos Creator 3.6.2** test project for exploring the **Facebook Instant Games (FBInstant) SDK**. Not a game - a hands-on sandbox for testing every major FBInstant API before integrating into a real project.

> Personal reference project. Nothing here is production-ready.

---

## What's Being Tested

| Feature | API |
|---------|-----|
| Game initialisation | `FBInstant.startGameAsync()` / `setLoadingProgress()` |
| Player profile photo | `FBInstant.player.getPhoto()` + remote image loading |
| Player persistent data | `player.setDataAsync()` / `player.getDataAsync()` |
| Connected players | `player.getConnectedPlayersAsync()` |
| Tournaments | `tournament.createAsync()` / `tournament.joinAsync()` |
| Leaderboards | `getLeaderboardAsync()` - set, retrieve, post scores |
| Context switching | `context.switchAsync()` / `context.createAsync()` |

---

## Tech

- **Engine:** Cocos Creator 3.6.2
- **Language:** TypeScript
- **SDK:** Facebook Instant Games (`FBInstant`)
- **Scene:** Single scene (`Start.scene`) with UI buttons wired to each API call

---

## Opening the Project

1. Install [Cocos Creator 3.6.2](https://www.cocos.com/en/creator)
2. Open Cocos Creator → **Open Project** → select this folder
3. Open `assets/Start.scene`
4. Build for **Facebook Instant Games** via **Project → Build**

> You'll need a Facebook App ID and a configured Instant Games app to run this against a real FBInstant environment.

---

## Notes

- All API calls log to the browser console - open DevTools to inspect responses
- The `switchID` EditBox in the scene accepts a context/tournament/leaderboard ID for testing switch and join flows
- Commented-out code includes Graph API exploration (`/me?fields=id,name,email`)

---

## License

MIT
