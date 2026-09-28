# 分平台活动数据（可 git clone 下载）

没有合并表。每个平台单独一个 CSV，图片打在该平台自己的 zip 里。
不含爬虫、不含 cookie。

## 下载

```bash
git clone -b cursor/share-ingest-zip-f853 https://github.com/netncity/hackathon-app.git
cd hackathon-app/share_ingest_bundle
```

已有仓库：

```bash
git fetch origin cursor/share-ingest-zip-f853
git checkout cursor/share-ingest-zip-f853
cd share_ingest_bundle
```

## 只上某一平台的表

直接用 `per_platform/` 里对应文件，不用解压图片：

| 平台 | CSV | 条数（约） |
|------|-----|------------|
| 秀动 | `per_platform/showstart.csv` | 300 |
| 豆瓣 | `per_platform/douban.csv` | 868 |
| 活动行 | `per_platform/huodongxing.csv` | 376 |
| AllEvents | `per_platform/allevents.csv` | 92 |
| 抖音 | `per_platform/douyin.csv` | 131 |
| 小红书 | `per_platform/xiaohongshu.csv` | 57 |

## 要封面时再解该平台的包

每个 zip 解开后是 `<平台>/<平台>.csv` + `<平台>/images/`。

小文件直接解压：

```bash
unzip huodongxing.zip
unzip allevents.zip
unzip xiaohongshu.zip
```

大文件先拼再解（GitHub 单文件不能超过 100MB）：

```bash
cat showstart.zip.part* > showstart.zip && unzip showstart.zip
cat douban.zip.part* > douban.zip && unzip douban.zip
cat douyin.zip.part* > douyin.zip && unzip douyin.zip
```

Windows PowerShell 把 `cat a.zip.part* > a.zip` 换成：

```powershell
Get-Content .\showstart.zip.part* -AsByteStream | Set-Content .\showstart.zip -AsByteStream
```

## 字段

见 `COLUMN_GUIDE.txt`、`INGEST_CONTRACT.md`、`STATS.json`。

社交平台地址可能只有城市名；活动行 story 为空；部分时间是默认 10:00–18:00。上线时按平台单独 ingest，不要混成一张表。
