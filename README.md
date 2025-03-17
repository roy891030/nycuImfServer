## **1. 連線到伺服器**
在 **Mac 本機終端** 輸入：
📌 NYCU 伺服器 Jupyter Notebook 使用流程

```markdown
ssh -L 8888:localhost:8888 313707050_iof@140.113.26.108
```
輸入密碼後，即可登入伺服器。

```markdown
密碼：nycu_手機
```

---

## **2. 啟動 Jupyter Notebook**
在 **伺服器終端** 執行：
```bash
~/.local/bin/jupyter notebook --ip=0.0.0.0 --port=8888 --no-browser
```
成功後會顯示類似：
```bash
http://127.0.0.1:8888/tree?token=xxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

---

## **3. 在本機存取 Jupyter Notebook**
1. **開啟瀏覽器**
   ```text
   http://localhost:8888/tree
   ```
2. 若要求 `token`，請從 SSH 終端複製：
   ```bash
   http://127.0.0.1:8888/tree?token=xxxxxxxxxxxxxxxxxxxxxxxxxxxxx
   ```
   並貼到瀏覽器中。

---

## **4. 結束並關閉 Jupyter**
### **4.1 儲存 Notebook**
在 Jupyter 介面：
- 點擊 **File → Save and Checkpoint**
- 或按 `Ctrl + S` / `Cmd + S`

### **4.2 關閉 Jupyter 伺服器**
在 **伺服器終端** 按：
```bash
Ctrl + C
```
出現提示：
```bash
Shutdown this Jupyter server (y/[n])?
```
輸入：
```bash
y
```

---

## **5. 登出伺服器**
- **關閉 SSH 連線**
  ```bash
  exit
  ```
  或直接按：
  ```bash
  Ctrl + D
  ```

---

## **6. 下次使用**
### **6.1 連線 SSH**
```bash
ssh -L 8888:localhost:8888 313707050_iof@140.113.26.108
```

### **6.2 啟動 Jupyter**
```bash
~/.local/bin/jupyter notebook --ip=0.0.0.0 --port=8888 --no-browser
```

### **6.3 在本機瀏覽器開啟**
```text
http://localhost:8888/tree
```

---
```
