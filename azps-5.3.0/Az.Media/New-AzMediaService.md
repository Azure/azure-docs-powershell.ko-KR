---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
ms.openlocfilehash: a7554468824e85dbd922c0fac874ca9d881c13d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496768"
---
# <span data-ttu-id="71fe4-101">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="71fe4-101">New-AzMediaService</span></span>

## <span data-ttu-id="71fe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="71fe4-103">미디어 서비스가 이미 있는 경우 미디어 서비스를 만듭니다. 모든 속성은 제공된 입력으로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="71fe4-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

## <span data-ttu-id="71fe4-104">구문</span><span class="sxs-lookup"><span data-stu-id="71fe4-104">SYNTAX</span></span>

### <span data-ttu-id="71fe4-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="71fe4-105">StorageAccountIdParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71fe4-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="71fe4-106">StorageAccountsParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71fe4-107">설명</span><span class="sxs-lookup"><span data-stu-id="71fe4-107">DESCRIPTION</span></span>
<span data-ttu-id="71fe4-108">**New-AzMediaService** cmdlet은 미디어 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="71fe4-108">The **New-AzMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="71fe4-109">미디어 서비스가 이미 있는 경우 이 cmdlet은 해당 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="71fe4-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="71fe4-110">예제</span><span class="sxs-lookup"><span data-stu-id="71fe4-110">EXAMPLES</span></span>

### <span data-ttu-id="71fe4-111">예제1: 기본 저장소 계정만 사용하여 미디어 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="71fe4-111">Example1: Create a media service with the primary storage account only</span></span>
```
PS C:\># Variables
## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName = "Storage1"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tag $Tags
```

<span data-ttu-id="71fe4-112">이 예제에서는 기본 저장소 계정만 지정하여 미디어 서비스를 만드는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="71fe4-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="71fe4-113">이 스크립트는 다른 여러 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71fe4-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="71fe4-114">예제 2: 여러 저장소가 있는 미디어 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="71fe4-114">Example 2: Create a media service with multiple storage</span></span>
```
PS C:\># Variables

## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName1 = "storage1"
$StorageName2 = "storage2"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tag $Tags
```

<span data-ttu-id="71fe4-115">이 예제에서는 여러 저장소 계정으로 미디어 서비스를 만드는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="71fe4-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="71fe4-116">이 스크립트는 다른 여러 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71fe4-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="71fe4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71fe4-117">PARAMETERS</span></span>

### <span data-ttu-id="71fe4-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="71fe4-118">-AccountName</span></span>
<span data-ttu-id="71fe4-119">이 cmdlet에서 만드는 미디어 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71fe4-119">Specifies the name of the media service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71fe4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71fe4-120">-DefaultProfile</span></span>
<span data-ttu-id="71fe4-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="71fe4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71fe4-122">-Location</span><span class="sxs-lookup"><span data-stu-id="71fe4-122">-Location</span></span>
<span data-ttu-id="71fe4-123">이 cmdlet이 미디어 서비스를 만드는 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71fe4-123">Specifies the region that this cmdlet creates the media service in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71fe4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71fe4-124">-ResourceGroupName</span></span>
<span data-ttu-id="71fe4-125">미디어 서비스가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71fe4-125">Specifies the name of the resource group that the media service is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71fe4-126">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="71fe4-126">-StorageAccountId</span></span>
<span data-ttu-id="71fe4-127">미디어 서비스 계정과 연결된 저장소 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71fe4-127">Specifies the storage account associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageAccountIdParamSet
Aliases: Id

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71fe4-128">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="71fe4-128">-StorageAccounts</span></span>
<span data-ttu-id="71fe4-129">미디어 서비스에 연결하기 위한 저장소 계정 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71fe4-129">Specifies an array of storage accounts to associate with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: StorageAccountsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71fe4-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="71fe4-130">-Tag</span></span>
<span data-ttu-id="71fe4-131">미디어 서비스 계정과 연결된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="71fe4-131">The tags associated with the media service account.</span></span>

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

### <span data-ttu-id="71fe4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71fe4-132">-Confirm</span></span>
<span data-ttu-id="71fe4-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="71fe4-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71fe4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71fe4-134">-WhatIf</span></span>
<span data-ttu-id="71fe4-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="71fe4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71fe4-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71fe4-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71fe4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71fe4-137">CommonParameters</span></span>
<span data-ttu-id="71fe4-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71fe4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71fe4-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="71fe4-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71fe4-140">입력</span><span class="sxs-lookup"><span data-stu-id="71fe4-140">INPUTS</span></span>

### <span data-ttu-id="71fe4-141">System.String</span><span class="sxs-lookup"><span data-stu-id="71fe4-141">System.String</span></span>

### <span data-ttu-id="71fe4-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span><span class="sxs-lookup"><span data-stu-id="71fe4-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="71fe4-143">출력</span><span class="sxs-lookup"><span data-stu-id="71fe4-143">OUTPUTS</span></span>

### <span data-ttu-id="71fe4-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="71fe4-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="71fe4-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="71fe4-145">NOTES</span></span>

## <span data-ttu-id="71fe4-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71fe4-146">RELATED LINKS</span></span>

[<span data-ttu-id="71fe4-147">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="71fe4-147">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="71fe4-148">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="71fe4-148">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="71fe4-149">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="71fe4-149">Set-AzMediaService</span></span>](./Set-AzMediaService.md)

