# IPTV Verification Report

验证时间：2026-10-01 11:56:30 JST
网络位置：Japan（出口国家码 JP，使用 ipinfo.io 检查）
汇总候选：132 个不同 HLS URL（此前 125 条，另测试 7 条日本新闻与电视剧候选）
汇总 HLS 链路 GET 通过：77；失败：55；后续完整片段测速中原 CCTV-5 源超时并移除
最终 M3U：61 个频道；重新读取文件后第二轮通过：61；第二轮失败：0
本次稳定性复查：对最终列表原有的 36 个体育频道各尝试下载最近两个完整片段；其中 CCTV-5+ 与 CCTV 高尔夫网球不满足实时播放要求。另测试 21 条 CCTV-5、11 条 NBA 相关、4 条 J SPORTS 低清、8 条日本体育、6 条高尔夫网球、12 条 CCTV-5+ 候选记录。当前汇总候选数包含替换入选的 2 条体育新 URL 与 7 条日本新闻及电视剧候选；其他复查候选另行记录。

验证标准：对原始 URL 执行 GET，跟随重定向；读取 master M3U8，若存在 variant 则读取最高可用 variant 的 media playlist；检查片段列表并 GET 最近片段（最多尝试最近 3 个）。若媒体使用 CMAF 初始化片段或 AES-128 密钥，也请求对应资源。没有使用 HEAD 代替 GET。HTTP 200/206 代表实际响应，`unknown` 分辨率表示媒体列表未声明分辨率。

## VERIFIED

