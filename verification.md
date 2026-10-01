# IPTV Verification Report

验证时间：2026-10-01 12:56:35 JST
网络位置：Japan（本机日本网络出口）
候选记录：197 条 HLS 测试记录；另有 13 条爱奇艺／咪咕候选失败记录。
首轮 HLS 链路通过：119；失败：78。
最终频道：87；四个分组：🇯🇵 日语频道 25、🇨🇳 中文频道 14、🌍 国际频道 22、🏟️ 国际体育 26。

## 验证方法和本次变更

- VERIFIED 表示曾对原始 URL 执行 GET、跟随重定向、读取 HLS master 和 media playlist，并 GET 视频片段，获得 HTTP 200/206；未以 HEAD 或目录存在代替播放验证。
- 根据用户要求，已通过的 77 条旧频道未重复联网测试；只核对最终 M3U 的频道名与原始 URL 和先前最终复验记录一一对应。
- 新增 9 条在首轮 HLS 验证后，各下载最近两个完整片段且速度快于实时；生成最终文件并重新读取后，又逐条 GET master、media 和片段，9/9 通过。
- NBA TV 依用户要求恢复：此前 HLS master、media 和片段 GET 通过，但持续播放测速有 9/10 个完整片段下载慢于节目时长。用户在 TiviMate 上也观察到卡顿。该条仅表示链路曾可读取，不能视为稳定。
- 本次仅改变分类及上述新增／恢复频道。国际新闻和英语影视放在「国际频道」，跨国体育放在「国际体育」；日语／中文体育留在相应语言类。

## VERIFIED

