# iPAS資安工程師中級 | 防護實務衝刺班 | 證照筆記 | Ver.20241218 [![Hits](https://hits.sh/github.com/heymrslat/ipas-intermediate-notes.svg)](https://hits.sh/github.com/heymrslat/ipas-intermediate-notes/)
> 此 repository 為 iPAS 資安工程師 中級證照筆記。\
> 範圍將著重在【防護實務】並以【歷屆難題與解析】與【名詞工具重點說明】方式呈現。

## Author
> 國立臺北科技大學 資安碩 Salt Liao 🧂

## 學術聲明
> 學術倫理聲明：此筆記僅限學術學習，嚴禁任意轉載，亦禁止改作、出版、或商業用途。\
> 也歡迎想參予的貢獻者發 PR 幫筆記更新讓它更完整；或發 Issue 來 提問 / 建議 / 討論 筆記上的內容。

## 前言
> 往年的 中級資安工程師證照考試【防護實務】通過率約 **三成**，\
> 此筆記以【防護實務衝刺班】為設計核心，目的為增加得分率通過率。

## 筆記方向
> 將採用 個人評估防護實務歷屆難題 與 個人評估資安重要專有名詞。

## 致敬
> 在本筆記的最底下【Refer】致敬了在過去考試提供資源的網上各 **大大** **前輩** **貢獻者** 們，\
> 他們的 iPAS 資安中級筆記都非常 詳細 厲害，是我撰寫本筆記的動力與起因。(本筆記內容不會與他們重疊)\
> 希望本篇能對正在學習資安的你有重點整理之幫助
> **最後祝大家順利通關取得證照 !!!**



---
</br>

```diff
- - - - - - - - - - - - - - - - - - - - 筆記正文開始 - - - - - - - - - - - - - - - - - - - -
```

</br>

