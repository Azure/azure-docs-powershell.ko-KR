---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 7612b323600b2f076c30225994d6e475d66c01ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973307"
---
# <span data-ttu-id="bda3a-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bda3a-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="bda3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bda3a-102">SYNOPSIS</span></span>
<span data-ttu-id="bda3a-103">Storage 파일 공유를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3a-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="bda3a-104">구문</span><span class="sxs-lookup"><span data-stu-id="bda3a-104">SYNTAX</span></span>

### <span data-ttu-id="bda3a-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="bda3a-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bda3a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="bda3a-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bda3a-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="bda3a-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bda3a-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="bda3a-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bda3a-109">설명</span><span class="sxs-lookup"><span data-stu-id="bda3a-109">DESCRIPTION</span></span>
<span data-ttu-id="bda3a-110">**New-AzRmStorageShare** cmdlet은 Storage 파일 공유를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3a-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="bda3a-111">예제</span><span class="sxs-lookup"><span data-stu-id="bda3a-111">EXAMPLES</span></span>

### <span data-ttu-id="bda3a-112">예제 1: Storage 파일 공유의 메타데이터를 수정하고 저장소 계정 이름 및 공유 이름으로 할당량 공유</span><span class="sxs-lookup"><span data-stu-id="bda3a-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  200

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="bda3a-113">이 명령은 Storage 파일 공유의 메타데이터를 수정하고 저장소 계정 이름 및 공유 이름과 할당량 공유를 공유하고 반환된 파일 공유 개체로 수정 결과를 보여 니다.</span><span class="sxs-lookup"><span data-stu-id="bda3a-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="bda3a-114">예제 2: Storage 계정 개체 및 공유 이름으로 Storage 파일 공유의 메타데이터 수정</span><span class="sxs-lookup"><span data-stu-id="bda3a-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="bda3a-115">이 명령은 Storage 계정 개체 및 공유 이름으로 Storage 파일 공유의 메타데이터를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3a-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="bda3a-116">예제 3: 파이프라인이 있는 Storage 계정의 모든 Storage 파일 공유에 대한 공유 할당량 수정</span><span class="sxs-lookup"><span data-stu-id="bda3a-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="bda3a-117">이 명령은 파이프라인이 있는 Storage 계정의 모든 Storage 파일 공유에 대해 공유 할당량 5000 GiB로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3a-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

### <span data-ttu-id="bda3a-118">예제 4: Accesstier를 Cool으로 저장소 파일 공유 수정</span><span class="sxs-lookup"><span data-stu-id="bda3a-118">Example 4: Modify a Storage file share with accesstier as Cool</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Cool

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Cool
```

<span data-ttu-id="bda3a-119">이 명령은 Accesstier를 Cool으로 사용하여 Storage 파일 공유를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3a-119">This command modifies a Storage file share with accesstier as Cool.</span></span>

## <span data-ttu-id="bda3a-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bda3a-120">PARAMETERS</span></span>

### <span data-ttu-id="bda3a-121">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="bda3a-121">-AccessTier</span></span>
<span data-ttu-id="bda3a-122">특정 공유에 대한 액세스 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="bda3a-122">Access tier for specific share.</span></span> <span data-ttu-id="bda3a-123">StorageV2 계정은 TransactionOptimized(기본값), 핫 및 쿨 중 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bda3a-123">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="bda3a-124">FileStorage 계정은 Premium을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bda3a-124">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="bda3a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bda3a-125">-DefaultProfile</span></span>
<span data-ttu-id="bda3a-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bda3a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bda3a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bda3a-127">-InputObject</span></span>
<span data-ttu-id="bda3a-128">Storage 공유 개체</span><span class="sxs-lookup"><span data-stu-id="bda3a-128">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bda3a-129">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="bda3a-129">-Metadata</span></span>
<span data-ttu-id="bda3a-130">메타데이터 공유</span><span class="sxs-lookup"><span data-stu-id="bda3a-130">Share Metadata</span></span>

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

### <span data-ttu-id="bda3a-131">-Name</span><span class="sxs-lookup"><span data-stu-id="bda3a-131">-Name</span></span>
<span data-ttu-id="bda3a-132">이름 공유</span><span class="sxs-lookup"><span data-stu-id="bda3a-132">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bda3a-133">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="bda3a-133">-QuotaGiB</span></span>
<span data-ttu-id="bda3a-134">Gibibyte에서 할당량 공유</span><span class="sxs-lookup"><span data-stu-id="bda3a-134">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="bda3a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bda3a-135">-ResourceGroupName</span></span>
<span data-ttu-id="bda3a-136">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bda3a-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="bda3a-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bda3a-137">-ResourceId</span></span>
<span data-ttu-id="bda3a-138">파일 공유 리소스 ID를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3a-138">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bda3a-139">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="bda3a-139">-StorageAccount</span></span>
<span data-ttu-id="bda3a-140">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="bda3a-140">Storage account object</span></span>

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

### <span data-ttu-id="bda3a-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bda3a-141">-StorageAccountName</span></span>
<span data-ttu-id="bda3a-142">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bda3a-142">Storage Account Name.</span></span>

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

### <span data-ttu-id="bda3a-143">-확인</span><span class="sxs-lookup"><span data-stu-id="bda3a-143">-Confirm</span></span>
<span data-ttu-id="bda3a-144">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bda3a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bda3a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bda3a-145">-WhatIf</span></span>
<span data-ttu-id="bda3a-146">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bda3a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bda3a-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bda3a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bda3a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bda3a-148">CommonParameters</span></span>
<span data-ttu-id="bda3a-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bda3a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bda3a-150">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bda3a-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bda3a-151">입력</span><span class="sxs-lookup"><span data-stu-id="bda3a-151">INPUTS</span></span>

### <span data-ttu-id="bda3a-152">System.String</span><span class="sxs-lookup"><span data-stu-id="bda3a-152">System.String</span></span>

### <span data-ttu-id="bda3a-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bda3a-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="bda3a-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="bda3a-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="bda3a-155">출력</span><span class="sxs-lookup"><span data-stu-id="bda3a-155">OUTPUTS</span></span>

### <span data-ttu-id="bda3a-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="bda3a-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="bda3a-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bda3a-157">NOTES</span></span>

## <span data-ttu-id="bda3a-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bda3a-158">RELATED LINKS</span></span>
