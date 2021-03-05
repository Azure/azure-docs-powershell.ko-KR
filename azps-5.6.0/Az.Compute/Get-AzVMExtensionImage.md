---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F46041A3-355F-4449-B582-4D2F7314CA05
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmextensionimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtensionImage.md
ms.openlocfilehash: ce726675946b2b8dc40feb82a529ccf27ccef443
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013824"
---
# <span data-ttu-id="c9635-101">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="c9635-101">Get-AzVMExtensionImage</span></span>

## <span data-ttu-id="c9635-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9635-102">SYNOPSIS</span></span>
<span data-ttu-id="c9635-103">Azure 확장에 대한 모든 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9635-103">Gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="c9635-104">구문</span><span class="sxs-lookup"><span data-stu-id="c9635-104">SYNTAX</span></span>

```
Get-AzVMExtensionImage -Location <String> -PublisherName <String> -Type <String> [-FilterExpression <String>]
 [-Version <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9635-105">설명</span><span class="sxs-lookup"><span data-stu-id="c9635-105">DESCRIPTION</span></span>
<span data-ttu-id="c9635-106">**Get-AzVMExtensionImage** cmdlet은 Azure 확장에 대한 모든 버전을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c9635-106">The **Get-AzVMExtensionImage** cmdlet gets all versions for an Azure extension.</span></span>

## <span data-ttu-id="c9635-107">예제</span><span class="sxs-lookup"><span data-stu-id="c9635-107">EXAMPLES</span></span>

### <span data-ttu-id="c9635-108">예제 1: 확장 이미지의 버전 얻기</span><span class="sxs-lookup"><span data-stu-id="c9635-108">Example 1: Get the versions of an extension image</span></span>
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

<span data-ttu-id="c9635-109">이 명령은 지정된 위치, 게시자 및 형식에 대한 확장 이미지의 모든 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9635-109">This command gets all the versions of the extension image for the specified location, publisher, and type.</span></span>

### <span data-ttu-id="c9635-110">예제 2: 버전 오버 필터를 사용하여 확장 이미지의 버전 다운로드</span><span class="sxs-lookup"><span data-stu-id="c9635-110">Example 2: Get the versions of an extension image with filter over version</span></span>
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

<span data-ttu-id="c9635-111">이 명령은 12부터 지정된 위치, 게시자, 형식 및 버전에 대한 확장 이미지의 모든 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9635-111">This command gets all the versions of the extension image for the specified location, publisher, type, and version starting with 12.</span></span>

### <span data-ttu-id="c9635-112">예제 3: 버전 오버 필터를 사용하여 확장 이미지의 버전 다운로드</span><span class="sxs-lookup"><span data-stu-id="c9635-112">Example 3: Get the versions of an extension image with filter over version</span></span>
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

<span data-ttu-id="c9635-113">이 명령은 지정된 위치, 게시자, 형식 및 버전에 대한 확장 이미지의 모든 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9635-113">This command gets all the versions of the extension image for the specified location, publisher, type, and version.</span></span>

## <span data-ttu-id="c9635-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c9635-114">PARAMETERS</span></span>

### <span data-ttu-id="c9635-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9635-115">-DefaultProfile</span></span>
<span data-ttu-id="c9635-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9635-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9635-117">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="c9635-117">-FilterExpression</span></span>
<span data-ttu-id="c9635-118">필터 식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9635-118">Specifies a filter expression.</span></span>

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

### <span data-ttu-id="c9635-119">-Location</span><span class="sxs-lookup"><span data-stu-id="c9635-119">-Location</span></span>
<span data-ttu-id="c9635-120">확장의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9635-120">Specifies the location of an extension.</span></span>

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

### <span data-ttu-id="c9635-121">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="c9635-121">-PublisherName</span></span>
<span data-ttu-id="c9635-122">확장 게시자의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9635-122">Specifies the name of an extension publisher.</span></span>
<span data-ttu-id="c9635-123">확장 퍼블리셔를 얻은 경우 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9635-123">To obtain an extension publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="c9635-124">-Type</span><span class="sxs-lookup"><span data-stu-id="c9635-124">-Type</span></span>
<span data-ttu-id="c9635-125">확장의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9635-125">Specifies the type of the extension.</span></span>
<span data-ttu-id="c9635-126">확장 형식을 얻은 경우 Get-AzVMExtensionImageType cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9635-126">To obtain an extension type, use the Get-AzVMExtensionImageType cmdlet.</span></span>

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

### <span data-ttu-id="c9635-127">-Version</span><span class="sxs-lookup"><span data-stu-id="c9635-127">-Version</span></span>
<span data-ttu-id="c9635-128">이 cmdlet에서 얻을 확장 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9635-128">Specifies the version of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c9635-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9635-129">CommonParameters</span></span>
<span data-ttu-id="c9635-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9635-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9635-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9635-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9635-132">입력</span><span class="sxs-lookup"><span data-stu-id="c9635-132">INPUTS</span></span>

### <span data-ttu-id="c9635-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c9635-133">System.String</span></span>

## <span data-ttu-id="c9635-134">출력</span><span class="sxs-lookup"><span data-stu-id="c9635-134">OUTPUTS</span></span>

### <span data-ttu-id="c9635-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span><span class="sxs-lookup"><span data-stu-id="c9635-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImage</span></span>

### <span data-ttu-id="c9635-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span><span class="sxs-lookup"><span data-stu-id="c9635-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtensionImageDetails</span></span>

## <span data-ttu-id="c9635-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c9635-137">NOTES</span></span>

## <span data-ttu-id="c9635-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9635-138">RELATED LINKS</span></span>

[<span data-ttu-id="c9635-139">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="c9635-139">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="c9635-140">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="c9635-140">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="c9635-141">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c9635-141">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)