# 目錄 TOC
- [【官方資訊】](#官方資訊)
- [【歷屆難題與解析】](#歷屆難題與解析)
  - [【113-2 中級 防護實務】](#113-2-中級-防護實務)
  - [【113-1 中級 防護實務】](#113-1-中級-防護實務)
- [【名詞工具重點說明】](#名詞工具重點說明)
  - [【SIEM vs IDS】](#siem-vs-ids)
  - [【APT 名詞說明 以及 常用技術手法】](#apt-名詞說明-以及-常用技術手法)
  - [【OWASP Top 10 的詳細解釋】](#owasp-top-10-的詳細解釋)
  - [【DDoS攻擊種類之對應OSI層級】](#ddos攻擊種類之對應osi層級) 
- [【Refer】](#refer)

---
</br>

# 官方資訊

## 鑑定制度與評鑑內容

### 鑑定制度架構

[Fig.Appraisal_System_Structure]
![Untitled](../Appendix-img/Appraisal_System_Structure.png)

懶人包 : 兩個都要70分才有證照，若一科過一科沒過，下次可只考沒過的那科 (限三年內)

### 評鑑內容

[Fig.Specialist_Examination_Evaluation]

懶人包 : 
- 弱點、威脅分類與攻擊手法(20%) 
- 防護與應變實務(30%) 
- 安全維運(20%)
- 滲透測試、源碼測試、資安健診(30%)

Refer : https://www.ipas.org.tw/ise/AbilityPageContent.aspx?mnuno=675cfae7-387b-4a6d-a4b8-f15a78bb10d4&pgeno=092c80f2-3f12-495b-b8d5-75feb46bd3c8

</br>

## 證書效期與換發

### 證書效期

初級證書：永久有效，不需換發
中級證書：有效期限為5年，需於證書有效期限屆滿3個月前申請換發

### 證書換發
> 2擇1

(1) 每5年內須接受資訊安全相關訓練，合計時數48小時以上
(2) 從事資訊安全相關工作，取得證書後每一年工作年資得抵訓練時數8小時

Refer : https://www.ipas.org.tw/ise/AbilityPageContent.aspx?mnuno=25150af2-dbc4-45e3-876e-a7214304168a&pgeno=007ad965-30c4-427a-a261-369b0c53d9dc

</br>

## 數發部-資通安全專業證照清單

[Fig.Certificate_Certification_List]

資通安全專業證照清單（1131106修正）

Refer : https://moda.gov.tw/ACS/laws/certificates/676

---
</br>

# 歷屆難題與解析

- [【113-2 中級 防護實務】](#113-2-中級-防護實務)
- [【113-1 中級 防護實務】](#113-1-中級-防護實務)

---
</br>

## 113-2 中級 防護實務

<details> 
  <summary>Q5.【題組】 依據公司高層的要求，工程師正評 估採用「弱點評估」工具來評估公司內部潛在的弱點項目，試問 下列有關「弱點評估」之敘述，下列何者「有誤」？</summary>

  123\

  456\

  ---

</details> 

【題組 1】情境如附圖所示
```
公司因供應鏈之客戶要求在執行受託業務時，必須針對所承接之受託業務有關的資訊安全有所作為，
因此公司高層下令有關人員針對公司在執行受託業務上可能面臨的資訊安全風險議題進行研議。
```
### Q5.【題組】 依據公司高層的要求，工程師正評 估採用「弱點評估」工具來評估公司內部潛在的弱點項目，試問 下列有關「弱點評估」之敘述，下列何者「有誤」？
(A) 可使用 Nessus Professional 工具來進行系統弱點評估\
(B) 可使用 Acunetix 工具來進行網站弱點評估\
(C) 可使用 Fortify SCA 動態原始碼檢測分析工具來進行軟體 系統之原始碼弱點評估\
(D) 可使用 Nmap 工具來進行網路設備弱點評估\
\
Ans : (C)\
\
原因如下：

(C) Fortify SCA（Static Code Analyzer）是一款 **靜態** 原始碼分析工具，旨在不執行程式的情況下，透過檢查源碼來找出潛在的安全漏洞。\
這種分析方式稱為「靜態應用安全測試」（SAST），適用於軟體開發的早期階段。\
題目中錯誤地將它描述為「動態」原始碼檢測分析工具，這是錯誤的。\
動態分析工具（DAST）通常會在執行程式時進行測試，而這不是 Fortify SCA 的功能​。

Refer : https://www.microfocus.com/documentation/fortify-static-code-analyzer-and-tools/2310/

其他選項解析：

(A) Nessus Professional 是一個廣泛用於系統弱點評估的工具，能夠幫助發現系統層級的安全漏洞​。\
(B) Acunetix 是專門針對網站和網頁應用程式的弱點掃描工具，能夠檢測網站常見的安全漏洞。\
(D) Nmap 雖然主要用於網絡設備的掃描和端口發現，但它可以協助發現網絡設備的潛在弱點，適用於網絡設備的弱點評估​。

Refer : https://www.datamation.com/security/nessus-vs-nmap

因此，(C) 只是因為錯誤描述 Fortify SCA 的用途，將其誤認為是「動態」分析工具，這是與實際不符的。
```diff
- 要知道的是 萬一題目 (C) 改成「靜態」分析工具，則這題將沒有正解。
```

---
</br>

## 113-1 中級 防護實務

### Q1. 關於 MITRE ATT&CK 中的憑證存取（Credential Access）戰術（Tactic），下列何項錯誤？
(A) 中間人攻擊（Adversary-in-the-Middle）屬於此類戰術\
(B) 暴力破解攻擊（Brute Force）屬於此類戰術\
(C) 密碼政策探索（Password Policy Discovery）屬於此類戰術\
(D) 變造網站憑證（Forge Web Credentials）屬於此類戰術\
\
Ans : (C)\
\
在 MITRE ATT&CK 框架中，憑證存取（Credential Access）戰術涉及攻擊者使用多種方法來偷取資料和證書，通常用於身份驗證和授權。\
\
(A) 中間人攻擊（Adversary-in-the-Middle）屬此戰術：這是正確的，因為攻擊者在此類攻擊中可能會攔截和竊取認證。\
(B) 暴力破解攻擊（Brute Force）屬類戰術：這也是正確的，因為暴力破解是一種常見的方法，用來嘗試許多密碼以獲取訪問權限。\
(C) 密碼政策探索（Password Policy Discovery）屬此戰術：這是錯的，密碼政策探索偏向於獲取有關系統密碼政策信息，而非直接存取憑證。\
(D) 變造網站憑證（Forge Web Credentials）屬此戰術：這是正確的，製造假的網站憑證是一種直接涉及憑證存取的攻擊方法。\
因此選項 **(C)** 是錯誤的。\
\
Refer :　https://www.netscout.com/what-is-mitre-attack/credential-access

---
</br>

### Q5.【題組】 情境如附圖所示。駭客首先在 WSL 環境中部署了一個專門編寫的惡意 script，該 script 旨在利用 Windows 與 WSL 之間的互操作性漏洞。請問其目的，最有可能是下列何項？（請選一個最合適的答案）

```
在 TechSecure Inc.，一家前沿的科技安全公司，資安團隊面臨著一項前所未有的挑戰。
隨著開發團隊需要更多的彈性和功能來進行軟體開發，公司決定在其開發環境中採用 Windows Subsystem for Linux 2 (WSL2)。
這個決策立即吸引了公司內的資安政策制定者 Alex 的注意。
身為公司資安政策訂定者，在面對該公司研發團隊必須使用 Windows Subsystem for Linux 2(WSL2)，必須對其資安攻防的應變性及那些安全管理措施。
```
```
與此同時，一群駭客正在密切關注 TechSecure 的這一舉措。
他們計劃利用 WSL 一個未被廣泛知的漏洞作為橋樑來部署惡意軟體，從而進行內部網絡入侵。
這個團隊本專門設計來利用 WSL2 環境中的漏洞，目標是獲取公司的敏感數據和內部系統的控制權。
駭客計劃藉著利用 Windows Subsystem for Linux (WSL) 來進行網絡入侵。
```
(A) 在 Windows 創立一個隱藏的管理員帳戶，以便未來存取\
(B) 為了直接加密 Windows 系統文件，進行勒索軟體攻擊\
(C) 通過 WSL 環境檢索並傳送 Windows 系統日誌，以分析可能的弱點\
(D) 利用 WSL 執行環境的特性，隱藏網路流量，以掩蓋資料外洩行為\
\
Ans : (D)\
\
選項 (D) 「利用 WSL 執行環境的特性，隱藏網路流量，以掩蓋資料外洩行為」是一個可能的答案，因為WSL提供了在Windows系統上運行Linux環境的功能，這可能被駭客用來隱藏其活動。這種互操作性可能允許駭客更輕易地在Windows環境中隱藏惡意活動，包括資料外洩。\
其他選項的可能性分析如下：\
(A) 這是一種常見的攻擊手法，但不一定與WSL的特殊功能直接相關。\
(B) 直接加密Windows系統文件更多地是一種直接的勒索軟體攻擊，並不需要WSL特定的互操作性。\
(C) 雖然可能透過WSL獲得Windows系統日誌，但不是WSL環境最直接的利用方式。\
因此，考慮到WSL的特殊能力和潛在用途，選項 (D) 描述了一個合理且與WSL特性相關的攻擊目的，即利用WSL環境的特點來隱藏其網路活動，從而掩蓋資料外洩行為。

---
</br>

### Q14. 根據 NIST Cybersecurity Framework 中的 Protect 功能，下列哪些項目是組織實施此功能時應考慮的關鍵要素？
(A) 實施身份管理及存取控制\
(B) 執行資料加密和保護\
(C) 建立災難復原程序\
(D) 定期執行弱點掃描\
\
Ans : (A) (B)\
\
這個題目是關於 NIST Cybersecurity Framework(美國國家標準與技術研究院網路安全框架)中的 Protect(保護)功能。該框架由 NIST 制定,旨在幫助組織管理和降低網路安全風險。\
框架包含五個核心功能:Identify(識別)、Protect(保護)、Detect(檢測)、Respond(響應)和 Recover(恢復)。\
Protect 功能的目的是開發和實施適當的保障措施,以確保關鍵服務的傳送。這包括訪問控制、員工培訓、資料安全和資訊保護流程等多個類別。\
讓我們逐個分析選項:\
```
(A) 實施身份管理及存取控制:
身份管理和訪問控制是 Protect 功能的關鍵要素之一。
它們確保只有經過授權的用戶才能訪問敏感資料和系統。這可以通過各種方法實現,例如強密碼、多因素身份驗證和最小權限原則。
資料來源:NIST Special Publication 800-53 Rev. 4, Security and Privacy Controls for Federal Information Systems and Organizations
```
```
(B) 執行資料加密和保護:
資料加密是保護資料免受未經授權訪問的重要手段。
通過加密,即使資料被盜,如果沒有正確的解密金鑰,也無法讀取資料內容。資料保護還包括其他措施,如資料備份和資料外洩防護。
資料來源:NIST Special Publication 800-175B, Guideline for Using Cryptographic Standards in the Federal Government: Cryptographic Mechanis
```
```
(C) 建立災難復原程序:
雖然災難復原程序對於組織的網路彈性至關重要,但它們通常被視為 Recover(恢復)功能的一部分,而不是 Protect 功能。
災難復原程序旨在幫助組織在發生重大事故(如自然災害或網路攻擊)後恢復其 IT 系統和業務運營。
資料來源:NIST Special Publication 800-34 Rev. 1, Contingency Planning Guide for Federal Information Systems
```
```
(D) 定期執行弱點掃描:
定期執行弱點掃描是 Detect(檢測)功能的一部分,而不是 Protect 功能。
弱點掃描有助於識別系統和應用程式中的安全弱點,使組織能夠在弱點被利用之前進行修復。
資料來源:NIST Special Publication 800-115, Technical Guide to Information Security Testing and Assessment
```
綜上所述,根據 NIST Cybersecurity Framework,實施身份管理及存取控制(A)和執行資料加密和保護(B)是組織在實施 Protect 功能時應考慮的關鍵要素。

---
</br>

# 名詞工具重點說明

- [【SIEM vs IDS】](#siem-vs-ids)
- [【APT 名詞說明 以及 常用技術手法】](#apt-名詞說明-以及-常用技術手法)
- [【OWASP Top 10 的詳細解釋】](#owasp-top-10-的詳細解釋)
- [【DDoS攻擊種類之對應OSI層級】](#ddos攻擊種類之對應osi層級)

</br>

## siem vs ids

- SIEM：
    全面監控和管理安全態勢
    分析多個數據來源
    進行威脅分析和合規報告
- IDS：
    即時檢測入侵行為
    快速生成安全警報
- 結論：
    SIEM 和 IDS 各有專長，互補增強安全防護。

---
</br>

## apt 名詞說明 以及 常用技術手法

### 名詞
* APT（Advanced Persistent Threat，高級持續性威脅）攻擊
* 是一種精密、長期、且持續的網絡攻擊方式，
* 攻擊者會使用多種技術手法來達成他們的目的。
* 以下是 APT 攻擊中常用的技術手法的詳細解釋：

### 1. **Privilege Escalation（提權）**：
   - **定義**：Privilege Escalation（提權）是指攻擊者通過利用系統漏洞或錯誤配置，將自己的權限從低權限（例如普通用戶）提升到更高的權限（如管理員或系統級權限）的過程。
   - **作用**：提權是 APT 攻擊中非常關鍵的一步，因為它可以讓攻擊者獲得更大的系統控制權，從而執行更多高級操作。例如，攻擊者可能最初只能訪問一個普通帳戶，但通過提權，他們能夠獲得對系統或網路的完全控制，進行任意文件讀取、系統設定更改或安裝惡意軟件。
   - **方法**：
     - **漏洞利用**：利用已知的或未披露的（零日）漏洞來提升權限。
     - **錯誤配置**：系統或應用程序中不當設置的權限也可能被利用。
     - **憑證竊取**：攻擊者可能會竊取高權限用戶的憑證（如密碼或 token），來冒充該用戶。

### 2. **Lateral Movement（橫向移動）**：
   - **定義**：Lateral Movement（橫向移動）是指攻擊者在獲得初始系統進入點後，在網絡中橫向擴展，進一步攻擊其他系統或資源的過程。
   - **作用**：橫向移動的目的是在網絡內部擴展攻擊範圍，尋找更多敏感信息或更高價值的目標。APT 攻擊者往往不滿足於入侵單一系統，而是會試圖進一步擴展他們的控制範圍，以便最終達到入侵目標系統或獲取關鍵數據的目的。
   - **方法**：
     - **使用已獲取的高權限**：在提權後，攻擊者會利用管理員或系統權限進行橫向移動。
     - **憑證轉移攻擊**：通過竊取或重用在網絡中的用戶憑證，攻擊者可以進一步侵入其他系統。
     - **遠程桌面協議（RDP）或 Windows 管理工具**：攻擊者利用網路中的合法工具，像是 RDP 或 WMI，來在不同系統之間移動，而不引起系統防禦警報。

### **APT 攻擊中的應用**：
- **提權和橫向移動**這兩個技術手法是 APT 攻擊中的常見步驟。通常，攻擊者會先取得某個系統的初步訪問權限（可能是透過魚叉式網釣、社交工程或已知漏洞），然後使用提權技術來提升自己的權限，接著再利用橫向移動技術在目標網絡內擴展控制範圍，最終達到攻擊目標。

總結來說，這些技術手法是 APT 攻擊持續性和高威脅性的核心所在，讓攻擊者能夠在被入侵系統內進行深度滲透並保持長時間隱蔽。

---
</br>

## owasp top 10 的詳細解釋

### 1. 失效的存取控制 (Broken Access Control):
* 定義: 這是指系統未能正確限制用戶對某些資源或功能的訪問。
* 詳細說明:
    * 垂直權限升級: 普通用戶可以執行只有管理員才能執行的操作。
    * 水平權限升級: 用戶A可以訪問用戶B的數據。
    * 目錄遍歷: 攻擊者可以訪問系統目錄中的敏感文件。
    * 未經授權的API訪問: API端點缺乏適當的訪問控制。
* 影響:
    * 數據洩露
    * 系統被完全接管
    * 聲譽損害
* 防禦方法:
    * 實施最小權限原則
    * 使用角色基礎的存取控制(RBAC)
    * 強制執行適當的會話管理
    * 在服務器端驗證所有存取控制決策
    * 禁用目錄列表
    * 定期審核和測試存取控制機制
### 2. 加密機制失效 (Cryptographic Failures):
* 定義: 這包括與數據保護相關的問題,特別是加密方面的失誤。
* 詳細說明:
    * 使用過時或弱加密算法(如MD5, SHA1)
    * 使用固定或可預測的加密密鑰
    * 不正確的證書驗證
    * 在客戶端存儲敏感數據
* 影響:
    * 敏感數據洩露(如密碼、信用卡信息)
    * 身份盜竊
    * 財務損失
* 防禦方法:
    * 使用強加密算法(如AES, RSA)
    * 實施適當的密鑰管理
    * 使用安全的隨機數生成器
    * 加密所有傳輸中和靜止狀態的敏感數據
    * 禁用較弱的加密協議和密碼套件
### 3. 注入 (Injection):
* 定義: 攻擊者能夠將惡意代碼注入應用程序,並在處理時執行。
* 詳細說明:
    * SQL注入: 攻擊者通過操縱輸入來修改SQL查詢。
    * 命令注入: 攻擊者能夠在系統上執行操作系統命令。
    * LDAP注入: 攻擊者可以操縱LDAP查詢。
    * XPath注入: 攻擊者可以修改XML查詢。
* 影響:
    * 未經授權的數據訪問和修改
    * 數據庫完整性損壞
    * 遠程代碼執行
* 防禦方法:
    * 使用參數化查詢
    * 使用ORM框架
    * 輸入驗證和轉義
    * 最小權限原則
    * 使用存儲過程(謹慎使用)
### 4. 不安全的設計 (Insecure Design):
* 定義: 在軟件設計階段就存在的安全缺陷。
* 詳細說明:
    * 缺乏適當的安全控制
    * 未考慮到所有可能的攻擊場景
    * 過度信任用戶輸入或外部系統
    * 不安全的數據流
* 影響:
    * 系統級別的安全漏洞
    * 難以修復的深層次問題
    * 可能導致多個其他安全問題
* 防禦方法:
    * 進行威脅建模
    * 實施安全開發生命週期(SDL)
    * 進行安全架構審查
    * 採用"安全即設計"的理念
    * 定期進行滲透測試和代碼審查
### 5. 安全配置錯誤 (Security Misconfiguration):
* 定義: 系統、框架、應用程序或服務器的配置不當或不安全。
* 詳細說明:
    * 使用默認密碼或弱密碼
    * 啟用不必要的功能、端口或服務
    * 錯誤處理機制暴露敏感信息
    * 缺少適當的安全標頭
    * 軟件過時或有漏洞
* 影響:
    * 未經授權的系統訪問
    * 系統信息洩露
    * 增加其他攻擊的成功率
* 防禦方法:
    * 採用"最小化"原則,只啟用必要的功能
    * 自動化配置和修補過程
    * 強密碼策略
    * 定期進行安全審計和掃描
    * 實施安全標頭和適當的錯誤處理
### 6. 易受攻擊和過時的元件 (Vulnerable and Outdated Components):
* 定義: 使用具有已知漏洞的庫、框架或其他軟件模塊。
* 詳細說明:
    * 使用過時的第三方庫
    * 未及時應用安全補丁
    * 客戶端庫的不安全配置
    * 繼續使用不再維護的軟件
* 影響:
    * 可能導致各種攻擊,取決於漏洞的性質
    * 系統可能被輕易入侵
* 防禦方法:
    * 定期更新所有依賴項
    * 使用軟件組成分析(SCA)工具
    * 訂閱安全公告
    * 實施虛擬補丁策略
    * 只使用官方和可信的來源
### 7. 識別與驗證失效 (Identification and Authentication Failures):
* 定義: 身份驗證和會話管理相關的問題
* 詳細說明:
    * 允許弱密碼
    * 不安全的密碼恢復機制
    * 缺少多因素認證
    * 會話固定攻擊
    * 不安全的會話管理
* 影響:
    * 未經授權的賬戶訪問
    * 身份盜竊
    * 會話劫持
* 防禦方法:
    * 實施強密碼策略
    * 使用多因素認證
    * 實施安全的會話管理
    * 限制失敗登錄嘗試
    * 使用安全的密碼存儲技術(如bcrypt)
### 8. 軟體和資料完整性失效 (Software and Data Integrity Failures):
* 定義: 代碼和數據在處理或存儲過程中未能維護其完整性。
* 詳細說明:
    * 不安全的反序列化
    * 使用不受信任的數據或代碼
    * 軟件更新過程中的完整性檢查失敗
    * CI/CD管道中的安全問題
* 影響:
    * 代碼執行
    * 數據操縱
    * 軟件供應鏈攻擊
* 防禦方法:
    * 使用數字簽名
    * 實施完整性檢查
    * 使用安全的反序列化技術
    * 對CI/CD管道進行安全審計
    * 實施軟件供應鏈安全措施
### 9. 安全記錄和監控失效 (Security Logging and Monitoring Failures):
* 定義: 缺乏足夠的日誌記錄、檢測、監控和主動響應。
* 詳細說明:
    * 可審核事件未被記錄
    * 警告和錯誤生成不清晰的日誌消息
    * 日誌未被監控或實時告警
    * 滲透測試和掃描無法觸發告警
* 影響:
    * 無法檢測和響應安全事件
    * 延遲事件響應和取證
    * 無法追踪攻擊者的活動
* 防禦方法:
    * 實施集中式日誌管理
    * 設置實時監控和告警系統
    * 確保日誌包含足夠的上下文信息
    * 定期審查和分析日誌
    * 實施安全信息和事件管理(SIEM)系統
### 10. 伺服器端請求偽造 (Server-Side Request Forgery, SSRF):
* 定義: 攻擊者可以使服務器向意外的目標發送請求。
* 詳細說明:
    * 攻擊者可以訪問內部服務
    * 可以繞過防火牆和其他網絡安全控制
    * 可能導致敏感數據洩露或系統入侵
* 影響:
    * 訪問內部系統和服務
    * 數據洩露
    * 遠程代碼執行
* 防禦方法:
    * 實施白名單驗證
    * 禁用不必要的協議
    * 使用網絡分段
    * 對輸出進行掃描和過濾
    * 限制對內部資源的訪問

---
</br>

## DDoS攻擊種類之對應OSI層級

| OSI 層級               | 攻擊類型                        | 攻擊描述                          | 攻擊方式      |
|------------------------|----------------------------------|-----------------------------------|--------------|
| **Application Layer <br>應用層 Layer7** | DNS Flooding<br>/DNS NXDOMAIN Flood<br>(DNS 洪水攻擊) | 利用大量無效的 DNS 查詢造成網絡過載       | 佔頻寬      |
|                        | DNS 放大/反射攻擊 |        | 佔頻寬      |
|                        | SNMP 放大/反射攻擊 |        | 佔頻寬      |
|                        | NTP 放大/反射攻擊 |        | 佔頻寬      |
|                        |        |        |        |
|                        | CC Attack <br>(CC 攻擊)            | 通過大量的請求<br>使目標無法處理，導致服務拒絕 | 消資源      |
|                        | Slow Attacks <br>(緩慢攻擊)         | 利用緩慢請求來耗盡目標的資源              | 消資源      |
|                        | HTTP(s) Flood <br>(HTTP 洪水攻擊)      | 通過大量 HTTP(s) 請求造成網絡服務過載      | 消資源      |
|                        | POST/GET 大量請求攻擊     | 通過大量 POST/GET 請求造成網絡服務過載      | 消資源      |
|                        | ReDoS <br>(Regular Expression Denial of Service)      | 通過設計特定正則表達式匹配負載使目標 CPU 過度消耗   | 消資源      |
|                        |        |        |        |
| **Presentation Layer <br>表示層 Layer6** | TLS Attacks <br>(Incomplete TLS Session) <br>(TLS 層攻擊 - 不完整 TLS 會話) | 利用不完整的 TLS 會話來消耗目標資源       | 消資源      |
|                        |        |        |        |
| **Session Layer <br>會話層 Layer5**     |        |        |       |
|                        |        |        |        |
| **Transport Layer <br>傳輸層 Layer4**   | Ack Flood <br>(ACK 洪水攻擊)       | 發送大量的 ACK 包來填滿目標的帶寬或資源    | 佔頻寬      |
|                        | SYN Flood Attack <br>(SYN 洪水攻擊) | 透過 SYN 請求過載目標的連接處理系統        | 佔頻寬      |
|                        | UDP Flood Attack <br>(UDP 洪水攻擊) | 利用 UDP 包造成大量流量，淹沒目標網絡       | 佔頻寬      |
|                        | TCP連接洪水攻擊  |     | 佔頻寬      |
|                        | PSH+ACK 洪水攻擊  |     | 佔頻寬      |
|                        | Ack Flood - Reflection Attack <br>(ACK 洪水攻擊-反射攻擊)       |      | 佔頻寬      |
|                        | RST 洪水攻擊  |     | 佔頻寬      |
|                        | SSL 洪水攻擊  |     | 佔頻寬      |
|                        | Fraggle Attack <br>(Fraggle 攻擊)  | 基於 UDP 拒絕服務攻擊，利用廣播放大流量   | 佔頻寬      |
|                        |        |        |        |
|                        | Sockstress 攻擊  |     | 消資源      |
|                        | THC SSL DOS 攻擊  |     | 消資源      |
|                        |        |        |        |
| **Network Layer <br>網絡層 Layer3**     | Smurf Attack (ICMP) <br>(Smurf 攻擊 - ICMP) | 利用 ICMP 請求放大攻擊流量               | 佔頻寬      |
|                        | ICMP Flood Attack <br>(ICMP 洪水攻擊) | 發送大量 ICMP 請求使目標網絡過載          | 佔頻寬      |
|                        | IGMP 洪水攻擊 直接攻擊 |       | 佔頻寬      |
|                        |        |        |        |
|                        | Ping of Death (ICMP) <br>(Ping of Death - ICMP) | 發送異常大且不合規的 Ping 請求使系統崩潰   | 消資源      |
|                        |        |        |        |
| **Data Link Layer <br>資料連接層 Layer2** | MAC Flooding Attack <br>(MAC 洪水攻擊) | 發送大量的 MAC 地址請求，消耗交換機資源    | 消資源      |
|                        |        |        |        |
| **Physical Layer <br>物理層 Layer1**    |        |        |        |

*Resource Exhaustion 資源耗竭 : 指攻擊目標的計算或處理能力，使系統過載<br>
*Bandwidth Exhaustion 頻寬耗竭 : 指透過大量流量填滿目標帶寬，使其無法正常運行

Refer : https://www.ithome.com.tw/news/166386

---

---

---

# refer

> 參考來源與致敬

1. [iPas-詳解表-1120805](https://docs.google.com/spreadsheets/d/1Nj3shzjCJZBqBOhLjRVV2iIYokPLWThtbadLJT9izfE/edit?gid=0#gid=0) 
2. [iPAS資安證照討論區 Q&A - @hiiii](https://hackmd.io/@hiiii/ryOzgaf0a)
3. [iPAS資訊安全工程師中級筆記 - @dkri3c1](https://hackmd.io/@dkri3c1/r1jWTXCtA)
4. [iPAS資訊安全工程師中級筆記 - @Not](https://hackmd.io/@Not/iPASInformationSecuritySpecialist)
5. [iPAS資訊安全工程師-中級-12天準備歷程記錄&考古題資源提供 - @Bad Mind](https://hackmd.io/@7ZcmfE2ETz-ntel2Ma6uTg/ByhWE-qs2)

---
