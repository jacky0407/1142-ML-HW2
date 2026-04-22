# 1142-ML-HW2

## Titanic 資料前處理實作：資料清理與轉換練習

## 作業背景
- 目標：**資料前處理 (Data Preprocessing)**
- 內容：使用 Titanic 乘客資料集，練習資料清理、異常值處理、類別變數編碼、數值標準化與資料切割。
- 資料檔案為 `titanic.csv`。

---

## 作業任務

請依照 `template.ipynb` 內的提示完成所有 `TODO` 區塊。

1. **載入資料 (`load_data`)**
   - 讀取 Titanic CSV 並回傳 DataFrame 與缺失值總數

2. **處理缺失值 (`handle_missing`)**
   - 以 `Age` 的中位數填補缺失值
   - 以 `Embarked` 的眾數填補缺失值

3. **移除異常值 (`remove_outliers`)**
   - 移除 `Fare > 平均 + 3×標準差` 的紀錄

4. **類別變數編碼 (`encode_features`)**
   - 使用 `pd.get_dummies()` 對 `Sex` 與 `Embarked` 進行 One-hot 編碼

5. **數值標準化 (`scale_features`)**
   - 使用 `StandardScaler` 對 `Age`、`Fare` 進行標準化

6. **資料切割 (`split_data`)**
   - 將 `Survived` 作為 y，其餘欄位作為 X
   - 使用 `train_test_split()` 切割為訓練與測試集 (`test_size=0.2, random_state=42`)

7. **輸出結果 (`save_data`)**
   - 將清理後資料輸出成 `titanic_processed.csv`（`encoding='utf-8-sig'`）

---

## 繳交方式

**Step 1｜Fork 此專案**

**Step 2｜複製模板並改名（將 `<學號>` 換成你的學號）**
```bash
cp template.ipynb submit/HW2_<學號>.ipynb
```

**Step 3｜在 `submit/HW2_<學號>.ipynb` 完成所有 TODO**
> ⚠️ 請在自己的 `.ipynb` 作答，勿直接修改 `template.ipynb`

**Step 4｜執行最後一格，自動產生 `submit/HW2_<學號>.py`**

**Step 5｜提交 Pull Request，標題格式：`HW2_<學號>`**

---

## 評分方式

| 項目 | 比例 |
|------|------|
| 完成 PR | 10% |
| 程式正確性 | 80% |
| Code Review | 10% |

---

## 注意事項

- 請勿修改 `template.ipynb`、`README.md`、`tests/` 及任何函式名稱與回傳值結構
- `submit/` 內只允許放 `HW2_<學號>.py` 與 `HW2_<學號>.ipynb`
- 開發環境：GitHub Codespaces（已預裝 Python 3.11、pandas、numpy、scikit-learn、pytest）
