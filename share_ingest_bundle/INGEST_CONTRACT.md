# Cloud Crawl → NetNCity ingest contract

contract_version: 2026-09-28

This delivery follows the chat-provided contract draft:
- Required columns incl. platform, source_id, title, start/end, city, publish_tier, cover_*, source_url
- address: preferred; temporarily optional for XHS/Douyin social notes (blank allowed; marked `address_optional` in notes)
- No tags; no publish_tier=ready
- Ended events excluded
- Eventbrite omitted by product request
- XHS/Douyin via cookie session (tmp-only, not in git)

## Time defaults

- Prefer parsed source clock times (HH:MM).
- Date-only fields are usually a parser/source gap, not intentional omission.
- When no clock can be recovered: start=`10:00`, end=`18:00` (same calendar dates), noted as `time_defaulted=10:00/18:00`.
