---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 70d3c8c435a88b4f0f968d1519efd9af6d9907e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494661"
---
# <span data-ttu-id="cd346-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cd346-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="cd346-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd346-102">SYNOPSIS</span></span>
<span data-ttu-id="cd346-103">삭제된 파일 공유를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="cd346-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="cd346-104">구문</span><span class="sxs-lookup"><span data-stu-id="cd346-104">SYNTAX</span></span>

### <span data-ttu-id="cd346-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="cd346-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd346-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="cd346-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd346-107">ShareObject</span><span class="sxs-lookup"><span data-stu-id="cd346-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd346-108">설명</span><span class="sxs-lookup"><span data-stu-id="cd346-108">DESCRIPTION</span></span>
<span data-ttu-id="cd346-109">**Restore-AzRmStorageShare** cmdlet은 공유 소프트 삭제를 사용하도록 설정된 경우 유효한 보존 기간 내에 삭제된 파일 공유를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="cd346-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="cd346-110">예제</span><span class="sxs-lookup"><span data-stu-id="cd346-110">EXAMPLES</span></span>

### <span data-ttu-id="cd346-111">예제 1: 공유 제거 및 복원</span><span class="sxs-lookup"><span data-stu-id="cd346-111">Example 1: Remove and restore a share</span></span>
```powershell
PS C:\> Remove-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -Force

PS C:\> Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6                

PS C:\> Restore-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -DeletedShareVersion 01D61FD1FC5498B6

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   100
```

<span data-ttu-id="cd346-112">이 명령은 먼저 파일 공유를 삭제한 다음 공유를 나열하고 삭제된 공유 버전을 보고 마지막으로 일반 공유로 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="cd346-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="cd346-113">공유를 삭제하기 전에 Update-AzStorageFileServiceProperty를 통해 공유 소프트 삭제를 사용하도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd346-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="cd346-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd346-114">PARAMETERS</span></span>

### <span data-ttu-id="cd346-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd346-115">-DefaultProfile</span></span>
<span data-ttu-id="cd346-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd346-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd346-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="cd346-117">-DeletedShareVersion</span></span>
<span data-ttu-id="cd346-118">삭제된 공유 버전에서 복원됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd346-118">Deleted Share Version, which will be restored from.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd346-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd346-119">-InputObject</span></span>
<span data-ttu-id="cd346-120">삭제된 공유 개체</span><span class="sxs-lookup"><span data-stu-id="cd346-120">Deleted Share object</span></span>

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

### <span data-ttu-id="cd346-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cd346-121">-Name</span></span>
<span data-ttu-id="cd346-122">삭제된 공유 이름( 복원됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd346-122">Deleted Share Name, which will be restored.</span></span>

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

### <span data-ttu-id="cd346-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd346-123">-ResourceGroupName</span></span>
<span data-ttu-id="cd346-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd346-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="cd346-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd346-125">-StorageAccount</span></span>
<span data-ttu-id="cd346-126">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="cd346-126">Storage account object</span></span>

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

### <span data-ttu-id="cd346-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cd346-127">-StorageAccountName</span></span>
<span data-ttu-id="cd346-128">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd346-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="cd346-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd346-129">-Confirm</span></span>
<span data-ttu-id="cd346-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd346-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd346-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd346-131">-WhatIf</span></span>
<span data-ttu-id="cd346-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cd346-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd346-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd346-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd346-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd346-134">CommonParameters</span></span>
<span data-ttu-id="cd346-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cd346-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd346-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cd346-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd346-137">입력</span><span class="sxs-lookup"><span data-stu-id="cd346-137">INPUTS</span></span>

### <span data-ttu-id="cd346-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd346-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="cd346-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="cd346-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="cd346-140">출력</span><span class="sxs-lookup"><span data-stu-id="cd346-140">OUTPUTS</span></span>

### <span data-ttu-id="cd346-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="cd346-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="cd346-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cd346-142">NOTES</span></span>

## <span data-ttu-id="cd346-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd346-143">RELATED LINKS</span></span>
