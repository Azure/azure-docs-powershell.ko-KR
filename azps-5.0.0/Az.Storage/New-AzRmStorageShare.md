---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 4dc3914e4a8bc9113dd16ab431db53ddcf00ab5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309422"
---
# <span data-ttu-id="62285-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="62285-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="62285-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62285-102">SYNOPSIS</span></span>
<span data-ttu-id="62285-103">저장소 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62285-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="62285-104">구문과</span><span class="sxs-lookup"><span data-stu-id="62285-104">SYNTAX</span></span>

### <span data-ttu-id="62285-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="62285-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62285-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="62285-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62285-107">설명은</span><span class="sxs-lookup"><span data-stu-id="62285-107">DESCRIPTION</span></span>
<span data-ttu-id="62285-108">**새 AzRmStorageShare** Cmdlet은 저장소 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62285-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="62285-109">예제의</span><span class="sxs-lookup"><span data-stu-id="62285-109">EXAMPLES</span></span>

### <span data-ttu-id="62285-110">예제 1: 저장소 계정 이름과 공유 이름으로 저장소 파일 공유를 만들고 메타 데이터와 공유 할당량을 100 GiB로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="62285-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="62285-111">이 명령은 메타 데이터를 사용 하 여 저장소 파일 공유를 만들고 할당량을 100 GiB로 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="62285-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="62285-112">예제 2: 저장소 계정 개체를 사용 하 여 저장소 파일 공유 만들기</span><span class="sxs-lookup"><span data-stu-id="62285-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="62285-113">이 명령은 저장소 계정 개체와 공유 이름을 사용 하 여 저장소 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62285-113">This command creates a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="62285-114">예제 3: accesstier를 사용 하 여 저장소 파일 공유 만들기</span><span class="sxs-lookup"><span data-stu-id="62285-114">Example 3: Create a Storage file share with accesstier as Hot</span></span>
```
PS C:\>$share = New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Hot

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Hot
```

<span data-ttu-id="62285-115">이 명령은 accesstier를 Hot으로 사용 하 여 저장소 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="62285-115">This command creates a Storage file share with accesstier as Hot.</span></span>

## <span data-ttu-id="62285-116">변수</span><span class="sxs-lookup"><span data-stu-id="62285-116">PARAMETERS</span></span>

### <span data-ttu-id="62285-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="62285-117">-AccessTier</span></span>
<span data-ttu-id="62285-118">특정 공유에 대 한 액세스 계층</span><span class="sxs-lookup"><span data-stu-id="62285-118">Access tier for specific share.</span></span> <span data-ttu-id="62285-119">StorageV2 account는 TransactionOptimized (기본값), Hot, 멋진 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62285-119">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="62285-120">FileStorage 계정에서 Premium을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62285-120">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="62285-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62285-121">-DefaultProfile</span></span>
<span data-ttu-id="62285-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62285-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62285-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="62285-123">-Metadata</span></span>
<span data-ttu-id="62285-124">메타 데이터 공유</span><span class="sxs-lookup"><span data-stu-id="62285-124">Share Metadata</span></span>

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

### <span data-ttu-id="62285-125">-이름</span><span class="sxs-lookup"><span data-stu-id="62285-125">-Name</span></span>
<span data-ttu-id="62285-126">Azure 파일 공유 이름</span><span class="sxs-lookup"><span data-stu-id="62285-126">Azure File share name</span></span>

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

### <span data-ttu-id="62285-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="62285-127">-QuotaGiB</span></span>
<span data-ttu-id="62285-128">Gid의 할당량을 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="62285-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="62285-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62285-129">-ResourceGroupName</span></span>
<span data-ttu-id="62285-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62285-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="62285-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="62285-131">-StorageAccount</span></span>
<span data-ttu-id="62285-132">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="62285-132">Storage account object</span></span>

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

### <span data-ttu-id="62285-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="62285-133">-StorageAccountName</span></span>
<span data-ttu-id="62285-134">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62285-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="62285-135">-확인</span><span class="sxs-lookup"><span data-stu-id="62285-135">-Confirm</span></span>
<span data-ttu-id="62285-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="62285-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62285-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62285-137">-WhatIf</span></span>
<span data-ttu-id="62285-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="62285-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62285-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62285-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62285-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62285-140">CommonParameters</span></span>
<span data-ttu-id="62285-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62285-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62285-142">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62285-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62285-143">입력</span><span class="sxs-lookup"><span data-stu-id="62285-143">INPUTS</span></span>

### <span data-ttu-id="62285-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="62285-144">System.String</span></span>

### <span data-ttu-id="62285-145">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="62285-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="62285-146">출력</span><span class="sxs-lookup"><span data-stu-id="62285-146">OUTPUTS</span></span>

### <span data-ttu-id="62285-147">Microsoft. i. m a i 공유.</span><span class="sxs-lookup"><span data-stu-id="62285-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="62285-148">상속자</span><span class="sxs-lookup"><span data-stu-id="62285-148">NOTES</span></span>

## <span data-ttu-id="62285-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62285-149">RELATED LINKS</span></span>
