

#2023_meta_politic_AD
2023政治廣告臉書資料

A.ads_ai91 所有一般廣告立場資料
*  ads_ai91 非政府非政黨非媒體的一般粉專廣告資料

  需特別解釋欄位如下
      * N1-N5 更名紀錄，統計分析上以N1為主（避免同一個粉專只是換了名字）
      * type else 非政府非政黨非媒體
      * messeageID 透過 page_nmae ad_creative_bodies page_id 進行 mapping
      * ai1 立場 tag
        * ai1 立場欄位分析和篩選會用包含的方式，
          * a 宣傳、稱讚侯友宜國民黨
          * b 批評侯友宜國民黨
          * c 宣傳、稱讚賴清德、蔡英文、民進黨
          * d 批評賴清德、蔡英文
          * e 宣傳、稱讚柯文哲、民眾黨
          * f 批評柯文哲、民眾黨
          * 不包含 abcdef 就當不含或是無法判斷立場

B.ads_ai95_2 所有一般廣告受眾資料
    * ads_ai95_2 非政府非政黨非媒體的一般粉專廣告「受眾」資料
    * ads_ai91 合併受眾資料 by data id

C.ads_mai8 媒體政府廣告資料
D.ads_mai82 媒體政府廣告受眾資料
E.media_gov_count 媒體政府立場篇數資料
F.else_count 一般粉專立場篇數資料
G.politic_ai 政黨政治人物專業廣告受眾資料



I.資料分析 coding

  * try.Rmd -> 抓取 api 資料的 rnotebook
  * analyze.Rmd +analyze.Rmd 搜集資料＋彙整 chatgpt ai 資料
  * analyze2.Rmd 處理受眾資料分析
  * analyze3.Rmd 處理媒體 ai 合併、政府
  * anaylyze_who.Rmd 處理媒體政府受眾資料分析
  * analyze4.Rmd 處理政黨受眾


J.原始資料
  * ads_ai9ver2
     * 修正後的 tagging 資料 ads_ai9ver2.csv -> 在資料裡還是用 ads_ai9 命名分析
     * 主要使用到 ai1 欄位資料
  
  * name_right
     * N1-N5 透過 page_id 可檢視更名紀錄及類型
  
  * message_mapping
     * 訊息廣告 mapping
     * 訊息 tagging 過濾重複，因此重新 mapping
  
  * ads_ai91 如何從 ads_ai9 得來
    * ads_ai9 <- left_join(message_mapping,ads_ai9)
      ads_ai9 <- ads_ai9[is.na(messeageID)==F,]
      ads_ai9$GPT<-NULL 
    * -> 將重複廣告 mapping 回每個廣告 id，再 mapping 立場 tag 原始資料
    
    
    
    
    