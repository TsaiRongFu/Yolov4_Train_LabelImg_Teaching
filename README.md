## 標記圖片使用LabelImg

[LabelImg Github](https://github.com/tzutalin/labelImg)

* git clone https://github.com/tzutalin/labelImg.git
* pip install lxml
* pip install pyqt5
* 如遇到`No module named 'libs.resources'`錯誤輸入下列指令

  ```
  pyrcc5 -o ./libs/resources.py resources.qrc
  ```

labelImg\data\predefined_classes.txt是預設類別名稱
如果要直接標記Yolo格式檔的人先把裡面的預設類別清除

## 開始標記照片

這邊分成兩種標記方式，一個是直接標記yolo專用格式檔
另一個是xml再轉成yolo專用格式檔

---

### 首先教學的是直接標記yolo格式檔

把照片分別放入放入yolo_train、yolo_test底下，數量為80%:20%

labelImg設定好讀取圖片檔案資料夾、儲存標記檔資料夾，就可以開始標記

* 標記完成後打開Command OR Terminal並輸入以下指令
  * cd 至 XOXO(您的專案名稱)_detection檔案資料夾底下
  * key入 `python Image Path Txt.py`

當您完成上述步驟會在test、train資料夾內出現對應圖片檔名稱的txt也就是for yolo的標記檔

在cfg資料夾內會出現test.txt、train.txt檔

有出現上述兩個檔案內容表示完成配置您標記和訓練檔路徑了！

---

### 接著開始教學xml格式轉成yolo用格式方法

把照片分別放入放入xml_train、xml_test底下的image，數量為80%:20%

labelImg設定好讀取圖片檔案資料夾、儲存標記檔資料夾(格別資料夾底下的xml資料夾)，就可以開始標記

* 標記完成後打開Command OR Terminal並輸入以下指令
  * cd 至 XOXO(您的專案名稱)_detection檔案資料夾底下
  * key入 `python PASCAL VOC xml to txt.py`

當您完成上述步驟會在test、train資料夾內出現對應圖片檔名稱的txt也就是for yolo的標記檔，還有從image資料夾內複製的圖片

在cfg資料夾內會出現test.txt、train.txt檔

有出現上述兩個檔案內容表示完成配置您標記和訓練檔路徑了！
