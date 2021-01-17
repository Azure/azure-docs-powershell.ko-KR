---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 4dc3914e4a8bc9113dd16ab431db53ddcf00ab5a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492086"
---
# <span data-ttu-id="c1a9e-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="c1a9e-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="c1a9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1a9e-102">SYNOPSIS</span></span>
<span data-ttu-id="c1a9e-103">Storage 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1a9e-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="c1a9e-104">구문</span><span class="sxs-lookup"><span data-stu-id="c1a9e-104">SYNTAX</span></span>

### <span data-ttu-id="c1a9e-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c1a9e-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1a9e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c1a9e-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1a9e-107">설명</span><span class="sxs-lookup"><span data-stu-id="c1a9e-107">DESCRIPTION</span></span>
<span data-ttu-id="c1a9e-108">**New-AzRmStorageShare** cmdlet은 Storage 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1a9e-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="c1a9e-109">예제</span><span class="sxs-lookup"><span data-stu-id="c1a9e-109">EXAMPLES</span></span>

### <span data-ttu-id="c1a9e-110">예제 1: Storage 계정 이름으로 Storage 파일 공유를 만들고 메타데이터를 사용하여 공유 이름을 만들고 할당량은 100 GiB로 공유합니다.</span><span class="sxs-lookup"><span data-stu-id="c1a9e-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="c1a9e-111">이 명령은 메타데이터를 사용하여 Storage 파일 공유를 만들고 할당량은 100 GiB로 공유합니다.</span><span class="sxs-lookup"><span data-stu-id="c1a9e-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="c1a9e-112">예제 2: Storage 계정 개체를 사용하여 Storage 파일 공유 만들기</span><span class="sxs-lookup"><span data-stu-id="c1a9e-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="c1a9e-113">이 명령은 Storage 계정 개체 및 공유 이름을 사용하여 Storage 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1a9e-113">This command creates a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="c1a9e-114">예제 3: Accesstier를 핫으로 사용하여 Storage 파일 공유 만들기</span><span class="sxs-lookup"><span data-stu-id="c1a9e-114">Example 3: Create a Storage file share with accesstier as Hot</span></span>
```
PS C:\>$share = New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Hot

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Hot
```

<span data-ttu-id="c1a9e-115">이 명령은 Accesstier를 핫으로 사용하여 Storage 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1a9e-115">This command creates a Storage file share with accesstier as Hot.</span></span>

## <span data-ttu-id="c1a9e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1a9e-116">PARAMETERS</span></span>

### <span data-ttu-id="c1a9e-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="c1a9e-117">-AccessTier</span></span>
<span data-ttu-id="c1a9e-118">특정 공유에 대한 액세스 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="c1a9e-118">Access tier for specific share.</span></span> <span data-ttu-id="c1a9e-119">StorageV2 계정은 TransactionOptimized(기본값), 핫 및 쿨 중 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1a9e-119">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="c1a9e-120">FileStorage 계정은 프리미엄을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1a9e-120">FileStorage account can choose Premium.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TransactionOptimized, Premium, Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a9e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1a9e-121">-DefaultProfile</span></span>
<span data-ttu-id="c1a9e-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1a9e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a9e-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c1a9e-123">-Metadata</span></span>
<span data-ttu-id="c1a9e-124">메타데이터 공유</span><span class="sxs-lookup"><span data-stu-id="c1a9e-124">Share Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a9e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c1a9e-125">-Name</span></span>
<span data-ttu-id="c1a9e-126">Azure 파일 공유 이름</span><span class="sxs-lookup"><span data-stu-id="c1a9e-126">Azure File share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a9e-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="c1a9e-127">-QuotaGiB</span></span>
<span data-ttu-id="c1a9e-128">Gibibyte에서 할당량 공유</span><span class="sxs-lookup"><span data-stu-id="c1a9e-128">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Quota

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a9e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1a9e-129">-ResourceGroupName</span></span>
<span data-ttu-id="c1a9e-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1a9e-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a9e-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1a9e-131">-StorageAccount</span></span>
<span data-ttu-id="c1a9e-132">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="c1a9e-132">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1a9e-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c1a9e-133">-StorageAccountName</span></span>
<span data-ttu-id="c1a9e-134">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1a9e-134">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a9e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1a9e-135">-Confirm</span></span>
<span data-ttu-id="c1a9e-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1a9e-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a9e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1a9e-137">-WhatIf</span></span>
<span data-ttu-id="c1a9e-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c1a9e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1a9e-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1a9e-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1a9e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a9e-140">CommonParameters</span></span>
<span data-ttu-id="c1a9e-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c1a9e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1a9e-142">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c1a9e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a9e-143">입력</span><span class="sxs-lookup"><span data-stu-id="c1a9e-143">INPUTS</span></span>

### <span data-ttu-id="c1a9e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c1a9e-144">System.String</span></span>

### <span data-ttu-id="c1a9e-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1a9e-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="c1a9e-146">출력</span><span class="sxs-lookup"><span data-stu-id="c1a9e-146">OUTPUTS</span></span>

### <span data-ttu-id="c1a9e-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="c1a9e-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="c1a9e-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c1a9e-148">NOTES</span></span>

## <span data-ttu-id="c1a9e-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1a9e-149">RELATED LINKS</span></span>
