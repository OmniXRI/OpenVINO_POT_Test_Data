# OpenVINO_POT_Test_Data
OpenVINO 訓練後優化工具 Post-Training Optimization Tool (POT) 測試用迷你ImageNet 2012版驗證集影像、標註及標籤檔。（僅供測試請勿移作它用）

/MiniImageNet 下共有100張影像。val.txt為影像分類標註檔，分類ID從0~999。ImageNet_Labels.txt為1000分類標籤檔。資料來源ImageNet ILSVRC 2012 驗證集中擷錄部份內容。


mobilenet_v2.yaml 為OpenVINO POT準確度檢查器(Accuracy_Checker)組態定義檔，執行後可檢查對應數值精度模型準確率。

例：accuracy_check -c mobilenet_v2.yaml -m ./public/mobilenet-v2/FP32/


mobilenet_v2_int8.json 為OpenVINO POT執行組態定義檔，可將FP32/FP16量化為INT8格式。

例：pot -c mobilenet_v2_int8.json -e
