# 🪂 DropRadar — Airdrop & Bounty Aggregator (MIT)

Live crypto opportunities board: quests, testnets, learn-to-earn and
audit competitions + live market prices. UI in EN/TR/AR.

## Data (all public, verified links)

- **Board (20 rows):** quest platforms (Galxe, Zealy, Layer3, TaskOn,
  QuestN), learn-to-earn (Coinbase, Binance Academy, CMC, CoinGecko),
  audit comps (Immunefi, Cantina, Sherlock, Code4rena), testnet hubs
  (Ethereum, Solana, Arbitrum, Optimism, Base, Starknet, zkSync).
  Links = official homepages/directories (HackerOne/Bugcrowd dirs verified).
  Reward tiers are broad bands — verify on platform.
- **Live markets:** CoinGecko `/coins/markets` + `/search/trending`,
  auto-refresh 5 min. No key needed.
- **Community submit:** visitors propose drops (localStorage, badged).

## Referrals (cumulative commissions)

`CONFIG.refs = { immunefi: 'https://...your-ref...' }` — any row with a
custom URL shows a REF badge. Without it, the official link is used.
**Add your real referral URLs here before promoting.**

## Money

- `CONFIG.ads`: CoinZilla (`coinzillaSrc`+`coinzillaZone`), Cointraffic,
  or AdSense fallback. Empty = placeholder. Crypto traffic = high CPM.
- Donate box: BTC + USDT-TRC20 live (see Minay for owner keys).

## Honest limits

- No backend: no true scraper cron — board is curated + importable;
  add a worker that writes JSON for fully automatic updates.
- Pro alerts (Telegram/Email) need the same backend; current alerts are
  browser-local (see VulnRadar pattern).

## Contact

📧 baranavisat@gmail.com · 📞 +90 531 326 37 22 · WhatsApp

## Run

```bash
cd dropradar
python3 -m http.server 8080
```

## License

MIT.

## Telegram (@BaranScanBot)

- Footer'da herkese açık "Telegram" butonu (`t.me/BaranScanBot`) — ziyaretçi
  doğrudan bota yazar, ek ayar gerekmez.
- Sipariş/satış bildirimleri (`tgSend`) yalnızca `CONFIG`... `TG.chat`
  doluysa sahibine gider. Chat ID'yi @userinfobot'tan alıp `TG.chat`e yazın.
- ⚠️ **GÜVENLİK:** Bot tokeni herkese açık istemci kodundadır; kaynağı
  gören herkes bot adına mesaj gönderebilir. Kötüye kullanımda BotFather'dan
  tokeni yenileyin ve asla bu botla hassas işlem yapmayın. Gerçek çözüm:
  backend proxy.
