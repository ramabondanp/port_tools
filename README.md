# Tools

This repository is a grab bag of binaries for unpacking and repacking Android OTA payloads and related filesystem images.

## Layout

- `bin/` – native executables. Add this directory to your `PATH` to call them directly.

## Binaries

| Tool | Description |
| --- | --- |
| `brotli` | Google Brotli compressor/decompressor; required when OTA payloads ship Brotli-compressed blobs. |
| `extract.erofs` | Extracts files from an EROFS image. Helpful for inspecting dynamic partitions in modern Android builds. |
| `mkfs.erofs` | Builds an EROFS filesystem from an input directory tree. |
| `ota_extractor` | Pulls partitions and payload metadata out of `payload.bin` archives. |
| `simg2img` | Converts Android sparse images (e.g., `system.img`) into raw ext images for mounting. |
| `zstd` | Zstandard compressor/decompressor used by recent OTAs and system partitions. |

## Getting Started

Add the executables to your environment path:

```bash
export PATH="$PWD/bin:$PATH"
```

Once the path is set, call a tool with `tool-name --help` (or `-h`) to inspect the available options.
