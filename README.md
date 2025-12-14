# 2025-Data-Science Steam遊戲熱門程度預測及分析

本專案以 Hugging Face 提供的 Steam Games Dataset 為基礎，透過資料清理、特徵工程與探索式資料分析，探討影響 Steam 遊戲熱門程度的關鍵因素，並建立迴歸模型預測遊戲的預估擁有者數（owners_log）。專案依序實作資料前處理、EDA、Baseline 模型、決策樹迴歸與隨機森林迴歸，評估不同方法在 MAE、RMSE 與 R² 等指標上的表現，並結合特徵重要性分析，說明評論數、價格、發行年份等特徵對遊戲熱門程度的影響。透過依照 README 指示執行各個 Notebook，使用者可完整重現報告中的圖表與模型結果。

## 環境安裝

### 建議版本: Python 3.13

### 安裝相關套件

`pip install pandas numpy matplotlib seaborn scikit-learn`


## 資料庫

資料庫來源為[**Steam Games Dataset**](https://huggingface.co/datasets/FronkonGames/steam-games-dataset?utm_source=chatgpt.com "https://huggingface.co/datasets/FronkonGames/steam-games-dataset?utm_source=chatgpt.com")


## 執行程式

請將所有檔案放置在同一個資料夾中，並按照順序執行下列程式

### 資料處理
請執行`Data_handeling.ipynb`，獲得`steam_games_featured.csv`，存於`data`資料夾中

### EDA
請執行`EDA.ipynb`可獲得EDA結果

### 模型訓練

#### Baseline
請執行`Model_baseline.ipynb`，可於執行結果看到各指標分數
#### Decision Tree Regresion
請執行`Model_DT.ipynb`，可於執行結果看到各指標分數及特徵重要性圖表
#### Random Forest Regression
請執行`Model_RF.ipynb`，可於執行結果看到各指標分數及特徵重要性圖表


### 重現結果

1. 請使用Hugging Face steam-games-dataset，會在執行`Data_handeling.ipynb`進行抓取，存於`data/steam_games_cleaned.csv`中
2. 依環境安裝建立環境
3. 依執行程式照順序正確執行相關程式，即可獲得相關圖表及結果
