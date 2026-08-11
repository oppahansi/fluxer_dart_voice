# fluxer_dart_voice

Voice support for the [fluxer_dart](https://github.com/oppahansi/fluxer_dart) ecosystem.

**Scaffolding only — not implemented yet.** Deferred until there's real
demand, same call [nyxx](https://pub.dev/packages/nyxx) made isolating
voice into `nyxx_lavalink` rather than building it speculatively. See the
roadmap in this ecosystem's planning docs for status.

Fluxer voice has two layers that this package will eventually need to
bridge: the gateway-level voice handshake (`VOICE_STATE_UPDATE`,
`VOICE_SERVER_UPDATE`, already-recognized-but-unhandled opcodes in
[`fluxer_dart_gateway`](https://github.com/oppahansi/fluxer_dart_gateway))
and the actual media transport, which is [LiveKit](https://livekit.io).
Neither has been verified against Fluxer's own source yet — nothing here
should be assumed to match Discord's voice protocol until it's actually
checked, the way every other verified fact in this ecosystem was.

## Part of the fluxer_dart ecosystem

| Package | Purpose |
|---|---|
| [`fluxer_dart_utils`](https://github.com/oppahansi/fluxer_dart_utils) | generic building blocks |
| [`fluxer_dart_core`](https://github.com/oppahansi/fluxer_dart_core) | domain models |
| [`fluxer_dart_rest`](https://github.com/oppahansi/fluxer_dart_rest) | REST client |
| [`fluxer_dart_gateway`](https://github.com/oppahansi/fluxer_dart_gateway) | WebSocket gateway client |
| [`fluxer_dart_voice`](https://github.com/oppahansi/fluxer_dart_voice) | *(this package)* voice support |
| [`fluxer_dart`](https://github.com/oppahansi/fluxer_dart) | main framework — the `Bot` facade |
| [`fluxer_dart_bot`](https://github.com/oppahansi/fluxer_dart_bot) | example bot |

## Installation

Not yet published to pub.dev. During development, depend on it via a path or
git dependency:

```yaml
dependencies:
  fluxer_dart_voice:
    git:
      url: https://github.com/oppahansi/fluxer_dart_voice.git
```

## License

MIT — see [LICENSE](LICENSE).
