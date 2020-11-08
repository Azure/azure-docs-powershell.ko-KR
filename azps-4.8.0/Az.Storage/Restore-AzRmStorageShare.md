---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 70d3c8c435a88b4f0f968d1519efd9af6d9907e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047507"
---
# <span data-ttu-id="886cf-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="886cf-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="886cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="886cf-102">SYNOPSIS</span></span>
<span data-ttu-id="886cf-103">삭제 된 파일 공유를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="886cf-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="886cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="886cf-104">SYNTAX</span></span>

### <span data-ttu-id="886cf-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="886cf-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="886cf-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="886cf-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="886cf-107">ShareObject</span><span class="sxs-lookup"><span data-stu-id="886cf-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="886cf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="886cf-108">DESCRIPTION</span></span>
<span data-ttu-id="886cf-109">**AzRmStorageShare** cmdlet은 공유 일시 삭제를 사용 하는 경우 유효 보존 일 내에 삭제 된 파일 공유를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="886cf-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="886cf-110">예제의</span><span class="sxs-lookup"><span data-stu-id="886cf-110">EXAMPLES</span></span>

### <span data-ttu-id="886cf-111">예제 1: 공유 제거 및 복원</span><span class="sxs-lookup"><span data-stu-id="886cf-111">Example 1: Remove and restore a share</span></span>
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

<span data-ttu-id="886cf-112">이 명령은 먼저 파일 공유를 삭제 한 다음 공유를 나열 하 고 삭제 된 공유 버전을 확인 한 후 마지막으로 다시 일반 공유로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="886cf-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="886cf-113">공유를 삭제 하기 전에 업데이트-AzStorageFileServiceProperty를 사용 하 여 공유 일시 삭제를 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="886cf-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="886cf-114">변수</span><span class="sxs-lookup"><span data-stu-id="886cf-114">PARAMETERS</span></span>

### <span data-ttu-id="886cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="886cf-115">-DefaultProfile</span></span>
<span data-ttu-id="886cf-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="886cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="886cf-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="886cf-117">-DeletedShareVersion</span></span>
<span data-ttu-id="886cf-118">이 (가) 복원 된 공유 버전을 삭제 했습니다.</span><span class="sxs-lookup"><span data-stu-id="886cf-118">Deleted Share Version, which will be restored from.</span></span>

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

### <span data-ttu-id="886cf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="886cf-119">-InputObject</span></span>
<span data-ttu-id="886cf-120">공유 개체 삭제 됨</span><span class="sxs-lookup"><span data-stu-id="886cf-120">Deleted Share object</span></span>

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

### <span data-ttu-id="886cf-121">-이름</span><span class="sxs-lookup"><span data-stu-id="886cf-121">-Name</span></span>
<span data-ttu-id="886cf-122">공유 이름 (삭제 됨)이 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="886cf-122">Deleted Share Name, which will be restored.</span></span>

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

### <span data-ttu-id="886cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="886cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="886cf-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="886cf-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="886cf-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="886cf-125">-StorageAccount</span></span>
<span data-ttu-id="886cf-126">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="886cf-126">Storage account object</span></span>

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

### <span data-ttu-id="886cf-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="886cf-127">-StorageAccountName</span></span>
<span data-ttu-id="886cf-128">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="886cf-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="886cf-129">-확인</span><span class="sxs-lookup"><span data-stu-id="886cf-129">-Confirm</span></span>
<span data-ttu-id="886cf-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="886cf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="886cf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="886cf-131">-WhatIf</span></span>
<span data-ttu-id="886cf-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="886cf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="886cf-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="886cf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="886cf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="886cf-134">CommonParameters</span></span>
<span data-ttu-id="886cf-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="886cf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="886cf-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="886cf-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="886cf-137">입력</span><span class="sxs-lookup"><span data-stu-id="886cf-137">INPUTS</span></span>

### <span data-ttu-id="886cf-138">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="886cf-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="886cf-139">Microsoft. i. m a i 공유.</span><span class="sxs-lookup"><span data-stu-id="886cf-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="886cf-140">출력</span><span class="sxs-lookup"><span data-stu-id="886cf-140">OUTPUTS</span></span>

### <span data-ttu-id="886cf-141">Microsoft. i. m a i 공유.</span><span class="sxs-lookup"><span data-stu-id="886cf-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="886cf-142">상속자</span><span class="sxs-lookup"><span data-stu-id="886cf-142">NOTES</span></span>

## <span data-ttu-id="886cf-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="886cf-143">RELATED LINKS</span></span>
