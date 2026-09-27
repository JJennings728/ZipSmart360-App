---
title: Getting started with the ZIPSmart portfolio demo
excerpt: Run the synthetic-data analysis pipeline, dashboard, and local API.
hidden: false
---
# Getting started

The runnable project is maintained in [JJennings728/ZipSmart360](https://github.com/JJennings728/ZipSmart360).

## Requirements

Python 3.10 or newer. No third-party Python packages or credentials are required.

```bash
git clone https://github.com/JJennings728/ZipSmart360.git
cd ZipSmart360
python zipsmart.py
python -m unittest discover -s tests -v
python server.py
```

Open http://127.0.0.1:8000 to use the dashboard. On Windows, `py` may be used instead of `python`.

## Implemented API

- `GET /api/health`: readiness and sample count.
- `GET /api/zips`: all synthetic records.
- `GET /api/zips?state=IA`: state-filtered sample records.
- `GET /api/zip?zip=00501`: one record, preserving leading zeros.

The server is local-only and requires no API key. It is not a hosted commercial service. The old proposed `/v1/score`, `/v1/compare`, `/v1/report`, and `/v1/dataset` endpoints are not part of this implementation.

All observations are synthetic. Read the working project's data dictionary and limitations before interpreting the output.
