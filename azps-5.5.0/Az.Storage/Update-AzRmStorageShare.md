---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 0f2d86fca85364fa71d50c05d83f278bd997252e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209085"
---
# <span data-ttu-id="34919-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="34919-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="34919-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34919-102">SYNOPSIS</span></span>
<span data-ttu-id="34919-103">Storage 파일 공유를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="34919-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="34919-104">구문</span><span class="sxs-lookup"><span data-stu-id="34919-104">SYNTAX</span></span>

### <span data-ttu-id="34919-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="34919-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34919-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="34919-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34919-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="34919-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34919-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="34919-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34919-109">설명</span><span class="sxs-lookup"><span data-stu-id="34919-109">DESCRIPTION</span></span>
<span data-ttu-id="34919-110">**New-AzRmStorageShare** cmdlet은 Storage 파일 공유를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="34919-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="34919-111">예제</span><span class="sxs-lookup"><span data-stu-id="34919-111">EXAMPLES</span></span>

### <span data-ttu-id="34919-112">예제 1: Storage 파일 공유의 메타데이터를 수정하고 저장소 계정 이름 및 공유 이름으로 할당량 공유</span><span class="sxs-lookup"><span data-stu-id="34919-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
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

<span data-ttu-id="34919-113">이 명령은 Storage 파일 공유의 메타데이터를 수정하고 저장소 계정 이름 및 공유 이름으로 할당량 공유하고 반환된 파일 공유 개체와 함께 수정 결과를 보여 주며,</span><span class="sxs-lookup"><span data-stu-id="34919-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="34919-114">예제 2: Storage 계정 개체 및 공유 이름을 사용하여 Storage 파일 공유의 메타데이터 수정</span><span class="sxs-lookup"><span data-stu-id="34919-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="34919-115">이 명령은 Storage 계정 개체 및 공유 이름을 사용하여 Storage 파일 공유의 메타데이터를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="34919-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="34919-116">예제 3: 파이프라인이 있는 Storage 계정의 모든 Storage 파일 공유에 대한 공유 할당량 수정</span><span class="sxs-lookup"><span data-stu-id="34919-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="34919-117">이 명령은 파이프라인이 있는 Storage 계정의 모든 Storage 파일 공유에 대해 공유 할당량(5000 GiB)을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="34919-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

### <span data-ttu-id="34919-118">예제 4: 액세스 권한을 쿨로 설정하여 Storage 파일 공유 수정</span><span class="sxs-lookup"><span data-stu-id="34919-118">Example 4: Modify a Storage file share with accesstier as Cool</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Cool

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Cool
```

<span data-ttu-id="34919-119">이 명령은 Accesstier를 쿨로 사용하여 Storage 파일 공유를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="34919-119">This command modifies a Storage file share with accesstier as Cool.</span></span>

## <span data-ttu-id="34919-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34919-120">PARAMETERS</span></span>

### <span data-ttu-id="34919-121">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="34919-121">-AccessTier</span></span>
<span data-ttu-id="34919-122">특정 공유에 대한 액세스 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="34919-122">Access tier for specific share.</span></span> <span data-ttu-id="34919-123">StorageV2 계정은 TransactionOptimized(기본값), 핫 및 쿨 중 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34919-123">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="34919-124">FileStorage 계정은 프리미엄을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34919-124">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="34919-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34919-125">-DefaultProfile</span></span>
<span data-ttu-id="34919-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34919-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34919-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34919-127">-InputObject</span></span>
<span data-ttu-id="34919-128">저장소 공유 개체</span><span class="sxs-lookup"><span data-stu-id="34919-128">Storage Share object</span></span>

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

### <span data-ttu-id="34919-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="34919-129">-Metadata</span></span>
<span data-ttu-id="34919-130">메타데이터 공유</span><span class="sxs-lookup"><span data-stu-id="34919-130">Share Metadata</span></span>

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

### <span data-ttu-id="34919-131">-Name</span><span class="sxs-lookup"><span data-stu-id="34919-131">-Name</span></span>
<span data-ttu-id="34919-132">공유 이름</span><span class="sxs-lookup"><span data-stu-id="34919-132">Share Name</span></span>

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

### <span data-ttu-id="34919-133">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="34919-133">-QuotaGiB</span></span>
<span data-ttu-id="34919-134">Gibibyte에서 할당량 공유</span><span class="sxs-lookup"><span data-stu-id="34919-134">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="34919-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34919-135">-ResourceGroupName</span></span>
<span data-ttu-id="34919-136">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34919-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="34919-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34919-137">-ResourceId</span></span>
<span data-ttu-id="34919-138">파일 공유 리소스 ID를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="34919-138">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="34919-139">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="34919-139">-StorageAccount</span></span>
<span data-ttu-id="34919-140">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="34919-140">Storage account object</span></span>

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

### <span data-ttu-id="34919-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="34919-141">-StorageAccountName</span></span>
<span data-ttu-id="34919-142">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34919-142">Storage Account Name.</span></span>

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

### <span data-ttu-id="34919-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34919-143">-Confirm</span></span>
<span data-ttu-id="34919-144">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="34919-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34919-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34919-145">-WhatIf</span></span>
<span data-ttu-id="34919-146">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="34919-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34919-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34919-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34919-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34919-148">CommonParameters</span></span>
<span data-ttu-id="34919-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="34919-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34919-150">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="34919-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34919-151">입력</span><span class="sxs-lookup"><span data-stu-id="34919-151">INPUTS</span></span>

### <span data-ttu-id="34919-152">System.String</span><span class="sxs-lookup"><span data-stu-id="34919-152">System.String</span></span>

### <span data-ttu-id="34919-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="34919-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="34919-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="34919-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="34919-155">출력</span><span class="sxs-lookup"><span data-stu-id="34919-155">OUTPUTS</span></span>

### <span data-ttu-id="34919-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="34919-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="34919-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="34919-157">NOTES</span></span>

## <span data-ttu-id="34919-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34919-158">RELATED LINKS</span></span>
