# Galactic Basic game support

GitHub Pages publishes `main` at https://agentburgundy.github.io/.

## AdMob ownership verification

The canonical file is https://agentburgundy.github.io/app-ads.txt. Keep this exact publisher record in plain UTF-8 text:

```text
google.com, pub-4310178866905015, DIRECT, f08c47fec0942fa0
```

All games using this AdMob publisher and website hostname share this file. An app-specific GitHub Pages path does not replace the domain-root file. Keep the file in this repository even when changing an individual game's support site.

| App | App Store Marketing URL |
| --- | --- |
| Emberbound: Endless Descent | https://agentburgundy.github.io/emberbound-support/ |
| Wrong Turn Factory | https://agentburgundy.github.io/wrong-turn-factory-support/ |
| Capybara Space Force | https://agentburgundy.github.io/ |

The **Marketing URL** supplies Apple's public Developer Website link; the Support URL alone is insufficient. Google verifies against the public store listing, so unpublished apps cannot yet complete that step. Link each released App Store app to its own AdMob app, then request verification there.

On September 17, 2026 the root file returned HTTP 200, `text/plain; charset=utf-8`, and the exact record above, without a redirect or byte-order mark. Emberbound's public Apple listing reported the expected developer website. AdMob's manual verification still failed and its app-ads.txt dashboard had no crawl results; successful verification was **not** confirmed. Google documents crawl delays of up to 24 hours; the dashboard warns domain changes can take up to 7 days. Do not replace the publisher ID or change the website domain simply to retry.

If the result remains unsuccessful after propagation, use AdMob's Help flow with the public App Store URL, canonical file URL, publisher record, and reported verification error. No iOS binary change is required for this website configuration.

References: [Google setup guide](https://support.google.com/admob/answer/9363762), [troubleshooting](https://support.google.com/admob/answer/9776740).
