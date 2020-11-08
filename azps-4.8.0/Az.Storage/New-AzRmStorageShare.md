---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 81e380f6b6d4b1c35a6cff98093dfedf94119a9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048589"
---
# <span data-ttu-id="9312d-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="9312d-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="9312d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9312d-102">SYNOPSIS</span></span>
<span data-ttu-id="9312d-103">저장소 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9312d-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="9312d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9312d-104">SYNTAX</span></span>

### <span data-ttu-id="9312d-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="9312d-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9312d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9312d-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9312d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9312d-107">DESCRIPTION</span></span>
<span data-ttu-id="9312d-108">**새 AzRmStorageShare** Cmdlet은 저장소 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9312d-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="9312d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9312d-109">EXAMPLES</span></span>

### <span data-ttu-id="9312d-110">예제 1: 저장소 계정 이름과 공유 이름으로 저장소 파일 공유를 만들고 메타 데이터와 공유 할당량을 100 GiB로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9312d-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="9312d-111">이 명령은 메타 데이터를 사용 하 여 저장소 파일 공유를 만들고 할당량을 100 GiB로 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="9312d-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="9312d-112">예제 2: 저장소 계정 개체를 사용 하 여 저장소 파일 공유 만들기</span><span class="sxs-lookup"><span data-stu-id="9312d-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="9312d-113">이 명령은 저장소 계정 개체와 공유 이름을 사용 하 여 저장소 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9312d-113">This command creates a Storage file share with Storage account object and share name.</span></span>

## <span data-ttu-id="9312d-114">변수</span><span class="sxs-lookup"><span data-stu-id="9312d-114">PARAMETERS</span></span>

### <span data-ttu-id="9312d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9312d-115">-DefaultProfile</span></span>
<span data-ttu-id="9312d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9312d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9312d-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9312d-117">-Metadata</span></span>
<span data-ttu-id="9312d-118">메타 데이터 공유</span><span class="sxs-lookup"><span data-stu-id="9312d-118">Share Metadata</span></span>

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

### <span data-ttu-id="9312d-119">-이름</span><span class="sxs-lookup"><span data-stu-id="9312d-119">-Name</span></span>
<span data-ttu-id="9312d-120">Azure 파일 공유 이름</span><span class="sxs-lookup"><span data-stu-id="9312d-120">Azure File share name</span></span>

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

### <span data-ttu-id="9312d-121">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="9312d-121">-QuotaGiB</span></span>
<span data-ttu-id="9312d-122">Gid의 할당량을 공유 합니다.</span><span class="sxs-lookup"><span data-stu-id="9312d-122">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="9312d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9312d-123">-ResourceGroupName</span></span>
<span data-ttu-id="9312d-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9312d-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="9312d-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9312d-125">-StorageAccount</span></span>
<span data-ttu-id="9312d-126">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="9312d-126">Storage account object</span></span>

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

### <span data-ttu-id="9312d-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9312d-127">-StorageAccountName</span></span>
<span data-ttu-id="9312d-128">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9312d-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="9312d-129">-확인</span><span class="sxs-lookup"><span data-stu-id="9312d-129">-Confirm</span></span>
<span data-ttu-id="9312d-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9312d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9312d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9312d-131">-WhatIf</span></span>
<span data-ttu-id="9312d-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9312d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9312d-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9312d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9312d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9312d-134">CommonParameters</span></span>
<span data-ttu-id="9312d-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9312d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9312d-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9312d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9312d-137">입력</span><span class="sxs-lookup"><span data-stu-id="9312d-137">INPUTS</span></span>

### <span data-ttu-id="9312d-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9312d-138">System.String</span></span>

### <span data-ttu-id="9312d-139">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9312d-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="9312d-140">출력</span><span class="sxs-lookup"><span data-stu-id="9312d-140">OUTPUTS</span></span>

### <span data-ttu-id="9312d-141">Microsoft. i. m a i 공유.</span><span class="sxs-lookup"><span data-stu-id="9312d-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="9312d-142">상속자</span><span class="sxs-lookup"><span data-stu-id="9312d-142">NOTES</span></span>

## <span data-ttu-id="9312d-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9312d-143">RELATED LINKS</span></span>
