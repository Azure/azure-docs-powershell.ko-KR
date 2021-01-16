---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: 06a37226c1915ef858d72ec123dd238011c19f19
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324876"
---
# <span data-ttu-id="759e2-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="759e2-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="759e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="759e2-102">SYNOPSIS</span></span>
<span data-ttu-id="759e2-103">Storage Blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="759e2-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="759e2-104">구문</span><span class="sxs-lookup"><span data-stu-id="759e2-104">SYNTAX</span></span>

### <span data-ttu-id="759e2-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="759e2-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="759e2-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="759e2-106">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="759e2-107">설명</span><span class="sxs-lookup"><span data-stu-id="759e2-107">DESCRIPTION</span></span>
<span data-ttu-id="759e2-108">**New-AzRmStorageContainer** cmdlet은 Storage Blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="759e2-108">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="759e2-109">예제</span><span class="sxs-lookup"><span data-stu-id="759e2-109">EXAMPLES</span></span>

### <span data-ttu-id="759e2-110">예제 1: 메타데이터를 사용하여 Storage 계정 이름 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="759e2-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="759e2-111">이 명령은 메타데이터를 사용하여 Storage 계정 이름 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="759e2-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="759e2-112">예제 2: Blob으로 공용 액세스가 있는 Storage 계정 개체 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너 만들기</span><span class="sxs-lookup"><span data-stu-id="759e2-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="759e2-113">이 명령은 공용 액세스를 Blob으로 사용하여 Storage 계정 개체 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="759e2-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="759e2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="759e2-114">PARAMETERS</span></span>

### <span data-ttu-id="759e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="759e2-115">-DefaultProfile</span></span>
<span data-ttu-id="759e2-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="759e2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="759e2-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="759e2-117">-Metadata</span></span>
<span data-ttu-id="759e2-118">컨테이너 메타데이터</span><span class="sxs-lookup"><span data-stu-id="759e2-118">Container Metadata</span></span>

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

### <span data-ttu-id="759e2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="759e2-119">-Name</span></span>
<span data-ttu-id="759e2-120">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="759e2-120">Container Name</span></span>

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

### <span data-ttu-id="759e2-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="759e2-121">-PublicAccess</span></span>
<span data-ttu-id="759e2-122">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="759e2-122">Container PublicAccess</span></span>

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

### <span data-ttu-id="759e2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="759e2-123">-ResourceGroupName</span></span>
<span data-ttu-id="759e2-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="759e2-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="759e2-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="759e2-125">-StorageAccount</span></span>
<span data-ttu-id="759e2-126">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="759e2-126">Storage account object</span></span>

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

### <span data-ttu-id="759e2-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="759e2-127">-StorageAccountName</span></span>
<span data-ttu-id="759e2-128">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="759e2-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="759e2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="759e2-129">-Confirm</span></span>
<span data-ttu-id="759e2-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="759e2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="759e2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="759e2-131">-WhatIf</span></span>
<span data-ttu-id="759e2-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="759e2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="759e2-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="759e2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="759e2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="759e2-134">CommonParameters</span></span>
<span data-ttu-id="759e2-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="759e2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="759e2-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="759e2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="759e2-137">입력</span><span class="sxs-lookup"><span data-stu-id="759e2-137">INPUTS</span></span>

### <span data-ttu-id="759e2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="759e2-138">System.String</span></span>

### <span data-ttu-id="759e2-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="759e2-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="759e2-140">출력</span><span class="sxs-lookup"><span data-stu-id="759e2-140">OUTPUTS</span></span>

### <span data-ttu-id="759e2-141">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="759e2-141">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="759e2-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="759e2-142">NOTES</span></span>

## <span data-ttu-id="759e2-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="759e2-143">RELATED LINKS</span></span>
