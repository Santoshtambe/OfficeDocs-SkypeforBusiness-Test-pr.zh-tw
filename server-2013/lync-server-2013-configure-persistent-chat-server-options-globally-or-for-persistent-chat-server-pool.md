﻿---
title: Lync Server 2013：以全域方式設定或針對常設聊天室伺服器集區設定常設聊天室伺服器選項
TOCTitle: 以全域方式設定或針對常設聊天室伺服器集區設定常設聊天室伺服器選項
ms:assetid: 1e8d5245-cd58-4aad-9a1c-35b24189bc40
ms:mtpsurl: https://technet.microsoft.com/zh-tw/library/JJ204731(v=OCS.15)
ms:contentKeyID: 49290288
ms.date: 08/10/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# 在 Lync Server 2013 中以全域方式設定或針對常設聊天室伺服器集區設定常設聊天室伺服器選項

 

_**上次修改主題的時間：** 2012-10-06_

在 Lync Server 2013 控制台中，您可以使用「 常設聊天室」 頁面的 \[ 常設聊天室設定\] 區段 ，以全域進行 常設聊天室設定，並使其套用至所有 Persistent Chat Server 集區或特定的 Persistent Chat Server 集區。

<table>
<thead>
<tr class="header">
<th><img src="images/Gg398811.note(OCS.15).gif" title="note" alt="note" />附註：</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>若要設定和使用 常設聊天室伺服器，必須先使用 拓撲產生器將 常設聊天室伺服器 支援新增至拓撲，然後發布該拓撲。如需詳細資訊，請參閱部署文件中的＜ <a href="lync-server-2013-adding-persistent-chat-server-to-your-deployment.md">在 Lync Server 2013 中將常設聊天室伺服器新增至您的部署</a>＞。</td>
</tr>
</tbody>
</table>


## 設定全域的 常設聊天室選項

1.  使用指派給 CsPersistentChatAdministrator 或 CsAdministrator 角色的使用者帳戶，登入內部部署中的任一部電腦。

2.  從 \[開始\] 功能表選取 Lync Server 控制台或開啟瀏覽器視窗，然後輸入 Admin URL。如需各種 Lync Server 控制台啟動方法的詳細資訊，請參閱＜ [開啟 Lync Server 系統管理工具](lync-server-2013-open-lync-server-administrative-tools.md)＞。
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Gg412908.important(OCS.15).gif" title="important" alt="important" />重要事項：</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>您也可以使用 Windows PowerShell Cmdlet。如需詳細資訊，請參閱部署移轉文件 <a href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">使用 Windows PowerShell Cmdlet 設定常設聊天室伺服器</a>＞。</td>
    </tr>
    </tbody>
    </table>


3.  在左導覽列中，按一下 \[ 常設聊天室\] ，然後按一下 \[ 常設聊天室設定\] 。

4.  在「 常設聊天室設定」 頁面上，按一下 \[新增\] ，然後按一下 \[站台組態\] 。
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Gg412908.important(OCS.15).gif" title="important" alt="important" />重要事項：</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>如果您想要將組態套用至部署在網站中的所有 Persistent Chat Server 集區，請選擇此選項。如果您想要將組態套用至特定的 Persistent Chat Server 集區，請按一下 [集區組態] 。</td>
    </tr>
    </tbody>
    </table>


5.  在 \[選取站台\] 中，選取要為 常設聊天室伺服器 網站組態設定的網站。

6.  在 \[新的 常設聊天室設定\] 中，執行下列動作：
    
      - 在 \[名稱\] 中，指定新組態設定的名稱。依預設，網站名稱已存在。
    
      - 在 \[預設聊天記錄\] 中，定義在第一次要求時，要為每個聊天室處理的聊天訊息數目。此數目預設為 30。這是全域預設值，系統管理員可針對每個類別停用聊天記錄。
        
        <table>
        <thead>
        <tr class="header">
        <th><img src="images/Gg412908.important(OCS.15).gif" title="important" alt="important" />重要事項：</th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td>常設聊天室伺服器 會在記憶體中快取這些訊息，因此如果您增加此數目，將可快取更多訊息。您可以隨時利用搜尋來存取記錄內容。預設數目只會決定最初連線至聊天室所看到的訊息數目上限。</td>
        </tr>
        </tbody>
        </table>
    
      - 在 \[檔案大小上限 (KB)\] 中，選取每個聊天記錄的檔案大小上限。此數目預設為 20 MB (20,000 KB)。這是可以上傳至系統中任何聊天室的檔案大小上限 (依其對應的 \[類別\] 設定來啟用檔案上傳)。
        
        <table>
        <thead>
        <tr class="header">
        <th><img src="images/Gg412908.important(OCS.15).gif" title="important" alt="important" />重要事項：</th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td>此設定會在伺服器上強制執行，因為自訂應用程式或使用 Office Communications Server 2007 R2群組聊天伺服器或 Lync Server 2010 群組聊天的舊版 群組聊天用戶端可以發佈檔案至聊天室。 Lync 2013 用戶端並沒有檔案上傳/下載的功能，所以您若僅有 Lync 2013 部署或 Lync 2013 用戶端，就無法在 常設聊天室伺服器 聊天室中發佈檔案。</td>
        </tr>
        </tbody>
        </table>
    
      - 在 \[參與者更新限制\] ，選取參與者更新的限制。 常設聊天室伺服器 會傳送名冊資訊 (包括哪些使用者連線至聊天室) 給所有參與者，直到連線的使用者數量達到此數目為止。此數目預設為 75。此限制指出給定聊天室的參與者數量上限，超過以後， 常設聊天室伺服器 就會停止將聊天室中有哪些使用者的名冊更新傳送給連線的用戶端。
    
      - (選用) 在 \[聊天室管理 URL\] , 中，選取聊天室管理 URL。這是 Web 聊天室部署的 URL。如果您不需要自訂聊天室管理，而直接使用預設設定，請將此選項留白。設定好此 URL 之後，其就會套用至內部和外部聊天室管理 URL。
        
        如果您要自訂聊天室建立體驗並包含特定商務工作流程，可以使用 常設聊天室伺服器 軟體開發套件 (SDK) 建立自訂聊天室管理解決方案、裝載於某處，然後將 URL 置於此處。此 URL 會下傳至用戶端，因此，當使用者嘗試檢視或建立聊天室時，就會將其導向至您的自訂聊天室管理解決方案。

