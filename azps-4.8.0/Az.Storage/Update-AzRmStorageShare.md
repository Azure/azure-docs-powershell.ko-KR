---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 9c5ff85ef608f623187d9132eea8af0f5da6a164
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212042"
---
# <span data-ttu-id="56724-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="56724-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="56724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56724-102">SYNOPSIS</span></span>
<span data-ttu-id="56724-103">저장소 파일 공유를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56724-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="56724-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56724-104">SYNTAX</span></span>

### <span data-ttu-id="56724-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="56724-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56724-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="56724-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56724-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="56724-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56724-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="56724-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56724-109">설명은</span><span class="sxs-lookup"><span data-stu-id="56724-109">DESCRIPTION</span></span>
<span data-ttu-id="56724-110">**새 AzRmStorageShare** Cmdlet은 저장소 파일 공유를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56724-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="56724-111">예제의</span><span class="sxs-lookup"><span data-stu-id="56724-111">EXAMPLES</span></span>

### <span data-ttu-id="56724-112">예제 1: 저장소 파일 공유의 메타 데이터를 수정 하 고 저장소 계정 이름과 공유 이름을 사용 하 여 할당량 공유</span><span class="sxs-lookup"><span data-stu-id="56724-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
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

<span data-ttu-id="56724-113">이 명령은 저장소 파일 공유의 메타 데이터를 수정 하 고 할당량을 저장소 계정 이름과 공유 이름으로 공유 하 고, 반환 된 파일 공유 개체를 사용 하 여 수정 결과를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="56724-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="56724-114">예제 2: 저장소 계정 개체 및 공유 이름으로 저장소 파일 공유의 메타 데이터 수정</span><span class="sxs-lookup"><span data-stu-id="56724-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="56724-115">이 명령은 저장소 계정 개체와 공유 이름을 사용 하 여 저장소 파일 공유의 메타 데이터를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56724-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="56724-116">예제 3: 파이프라인을 사용 하 여 저장소 계정의 모든 저장소 파일 공유에 대 한 공유 할당량 수정</span><span class="sxs-lookup"><span data-stu-id="56724-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="56724-117">이 명령은 파이프라인이 있는 저장소 계정의 모든 저장소 파일 공유에 대 한 공유 할당량을 5000 GiB로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56724-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="56724-118">변수</span><span class="sxs-lookup"><span data-stu-id="56724-118">PARAMETERS</span></span>

### <span data-ttu-id="56724-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56724-119">-DefaultProfile</span></span>
<span data-ttu-id="56724-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56724-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56724-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56724-121">-InputObject</span></span>
<span data-ttu-id="56724-122">저장소 공유 개체</span><span class="sxs-lookup"><span data-stu-id="56724-122">Storage Share object</span></span>

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

### <span data-ttu-id="56724-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="56724-123">-Metadata</span></span>
<span data-ttu-id="56724-124">메타 데이터 공유</span><span class="sxs-lookup"><span data-stu-id="56724-124">Share Metadata</span></span>

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

### <span data-ttu-id="56724-125">-이름</span><span class="sxs-lookup"><span data-stu-id="56724-125">-Name</span></span>
<span data-ttu-id="56724-126">공유 이름</span><span class="sxs-lookup"><span data-stu-id="56724-126">Share Name</span></span>

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

### <span data-ttu-id="56724-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="56724-127">-QuotaGiB</span></span>
<span data-ttu-id="56724-128">Gid의 할당량을 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="56724-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="56724-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56724-129">-ResourceGroupName</span></span>
<span data-ttu-id="56724-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56724-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="56724-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56724-131">-ResourceId</span></span>
<span data-ttu-id="56724-132">파일 공유 리소스 Id를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="56724-132">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="56724-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="56724-133">-StorageAccount</span></span>
<span data-ttu-id="56724-134">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="56724-134">Storage account object</span></span>

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

### <span data-ttu-id="56724-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="56724-135">-StorageAccountName</span></span>
<span data-ttu-id="56724-136">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56724-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="56724-137">-확인</span><span class="sxs-lookup"><span data-stu-id="56724-137">-Confirm</span></span>
<span data-ttu-id="56724-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="56724-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56724-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56724-139">-WhatIf</span></span>
<span data-ttu-id="56724-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="56724-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56724-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56724-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56724-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56724-142">CommonParameters</span></span>
<span data-ttu-id="56724-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56724-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56724-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56724-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56724-145">입력</span><span class="sxs-lookup"><span data-stu-id="56724-145">INPUTS</span></span>

### <span data-ttu-id="56724-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="56724-146">System.String</span></span>

### <span data-ttu-id="56724-147">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56724-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="56724-148">Microsoft. i. m a i 공유.</span><span class="sxs-lookup"><span data-stu-id="56724-148">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="56724-149">출력</span><span class="sxs-lookup"><span data-stu-id="56724-149">OUTPUTS</span></span>

### <span data-ttu-id="56724-150">Microsoft. i. m a i 공유.</span><span class="sxs-lookup"><span data-stu-id="56724-150">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="56724-151">상속자</span><span class="sxs-lookup"><span data-stu-id="56724-151">NOTES</span></span>

## <span data-ttu-id="56724-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56724-152">RELATED LINKS</span></span>
