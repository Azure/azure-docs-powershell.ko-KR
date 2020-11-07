---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
ms.openlocfilehash: 86f1667c1383f226d47afed2a842af6386dad81e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703700"
---
# <span data-ttu-id="5c25c-101">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="5c25c-101">New-AzureRmMediaService</span></span>

## <span data-ttu-id="5c25c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c25c-102">SYNOPSIS</span></span>
<span data-ttu-id="5c25c-103">미디어 서비스를 만듭니다. 미디어 서비스가 이미 있으면 해당 속성이 제공 된 입력으로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c25c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5c25c-104">SYNTAX</span></span>

### <span data-ttu-id="5c25c-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="5c25c-105">StorageAccountIdParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c25c-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="5c25c-106">StorageAccountsParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c25c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5c25c-107">DESCRIPTION</span></span>
<span data-ttu-id="5c25c-108">**AzureRmMediaService** cmdlet은 미디어 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-108">The **New-AzureRmMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="5c25c-109">미디어 서비스가 이미 있는 경우이 cmdlet은 해당 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="5c25c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5c25c-110">EXAMPLES</span></span>

### <span data-ttu-id="5c25c-111">Example1: 기본 저장소 계정만 사용 하 여 미디어 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="5c25c-111">Example1: Create a media service with the primary storage account only</span></span>
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

<span data-ttu-id="5c25c-112">이 예제에서는 기본 저장소 계정만 지정 하 여 미디어 서비스를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="5c25c-113">이 스크립트는 여러 다른 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="5c25c-114">예제 2: 저장소를 여러 개 사용 하 여 미디어 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="5c25c-114">Example 2: Create a media service with multiple storage</span></span>
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

<span data-ttu-id="5c25c-115">이 예제에서는 여러 저장소 계정을 사용 하 여 미디어 서비스를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="5c25c-116">이 스크립트는 여러 다른 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="5c25c-117">변수</span><span class="sxs-lookup"><span data-stu-id="5c25c-117">PARAMETERS</span></span>

### <span data-ttu-id="5c25c-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5c25c-118">-AccountName</span></span>
<span data-ttu-id="5c25c-119">이 cmdlet이 만드는 미디어 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-119">Specifies the name of the media service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5c25c-120">-위치</span><span class="sxs-lookup"><span data-stu-id="5c25c-120">-Location</span></span>
<span data-ttu-id="5c25c-121">이 cmdlet이 미디어 서비스를 만드는 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-121">Specifies the region that this cmdlet creates the media service in.</span></span>

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

### <span data-ttu-id="5c25c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c25c-122">-ResourceGroupName</span></span>
<span data-ttu-id="5c25c-123">미디어 서비스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-123">Specifies the name of the resource group that the media service is assigned to.</span></span>

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

### <span data-ttu-id="5c25c-124">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5c25c-124">-StorageAccountId</span></span>
<span data-ttu-id="5c25c-125">미디어 서비스 계정과 연결 된 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-125">Specifies the storage account associated with the media service account.</span></span>

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

### <span data-ttu-id="5c25c-126">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="5c25c-126">-StorageAccounts</span></span>
<span data-ttu-id="5c25c-127">미디어 서비스와 연결할 저장소 계정의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-127">Specifies an array of storage accounts to associate with the media service.</span></span>

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

### <span data-ttu-id="5c25c-128">태그</span><span class="sxs-lookup"><span data-stu-id="5c25c-128">-Tags</span></span>
<span data-ttu-id="5c25c-129">미디어 서비스에 대 한 태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-129">Specifies tags for the media service.</span></span>

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

### <span data-ttu-id="5c25c-130">-확인</span><span class="sxs-lookup"><span data-stu-id="5c25c-130">-Confirm</span></span>
<span data-ttu-id="5c25c-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c25c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c25c-132">-WhatIf</span></span>
<span data-ttu-id="5c25c-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c25c-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c25c-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c25c-135">-DefaultProfile</span></span>
<span data-ttu-id="5c25c-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c25c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c25c-137">CommonParameters</span></span>
<span data-ttu-id="5c25c-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c25c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c25c-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c25c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c25c-140">입력</span><span class="sxs-lookup"><span data-stu-id="5c25c-140">INPUTS</span></span>

## <span data-ttu-id="5c25c-141">출력</span><span class="sxs-lookup"><span data-stu-id="5c25c-141">OUTPUTS</span></span>

### <span data-ttu-id="5c25c-142">PSMediaService (\*).</span><span class="sxs-lookup"><span data-stu-id="5c25c-142">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="5c25c-143">상속자</span><span class="sxs-lookup"><span data-stu-id="5c25c-143">NOTES</span></span>

## <span data-ttu-id="5c25c-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c25c-144">RELATED LINKS</span></span>

[<span data-ttu-id="5c25c-145">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="5c25c-145">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="5c25c-146">제거-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="5c25c-146">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="5c25c-147">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="5c25c-147">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


