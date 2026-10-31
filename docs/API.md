# API

The only endpoint that exists is a status document, and today it returns an empty chain on purpose.

```
GET /api/status
```

```json
{
  "height": 0,
  "supply": 0,
  "peers": 0,
  "error": "no chain"
}
```

## Contract

- `height` is an integer and is 0 when no genesis block exists.
- `supply` is circulating coins, not the cap.
- `peers` is the number of connected peers, which is 0 without a network.
- `error` is present only when the answer is not a live reading.

Any client written against this shape will keep working when the numbers stop being zero. That is the point of publishing it now: the emptiness is a contract, not an accident.
