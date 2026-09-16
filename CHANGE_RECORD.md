Feature	Id	Description	MVP or Future	frontend file related	backend file related	table related	funcs other then web frontend & backend & database required
EventsExcel	1	Collect ongoing/upcoming events for selected China cities/regions (next 3 months) into Excel	MVP			output/china_events_2026_09_to_12.xlsx	scripts/build_china_events_xlsx.py; public web + social-mention research
EventsExcel	2	Columns: title, owner, start/end, people limits, address, links, poster, price, category, province, city, how_to_pay + source metadata	MVP			output/china_events_2026_09_to_12.xlsx	
EventsExcel	3	Include Chinese-organized and foreigner/expat events; social phase as indexed mentions not full Douyin/XHS scrape	MVP			output/china_events_2026_09_to_12.xlsx	
EventsExcel	4	Coverage sheet for Tibet/small-market gaps and refresh notes	MVP			output/china_events_2026_09_to_12.xlsx	
EventsExcel	5	Bulk Approach A harvest from 秀动/豆瓣/活动行/Meetup/Eventbrite/AllEvents/SmartShanghai; overwrite local xlsx/csv (~2700 rows); blanks allowed; no git push	MVP	china_events_2026_09_to_12.xlsx / .csv		scripts/harvest_events_bulk.py, scripts/expand_events_harvest.py	public platform list pages + mobile Douban; 小红书/抖音 only via public index crumbs (apps blocked)
EventsExcel	6	Make links/poster real Excel hyperlinks so they are clickable in Excel/WPS	MVP	china_events_2026_09_to_12.xlsx			openpyxl hyperlink conversion
