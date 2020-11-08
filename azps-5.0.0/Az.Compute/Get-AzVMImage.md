---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 350e03d6e238eb0cf1aa6b27da6b9a321603a664
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217634"
---
# <span data-ttu-id="e4bfc-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="e4bfc-101">Get-AzVMImage</span></span>

## <span data-ttu-id="e4bfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4bfc-102">SYNOPSIS</span></span>
<span data-ttu-id="e4bfc-103">모든 버전의 VMImage를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="e4bfc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e4bfc-104">SYNTAX</span></span>

### <span data-ttu-id="e4bfc-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="e4bfc-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> [-Top <Int32>]
 [-OrderBy <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4bfc-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="e4bfc-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4bfc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e4bfc-107">DESCRIPTION</span></span>
<span data-ttu-id="e4bfc-108">**AzVMImage** Cmdlet은 VMImage의 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="e4bfc-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e4bfc-109">EXAMPLES</span></span>

### <span data-ttu-id="e4bfc-110">예제 1: VMImage 개체 가져오기</span><span class="sxs-lookup"><span data-stu-id="e4bfc-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190104                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190115                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190204                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190218                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="e4bfc-111">이 명령은 지정 된 값과 일치 하는 모든 버전의 VMImage를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="e4bfc-112">예제 2: VMImage 개체 가져오기</span><span class="sxs-lookup"><span data-stu-id="e4bfc-112">Example 2: Get VMImage object</span></span>
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
FilterExpression :
Name             : 4.127.20180315
OSDiskImage      : {
                     "operatingSystem": "Windows"
                   }
PurchasePlan     : null
DataDiskImages   : []
```

<span data-ttu-id="e4bfc-113">이 명령은 지정 된 값과 일치 하는 특정 버전의 VMImage를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="e4bfc-114">예제 3: VMImage 개체 가져오기</span><span class="sxs-lookup"><span data-stu-id="e4bfc-114">Example 3: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.2018*

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="e4bfc-115">이 명령은 지정 된 값과 일치 하는 모든 버전의 VMImage를이에 대 한 필터링과 함께 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="e4bfc-116">변수</span><span class="sxs-lookup"><span data-stu-id="e4bfc-116">PARAMETERS</span></span>

### <span data-ttu-id="e4bfc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4bfc-117">-DefaultProfile</span></span>
<span data-ttu-id="e4bfc-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4bfc-119">-위치</span><span class="sxs-lookup"><span data-stu-id="e4bfc-119">-Location</span></span>
<span data-ttu-id="e4bfc-120">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-120">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="e4bfc-121">-제공</span><span class="sxs-lookup"><span data-stu-id="e4bfc-121">-Offer</span></span>
<span data-ttu-id="e4bfc-122">VMImage 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-122">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="e4bfc-123">이미지 제안을 얻으려면 Get-AzVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-123">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="e4bfc-124">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="e4bfc-124">-OrderBy</span></span>
<span data-ttu-id="e4bfc-125">반환 되는 결과의 순서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-125">Specifies the order of the results returned.</span></span> <span data-ttu-id="e4bfc-126">OData 쿼리로 형식이 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-126">Formatted as an OData query.</span></span>

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

### <span data-ttu-id="e4bfc-127">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="e4bfc-127">-PublisherName</span></span>
<span data-ttu-id="e4bfc-128">VMImage의 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-128">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="e4bfc-129">이미지 게시자를 얻으려면 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-129">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="e4bfc-130">-Sku</span><span class="sxs-lookup"><span data-stu-id="e4bfc-130">-Skus</span></span>
<span data-ttu-id="e4bfc-131">VMImage SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-131">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="e4bfc-132">SKU를 얻으려면 Get-AzVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-132">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="e4bfc-133">-위쪽</span><span class="sxs-lookup"><span data-stu-id="e4bfc-133">-Top</span></span>
<span data-ttu-id="e4bfc-134">반환 되는 최대 가상 머신 이미지 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-134">Specifies the maximum number of virtual machine images returned.</span></span> 

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

### <span data-ttu-id="e4bfc-135">-버전</span><span class="sxs-lookup"><span data-stu-id="e4bfc-135">-Version</span></span>
<span data-ttu-id="e4bfc-136">VMImage의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-136">Specifies the version of the VMImage.</span></span>

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

### <span data-ttu-id="e4bfc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4bfc-137">CommonParameters</span></span>
<span data-ttu-id="e4bfc-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4bfc-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4bfc-140">입력</span><span class="sxs-lookup"><span data-stu-id="e4bfc-140">INPUTS</span></span>

### <span data-ttu-id="e4bfc-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e4bfc-141">System.String</span></span>

## <span data-ttu-id="e4bfc-142">출력</span><span class="sxs-lookup"><span data-stu-id="e4bfc-142">OUTPUTS</span></span>

### <span data-ttu-id="e4bfc-143">Microsoft. a \* PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="e4bfc-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="e4bfc-144">Microsoft. a g m. a g m.</span><span class="sxs-lookup"><span data-stu-id="e4bfc-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="e4bfc-145">상속자</span><span class="sxs-lookup"><span data-stu-id="e4bfc-145">NOTES</span></span>

## <span data-ttu-id="e4bfc-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4bfc-146">RELATED LINKS</span></span>

[<span data-ttu-id="e4bfc-147">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="e4bfc-147">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="e4bfc-148">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e4bfc-148">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="e4bfc-149">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="e4bfc-149">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="e4bfc-150">저장-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="e4bfc-150">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