| Channel | Group | Resolution | Result | Source |
|---|---|---|---|---|
| 日テレNEWS | 🇯🇵 日本新闻 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [Free-TV/IPTV](https://github.com/Free-TV/IPTV) · [HLS](https://cdn-apne1.tsv2.amagi.tv/linear/amg01287-rakutentvjapan-news1hlscmaf-rakutenjp/playlist.m3u8) |
| FNNプライムオンライン | 🇯🇵 日本新闻 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [Free-TV/IPTV](https://github.com/Free-TV/IPTV) · [HLS](https://cdn-uw2-prod.tsv2.amagi.tv/linear/amg01287-rakutentvjapan-news4-cmaf-rakutenjp/playlist.m3u8) |
| MBSニュース | 🇯🇵 日本新闻 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [Free-TV/IPTV](https://github.com/Free-TV/IPTV) · [HLS](https://cdn-uw2-prod.tsv2.amagi.tv/linear/amg01287-rakutentvjapan-news5-cmaf-rakutenjp/playlist.m3u8) |
| ウェザーニュースLiVE | 🇯🇵 日本新闻 | 1280x720 | VERIFIED（master/media/segment 200/200/206） | [Free-TV/IPTV](https://github.com/Free-TV/IPTV) · [HLS](https://rch01e-alive-hls.akamaized.net/38fb45b25cdb05a1/out/v1/4e907bfabc684a1dae10df8431a84d21/index.m3u8) |
| NHK WORLD-JAPAN | 🇯🇵 日本新闻 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://masterpl.hls.nhkworld.jp/hls/w/live/smarttv.m3u8) |
| TBS NEWS | 🇯🇵 日本新闻 | unknown | VERIFIED（master/media/segment 200/200/206） | [TvJapan/iptv-jp](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=cs11#.m3u8) |
| TBS NEWS DIG | 🇯🇵 日本新闻 | unknown | VERIFIED（master/media/segment 200/200/206） | [worldmonitor](https://github.com/koala73/worldmonitor/issues/4332) · [HLS](https://dp57jmgi8kb6i.cloudfront.net/out/v1/197c216d82a449f89c55f451d995daed/index_7.m3u8) |
| J SPORTS 1 | 🇯🇵 日本体育 | unknown | VERIFIED（master/media/segment 200/200/206） | [TvJapan/iptv-jp](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=bs18#.m3u8) |
| J SPORTS 2 | 🇯🇵 日本体育 | unknown | VERIFIED（master/media/segment 200/200/206；首次并发 429，串行重试通过） | [TvJapan/iptv-jp](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=bs19#.m3u8) |
| J SPORTS 3 | 🇯🇵 日本体育 | unknown | VERIFIED（master/media/segment 200/200/206；首次并发 429，串行重试通过） | [TvJapan/iptv-jp](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=bs21#.m3u8) |
| J SPORTS 4 | 🇯🇵 日本体育 | unknown | VERIFIED（master/media/segment 200/200/206） | [TvJapan/iptv-jp](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=bs22#.m3u8) |
| グリーンチャンネル | 🇯🇵 日本体育 | unknown | VERIFIED（master/media/segment 200/200/206；首次并发 429，串行重试通过） | [TvJapan/iptv-jp](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=bs14#.m3u8) |
| GAORA SPORTS | 🇯🇵 日本体育 | unknown | VERIFIED（master/media/segment 200/200/206） | [TvJapan/iptv-jp](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=cs17#.m3u8) |
| ゴルフネットワーク | 🇯🇵 日本体育 | unknown | VERIFIED（master/media/segment 200/200/206） | [TvJapan/iptv-jp](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=cs03#.m3u8) |
| CCTV-13 新闻 | 🇨🇳 中文新闻 | unknown | VERIFIED（master/media/segment 200/200/206；重定向） | [Free-TV/IPTV](https://github.com/Free-TV/IPTV) · [HLS](http://74.91.26.218:82/live/cctv13hd.m3u8) |
| FZTV-1 News 新闻综合频道 | 🇨🇳 中文新闻 | unknown | VERIFIED（master/media/segment 200/200/206） | [Free-TV/IPTV](https://github.com/Free-TV/IPTV) · [HLS](http://live.zohi.tv/video/s10001-fztv-1/index.m3u8) |
| Chifeng Comprehensive News Chanel | 🇨🇳 中文新闻 | unknown | VERIFIED（master/media/segment 200/200/200） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](http://play1-qk.nmtv.cn/live/1735546697341033.m3u8) |
| Harbin Comprehensive News Channel | 🇨🇳 中文新闻 | unknown | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://stream.hrbtv.net/xwzh/playlist.m3u8?_upt=ef41dd531755913594) |
| Lanzhou Comprehensive News Channel | 🇨🇳 中文新闻 | unknown | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://liveplus.lzr.com.cn/xwzh/HD/live.m3u8) |
| CCTV 风云足球 | 🇨🇳 中文体育 | unknown | VERIFIED（master/media/segment 200/200/206；重定向） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](http://38.75.136.137:98/gslb/dsdqpub/fyzq.m3u8?auth=testpub) |
| CCTV-5 体育 | 🇨🇳 中文体育 | unknown | VERIFIED（master/media/segment 200/200/206；重定向） | [cloudplains/jnsj](https://github.com/cloudplains/jnsj/blob/main/tv202303.txt) · [HLS](http://104.152.209.49:8181/720p/cctv5.m3u8) |
| CCTV 高尔夫网球 | 🇨🇳 中文体育 | unknown | VERIFIED（master/media/segment 200/200/206；重定向） | [CCSH/IPTV](https://github.com/CCSH/IPTV/blob/main/live_lite.txt) · [HLS](http://63.141.230.178:82/gslb/zbdq5.m3u8?id=gefwq) |
| CCTV-5+ 体育赛事 | 🇨🇳 中文体育 | unknown | VERIFIED（master/media/segment 200/200/206；重定向） | [250992941/TV](https://github.com/250992941/TV/blob/master/output/result.m3u) · [HLS](http://173.208.234.146/live/cctv5p.m3u8) |
| Al Jazeera English | 🌍 国际新闻 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [Free-TV/IPTV](https://github.com/Free-TV/IPTV) · [HLS](https://live-hls-apps-aje-fa.getaj.net/AJE/index.m3u8) |
| Bloomberg Television | 🌍 国际新闻 | 1280x720 | VERIFIED（master/media/segment 200/200/206；重定向） | [Free-TV/IPTV](https://github.com/Free-TV/IPTV) · [HLS](https://bloomberg.com/media-manifest/streams/us.m3u8) |
| Bloomberg TV+ | 🌍 国际新闻 | 1920x1080 | VERIFIED（master/media/segment 200/200/206；重定向） | [Free-TV/IPTV](https://github.com/Free-TV/IPTV) · [HLS](https://bloomberg.com/media-manifest/streams/phoenix-us.m3u8) |
| CBS News | 🌍 国际新闻 | 1920x1080 | VERIFIED（master/media/segment 200/200/206；重定向） | [Free-TV/IPTV](https://github.com/Free-TV/IPTV) · [HLS](https://dai.google.com/linear/hls/event/Sid4xiTQTkCT1SLu6rjUSQ/master.m3u8) |
| NBC News NOW | 🌍 国际新闻 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [Free-TV/IPTV](https://github.com/Free-TV/IPTV) · [HLS](https://d1si3n1st4nkgb.cloudfront.net/10502/88896001/hls/master.m3u8?ads.xumo_channelId=88896001) |
| Scripps News | 🌍 国际新闻 | 1280x720 | VERIFIED（master/media/segment 200/200/206） | [Free-TV/IPTV](https://github.com/Free-TV/IPTV) · [HLS](https://content.uplynk.com/channel/4bb4901b934c4e029fd4c1abfc766c37.m3u8) |
| BBC News | 🌍 国际新闻 | unknown | VERIFIED（master/media/segment 200/200/206） | [Free-TV/IPTV](https://github.com/Free-TV/IPTV) · [HLS](https://vs-hls-push-ww-live.akamaized.net/x=4/i=urn:bbc:pips:service:bbc_news_channel_hd/t=3840/v=pv14/b=5070016/main.m3u8) |
| GB News | 🌍 国际新闻 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [Free-TV/IPTV](https://github.com/Free-TV/IPTV) · [HLS](https://live-gbnews.simplestreamcdn.com/live5/gbnews/bitrate1.isml/manifest.m3u8) |
| DW English | 🌍 国际新闻 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://amg01644-amg01644c1-amgplt0343.playout.now3.amagi.tv/ts-eu-w1-n2/playlist/amg01644-amg01644c1-amgplt0343/playlist.m3u8) |
| France 24 English | 🌍 国际新闻 | unknown | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://live.france24.com/hls/live/2037218-b/F24_EN_HI_HLS/master_5000.m3u8) |
| Euronews English | 🌍 国际新闻 | unknown | VERIFIED（master/media/segment 200/200/200） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://dash4.antik.sk/live/test_euronews/playlist.m3u8) |
| LiveNOW from FOX | 🌍 国际新闻 | 1280x720 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://fox-foxnewsnow-vizio.amagi.tv/playlist.m3u8) |
| ACC Digital Network | ⚽ 国际体育 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://raycom-accdn-firetv.amagi.tv/playlist.m3u8) |
| beIN SPORTS XTRA | ⚽ 国际体育 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://bein-xtra-bein.amagi.tv/playlist.m3u8) |
| Bellator MMA | ⚽ 国际体育 | unknown | VERIFIED（master/media/segment 200/200/206；重定向） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://jmp2.uk/plu-5ebc8688f3697d00072f7cf8.m3u8) |
| CBS Sports HQ | ⚽ 国际体育 | unknown | VERIFIED（master/media/segment 200/200/206；重定向） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://jmp2.uk/plu-5e9f2c05172a0f0007db4786.m3u8) |
| DraftKings Network | ⚽ 国际体育 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://na.linear.zype.com/e0bd0e23-a958-4e43-8164-4f2fef8876a8/fd3614bd-90bf-4530-a277-65ae3a1720c8-zype/live.m3u8) |
| FIFA+ | ⚽ 国际体育 | 1280x720 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://d2w9q46ikgrcwx.cloudfront.net/v1/master/3722c60a815c199d9c0ef36c5b73da68a62b09d1/cc-of5cbk3sav3w5/v1/sysdata_s_p_a_fifa_7/samsungheadend_us/latest/main/hls/playlist.m3u8) |
| FITE 24/7 | ⚽ 国际体育 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://d3d85c7qkywguj.cloudfront.net/scheduler/scheduleMaster/263.m3u8) |
| FTF Sports | ⚽ 国际体育 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://1593604785.rsc.cdn77.org/FTF/FTF_SCTE.m3u8) |
| MLB | ⚽ 国际体育 | unknown | VERIFIED（master/media/segment 200/200/206；重定向） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://jmp2.uk/plu-5e66968a70f34c0007d050be.m3u8) |
| NBC Sports NOW | ⚽ 国际体育 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://d4whmvwm0rdvi.cloudfront.net/10007/99993008/hls/master.m3u8?ads.xumo_channelId=99993008) |
| NFL Channel | ⚽ 国际体育 | unknown | VERIFIED（master/media/segment 200/200/206；重定向） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://jmp2.uk/plu-5ced7d5df64be98e07ed47b6.m3u8) |
| NHL Network | ⚽ 国际体育 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://nhl-firetv.amagi.tv/playlist.m3u8) |
| Pac-12 Insider | ⚽ 国际体育 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://pac12-firetv.amagi.tv/playlist.m3u8) |
| PBR RidePass | ⚽ 国际体育 | unknown | VERIFIED（master/media/segment 200/200/206；重定向） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://jmp2.uk/plu-60d39387706fe50007fda8e8.m3u8) |
| PGA Tour | ⚽ 国际体育 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://d11k1mnrgfposz.cloudfront.net/playlist.m3u8) |
| Rally TV | ⚽ 国际体育 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://rally-tv-live.akamaized.net/hls/live/2117704/RallyTV-Pri/master.m3u8) |
| Red Bull TV | ⚽ 国际体育 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://0b73ace69ebb45eaa249bb87837cb958.mediatailor.us-west-2.amazonaws.com/v1/master/ba62fe743df0fe93366eba3a257d792884136c7f/LINEAR-644-WORBUSENFAST-LG_US/644/lgtv/hls/master/playlist.m3u8) |
| SportsGrid | ⚽ 国际体育 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://sportsgrid-tribal.amagi.tv/playlist.m3u8) |
| Stadium | ⚽ 国际体育 | 1280x720 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://wurl120sports.global.transmit.live/hls/679a907dce42a042c23ace37/v1/stadium_gracenote/samsung_us/latest/main/hls/playlist.m3u8) |
| Swerve Combat | ⚽ 国际体育 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://linear-253.frequency.stream/mt/roku/253/hls/master/playlist.m3u8) |
| Tennis Channel | ⚽ 国际体育 | 1920x1080 | VERIFIED（master/media/segment 200/200/206；重定向） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://cdn-ue1-prod.tsv2.amagi.tv/linear/amg01444-tennischannelth-tennischannelnl-samsungnl/playlist.m3u8) |
| Tennis Channel 2 | ⚽ 国际体育 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://mumbai-edge.smartplaytv.in/Tennis2/index.m3u8) |
| Unbeaten | ⚽ 国际体育 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://d1t5afz6qed3xk.cloudfront.net/Unbeaten.m3u8) |
| FIFA+ Women | ⚽ 国际体育 | 1280x720 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://cffda8ff.wurl.com/master/f36d25e7e52f1ba8d7e56eb859c636563214f541/U2Ftc3VuZy1nYl9GSUZBUGx1c3dvbWVuX0hMUw/playlist.m3u8) |
| FloRacing | ⚽ 国际体育 | 1920x1080 | VERIFIED（master/media/segment 200/200/206） | [iptv-org/iptv](https://github.com/iptv-org/iptv) · [HLS](https://amg02278-amg02278c1-flosports-worldwide-7592.playouts.now.amagi.tv/playlist.m3u8) |
| 時代劇専門チャンネル | 🎬 电视剧 | unknown | VERIFIED（master/media/segment 200/200/206） | [TvJapan/iptv-jp](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=cs04#.m3u8) |

## FAILED

| Channel | URL | Reason |
|---|---|---|
| NHK WORLD JAPAN | `https://master.nhkworld.jp/nhkworld-tv/playlist/live.m3u8` | ValueError: all sampled variants failed: HTTPError: HTTP Error 404: Not Found \| HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 404: Not Found \| HTTPError: HTTP Error 403: Forbidden |
| ANN News（印度频道，非日本 ANN） | `http://51.75.127.199:3141/annnews/index.m3u8` | HTTPError: HTTP Error 404: Not Found; tvg-id ANNNews.in@HD |
| Anshun Comprehensive News Channel | `https://hplayer1.juyun.tv/camera/154379194.m3u8` | ValueError: all sampled variants failed: TimeoutError: The read operation timed out |
| Chuzhou News Channel (1080p) | `http://live.cztv.cc:85/live/xwpd.m3u8` | URLError: <urlopen error timed out> |
| Hebi News Channel (480p) [Not 24/7] | `http://pili-live-hls.hebitv.com/hebi/hebi.m3u8` | ValueError: all sampled variants failed: TimeoutError: timed out |
| Hunan News Channel [Geo-blocked] | `http://35848.hlsplay.aodianyun.com/guangdianyun_35848/tv_channel_346.m3u8` | HTTPError: HTTP Error 403: Forbidden |
| Jiuquan TV News Comprehensive Channel (576p) | `http://117.156.28.119/270000001111/1110000001/index.m3u8` | URLError: <urlopen error timed out> |
| Pingxiang TV News Channel (576p) [Not 24/7] | `http://www.pxitv.com:8099/hls-live/livepkgr/_definst_/pxitvevent/pxtv1stream.m3u8` | URLError: <urlopen error timed out> |
| CTS News [Geo-blocked] | `http://seb.sason.top/sc/hsxw_fhd.m3u8` | URLError: <urlopen error [Errno 11001] getaddrinfo failed> |
| EBC Financial News (1080p) [Not 24/7] | `http://seb.sason.top/sc/dscjxw_fhd.m3u8` | URLError: <urlopen error [Errno 11001] getaddrinfo failed> |
| EBC News (1080p) [Not 24/7] | `http://seb.sason.top/sc/dsxw_fhd.m3u8` | URLError: <urlopen error [Errno 11001] getaddrinfo failed> |
| SET News (1080p) [Geo-blocked] | `http://seb.sason.top/sc/sllive_fhd.m3u8` | URLError: <urlopen error [Errno 11001] getaddrinfo failed> |
| TVBS News [Geo-blocked] | `http://seb.sason.top/sc/tvbsxw_fhd.m3u8` | URLError: <urlopen error [Errno 11001] getaddrinfo failed> |
| Phoenix InfoNews Channel (720p) | `http://223.110.245.167/ott.js.chinamobile.com/PLTV/3/224/3221226923/index.m3u8` | URLError: <urlopen error timed out> |
| RTHK TV 35 (1080p) [Geo-blocked] | `https://rthktv35-live.akamaized.net/hls/live/2101643/RTHKTV35/master.m3u8` | HTTPError: HTTP Error 403: Forbidden |
| Shandong TV Sports Channel (1080p) [Geo-blocked] | `http://livealone302.iqilu.com/iqilu/typd.m3u8` | HTTPError: HTTP Error 403: Forbidden |
| TDM Sport | `https://live3.tdm.com.mo/ch4/sport_ch4.live/playlist.m3u8` | URLError: <urlopen error timed out> |
| ABC News Live | `https://abcnews-streams.akamaized.net/hls/live/2023560/abcnewshudson1/master.m3u8` | ValueError: all sampled variants failed: HTTPError: HTTP Error 404: Not Found \| HTTPError: HTTP Error 404: Not Found \| HTTPError: HTTP Error 404: Not Found \| HTTPError: HTTP Error 404: Not Found |
| CBS News | `https://cbsnews.akamaized.net/hls/live/2020607/cbsnlineup_8/master.m3u8` | ValueError: all sampled variants failed: ValueError: latest segments inaccessible: HTTPError: HTTP Error 404: Not Found \| HTTPError: HTTP Error 404: Not Found \| HTTPError: HTTP Error 404: Not Found \| ValueError: latest segments inaccessible: HTTPError: HTTP Error 404: Not Found \| HTTPError: HTTP Error 404: Not Found \| HTTPError: HTTP Error 404: Not Found \| ValueError: latest segments inaccessible: HTTPError: HTTP Error 404: Not Found \| HTTPError: HTTP Error 404: Not Found \| HTTPError: HTTP Error |
| Ticker News | `https://cdn-uw2-prod.tsv2.amagi.tv/linear/amg01486-tickernews-tickernewsweb-ono/playlist.m3u8` | URLError: <urlopen error [Errno 11001] getaddrinfo failed> |
| CBC News | `https://cbcnewshd-f.akamaihd.net/i/cbcnews_1@8981/index_2500_av-p.m3u8` | HTTPError: HTTP Error 404: Not Found |
| Sky News Ⓖ | `https://linear021-gb-hls1-prd-ak.cdn.skycdp.com/Content/HLS_001_hd/Live/channel(skynews)/index_mob.m3u8` | HTTPError: HTTP Error 403: Forbidden |
| Reuters TV | `https://reuters-reutersnow-1-eu.rakuten.wurl.tv/playlist.m3u8` | URLError: <urlopen error [Errno 11001] getaddrinfo failed> |
| i24 News | `https://bcovlive-a.akamaihd.net/6e3dd61ac4c34d6f8fb9698b565b9f50/eu-central-1/5377161796001/playlist-all_dvr.m3u8` | HTTPError: HTTP Error 503: Service Unavailable |
| CBS Sports Golazo Network (720p) | `https://dai.google.com/linear/hls/event/7f3Wv6f7QEKfQna22jHqLQ/master.m3u8` | ValueError: all sampled variants failed: ValueError: latest segments inaccessible: HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| ValueError: latest segments inaccessible: HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| ValueError: latest segments inaccessible: HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error |
| F1 Channel (1080p) [Geo-blocked] | `https://amg12058-c15studio-amg12058c1-lg-us-5787.playouts.now.amagi.tv/playlist.m3u8` | HTTPError: HTTP Error 403: Forbidden |
| Fubo Sports Network (1080p) | `https://dnf08l6u6uxnz.cloudfront.net/master.m3u8` | ValueError: all sampled variants failed: ValueError: latest segments inaccessible: HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| ValueError: latest segments inaccessible: HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| ValueError: latest segments inaccessible: HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error |
| NHRA TV (1080p) | `https://d265y4sk8257lt.cloudfront.net/nh.m3u8` | ValueError: all sampled variants failed: ValueError: latest segments inaccessible: HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| ValueError: latest segments inaccessible: HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| ValueError: latest segments inaccessible: HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error |
| Overtime (1080p) | `https://d1a8aq6t30gkqj.cloudfront.net/v1/amc_overtime_1/samsungheadend_us/latest/main/hls/playlist_hd.m3u8` | ValueError: all sampled variants failed: ValueError: latest segments inaccessible: HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| ValueError: latest segments inaccessible: HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| ValueError: latest segments inaccessible: HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error |
| Olympic Channel (1080p) [Geo-blocked] | `https://ocshls-2-olympicchannel.akamaized.net/ocshls/OCTV_1.m3u8` | HTTPError: HTTP Error 403: Forbidden |
| Racing.com (720p) | `https://racingvic-i.akamaized.net/hls/live/598695/racingvic/index1500.m3u8` | HTTPError: HTTP Error 400: Bad Request |
| SuperTennis (1080p) | `https://live-embed.supertennix.hiway.media/restreamer/supertennix_client/gpu-a-c0-16/restreamer/outgest/aa3673f1-e178-44a9-a947-ef41db73211a/manifest.m3u8` | HTTPError: HTTP Error 403: Forbidden |
| The Cycling Channel | `https://cyclingtv.playout.vju.tv/cyclingtv/main.m3u8` | URLError: <urlopen error timed out> |
| Sportitalia Plus | `https://sportsitalia-samsungitaly.amagi.tv/playlist.m3u8` | HTTPError: HTTP Error 403: Forbidden |
| Abu Dhabi Sports 1 | `https://vo-live.cdb.cdn.orange.com/Content/Channel/AbuDhabiSportsChannel1/HLS/index.m3u8` | URLError: <urlopen error [SSL: TLSV1_ALERT_INTERNAL_ERROR] tlsv1 alert internal error (_ssl.c:1010)> |
| Dubai Sports 1 | `https://dmitnthfr.cdn.mgmlcdn.com/dubaisports/smil:dubaisports.stream.smil/chunklist.m3u8` | URLError: <urlopen error [Errno 11001] getaddrinfo failed> |
| NTV News24 | `https://akariko−bck1.sankuria.sbs/stream/jp/ntv_news24/stream-output.m3u8?mode=hls` | UnicodeEncodeError: 'latin-1' codec can't encode character '\u2212' in position 7: ordinal not in range(256) |
| Sport live plus | `https://akariko−bck1.sankuria.sbs/stream/jp/sport_live_plus/stream-output.m3u8?mode=hls` | UnicodeEncodeError: 'latin-1' codec can't encode character '\u2212' in position 7: ordinal not in range(256) |
| CCTV5 体育1 | `http://39.134.216.5:80/mgsp.live.miguvideo.com/wd_r2/cctv/cctv5hdnew/2500/index.m3u8?&encrypt=1` | URLError: <urlopen error timed out> |
| CCTV5 体育2 | `http://ottrrs.hl.chinamobile.com/PLTV/88888888/224/3221226019/index.m3u8` | URLError: <urlopen error timed out> |
| CCTV5 体育3 | `http://dbiptv.sn.chinamobile.com/PLTV/88888890/224/3221225837/index.m3u8` | URLError: <urlopen error timed out> |
| CCTV5+ 体育赛事1 | `http://39.134.216.5:80/mgsp.live.miguvideo.com/wd_r2/cctv/cctv5plusnew/2500/index.m3u8?&encrypt=1` | URLError: <urlopen error timed out> |
| CCTV5+ 体育赛事2 | `http://117.136.154.98/PLTV/88888888/224/3221225512/index.m3u8` | URLError: <urlopen error timed out> |
| CCTV5+ 体育赛事3 | `http://dbiptv.sn.chinamobile.com/PLTV/88888890/224/3221226221/index.m3u8` | URLError: <urlopen error timed out> |
| CCTV-5+ | `https://myip.pdtvhd.com/Sports/streams/CCTV5pul.m3u8` | HTTPError: HTTP Error 404:  |
| CCTV-5 candidate 1 | `http://1.85.0.62:808/hls/503/index.m3u8` | URLError: <urlopen error timed out> |
| CCTV-5 candidate 7 | `http://123.118.55.165:45237/tsfile/live/0005_1.m3u8?key=txiptv&playlive=1&authid=0` | URLError: <urlopen error timed out> |
| CCTV-5 candidate 8 | `http://111.4.59.41:60901/tsfile/live/1004_1.m3u8?key=txiptv&playlive=0&authid=0` | URLError: <urlopen error timed out> |
| CCTV-5 candidate 9 | `http://219.135.180.210:18888/hls/5/index.m3u8` | URLError: <urlopen error timed out> |
| CCTV-5 candidate 10 | `http://140.207.241.2:8080/live/program/live/cctv5hd/4000000/mnf.m3u8` | URLError: <urlopen error timed out> |
| ABEMA NEWS | `https://ds-linear-abematv.akamaized.net/channel/abema-news/playlist.m3u8` | ValueError: all sampled variants failed: URLError: <urlopen error unknown url type: abematv-license> \| URLError: <urlopen error unknown url type: abematv-license> \| URLError: <urlopen error unknown url type: abematv-license> \| URLError: <urlopen error unknown url type: abematv-license> |
| ABEMA NEWS 海外版 | `https://ds-glb-linear-abematv.akamaized.net/channel/news-global/playlist.m3u8?global=1` | ValueError: all sampled variants failed: HTTPError: HTTP Error 503: Service Unavailable \| HTTPError: HTTP Error 503: Service Unavailable \| HTTPError: HTTP Error 503: Service Unavailable \| HTTPError: HTTP Error 503: Service Unavailable |
| ANNニュース (redrainl) | `http://tv.redrainl.site:9500/live.m3u8?c=29` | URLError: <urlopen error timed out> |
| 日テレNEWS24 CDN | `https://n24-cdn-live.ntv.co.jp/ch01/High.m3u8` | URLError: <urlopen error [Errno 11001] getaddrinfo failed> |
| TBSチャンネル1 | `https://akariko−bck1.sankuria.sbs/stream/jp/tbs_channel_1/stream-output.m3u8?mode=hls` | UnicodeEncodeError: 'latin-1' codec can't encode character '\u2212' in position 7: ordinal not in range(256) |
| CCTV-5 原源（后续测速失败） | `http://222.169.85.8:9901/tsfile/live/0005_1.m3u8?key=txiptv&playlive=1&authid=0` | TimeoutError: timed out；已替换 |
| NBA TV（持续播放测速失败） | `http://23.237.104.106:8080/USA_NBA/index.m3u8` | HLS 链路可访问，但 10 个完整片段中 9 个下载时间超过片段时长；用户反馈卡顿，已从最终列表移除 |
| Euronews English 原源（最终复验失败） | `https://jmp2.uk/plu-61de96114757070008d33cae.m3u8` | 最终全列表复验返回 HTTP 404；改用已复测的 HD 备选源 |
| CCTV-5+ 原源（持续播放测速失败） | `http://59.39.89.130:60901/tsfile/live/0016_1.m3u8?key=txiptv&playlive=1&authid=0` | 两个 5 秒片段各下载 25 秒仍未完成；已替换 |
| CCTV 高尔夫网球原源（持续播放测速失败） | `http://38.75.136.137:98/gslb/dsdqpub/gefwq.m3u8?auth=testpub` | 两个片段分别需 13.76/10.32 秒，均慢于 11.8/9.32 秒节目时长；已替换 |

## 未收录但已测试

HLS 链路成功后有 16 条因重复、完整片段下载过慢、非持续播放或不符合新闻体育主题而移除。

| Channel | Reason |
|---|---|
| Chuxiong News Channel [Not 24/7] | not continuous |
| CCTV-Golf & Tennis (1080p) | both full segments slower than real time |
| CCTV5 | timed out in sustained-playback probe |
| CCTV-5 | duplicate CCTV-5; keep simpler URL |
| CCTV5+ | both full segments timed out after 25 seconds |
| CCTV-5 candidate 2 | high bitrate with intermittent slower-than-realtime segments |
| CCTV-5 candidate 3 | slower-than-realtime segment download |
| CCTV-5 candidate 4 | slower-than-realtime segment download |
| CCTV-5 candidate 5 | slower-than-realtime segment download |
| Rai News 24 | outside language focus |
| Euronews English (720p) | HTTP 404 in final full-playlist recheck |
| CBS News 24/7 (720p) | duplicate CBS News |
| NBA TV (720p) | full segment downloads slower than real time in 9 of 10 sustained samples |
| World Poker Tour (1080p) | outside requested sports focus |
| FIFA+ (720p) | duplicate FIFA+ |
| Red Bull TV SD (1080p) | duplicate Red Bull TV |

## 值得关注

- J SPORTS 1–4：Free-TV 的日本列表标记 `NO PUBLIC STREAM`。TvJapan 列出的第三方源在日本出口完成片段 GET，且最终复验通过。该源对并发请求返回过 429，因此最终复验对其串行执行。
- CCTV-5：用户反馈 TiviMate 播放不稳。当前源在本机持续约 3 分钟测试中 17 个完整 10 秒片段全部成功，最慢 2.34 秒，媒体序号 44416→44432。当前源保留。另一条来自 `jiandantv/IPTV2026` 的备选源虽然下载快，但媒体序号在约 10 秒内从 44400 跳到 44462，因此未替换。用户确认 TiviMate 与测试机器处于同一 Wi-Fi 且无 VPN；设备端卡顿尚未在本机复现，可能与播放器、设备或设备 Wi-Fi 表现有关，未将推测标为已证实。
- NBA TV：当前源 10 个完整片段中 9 个下载耗时超过节目时长，中位下载耗时约 11.07 秒；公开备选源或 GET 失败，或持续测速仍低于实时速度（另一个可打开的备选 11 个完整片段中 10 个慢于实时）。遵循只保留可稳定播放源的要求，暂时移除 NBA TV。
- Euronews English：原源在最终复验返回 HTTP 404。首轮通过的 `Euronews English HD` 备选源经再次 GET 验证，并连续约 70 秒读取 7 个完整片段，全部快于各自节目时长；已恢复该频道，最终第二轮验证通过。
- 体育频道全面测速：共 36 个，逐台 GET 媒体列表并尝试下载最近两个完整片段。除 CCTV-5+ 和 CCTV 高尔夫网球外，其余 34 个频道的正常时长片段均在节目时长内下载完成。NHL Network、Tennis Channel、Unbeaten 各有一个不足 1 秒的短片段，其下载耗时不能与正常时长片段直接比较。
- CCTV 高尔夫网球：原源两个片段均慢于实时；备选 `CCSH/IPTV` 在约 2.5 分钟连续测试中成功下载 13 个完整片段，最慢 3.92 秒，媒体序号 40422→40437，已替换。
- CCTV-5+：原源两个 5 秒片段在 25 秒内均下载不完整；备选 `250992941/TV` 在约 3 分钟连续测试中成功下载 15 个完整片段，最慢 9.36 秒，媒体序号 44572→44589，已替换。
- J SPORTS 1–4、グリーンチャンネル：现有源完整片段可下载，J SPORTS 1 单次 10 秒片段最慢 9.47 秒，余量较小。4 条低清备选返回 403，另 8 条候选返回 HTML、DNS 失败等，未找到更流畅且完整 HLS 验证通过的替代源，故保留现有源。
- TBS NEWS 与 TBS NEWS DIG：两条不同直播源均通过两轮 HLS 验证。新增的 DIG 源连续约 95 秒下载 12 个完整 6 秒片段，最慢 0.38 秒，媒体序号 14315360→14315375。
- 時代劇専門チャンネル：日本时代剧专题频道，第三方源连续约 95 秒下载 7 个完整 10 秒片段，最慢 8.12 秒，媒体序号 26602601→26602609；新增至电视剧分组。
- ANN/テレ朝NEWS：未找到符合本次 HLS 链路验证要求的日本新闻流。目录里的 `ANN News` 实际标识为印度频道，且请求返回 404。
- NHK総合：一个第三方地上波 URL 的片段读取成功，但该台是综合节目频道，不符合新闻体育主题，因此未收录。
- 凤凰资讯：候选 URL 超时；台湾新闻候选的域名解析失败。ABC News Live 返回 404；Sky News、F1 Channel、Olympic Channel 返回 403。