7.  按一下 \[認可\] 。

## 為特定 Persistent Chat Server 集區設定 常設聊天室選項

1.  使用指派給 CsPersistentChatAdministrator 或 CsAdministrator 角色的使用者帳戶，登入內部部署中的任一部電腦。

2.  從 \[開始\] 功能表中選取 \[ Lync Server 控制台\] 或開啟瀏覽器視窗，然後輸入管理 URL。如需各種 Lync Server 控制台啟動方法的詳細資訊，請參閱＜ [開啟 Lync Server 系統管理工具](lync-server-2013-open-lync-server-administrative-tools.md)＞。
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Gg412908.important(OCS.15).gif" title="important" alt="important" />重要事項：</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>您也可以使用 Windows PowerShell Cmdlet。如需詳細資訊，請參閱部署移轉文件 <a href="configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md">使用 Windows PowerShell Cmdlet 設定常設聊天室伺服器</a>＞。</td>
    </tr>
    </tbody>
    </table>


3.  在左導覽列中，按一下 \[ 常設聊天室\] ，然後按一下 \[ 常設聊天室設定\] 。

4.  在「 常設聊天室設定」 頁面上，按一下 \[新增\] ，然後按一下 \[集區組態\] 。

5.  在 \[選取服務\] 中，選取與所要設定之 Persistent Chat Server 集區相關聯的服務。

6.  在 \[新的 常設聊天室設定\] 中，執行下列動作：
    
      - 在 \[名稱\] 中，指定新組態設定的名稱。依預設，網站集區名稱已存在。
    
      - 在 \[預設聊天記錄\] 中，定義在第一次要求時，要為每個聊天室處理的聊天訊息數目。此數目預設為 30。這是全域預設值，系統管理員可針對每個類別停用聊天記錄。
        
        <table>
        <thead>
        <tr class="header">
        <th><img src="images/Gg412908.important(OCS.15).gif" title="important" alt="important" />重要事項：</th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td>常設聊天室伺服器 會在記憶體中快取這些訊息，因此如果您增加此數目，將可快取更多訊息。您可以隨時利用搜尋來存取記錄內容。預設數目只會決定最初連線至聊天室所看到的訊息數目上限。</td>
        </tr>
        </tbody>
        </table>
    
      - 在 \[檔案大小上限 (KB)\] 中，選取每個聊天記錄的檔案大小上限。此數目預設為 20 MB (20,000 KB)。這是可以上傳至系統中任何聊天室的檔案大小上限 (依其對應的 \[類別\] 設定來啟用檔案上傳)。
        
        <table>
        <thead>
        <tr class="header">
        <th><img src="images/Gg412908.important(OCS.15).gif" title="important" alt="important" />重要事項：</th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td>此設定會在伺服器上強制執行，因為自訂應用程式或舊版 群組聊天用戶端 ( Office Communications Server 2007 R2群組聊天伺服器或 Lync Server 2010 群組聊天) 可以發佈檔案至聊天室。 Lync 2013 用戶端並沒有檔案上傳/下載的功能，所以您若僅有 Lync 2013 部署或 Lync 2013 用戶端，就無法在 常設聊天室伺服器 聊天室中發佈檔案。</td>
        </tr>
        </tbody>
        </table>
    
      - 在 \[參與者更新限制\] ，選取參與者更新的限制。 常設聊天室伺服器 會傳送名冊資訊 (包括哪些使用者連線至聊天室) 給所有參與者，直到連線的使用者數量達到此數目為止。此數目預設為 75。此限制指出給定聊天室的參與者數量上限，超過以後， 常設聊天室伺服器 就會停止將聊天室中有哪些使用者的名冊更新傳送給連線的用戶端。
    
      - 在 \[聊天室管理 URL\] 中，選取聊天室管理 URL。這是 Web 型聊天室管理部署的 URL。如果您不需要自訂聊天室管理，而只要使用預設設定，請將此選項保留空白。
        
        如果您要自訂聊天室建立體驗並包含特定商務工作流程，可以使用 常設聊天室伺服器 軟體開發套件 (SDK) 建立自訂聊天室管理解決方案、裝載於某處，並將 URL 置於此處。此 URL 會接著傳送至下游用戶端，因此，當使用者嘗試檢視/建立聊天室時，則會將使用者其導向至您的自訂聊天室管理解決方案。

7.  按一下 \[認可\] 。

