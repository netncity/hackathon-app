# Share ingest delivery (Shanghai + Shenzhen, 7 platforms)

## Download the full zip (CSV + images)

GitHub blocks files >100MB, so the zip is split into parts:

| File | Size |
|------|------|
| `netncity_share_7platforms_sh_sz.zip.part00` … `part05` | ~40MB each (last ~11MB) |

### Reassemble locally

```bash
# Mac / Linux
cd share_ingest_bundle
cat netncity_share_7platforms_sh_sz.zip.part* > netncity_share_7platforms_sh_sz.zip
unzip netncity_share_7platforms_sh_sz.zip
```

```powershell
# Windows PowerShell
cd share_ingest_bundle
Get-Content .\netncity_share_7platforms_sh_sz.zip.part* -AsByteStream | Set-Content .\netncity_share_7platforms_sh_sz.zip -AsByteStream
Expand-Archive .\netncity_share_7platforms_sh_sz.zip
```

### Or: CSV-only (no images)

Use `merged_sh_sz.csv` and `per_platform/*.csv` in this folder directly.

## Stats (success rows, cover ≥4KB required)

See `STATS.json` / `DELIVERY_REPORT.txt`.

No crawler code is included — data delivery only.
