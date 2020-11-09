---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 0f2d86fca85364fa71d50c05d83f278bd997252e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309418"
---
# <span data-ttu-id="0cabf-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0cabf-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="0cabf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cabf-102">SYNOPSIS</span></span>
<span data-ttu-id="0cabf-103">저장소 파일 공유를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cabf-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="0cabf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0cabf-104">SYNTAX</span></span>

### <span data-ttu-id="0cabf-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="0cabf-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cabf-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0cabf-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0cabf-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="0cabf-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cabf-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="0cabf-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cabf-109">설명은</span><span class="sxs-lookup"><span data-stu-id="0cabf-109">DESCRIPTION</span></span>
<span data-ttu-id="0cabf-110">**새 AzRmStorageShare** Cmdlet은 저장소 파일 공유를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cabf-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="0cabf-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0cabf-111">EXAMPLES</span></span>

### <span data-ttu-id="0cabf-112">예제 1: 저장소 파일 공유의 메타 데이터를 수정 하 고 저장소 계정 이름과 공유 이름을 사용 하 여 할당량 공유</span><span class="sxs-lookup"><span data-stu-id="0cabf-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
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

<span data-ttu-id="0cabf-113">이 명령은 저장소 파일 공유의 메타 데이터를 수정 하 고 할당량을 저장소 계정 이름과 공유 이름으로 공유 하 고, 반환 된 파일 공유 개체를 사용 하 여 수정 결과를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cabf-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="0cabf-114">예제 2: 저장소 계정 개체 및 공유 이름으로 저장소 파일 공유의 메타 데이터 수정</span><span class="sxs-lookup"><span data-stu-id="0cabf-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="0cabf-115">이 명령은 저장소 계정 개체와 공유 이름을 사용 하 여 저장소 파일 공유의 메타 데이터를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cabf-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="0cabf-116">예제 3: 파이프라인을 사용 하 여 저장소 계정의 모든 저장소 파일 공유에 대 한 공유 할당량 수정</span><span class="sxs-lookup"><span data-stu-id="0cabf-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="0cabf-117">이 명령은 파이프라인이 있는 저장소 계정의 모든 저장소 파일 공유에 대 한 공유 할당량을 5000 GiB로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cabf-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

### <span data-ttu-id="0cabf-118">예제 4: accesstier를 사용 하 여 저장소 파일 공유 수정</span><span class="sxs-lookup"><span data-stu-id="0cabf-118">Example 4: Modify a Storage file share with accesstier as Cool</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Cool

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Cool
```

<span data-ttu-id="0cabf-119">이 명령은 accesstier으로 저장소 파일 공유를 멋지게 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cabf-119">This command modifies a Storage file share with accesstier as Cool.</span></span>

## <span data-ttu-id="0cabf-120">변수</span><span class="sxs-lookup"><span data-stu-id="0cabf-120">PARAMETERS</span></span>

### <span data-ttu-id="0cabf-121">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="0cabf-121">-AccessTier</span></span>
<span data-ttu-id="0cabf-122">특정 공유에 대 한 액세스 계층</span><span class="sxs-lookup"><span data-stu-id="0cabf-122">Access tier for specific share.</span></span> <span data-ttu-id="0cabf-123">StorageV2 account는 TransactionOptimized (기본값), Hot, 멋진 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0cabf-123">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="0cabf-124">FileStorage 계정에서 Premium을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0cabf-124">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="0cabf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cabf-125">-DefaultProfile</span></span>
<span data-ttu-id="0cabf-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0cabf-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cabf-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0cabf-127">-InputObject</span></span>
<span data-ttu-id="0cabf-128">저장소 공유 개체</span><span class="sxs-lookup"><span data-stu-id="0cabf-128">Storage Share object</span></span>

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

### <span data-ttu-id="0cabf-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="0cabf-129">-Metadata</span></span>
<span data-ttu-id="0cabf-130">메타 데이터 공유</span><span class="sxs-lookup"><span data-stu-id="0cabf-130">Share Metadata</span></span>

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

### <span data-ttu-id="0cabf-131">-이름</span><span class="sxs-lookup"><span data-stu-id="0cabf-131">-Name</span></span>
<span data-ttu-id="0cabf-132">공유 이름</span><span class="sxs-lookup"><span data-stu-id="0cabf-132">Share Name</span></span>

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

### <span data-ttu-id="0cabf-133">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="0cabf-133">-QuotaGiB</span></span>
<span data-ttu-id="0cabf-134">Gid의 할당량을 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cabf-134">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="0cabf-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cabf-135">-ResourceGroupName</span></span>
<span data-ttu-id="0cabf-136">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0cabf-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="0cabf-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cabf-137">-ResourceId</span></span>
<span data-ttu-id="0cabf-138">파일 공유 리소스 Id를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cabf-138">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="0cabf-139">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0cabf-139">-StorageAccount</span></span>
<span data-ttu-id="0cabf-140">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="0cabf-140">Storage account object</span></span>

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

### <span data-ttu-id="0cabf-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0cabf-141">-StorageAccountName</span></span>
<span data-ttu-id="0cabf-142">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0cabf-142">Storage Account Name.</span></span>

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

### <span data-ttu-id="0cabf-143">-확인</span><span class="sxs-lookup"><span data-stu-id="0cabf-143">-Confirm</span></span>
<span data-ttu-id="0cabf-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cabf-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cabf-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cabf-145">-WhatIf</span></span>
<span data-ttu-id="0cabf-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0cabf-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cabf-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0cabf-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cabf-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cabf-148">CommonParameters</span></span>
<span data-ttu-id="0cabf-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cabf-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cabf-150">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cabf-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cabf-151">입력</span><span class="sxs-lookup"><span data-stu-id="0cabf-151">INPUTS</span></span>

### <span data-ttu-id="0cabf-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0cabf-152">System.String</span></span>

### <span data-ttu-id="0cabf-153">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0cabf-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="0cabf-154">Microsoft. i. m a i 공유.</span><span class="sxs-lookup"><span data-stu-id="0cabf-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="0cabf-155">출력</span><span class="sxs-lookup"><span data-stu-id="0cabf-155">OUTPUTS</span></span>

### <span data-ttu-id="0cabf-156">Microsoft. i. m a i 공유.</span><span class="sxs-lookup"><span data-stu-id="0cabf-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="0cabf-157">상속자</span><span class="sxs-lookup"><span data-stu-id="0cabf-157">NOTES</span></span>

## <span data-ttu-id="0cabf-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0cabf-158">RELATED LINKS</span></span>
