---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 0075b057cecb91b618d06ad36788801a672268aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958955"
---
# <span data-ttu-id="dc35e-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="dc35e-101">Get-AzVMImage</span></span>

## <span data-ttu-id="dc35e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc35e-102">SYNOPSIS</span></span>
<span data-ttu-id="dc35e-103">VMImage의 모든 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="dc35e-104">구문</span><span class="sxs-lookup"><span data-stu-id="dc35e-104">SYNTAX</span></span>

### <span data-ttu-id="dc35e-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="dc35e-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> [-Top <Int32>]
 [-OrderBy <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc35e-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="dc35e-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc35e-107">설명</span><span class="sxs-lookup"><span data-stu-id="dc35e-107">DESCRIPTION</span></span>
<span data-ttu-id="dc35e-108">**Get-AzVMImage** cmdlet은 VMImage의 모든 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="dc35e-109">예제</span><span class="sxs-lookup"><span data-stu-id="dc35e-109">EXAMPLES</span></span>

### <span data-ttu-id="dc35e-110">예제 1: VMImage 개체 얻기</span><span class="sxs-lookup"><span data-stu-id="dc35e-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"

Version        Skus               Offer         PublisherName          Location  Id
-------        ----               -----         -------------          --------  --
4.127.20180315 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190104 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190115 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190204 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190218 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="dc35e-111">이 명령은 지정된 값과 일치하는 VMImage의 모든 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="dc35e-112">예제 2: VMImage 개체 얻기</span><span class="sxs-lookup"><span data-stu-id="dc35e-112">Example 2: Get VMImage object</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.20180315

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/centralus/
                   Publishers/MicrosoftWindowsServer/ArtifactTypes/VMImage/Offers/windowsserver/Skus/2012-R2-Datacenter
                   /Versions/4.127.20180315
Location         : centralus
PublisherName    : MicrosoftWindowsServer
Offer            : windowsserver
Skus             : 2012-R2-Datacenter
Version          : 4.127.20180315
Name             : 4.127.20180315
OSDiskImage      : {
                     "operatingSystem": "Windows"
                   }
PurchasePlan     : null
DataDiskImages   : []
```

<span data-ttu-id="dc35e-113">이 명령은 지정된 값과 일치하는 특정 버전의 VMImage를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="dc35e-114">예제 3: VMImage 개체 얻기</span><span class="sxs-lookup"><span data-stu-id="dc35e-114">Example 3: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.2018*

Version        Skus               Offer         PublisherName          Location  Id
-------        ----               -----         -------------          --------  --
4.127.20180315 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125 2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="dc35e-115">이 명령은 지정된 값과 버전 필터링에 일치하는 VMImage의 모든 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="dc35e-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="dc35e-116">PARAMETERS</span></span>

### <span data-ttu-id="dc35e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc35e-117">-DefaultProfile</span></span>
<span data-ttu-id="dc35e-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc35e-119">-Location</span><span class="sxs-lookup"><span data-stu-id="dc35e-119">-Location</span></span>
<span data-ttu-id="dc35e-120">VMImage의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-120">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="dc35e-121">-제품</span><span class="sxs-lookup"><span data-stu-id="dc35e-121">-Offer</span></span>
<span data-ttu-id="dc35e-122">VMImage 제품 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-122">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="dc35e-123">이미지 제안을 얻은 경우 Get-AzVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-123">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="dc35e-124">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="dc35e-124">-OrderBy</span></span>
<span data-ttu-id="dc35e-125">반환된 결과의 순서를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-125">Specifies the order of the results returned.</span></span> <span data-ttu-id="dc35e-126">OData 쿼리로 서식이 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-126">Formatted as an OData query.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc35e-127">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="dc35e-127">-PublisherName</span></span>
<span data-ttu-id="dc35e-128">VMImage의 게시자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-128">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="dc35e-129">이미지 퍼블리셔를 얻은 경우 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-129">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="dc35e-130">-Skus</span><span class="sxs-lookup"><span data-stu-id="dc35e-130">-Skus</span></span>
<span data-ttu-id="dc35e-131">VMImage SKU를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-131">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="dc35e-132">SKU를 얻지 위해 Get-AzVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-132">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="dc35e-133">-Top</span><span class="sxs-lookup"><span data-stu-id="dc35e-133">-Top</span></span>
<span data-ttu-id="dc35e-134">반환된 가상 머신 이미지의 최대 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-134">Specifies the maximum number of virtual machine images returned.</span></span> 

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc35e-135">-Version</span><span class="sxs-lookup"><span data-stu-id="dc35e-135">-Version</span></span>
<span data-ttu-id="dc35e-136">VMImage 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-136">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc35e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc35e-137">CommonParameters</span></span>
<span data-ttu-id="dc35e-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc35e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc35e-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc35e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc35e-140">입력</span><span class="sxs-lookup"><span data-stu-id="dc35e-140">INPUTS</span></span>

### <span data-ttu-id="dc35e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="dc35e-141">System.String</span></span>

## <span data-ttu-id="dc35e-142">출력</span><span class="sxs-lookup"><span data-stu-id="dc35e-142">OUTPUTS</span></span>

### <span data-ttu-id="dc35e-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="dc35e-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="dc35e-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span><span class="sxs-lookup"><span data-stu-id="dc35e-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="dc35e-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dc35e-145">NOTES</span></span>

## <span data-ttu-id="dc35e-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc35e-146">RELATED LINKS</span></span>

[<span data-ttu-id="dc35e-147">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="dc35e-147">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="dc35e-148">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="dc35e-148">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="dc35e-149">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="dc35e-149">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="dc35e-150">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="dc35e-150">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


