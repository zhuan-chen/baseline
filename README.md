# baseline

Home for the conventions that my downstream projects share. AI agents apply them
in those projects and in this repository, so behavior stays consistent.

## Setup

```text
./
├── AGENTS.md -> baseline/AGENTS.md
├── baseline/
├── downstream-project-1/
├── downstream-project-2/
├── .../
└── downstream-project-n/
```

1. Place this repository and its downstream projects as siblings under one
   parent directory (the `./` above).

2. Symlink `AGENTS.md` under `./` so one file serves this repository and every
   downstream project. The link is outside those repositories, so it is not a
   new tracked file and does not need an ignore rule.

3. Launch the AI agent from `./` so it sees the `AGENTS.md` symlink and every
   project under that directory.

## License

MIT. See [`LICENSE`](LICENSE).
