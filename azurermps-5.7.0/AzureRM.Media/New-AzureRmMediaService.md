---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/new-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
ms.openlocfilehash: 72e42153e46c02a3e721400c83b4cba886485db4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703039"
---
# <span data-ttu-id="42439-101">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="42439-101">New-AzureRmMediaService</span></span>

## <span data-ttu-id="42439-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42439-102">SYNOPSIS</span></span>
<span data-ttu-id="42439-103">미디어 서비스를 만듭니다. 미디어 서비스가 이미 있으면 해당 속성이 제공 된 입력으로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="42439-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42439-104">구문과</span><span class="sxs-lookup"><span data-stu-id="42439-104">SYNTAX</span></span>

### <span data-ttu-id="42439-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="42439-105">StorageAccountIdParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42439-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="42439-106">StorageAccountsParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42439-107">설명은</span><span class="sxs-lookup"><span data-stu-id="42439-107">DESCRIPTION</span></span>
<span data-ttu-id="42439-108">**AzureRmMediaService** cmdlet은 미디어 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="42439-108">The **New-AzureRmMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="42439-109">미디어 서비스가 이미 있는 경우이 cmdlet은 해당 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="42439-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="42439-110">예제의</span><span class="sxs-lookup"><span data-stu-id="42439-110">EXAMPLES</span></span>

### <span data-ttu-id="42439-111">Example1: 기본 저장소 계정만 사용 하 여 미디어 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="42439-111">Example1: Create a media service with the primary storage account only</span></span>
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
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tags $Tags
```

<span data-ttu-id="42439-112">이 예제에서는 기본 저장소 계정만 지정 하 여 미디어 서비스를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="42439-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="42439-113">이 스크립트는 여러 다른 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="42439-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="42439-114">예제 2: 저장소를 여러 개 사용 하 여 미디어 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="42439-114">Example 2: Create a media service with multiple storage</span></span>
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
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tags $Tags
```

<span data-ttu-id="42439-115">이 예제에서는 여러 저장소 계정을 사용 하 여 미디어 서비스를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="42439-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="42439-116">이 스크립트는 여러 다른 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="42439-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="42439-117">변수</span><span class="sxs-lookup"><span data-stu-id="42439-117">PARAMETERS</span></span>

### <span data-ttu-id="42439-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="42439-118">-AccountName</span></span>
<span data-ttu-id="42439-119">이 cmdlet이 만드는 미디어 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42439-119">Specifies the name of the media service that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42439-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42439-120">-DefaultProfile</span></span>
<span data-ttu-id="42439-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="42439-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42439-122">-위치</span><span class="sxs-lookup"><span data-stu-id="42439-122">-Location</span></span>
<span data-ttu-id="42439-123">이 cmdlet이 미디어 서비스를 만드는 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42439-123">Specifies the region that this cmdlet creates the media service in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42439-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42439-124">-ResourceGroupName</span></span>
<span data-ttu-id="42439-125">미디어 서비스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42439-125">Specifies the name of the resource group that the media service is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42439-126">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="42439-126">-StorageAccountId</span></span>
<span data-ttu-id="42439-127">미디어 서비스 계정과 연결 된 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42439-127">Specifies the storage account associated with the media service account.</span></span>

```yaml
Type: String
Parameter Sets: StorageAccountIdParamSet
Aliases: Id

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42439-128">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="42439-128">-StorageAccounts</span></span>
<span data-ttu-id="42439-129">미디어 서비스와 연결할 저장소 계정의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42439-129">Specifies an array of storage accounts to associate with the media service.</span></span>

```yaml
Type: PSStorageAccount[]
Parameter Sets: StorageAccountsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42439-130">태그</span><span class="sxs-lookup"><span data-stu-id="42439-130">-Tag</span></span>
<span data-ttu-id="42439-131">미디어 서비스 계정과 연결 된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="42439-131">The tags associated with the media service account.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42439-132">-확인</span><span class="sxs-lookup"><span data-stu-id="42439-132">-Confirm</span></span>
<span data-ttu-id="42439-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="42439-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42439-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42439-134">-WhatIf</span></span>
<span data-ttu-id="42439-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="42439-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42439-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42439-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42439-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42439-137">CommonParameters</span></span>
<span data-ttu-id="42439-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="42439-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42439-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42439-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42439-140">입력</span><span class="sxs-lookup"><span data-stu-id="42439-140">INPUTS</span></span>

### <span data-ttu-id="42439-141">않아야</span><span class="sxs-lookup"><span data-stu-id="42439-141">None</span></span>
<span data-ttu-id="42439-142">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42439-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="42439-143">출력</span><span class="sxs-lookup"><span data-stu-id="42439-143">OUTPUTS</span></span>

### <span data-ttu-id="42439-144">PSMediaService (\*).</span><span class="sxs-lookup"><span data-stu-id="42439-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="42439-145">상속자</span><span class="sxs-lookup"><span data-stu-id="42439-145">NOTES</span></span>

## <span data-ttu-id="42439-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42439-146">RELATED LINKS</span></span>

[<span data-ttu-id="42439-147">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="42439-147">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="42439-148">제거-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="42439-148">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="42439-149">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="42439-149">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