| Channel | Group | Resolution | Result | Source |
|---|---|---|---|---|
| 日テレNEWS | 🇯🇵 日语频道 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | [free_all](https://github.com/Free-TV/IPTV) · [HLS](https://cdn-apne1.tsv2.amagi.tv/linear/amg01287-rakutentvjapan-news1hlscmaf-rakutenjp/playlist.m3u8) |
| FNNプライムオンライン | 🇯🇵 日语频道 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | [free_all](https://github.com/Free-TV/IPTV) · [HLS](https://cdn-uw2-prod.tsv2.amagi.tv/linear/amg01287-rakutentvjapan-news4-cmaf-rakutenjp/playlist.m3u8) |
| MBSニュース | 🇯🇵 日语频道 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | [free_all](https://github.com/Free-TV/IPTV) · [HLS](https://cdn-uw2-prod.tsv2.amagi.tv/linear/amg01287-rakutentvjapan-news5-cmaf-rakutenjp/playlist.m3u8) |
| ウェザーニュースLiVE | 🇯🇵 日语频道 | 1280x720 | VERIFIED（200/200/206；先前最终复验） | [free_all](https://github.com/Free-TV/IPTV) · [HLS](https://rch01e-alive-hls.akamaized.net/38fb45b25cdb05a1/out/v1/4e907bfabc684a1dae10df8431a84d21/index.m3u8) |
| TBS NEWS | 🇯🇵 日语频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [tvjapan](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=cs11#.m3u8) |
| TBS NEWS DIG | 🇯🇵 日语频道 | unknown | VERIFIED（200/200/206；先前最终复验） | koala73/worldmonitor · [HLS](https://dp57jmgi8kb6i.cloudfront.net/out/v1/197c216d82a449f89c55f451d995daed/index_7.m3u8) |
| 共同通信ニュース | 🇯🇵 日语频道 | 1920x1080 | VERIFIED（200/200/206；本次新增复验；完整片段 2/2，最慢实时倍速 6.93×） | [katana0357/Rチャンネル](https://gitea.moe/katana0357/RAW/src/branch/main/R%E3%83%81%E3%83%A3%E3%83%B3%E3%83%8D%E3%83%AB) · [HLS](https://cdn-apne1.tsv2.amagi.tv/linear/amg01287-rakutentvjapan-news3hlscmaf-rakutenjp/playlist.m3u8) |
| 日テレNEWSセレクト | 🇯🇵 日语频道 | 1920x1080 | VERIFIED（200/200/206；本次新增复验；完整片段 2/2，最慢实时倍速 6.42×） | [katana0357/Rチャンネル](https://gitea.moe/katana0357/RAW/src/branch/main/R%E3%83%81%E3%83%A3%E3%83%B3%E3%83%8D%E3%83%AB) · [HLS](https://cdn-uw2-prod.tsv2.amagi.tv/linear/amg01287-rakutentvjapan-ntv-newsselect-cmaf-rakutenjp/playlist.m3u8) |
| オリコンニュース | 🇯🇵 日语频道 | 1920x1080 | VERIFIED（200/200/206；本次新增复验；完整片段 2/2，最慢实时倍速 8.63×） | [katana0357/Rチャンネル](https://gitea.moe/katana0357/RAW/src/branch/main/R%E3%83%81%E3%83%A3%E3%83%B3%E3%83%8D%E3%83%AB) · [HLS](https://cdn-apne1.tsv2.amagi.tv/linear/amg01287-rakutentvjapan-news2cmafhls-rakutenjp/playlist.m3u8) |
| J SPORTS 1 | 🇯🇵 日语频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [tvjapan](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=bs18#.m3u8) |
| J SPORTS 2 | 🇯🇵 日语频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [tvjapan](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=bs19#.m3u8) |
| J SPORTS 3 | 🇯🇵 日语频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [tvjapan](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=bs21#.m3u8) |
| J SPORTS 4 | 🇯🇵 日语频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [tvjapan](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=bs22#.m3u8) |
| グリーンチャンネル | 🇯🇵 日语频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [tvjapan](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=bs14#.m3u8) |
| GAORA SPORTS | 🇯🇵 日语频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [tvjapan](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=cs17#.m3u8) |
| ゴルフネットワーク | 🇯🇵 日语频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [tvjapan](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=cs03#.m3u8) |
| 時代劇専門チャンネル | 🇯🇵 日语频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [tvjapan](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=cs04#.m3u8) |
| 日本映画専門チャンネル | 🇯🇵 日语频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [tvjapan](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=bs23#.m3u8) |
| ホームドラマチャンネル | 🇯🇵 日语频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [tvjapan](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=cs05#.m3u8) |
| ファミリー劇場 | 🇯🇵 日语频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [tvjapan](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=cs20#.m3u8) |
| ムービープラス | 🇯🇵 日语频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [tvjapan](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=cs14#.m3u8) |
| 衛星劇場 | 🇯🇵 日语频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [tvjapan](https://github.com/TvJapan/iptv-jp) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=cs22#.m3u8) |
| NHK Eテレ（東京） | 🇯🇵 日语频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [free_jp](https://github.com/Free-TV/IPTV/blob/master/playlists/playlist_japan.m3u8) · [HLS](https://naori-test.netgenx.site/pxx.php?shk_cid=hdgd02#.m3u8) |
| TOKYO MX チャンネル | 🇯🇵 日语频道 | 1920x1080 | VERIFIED（200/200/206；本次新增复验；完整片段 2/2，最慢实时倍速 11.3×） | [free_jp](https://github.com/Free-TV/IPTV/blob/master/playlists/playlist_japan.m3u8) · [HLS](https://cdn-uw2-prod.tsv2.amagi.tv/linear/amg01287-rakutentvjapan-tokyomx-cmaf-rakutenjp/playlist.m3u8) |
| 九州・沖縄 街ネタ | 🇯🇵 日语频道 | 1920x1080 | VERIFIED（200/200/206；本次新增复验；完整片段 2/2，最慢实时倍速 7.68×） | [katana0357/Rチャンネル](https://gitea.moe/katana0357/RAW/src/branch/main/R%E3%83%81%E3%83%A3%E3%83%B3%E3%83%8D%E3%83%AB) · [HLS](https://cdn-uw2-prod.tsv2.amagi.tv/linear/amg01287-rakutentvjapan-local-contents-cmaf-rakutenjp/playlist.m3u8) |
| CCTV-13 新闻 | 🇨🇳 中文频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [free_all](https://github.com/Free-TV/IPTV) · [HLS](http://74.91.26.218:82/live/cctv13hd.m3u8) |
| FZTV-1 News 新闻综合频道 | 🇨🇳 中文频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [free_all](https://github.com/Free-TV/IPTV) · [HLS](http://live.zohi.tv/video/s10001-fztv-1/index.m3u8) |
| Chifeng Comprehensive News Chanel | 🇨🇳 中文频道 | unknown | VERIFIED（200/200/200；先前最终复验） | iptv_cn · [HLS](http://play1-qk.nmtv.cn/live/1735546697341033.m3u8) |
| Harbin Comprehensive News Channel | 🇨🇳 中文频道 | unknown | VERIFIED（200/200/206；先前最终复验） | iptv_cn · [HLS](https://stream.hrbtv.net/xwzh/playlist.m3u8?_upt=ef41dd531755913594) |
| Lanzhou Comprehensive News Channel | 🇨🇳 中文频道 | unknown | VERIFIED（200/200/206；先前最终复验） | iptv_cn · [HLS](https://liveplus.lzr.com.cn/xwzh/HD/live.m3u8) |
| CCTV-5 体育 | 🇨🇳 中文频道 | unknown | VERIFIED（200/200/206；先前最终复验） | cloudplains/jnsj · [HLS](http://104.152.209.49:8181/720p/cctv5.m3u8) |
| CCTV 高尔夫网球 | 🇨🇳 中文频道 | unknown | VERIFIED（200/200/206；先前最终复验） | CCSH/IPTV · [HLS](http://63.141.230.178:82/gslb/zbdq5.m3u8?id=gefwq) |
| CCTV-5+ 体育赛事 | 🇨🇳 中文频道 | unknown | VERIFIED（200/200/206；先前最终复验） | 250992941/TV · [HLS](http://173.208.234.146/live/cctv5p.m3u8) |
| CCTV-6 电影 | 🇨🇳 中文频道 | unknown | VERIFIED（200/200/206；先前最终复验） | iptv_cn · [HLS](http://69.30.245.50/live/cctv6.m3u8) |
| CCTV-8 电视剧 | 🇨🇳 中文频道 | unknown | VERIFIED（200/200/206；先前最终复验） | iptv_cn · [HLS](http://74.91.26.218:82/live/cctv8hd.m3u8) |
| Harbin Movie Channel | 🇨🇳 中文频道 | unknown | VERIFIED（200/200/206；先前最终复验） | iptv_cn · [HLS](https://stream.hrbtv.net/yspd/playlist.m3u8) |
| 亚洲剧场（香港） | 🇨🇳 中文频道 | 1920x1080 | VERIFIED（200/200/200；先前最终复验） | iptv_hk · [HLS](http://103.172.187.30:12000/stream/mytv/null-11/master.m3u8) |
| 美亚电影台 | 🇨🇳 中文频道 | 1920x1080 | VERIFIED（200/200/200；先前最终复验） | iptv_hk · [HLS](http://103.172.187.30:12000/stream/mytv/null-9/master.m3u8) |
| CCTV-3 综艺 | 🇨🇳 中文频道 | unknown | VERIFIED（200/200/206；本次新增复验；完整片段 2/2，最慢实时倍速 4.21×） | [free_all](https://github.com/Free-TV/IPTV) · [HLS](http://74.91.26.218:82/live/cctv3hd.m3u8) |
| NHK WORLD-JAPAN | 🌍 国际频道 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_news · [HLS](https://masterpl.hls.nhkworld.jp/hls/w/live/smarttv.m3u8) |
| Bloomberg Television | 🌍 国际频道 | 1280x720 | VERIFIED（200/200/206；先前最终复验） | [free_all](https://github.com/Free-TV/IPTV) · [HLS](https://bloomberg.com/media-manifest/streams/us.m3u8) |
| Bloomberg TV+ | 🌍 国际频道 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | [free_all](https://github.com/Free-TV/IPTV) · [HLS](https://bloomberg.com/media-manifest/streams/phoenix-us.m3u8) |
| CBS News | 🌍 国际频道 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | [free_all](https://github.com/Free-TV/IPTV) · [HLS](https://dai.google.com/linear/hls/event/Sid4xiTQTkCT1SLu6rjUSQ/master.m3u8) |
| NBC News NOW | 🌍 国际频道 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | [free_all](https://github.com/Free-TV/IPTV) · [HLS](https://d1si3n1st4nkgb.cloudfront.net/10502/88896001/hls/master.m3u8?ads.xumo_channelId=88896001) |
| Scripps News | 🌍 国际频道 | 1280x720 | VERIFIED（200/200/206；先前最终复验） | [free_all](https://github.com/Free-TV/IPTV) · [HLS](https://content.uplynk.com/channel/4bb4901b934c4e029fd4c1abfc766c37.m3u8) |
| BBC News | 🌍 国际频道 | unknown | VERIFIED（200/200/206；先前最终复验） | [free_all](https://github.com/Free-TV/IPTV) · [HLS](https://vs-hls-push-ww-live.akamaized.net/x=4/i=urn:bbc:pips:service:bbc_news_channel_hd/t=3840/v=pv14/b=5070016/main.m3u8) |
| GB News | 🌍 国际频道 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | [free_all](https://github.com/Free-TV/IPTV) · [HLS](https://live-gbnews.simplestreamcdn.com/live5/gbnews/bitrate1.isml/manifest.m3u8) |
| DW English | 🌍 国际频道 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_news · [HLS](https://amg01644-amg01644c1-amgplt0343.playout.now3.amagi.tv/ts-eu-w1-n2/playlist/amg01644-amg01644c1-amgplt0343/playlist.m3u8) |
| France 24 English | 🌍 国际频道 | unknown | VERIFIED（200/200/206；先前最终复验） | iptv_news · [HLS](https://live.france24.com/hls/live/2037218-b/F24_EN_HI_HLS/master_5000.m3u8) |
| Euronews English | 🌍 国际频道 | unknown | VERIFIED（200/200/200；先前最终复验） | iptv_news · [HLS](https://dash4.antik.sk/live/test_euronews/playlist.m3u8) |
| LiveNOW from FOX | 🌍 国际频道 | 1280x720 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://fox-foxnewsnow-vizio.amagi.tv/playlist.m3u8) |
| Gravitas Movies | 🌍 国际频道 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://d6dg3ebeih71x.cloudfront.net/Gravitas_Movies.m3u8) |
| Hallmark Movies & More | 🌍 国际频道 | 1280x720 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://dbrb49pjoymg4.cloudfront.net/v1/master/3fec3e5cac39a52b2132f9c66c83dae043dc17d4/prod_default_xumo-ams-aws/master.m3u8?ads.xumo_channelId=99991709) |
| Maverick Black Cinema | 🌍 国际频道 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://maverick-maverick-black-cinema-3-us.roku.wurl.tv/playlist.m3u8) |
| MovieSphere | 🌍 国际频道 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://amg00353-lionsgatestudio-moviesphere-xumo-zh5u0.amagi.tv/playlist.m3u8) |
| The Film Detective | 🌍 国际频道 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://cinedigm-entertainment-corp-thefilmdetective-1-us.ono.wurl.tv/playlist.m3u8) |
| Doctor Who Classic | 🌍 国际频道 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://bbc-classicdrwho-1-us.roku.wurl.tv/playlist.m3u8) |
| Midsomer Murders | 🌍 国际频道 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://all3media-midsomer-1-us.roku.wurl.tv/playlist.m3u8) |
| Dry Bar Comedy+ | 🌍 国际频道 | 1280x720 | VERIFIED（200/200/206；本次新增复验；完整片段 2/2，最慢实时倍速 3.34×） | iptv_us · [HLS](https://drybar-drybarcomedy-1-au.samsung.wurl.tv/playlist.m3u8) |
| SNL Vault | 🌍 国际频道 | 1920x1080 | VERIFIED（200/200/206；本次新增复验；完整片段 2/2，最慢实时倍速 3.86×） | iptv_us · [HLS](https://d4whmvwm0rdvi.cloudfront.net/10007/99993017/hls/master.m3u8?ads.xumo_channelId=99993017) |
| The Chat Show Channel | 🌍 国际频道 | 1920x1080 | VERIFIED（200/200/206；本次新增复验；完整片段 2/2，最慢实时倍速 2.5×） | iptv_us · [HLS](https://amg00426-littledotstudio-thechatshow-samsungnz-uqmtt.amagi.tv/playlist/amg00426-littledotstudio-thechatshow-samsungnz/playlist.m3u8) |
| ACC Digital Network | 🏟️ 国际体育 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://raycom-accdn-firetv.amagi.tv/playlist.m3u8) |
| beIN SPORTS XTRA | 🏟️ 国际体育 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://bein-xtra-bein.amagi.tv/playlist.m3u8) |
| Bellator MMA | 🏟️ 国际体育 | unknown | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://jmp2.uk/plu-5ebc8688f3697d00072f7cf8.m3u8) |
| CBS Sports HQ | 🏟️ 国际体育 | unknown | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://jmp2.uk/plu-5e9f2c05172a0f0007db4786.m3u8) |
| FIFA+ | 🏟️ 国际体育 | 1280x720 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://d2w9q46ikgrcwx.cloudfront.net/v1/master/3722c60a815c199d9c0ef36c5b73da68a62b09d1/cc-of5cbk3sav3w5/v1/sysdata_s_p_a_fifa_7/samsungheadend_us/latest/main/hls/playlist.m3u8) |
| FITE 24/7 | 🏟️ 国际体育 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://d3d85c7qkywguj.cloudfront.net/scheduler/scheduleMaster/263.m3u8) |
| FTF Sports | 🏟️ 国际体育 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://1593604785.rsc.cdn77.org/FTF/FTF_SCTE.m3u8) |
| MLB | 🏟️ 国际体育 | unknown | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://jmp2.uk/plu-5e66968a70f34c0007d050be.m3u8) |
| NBA TV | 🏟️ 国际体育 | 1920x1080 | VERIFIED（200/200/206；先前首轮验证；持续测速慢；持续播放卡顿） | iptv_us · [HLS](http://23.237.104.106:8080/USA_NBA/index.m3u8) |
| NBC Sports NOW | 🏟️ 国际体育 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://d4whmvwm0rdvi.cloudfront.net/10007/99993008/hls/master.m3u8?ads.xumo_channelId=99993008) |
| NFL Channel | 🏟️ 国际体育 | unknown | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://jmp2.uk/plu-5ced7d5df64be98e07ed47b6.m3u8) |
| NHL Network | 🏟️ 国际体育 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://nhl-firetv.amagi.tv/playlist.m3u8) |
| Pac-12 Insider | 🏟️ 国际体育 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://pac12-firetv.amagi.tv/playlist.m3u8) |
| PBR RidePass | 🏟️ 国际体育 | unknown | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://jmp2.uk/plu-60d39387706fe50007fda8e8.m3u8) |
| PGA Tour | 🏟️ 国际体育 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://d11k1mnrgfposz.cloudfront.net/playlist.m3u8) |
| Rally TV | 🏟️ 国际体育 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://rally-tv-live.akamaized.net/hls/live/2117704/RallyTV-Pri/master.m3u8) |
| Red Bull TV | 🏟️ 国际体育 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://0b73ace69ebb45eaa249bb87837cb958.mediatailor.us-west-2.amazonaws.com/v1/master/ba62fe743df0fe93366eba3a257d792884136c7f/LINEAR-644-WORBUSENFAST-LG_US/644/lgtv/hls/master/playlist.m3u8) |
| SportsGrid | 🏟️ 国际体育 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://sportsgrid-tribal.amagi.tv/playlist.m3u8) |
| Stadium | 🏟️ 国际体育 | 1280x720 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://wurl120sports.global.transmit.live/hls/679a907dce42a042c23ace37/v1/stadium_gracenote/samsung_us/latest/main/hls/playlist.m3u8) |
| Swerve Combat | 🏟️ 国际体育 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://linear-253.frequency.stream/mt/roku/253/hls/master/playlist.m3u8) |
| Tennis Channel | 🏟️ 国际体育 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://cdn-ue1-prod.tsv2.amagi.tv/linear/amg01444-tennischannelth-tennischannelnl-samsungnl/playlist.m3u8) |
| Tennis Channel 2 | 🏟️ 国际体育 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://mumbai-edge.smartplaytv.in/Tennis2/index.m3u8) |
| Unbeaten | 🏟️ 国际体育 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_us · [HLS](https://d1t5afz6qed3xk.cloudfront.net/Unbeaten.m3u8) |
| FIFA+ Women | 🏟️ 国际体育 | 1280x720 | VERIFIED（200/200/206；先前最终复验） | iptv_sports · [HLS](https://cffda8ff.wurl.com/master/f36d25e7e52f1ba8d7e56eb859c636563214f541/U2Ftc3VuZy1nYl9GSUZBUGx1c3dvbWVuX0hMUw/playlist.m3u8) |
| FloRacing | 🏟️ 国际体育 | 1920x1080 | VERIFIED（200/200/206；先前最终复验） | iptv_sports · [HLS](https://amg02278-amg02278c1-flosports-worldwide-7592.playouts.now.amagi.tv/playlist.m3u8) |
| DAZN Darts x Pluto TV | 🏟️ 国际体育 | unknown | VERIFIED（200/200/206；先前最终复验） | iptv_de · [HLS](https://jmp2.uk/plu-64b67f0424ade50008a3be17.m3u8) |

## FAILED

| Channel | URL | Reason |
|---|---|---|
| NHK WORLD JAPAN | `https://master.nhkworld.jp/nhkworld-tv/playlist/live.m3u8` | ValueError: all sampled variants failed: HTTPError: HTTP Error 404: Not Found \| HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 404: Not Found \| HTTPError: HTTP Error 403: Forbidden |
| ANN News (576p) | `http://51.75.127.199:3141/annnews/index.m3u8` | HTTPError: HTTP Error 404: Not Found |
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
| CCTV6 电影 | `http://39.135.34.150:8080/000000001000/1000000001000016466/1.m3u8?xtkg` | URLError: <urlopen error timed out> |
| CHC Home Theater (1080p) | `http://39.134.19.153/dbiptv.sn.chinamobile.com/PLTV/88888888/224/3221226462/index.m3u8` | URLError: <urlopen error timed out> |
| Jiangxi Movie Channel | `https://play-live-hls.jxtvcn.com.cn/live-city/tv_jxtv4.m3u8` | HTTPError: HTTP Error 403: Forbidden |
| Jilin Movie Channel | `https://lsfb.avap.jilintv.cn/zqvk7vpj/channel/906341e6f19b4c4bacdc89941eb85d12/index.m3u8` | HTTPError: HTTP Error 567: Unknown Status |
| Cinevault 80s (720p) | `https://aegis-cloudfront-1.tubi.video/ea1ab5d1-f554-4f6b-b03f-2611fcd94257/playlist.m3u8` | HTTPError: HTTP Error 404: Not Found |
| Magnificent Movies Network | `https://mmn1-301f.kxcdn.com/hls/MMN-HLS.m3u8` | HTTPError: HTTP Error 404: Not Found |
| The Asylum (1080p) | `https://d1i3g4v4xlfhad.cloudfront.net/The_Asylum.m3u8` | ValueError: all sampled variants failed: ValueError: latest segments inaccessible: HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| ValueError: latest segments inaccessible: HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| ValueError: latest segments inaccessible: HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error 403: Forbidden \| HTTPError: HTTP Error |
| Baywatch (1080p) | `https://amg00145-fremantlemedian-baywatch-samsungau-gtsd6.amagi.tv/playlist/amg00145-fremantlemedian-baywatch-samsungau/playlist.m3u8` | URLError: <urlopen error [Errno 11001] getaddrinfo failed> |
| CCTV-8 alternate 2 | `http://ottrrs.hl.chinamobile.com/PLTV/88888888/224/3221226008/index.m3u8` | URLError: <urlopen error timed out> |
| CCTV-8 alternate 3 | `http://39.134.115.163:8080/PLTV/88888910/224/3221225635/index.m3u8` | URLError: <urlopen error timed out> |
| CCTV-8 alternate 4 | `http://183.207.248.12/PLTV/3/224/3221227204/index.m3u8` | ConnectionResetError: [WinError 10054] 既存の接続はリモート ホストに強制的に切断されました。 |
| CCTV-8 alternate 5 | `http://223.110.246.67/ott.js.chinamobile.com/PLTV/4/224/3221227205/index.m3u8` | URLError: <urlopen error timed out> |
| Zona DAZN | `https://7nyaler.streamhostingcdn.top/stream/24/index.m3u8` | HTTPError: HTTP Error 403: Forbidden |
| STOCK VOICE | `https://cdn-uw2-prod.tsv2.amagi.tv/linear/amg01287-rakutentvjapan-stockvoice-cmaf-rakutenjp/playlist.m3u8` | ValueError: all sampled variants failed: HTTPError: HTTP Error 504: Gateway Time-out \| HTTPError: HTTP Error 504: Gateway Time-out \| HTTPError: HTTP Error 504: Gateway Time-out \| HTTPError: HTTP Error 504: Gateway Time-out |
| しまじろうチャンネル | `https://cdn-apne1.tsv2.amagi.tv/linear/amg01287-rakutentvjapan-rchannelbenessehlscmaf-rakutenjp/playlist.m3u8` | HTTPError: HTTP Error 504: Gateway Time-out |
| BS Yoshimoto | `https://akariko−bck1.sankuria.sbs/stream/jp/bs_yoshimoto/stream-output.m3u8?mode=hls` | UnicodeEncodeError: 'latin-1' codec can't encode character '\u2212' in position 7: ordinal not in range(256) |
| Comedy Dynamics (1080p) | `https://comedydynamics-plex-ingest.cinedigm.com/playlist.m3u8` | URLError: <urlopen error [SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: certificate has expired (_ssl.c:1010)> |
| Kevin Hart's LOL! Network (720p) | `https://d1kt53vrikzr5o.cloudfront.net/v1/lol_lolnetwork_5/samsungheadend_us/latest/main/hls/playlist.m3u8` | HTTPError: HTTP Error 502: Bad Gateway |
| NBA G League TV (Tubi event channel) | `https://apollo.production-public.tubi.io/live/nba-g-league.m3u8` | URLError: <urlopen error [Errno 11001] getaddrinfo failed> |
| NBA TV 212.102.60.231 | `http://212.102.60.231/NBA_TV/index.m3u8` | HTTPError: HTTP Error 403: Forbidden |
| NBA TV event 1 | `http://fl5.moveonjoy.com/NBA_1/index.m3u8` | URLError: <urlopen error [Errno 11001] getaddrinfo failed> |
| NBA TV ayitistream 1080p | `https://cdn1.ayitistream.com/NBATV/index.m3u8` | HTTPError: HTTP Error 404: Not Found |
| NBA Live TV FlossyIPTV | `http://142.4.216.60:1935/edge/_definst_/2qmiwfydbj6yu89/playlist.m3u8` | URLError: <urlopen error timed out> |
| 爱奇艺_电影大片 | `http://101.72.196.41/r/baiducdnct.inter.iqiyi.com/tslive/c15_lb_dianyingjingxuan_1080p_t10/c15_lb_dianyingjingxuan_1080p_t10.m3u8` | URLError: <urlopen error timed out> |
| 爱奇艺_欢乐剧场 | `http://101.72.196.41/r/baiducdnct.inter.iqiyi.com/tslive/c16_lb_xijudianying_1080p_t10/c16_lb_xijudianying_1080p_t10.m3u8` | URLError: <urlopen error timed out> |
| 爱奇艺_经典港片 | `http://101.72.196.41/r/baiducdnct.inter.iqiyi.com/tslive/c15_lb_jingdianguangpian_1080p_t10/c15_lb_jingdianguangpian_1080p_t10.m3u8` | URLError: <urlopen error timed out> |
| 爱奇艺_华语院线 | `http://101.72.196.41/r/baiducdnct.inter.iqiyi.com/tslive/c16_lb_huayuyuanxian_1080p_t10/c16_lb_huayuyuanxian_1080p_t10.m3u8` | URLError: <urlopen error timed out> |
| 爱奇艺_怀旧剧场 | `http://101.72.196.41/r/baiducdnct.inter.iqiyi.com/tslive/c16_lb_huaijiujuchang_1080p_t10/c16_lb_huaijiujuchang_1080p_t10.m3u8` | URLError: <urlopen error timed out> |
| 爱奇艺_日韩院线 | `http://101.72.196.41/r/baiducdnct.inter.iqiyi.com/tslive/c16_lb_rihanyuanxian_1080p_t10/c16_lb_rihanyuanxian_1080p_t10.m3u8` | URLError: <urlopen error timed out> |
| 爱奇艺_老剧超清修复 | `http://101.72.196.41/r/baiducdnct.inter.iqiyi.com/tslive/c16_lb_longmenbiaoju_1080p_t10/c16_lb_longmenbiaoju_1080p_t10.m3u8` | URLError: <urlopen error timed out> |
| 爱奇艺_热播电视剧 | `http://101.72.196.41/r/baiducdnct.inter.iqiyi.com/tslive/c15_lb_reboju_1080p_t10/c15_lb_reboju_1080p_t10.m3u8` | URLError: <urlopen error timed out> |
| 睛彩竞技「移动」 | `http://gslbserv.itv.cmvideo.cn/index.m3u8?channel-id=FifastbLive&Contentid=3000000020000011528&livemode=1&stbId=YanG-1989` | HTTPError: HTTP Error 403: Forbidden |
| 睛彩篮球「移动」 | `http://gslbserv.itv.cmvideo.cn/index.m3u8?channel-id=FifastbLive&Contentid=3000000020000011529&livemode=1&stbId=YanG-1989` | HTTPError: HTTP Error 403: Forbidden |
| 咪咕直播 𝟜𝕂-𝟙「移动」 | `http://gslbserv.itv.cmvideo.cn/index.m3u8?channel-id=FifastbLive&Contentid=3000000010000005180&livemode=1&stbId=YanG-1989` | HTTPError: HTTP Error 403: Forbidden |
| 咪咕直播 𝟙「移动」 | `http://gslbserv.itv.cmvideo.cn/index.m3u8?channel-id=FifastbLive&Contentid=3000000001000005308&livemode=1&stbId=YanG-1989` | HTTPError: HTTP Error 403: Forbidden |
| 咪咕直播 𝟚「移动」 | `http://gslbserv.itv.cmvideo.cn/index.m3u8?channel-id=FifastbLive&Contentid=3000000001000005969&livemode=1&stbId=YanG-1989` | HTTPError: HTTP Error 403: Forbidden |

## 需关注

- NBA TV：现有源可读取但持续播放会卡。新测的 ayitistream 1080p 返回 404，另外两条 NBA TV 候选返回 403，另有 DNS 失败和超时；Pluto NBA FAST 虽有 HLS 响应，但约 100 秒只循环同一广告片段，因此没有用它替换。免费 NBA FAST 频道也不等同于 NBA 正赛直播。
- J SPORTS 1–4：Free-TV 日本列表标记无公开源；本列表使用此前在日本出口完成 HLS GET 验证的第三方源。源服务曾在并发请求时返回 429。
- NHK 総合：此前找到的第三方地上波源曾有片段可读，但没有作为新闻专题台收录。
- ANN／テレ朝NEWS：尚无本机通过完整 HLS 验证的日本频道源。检索到的 `ANN News` 实为印度频道。
- 咪咕体育、爱奇艺、腾讯视频：截至本次验证，没有找到可在本机通过完整 HLS 链路验证、直接导入 TiviMate 的持续直播源。网页或 App 点播地址没有冒充 M3U8。
- DAZN Darts：此前通过 HLS 与完整片段测试，保留。两个 DAZN 相关 Pluto 源只循环广告片段，未加入。
