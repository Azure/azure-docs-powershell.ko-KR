---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: dcb4819a3ac13056acd1b51dde2ee67774d51693
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994751"
---
# <span data-ttu-id="d8d25-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="d8d25-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="d8d25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8d25-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d25-103">Storage 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8d25-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="d8d25-104">구문</span><span class="sxs-lookup"><span data-stu-id="d8d25-104">SYNTAX</span></span>

### <span data-ttu-id="d8d25-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="d8d25-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8d25-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d8d25-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8d25-107">설명</span><span class="sxs-lookup"><span data-stu-id="d8d25-107">DESCRIPTION</span></span>
<span data-ttu-id="d8d25-108">**New-AzRmStorageShare** cmdlet은 Storage 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8d25-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="d8d25-109">예제</span><span class="sxs-lookup"><span data-stu-id="d8d25-109">EXAMPLES</span></span>

### <span data-ttu-id="d8d25-110">예제 1: 메타데이터를 사용하여 Storage 계정 이름 및 공유 이름으로 Storage 파일 공유를 만들고 할당량은 100 GiB로 공유합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d25-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="d8d25-111">이 명령은 메타데이터와 함께 Storage 파일 공유를 만들고 할당량은 100 GiB로 공유합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d25-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="d8d25-112">예제 2: Storage 계정 개체와 저장소 파일 공유 만들기</span><span class="sxs-lookup"><span data-stu-id="d8d25-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="d8d25-113">이 명령은 Storage 계정 개체와 저장소 파일 공유를 만들고 이름을 공유합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d25-113">This command creates a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="d8d25-114">예제 3: Accesstier를 핫으로 사용하여 Storage 파일 공유 만들기</span><span class="sxs-lookup"><span data-stu-id="d8d25-114">Example 3: Create a Storage file share with accesstier as Hot</span></span>
```
PS C:\>$share = New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Hot

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Hot
```

<span data-ttu-id="d8d25-115">이 명령은 Accesstier를 Hot으로 사용하여 Storage 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d8d25-115">This command creates a Storage file share with accesstier as Hot.</span></span>

## <span data-ttu-id="d8d25-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d8d25-116">PARAMETERS</span></span>

### <span data-ttu-id="d8d25-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="d8d25-117">-AccessTier</span></span>
<span data-ttu-id="d8d25-118">특정 공유에 대한 액세스 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="d8d25-118">Access tier for specific share.</span></span> <span data-ttu-id="d8d25-119">StorageV2 계정은 TransactionOptimized(기본값), 핫 및 쿨 중 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8d25-119">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="d8d25-120">FileStorage 계정은 Premium을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8d25-120">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="d8d25-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d25-121">-DefaultProfile</span></span>
<span data-ttu-id="d8d25-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8d25-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8d25-123">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="d8d25-123">-Metadata</span></span>
<span data-ttu-id="d8d25-124">메타데이터 공유</span><span class="sxs-lookup"><span data-stu-id="d8d25-124">Share Metadata</span></span>

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

### <span data-ttu-id="d8d25-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d8d25-125">-Name</span></span>
<span data-ttu-id="d8d25-126">Azure 파일 공유 이름</span><span class="sxs-lookup"><span data-stu-id="d8d25-126">Azure File share name</span></span>

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

### <span data-ttu-id="d8d25-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="d8d25-127">-QuotaGiB</span></span>
<span data-ttu-id="d8d25-128">Gibibyte에서 할당량 공유</span><span class="sxs-lookup"><span data-stu-id="d8d25-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="d8d25-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d25-129">-ResourceGroupName</span></span>
<span data-ttu-id="d8d25-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8d25-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="d8d25-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d8d25-131">-StorageAccount</span></span>
<span data-ttu-id="d8d25-132">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="d8d25-132">Storage account object</span></span>

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

### <span data-ttu-id="d8d25-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d8d25-133">-StorageAccountName</span></span>
<span data-ttu-id="d8d25-134">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8d25-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="d8d25-135">-확인</span><span class="sxs-lookup"><span data-stu-id="d8d25-135">-Confirm</span></span>
<span data-ttu-id="d8d25-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8d25-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8d25-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8d25-137">-WhatIf</span></span>
<span data-ttu-id="d8d25-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d8d25-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8d25-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8d25-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8d25-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d25-140">CommonParameters</span></span>
<span data-ttu-id="d8d25-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d25-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d25-142">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d8d25-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d25-143">입력</span><span class="sxs-lookup"><span data-stu-id="d8d25-143">INPUTS</span></span>

### <span data-ttu-id="d8d25-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d8d25-144">System.String</span></span>

### <span data-ttu-id="d8d25-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d8d25-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="d8d25-146">출력</span><span class="sxs-lookup"><span data-stu-id="d8d25-146">OUTPUTS</span></span>

### <span data-ttu-id="d8d25-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="d8d25-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="d8d25-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d8d25-148">NOTES</span></span>

## <span data-ttu-id="d8d25-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8d25-149">RELATED LINKS</span></span>
