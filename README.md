# Hackathon App

Starter repository for Hackathon App. This branch also includes a **China events research Excel** deliverable.

## China events Excel (MVP)

**File:** [`output/china_events_2026_09_to_12.xlsx`](output/china_events_2026_09_to_12.xlsx)

**Window:** 2026-09-15 → 2026-12-15  
**Regions:** Beijing, Shanghai, Shenzhen, Chengdu, Chongqing, Changsha, Xinjiang, Xizang, Guizhou, Hong Kong, Macau, Taiwan

### Sheets

| Sheet | Purpose |
| --- | --- |
| `events` | Main table (requested columns + source metadata) |
| `coverage` | Per-region completeness notes |
| `sources` | Source types used |
| `meta` | Collection date, method, disclaimer |

### Columns

`title`, `owner`, `start_time`, `end_time`, `people_limits`, `address`, `links`, `poster`, `price`, `category`, `province`, `city`, `how_to_pay`, plus `source_type`, `audience`, `confidence`, `notes`.

### Method

1. Public ticketing / venue / government / media listings  
2. Expat chamber & community calendars  
3. Indexed social mentions (e.g. Xiaohongshu public accounts / press reprints) — **not** a full Douyin/XHS scrape  

Rebuild:

```bash
pip install openpyxl
python3 scripts/build_china_events_xlsx.py
```

### Limits

- Not exhaustive; prices/dates change — verify before buying.  
- Poster URLs are often not exposed in crawlable HTML (column may be blank).  
- Tibet / small pop-up markets are sparse in public sources.  
- Change log: [`CHANGE_RECORD.md`](CHANGE_RECORD.md)

## License

TBD.
