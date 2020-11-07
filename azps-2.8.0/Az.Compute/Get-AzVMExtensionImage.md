---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: ebe1720154c45b08eb84cfe6c1ee4e339859e5fb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697436"
---
# <span data-ttu-id="8040c-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="8040c-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="8040c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8040c-102">SYNOPSIS</span></span>
<span data-ttu-id="8040c-103">Azure 확장에 대 한 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8040c-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="8040c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8040c-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8040c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8040c-105">DESCRIPTION</span></span>
<span data-ttu-id="8040c-106">**AzVMExtensionImage** Cmdlet은 Azure 확장에 대 한 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8040c-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="8040c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8040c-107">EXAMPLES</span></span>

### <span data-ttu-id="8040c-108">예제 1: 확장 이미지 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="8040c-108">Example 1: Get the versions of an extension image</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient"

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/11.18.6.2
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 11.18.6.2
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="8040c-109">이 명령은 지정 된 위치, 게시자 및 형식에 대 한 확장 이미지의 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8040c-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="8040c-110">예제 2: 버전 필터링을 사용 하 여 확장 이미지 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="8040c-110">Example 2: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 12*

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1207.12.3.0
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1207.12.3.0
FilterExpression :

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/westus/Pub
                   lishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/Versions/1210.12.109.
                   1004
Location         : westus
PublisherName    : Chef.Bootstrap.WindowsAzure
Type             : ChefClient
Version          : 1210.12.109.1004
FilterExpression :
```

<span data-ttu-id="8040c-111">이 명령은 지정 된 위치, 게시자, 형식 및 12로 시작 하는 버전에 대 한 확장 이미지의 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8040c-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="8040c-112">예제 3: 버전 필터링을 사용 하 여 확장 이미지 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="8040c-112">Example 3: Get the versions of an extension image with filter over version</span></span>
```
PS C:\> Get-AzVMExtensionImage -Location "West US" -PublisherName "Chef.Bootstrap.WindowsAzure" -Type "ChefClient" -Version 1207.12.3.0

Id                         : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/
                             westus/Publishers/Chef.Bootstrap.WindowsAzure/ArtifactTypes/VMExtension/Types/ChefClient/V
                             ersions/1207.12.3.0
Location                   : westus
PublisherName              : Chef.Bootstrap.WindowsAzure
Type                       : ChefClient
Version                    : 1207.12.3.0
FilterExpression           :
Name                       :
HandlerSchema              :
OperatingSystem            : Windows
ComputeRole                : IaaS
SupportsMultipleExtensions : False
VMScaleSetEnabled          : False
```

<span data-ttu-id="8040c-113">이 명령은 지정 된 위치, 게시자, 형식 및 버전에 대 한 확장 이미지의 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8040c-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="8040c-114">변수</span><span class="sxs-lookup"><span data-stu-id="8040c-114">PARAMETERS</span></span>

### <span data-ttu-id="8040c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8040c-115">-DefaultProfile</span></span>
<span data-ttu-id="8040c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8040c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8040c-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="8040c-117">-FilterExpression</span></span>
<span data-ttu-id="8040c-118">필터 식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8040c-118">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8040c-119">-위치</span><span class="sxs-lookup"><span data-stu-id="8040c-119">-Location</span></span>
<span data-ttu-id="8040c-120">확장의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8040c-120">Specifies the location of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8040c-121">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="8040c-121">-PublisherName</span></span>
<span data-ttu-id="8040c-122">확장 게시자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8040c-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="8040c-123">확장 게시자를 가져오려면 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8040c-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8040c-124">-Type</span><span class="sxs-lookup"><span data-stu-id="8040c-124">-Type</span></span>
<span data-ttu-id="8040c-125">확장 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8040c-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="8040c-126">확장 형식을 가져오려면 Get-AzVMExtensionImageType cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8040c-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8040c-127">-버전</span><span class="sxs-lookup"><span data-stu-id="8040c-127">-Version</span></span>
<span data-ttu-id="8040c-128">이 cmdlet이 가져오는 확장의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8040c-128">Specifies the version of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8040c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8040c-129">CommonParameters</span></span>
<span data-ttu-id="8040c-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8040c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8040c-131">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8040c-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8040c-132">입력</span><span class="sxs-lookup"><span data-stu-id="8040c-132">INPUTS</span></span>

### <span data-ttu-id="8040c-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8040c-133">System.String</span></span>

## <span data-ttu-id="8040c-134">출력</span><span class="sxs-lookup"><span data-stu-id="8040c-134">OUTPUTS</span></span>

### <span data-ttu-id="8040c-135">Microsoft Azure. PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="8040c-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="8040c-136">Microsoft. PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="8040c-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="8040c-137">상속자</span><span class="sxs-lookup"><span data-stu-id="8040c-137">NOTES</span></span>

## <span data-ttu-id="8040c-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8040c-138">RELATED LINKS</span></span>

[<span data-ttu-id="8040c-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="8040c-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="8040c-140">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="8040c-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="8040c-141">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8040c-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

