# fluxer_dart_voice

[![Discord](https://img.shields.io/static/v1?logo=discord&label=discord&message=Join&color=blue)](https://discord.gg/ncKmDEArqg)

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

## Fluxer version

Not yet applicable — as noted above, nothing in this package has been
implemented or verified against Fluxer's voice protocol (gateway voice
opcodes or the LiveKit media transport) yet. The rest of the ecosystem
is verified against REST API version `1.0.0` and gateway protocol
version `1`, checked against a self-hosted instance running image tag
`v1` as of 2026-08-12 — see
[`fluxer_dart_core`](https://github.com/oppahansi/fluxer_dart_core)'s
README for how. Whoever implements this package should pin down and
record the same detail for voice specifically, not assume it inherits
the rest of the ecosystem's verification.

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

Not yet published to pub.dev — depend on it via a git dependency, pinned
to a tagged release:

```yaml
dependencies:
  fluxer_dart_voice:
    git:
      url: https://github.com/oppahansi/fluxer_dart_voice.git
      ref: v0.1.0
```

See [CHANGELOG.md](CHANGELOG.md) for what's in each tagged release.

## License

MIT — see [LICENSE](LICENSE).
