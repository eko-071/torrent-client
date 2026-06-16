# torrent-client

A BitTorrent client written in Go. Built to learn the protocol.

## Usage

```bash
go build .
./torrent-client <file.torrent> <output>
```

## How it works

Parses a `.torrent` file, contacts the tracker for peers, then downloads pieces concurrently across all peers with pipelining and SHA-1 verification.

## Limitations

- HTTP trackers only (no UDP)
- Single-file torrents only
- No seeding, no resume, no magnet links

## Credit

Inspired by [Building a BitTorrent client from scratch](https://blog.jse.li/posts/torrent/) by Jesse Li.
