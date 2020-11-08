---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: 06a37226c1915ef858d72ec123dd238011c19f19
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043150"
---
# <span data-ttu-id="447c6-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="447c6-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="447c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="447c6-102">SYNOPSIS</span></span>
<span data-ttu-id="447c6-103">저장소 blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="447c6-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="447c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="447c6-104">SYNTAX</span></span>

### <span data-ttu-id="447c6-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="447c6-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="447c6-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="447c6-106">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="447c6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="447c6-107">DESCRIPTION</span></span>
<span data-ttu-id="447c6-108">**새 AzRmStorageContainer** Cmdlet은 저장소 blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="447c6-108">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="447c6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="447c6-109">EXAMPLES</span></span>

### <span data-ttu-id="447c6-110">예제 1: 저장소 계정 이름과 컨테이너 이름이 있는 저장소 blob 컨테이너 만들기 (메타 데이터 포함)</span><span class="sxs-lookup"><span data-stu-id="447c6-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="447c6-111">이 명령은 저장소 계정 이름과 컨테이너 이름으로 메타 데이터를 사용 하 여 저장소 blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="447c6-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="447c6-112">예제 2: 저장소 계정 개체 및 컨테이너 이름이 있는 저장소 blob 컨테이너 만들기 (Blob로 공용 액세스 사용)</span><span class="sxs-lookup"><span data-stu-id="447c6-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="447c6-113">이 명령은 저장소 계정 개체와 컨테이너 이름이 있는 저장소 blob 컨테이너를 만들고 공용 액세스를 Blob로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="447c6-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="447c6-114">변수</span><span class="sxs-lookup"><span data-stu-id="447c6-114">PARAMETERS</span></span>

### <span data-ttu-id="447c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="447c6-115">-DefaultProfile</span></span>
<span data-ttu-id="447c6-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="447c6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="447c6-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="447c6-117">-Metadata</span></span>
<span data-ttu-id="447c6-118">컨테이너 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="447c6-118">Container Metadata</span></span>

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

### <span data-ttu-id="447c6-119">-이름</span><span class="sxs-lookup"><span data-stu-id="447c6-119">-Name</span></span>
<span data-ttu-id="447c6-120">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="447c6-120">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="447c6-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="447c6-121">-PublicAccess</span></span>
<span data-ttu-id="447c6-122">컨테이너 PublicAccess</span><span class="sxs-lookup"><span data-stu-id="447c6-122">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="447c6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="447c6-123">-ResourceGroupName</span></span>
<span data-ttu-id="447c6-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="447c6-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="447c6-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="447c6-125">-StorageAccount</span></span>
<span data-ttu-id="447c6-126">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="447c6-126">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="447c6-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="447c6-127">-StorageAccountName</span></span>
<span data-ttu-id="447c6-128">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="447c6-128">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="447c6-129">-확인</span><span class="sxs-lookup"><span data-stu-id="447c6-129">-Confirm</span></span>
<span data-ttu-id="447c6-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="447c6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="447c6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="447c6-131">-WhatIf</span></span>
<span data-ttu-id="447c6-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="447c6-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="447c6-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="447c6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="447c6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="447c6-134">CommonParameters</span></span>
<span data-ttu-id="447c6-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="447c6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="447c6-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="447c6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="447c6-137">입력</span><span class="sxs-lookup"><span data-stu-id="447c6-137">INPUTS</span></span>

### <span data-ttu-id="447c6-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="447c6-138">System.String</span></span>

### <span data-ttu-id="447c6-139">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="447c6-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="447c6-140">출력</span><span class="sxs-lookup"><span data-stu-id="447c6-140">OUTPUTS</span></span>

### <span data-ttu-id="447c6-141">Microsoft. m a. 모델. PSContainer</span><span class="sxs-lookup"><span data-stu-id="447c6-141">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="447c6-142">상속자</span><span class="sxs-lookup"><span data-stu-id="447c6-142">NOTES</span></span>

## <span data-ttu-id="447c6-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="447c6-143">RELATED LINKS</span></span>
