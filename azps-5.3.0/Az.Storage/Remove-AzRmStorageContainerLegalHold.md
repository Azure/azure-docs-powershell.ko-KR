---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 494995a97ccb74df9ad9a9fc1f88272505598bb9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376195"
---
# <span data-ttu-id="45a7b-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="45a7b-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="45a7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45a7b-102">SYNOPSIS</span></span>
<span data-ttu-id="45a7b-103">Storage Blob 컨테이너에서 법적 보류 태그를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="45a7b-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="45a7b-104">구문</span><span class="sxs-lookup"><span data-stu-id="45a7b-104">SYNTAX</span></span>

### <span data-ttu-id="45a7b-105">AccountName(기본값)</span><span class="sxs-lookup"><span data-stu-id="45a7b-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45a7b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="45a7b-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45a7b-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="45a7b-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45a7b-108">설명</span><span class="sxs-lookup"><span data-stu-id="45a7b-108">DESCRIPTION</span></span>
<span data-ttu-id="45a7b-109">**Remove-AzRmStorageContainerLegalHold** cmdlet은 Storage Blob 컨테이너에서 법적 보류 태그를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="45a7b-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="45a7b-110">예제</span><span class="sxs-lookup"><span data-stu-id="45a7b-110">EXAMPLES</span></span>

### <span data-ttu-id="45a7b-111">예제 1: Storage 계정 이름 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너에서 법적 보관 태그 제거</span><span class="sxs-lookup"><span data-stu-id="45a7b-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="45a7b-112">이 명령은 Storage 계정 이름 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너에서 법적 보류 태그를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="45a7b-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="45a7b-113">예제 2: Storage 계정 개체 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너에서 법적 보관 태그 제거</span><span class="sxs-lookup"><span data-stu-id="45a7b-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="45a7b-114">이 명령은 Storage 계정 개체 및 컨테이너 이름을 사용하여 Storage Blob 컨테이너에서 법적 보류 태그를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="45a7b-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="45a7b-115">예제 3: 파이프라인이 있는 Storage 계정의 모든 Storage Blob 컨테이너에서 법적 보관 태그 제거</span><span class="sxs-lookup"><span data-stu-id="45a7b-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="45a7b-116">이 명령은 파이프라인이 있는 Storage 계정의 모든 Storage Blob 컨테이너에서 법적 보류 태그를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="45a7b-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="45a7b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45a7b-117">PARAMETERS</span></span>

### <span data-ttu-id="45a7b-118">-Container</span><span class="sxs-lookup"><span data-stu-id="45a7b-118">-Container</span></span>
<span data-ttu-id="45a7b-119">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="45a7b-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45a7b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a7b-120">-DefaultProfile</span></span>
<span data-ttu-id="45a7b-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="45a7b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45a7b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="45a7b-122">-Name</span></span>
<span data-ttu-id="45a7b-123">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="45a7b-123">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45a7b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45a7b-124">-ResourceGroupName</span></span>
<span data-ttu-id="45a7b-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="45a7b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="45a7b-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="45a7b-126">-StorageAccount</span></span>
<span data-ttu-id="45a7b-127">Storage 계정 개체</span><span class="sxs-lookup"><span data-stu-id="45a7b-127">Storage account object</span></span>

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

### <span data-ttu-id="45a7b-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="45a7b-128">-StorageAccountName</span></span>
<span data-ttu-id="45a7b-129">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="45a7b-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="45a7b-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="45a7b-130">-Tag</span></span>
<span data-ttu-id="45a7b-131">컨테이너 LegalHold 태그</span><span class="sxs-lookup"><span data-stu-id="45a7b-131">Container LegalHold Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a7b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45a7b-132">-Confirm</span></span>
<span data-ttu-id="45a7b-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="45a7b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45a7b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45a7b-134">-WhatIf</span></span>
<span data-ttu-id="45a7b-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="45a7b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45a7b-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="45a7b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45a7b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a7b-137">CommonParameters</span></span>
<span data-ttu-id="45a7b-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="45a7b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a7b-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="45a7b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a7b-140">입력</span><span class="sxs-lookup"><span data-stu-id="45a7b-140">INPUTS</span></span>

### <span data-ttu-id="45a7b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="45a7b-141">System.String</span></span>

### <span data-ttu-id="45a7b-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45a7b-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="45a7b-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="45a7b-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="45a7b-144">출력</span><span class="sxs-lookup"><span data-stu-id="45a7b-144">OUTPUTS</span></span>

### <span data-ttu-id="45a7b-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="45a7b-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="45a7b-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="45a7b-146">NOTES</span></span>

## <span data-ttu-id="45a7b-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45a7b-147">RELATED LINKS</span></span>
