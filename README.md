
ad_non_political.csv非政黨、非政治人物臉書廣告
* 這份資料是以 Meta 廣告庫 API 抓取（2019 至 2023-11-30）
* 其選舉及社會議題所有廣告以 2024 年 3 組總統候選人的名字和推薦政黨為關鍵字搜尋
* 再以人工分類標示併選出非政治人物、非政府、非政黨的粉絲專頁與媒體粉絲專頁。
* 這份資料為 READr 2024 臉書廣告專題《不是政治人物也掏錢下選舉廣告：意見領袖加入　打「口水仗」還是重建討論空間？》所用

相關欄位
1. id 檔案庫不重複編號
2. page_id 粉絲專頁編號
3. page_name 粉絲專頁名稱
4. ad_creation_time 廣告建立日期
5. ad_creative_bodies 廣告文字內容
6. spend.lower_bound,spend.upper_bound 廣告支出區間（新台幣）
8. impressions.lower_bound,impressions.upper_bound 觸及曝光區間
10. bylines 廣告主／出資者
11. NN1 NN2 NN3 NN4 NN5 廣告庫中的粉絲專頁歷史名稱
12. type 人工標示粉絲專頁類別

ad_non_political_audience.csv 非政黨、非政治人物臉書廣告受眾資料
*為 ad_non_political 受眾資料

all_ads_nofilter.csv 以 2024 年 3 組總統候選人的名字和推薦政黨為關鍵字搜尋臉書廣告資料
