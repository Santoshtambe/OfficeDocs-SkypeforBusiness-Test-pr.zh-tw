﻿---
title: 從 Office Communications Server 2007 R2 移轉至 Lync Server 2013
TOCTitle: 從 Office Communications Server 2007 R2 移轉至 Lync Server 2013
ms:assetid: f3fa4f5f-e9a2-4fb7-a12d-20f04173e697
ms:mtpsurl: https://technet.microsoft.com/zh-tw/library/JJ205375(v=OCS.15)
ms:contentKeyID: 49292807
ms.date: 08/24/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# 從 Office Communications Server 2007 R2 移轉至 Lync Server 2013

 

_**上次修改主題的時間：** 2012-10-19_

本節的主題將逐步引導您進行從 Office Communications Server 2007 R2 移轉至 Lync Server 2013 的程序。

<table>
<thead>
<tr class="header">
<th><img src="images/Gg412908.important(OCS.15).gif" title="important" alt="important" />重要事項：</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>本文件說明完成移轉過程中每項階段所需的一般步驟。本文件並不會說明每項可能的舊式部署拓撲或是每種可能的移轉情況。因此，視您部署之不同，您可能不需要執行所述的每項步驟，或是有可能會需要執行額外的步驟。本文件也同時提供各式驗證步驟的範例。提供這些驗證步驟有助於您了解要查看哪些內容，以確認進行移轉的過程中，每個階段都已順利完成。請為您專屬的移轉處理程序修改這些驗證步驟。</td>
</tr>
</tbody>
</table>


本指南所提供的資訊旨在升級現有部署，並不會說明如何變更現有拓撲。本指南不包括新功能的實作。當詳細的程序記載於他處時，本指南將會引導您移至適當的文件或文件章節。

本文件定義下表所列之詞彙。

  - *移轉*   
    將實際執行的部署從前版 Office Communications Server 2007 R2 移至 Lync Server 2013。

<!-- end list -->

  - *升級*   
    在伺服器上或在用戶端電腦上安裝較新版的軟體。

<!-- end list -->

  - *共存*   
    移轉期間所存在的暫時環境，某些功能會已移轉至 Lync Server 2013 而其他功能則仍停留在前版 Office Communications Server 2007 R2 中。

<!-- end list -->

  - *互通性*   
    共存期間順利運作您部署的能力。

## 本節內容

  - [開始移轉之前](before-you-begin-the-migration_1.md)

  - [移轉階段](migration-phases_1.md)

  - [第 1 階段：規劃從 Office Communications Server 2007 R2 移轉](phase-1-plan-your-migration-from-office-communications-server-2007-r2.md)

  - [第 2 階段：準備移轉](phase-2-prepare-for-migration_1.md)

  - [第 3 階段：部署 Lync Server 2013 試驗集區](phase-3-deploy-lync-server-2013-pilot-pool_1.md)

  - [第 4 階段：合併拓撲](phase-4-merge-topologies.md)

  - [第 5 階段：設定試驗集區](phase-5-configure-the-pilot-pool.md)

  - [第 6 階段：將使用者移至試驗集區](phase-6-move-users-to-the-pilot-pool.md)

  - [第 7 階段：將 Lync Server 2013 Edge Server 新增至試驗集區](phase-7-add-lync-server-2013-edge-server-to-pilot-pool.md)

  - [第 8 階段：從試驗部署到實際執行](phase-8-move-from-pilot-deployment-into-production.md)

  - [第 9 階段：完成移轉後工作](phase-9-complete-post-migration-tasks.md)

  - [第 10 階段：解除委任舊版網站](phase-10-decommission-legacy-site.md)

