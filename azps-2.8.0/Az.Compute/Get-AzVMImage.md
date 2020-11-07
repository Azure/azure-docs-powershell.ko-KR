---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 13871100efbe2fe62de769adcc40ee434e86eb21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697433"
---
# <span data-ttu-id="9ea9c-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9ea9c-101">Get-AzVMImage</span></span>

## <span data-ttu-id="9ea9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ea9c-102">SYNOPSIS</span></span>
<span data-ttu-id="9ea9c-103">모든 버전의 VMImage를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="9ea9c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ea9c-104">SYNTAX</span></span>

### <span data-ttu-id="9ea9c-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="9ea9c-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ea9c-106">GetVMImageDetail</span><span class="sxs-lookup"><span data-stu-id="9ea9c-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ea9c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9ea9c-107">DESCRIPTION</span></span>
<span data-ttu-id="9ea9c-108">**AzVMImage** Cmdlet은 VMImage의 모든 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="9ea9c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9ea9c-109">EXAMPLES</span></span>

### <span data-ttu-id="9ea9c-110">예제 1: VMImage 개체 가져오기</span><span class="sxs-lookup"><span data-stu-id="9ea9c-110">Example 1: Get VMImage objects</span></span>
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

<span data-ttu-id="9ea9c-111">이 명령은 지정 된 값과 일치 하는 모든 버전의 VMImage를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="9ea9c-112">예제 2: VMImage 개체 가져오기</span><span class="sxs-lookup"><span data-stu-id="9ea9c-112">Example 2: Get VMImage object</span></span>
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

<span data-ttu-id="9ea9c-113">이 명령은 지정 된 값과 일치 하는 특정 버전의 VMImage를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="9ea9c-114">예제 3: VMImage 개체 가져오기</span><span class="sxs-lookup"><span data-stu-id="9ea9c-114">Example 3: Get VMImage objects</span></span>
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

<span data-ttu-id="9ea9c-115">이 명령은 지정 된 값과 일치 하는 모든 버전의 VMImage를이에 대 한 필터링과 함께 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="9ea9c-116">변수</span><span class="sxs-lookup"><span data-stu-id="9ea9c-116">PARAMETERS</span></span>

### <span data-ttu-id="9ea9c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ea9c-117">-DefaultProfile</span></span>
<span data-ttu-id="9ea9c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ea9c-119">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="9ea9c-119">-FilterExpression</span></span>
<span data-ttu-id="9ea9c-120">필터 식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-120">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ea9c-121">-위치</span><span class="sxs-lookup"><span data-stu-id="9ea9c-121">-Location</span></span>
<span data-ttu-id="9ea9c-122">VMImage의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-122">Specifies the location of a VMImage.</span></span>

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

### <span data-ttu-id="9ea9c-123">-제공</span><span class="sxs-lookup"><span data-stu-id="9ea9c-123">-Offer</span></span>
<span data-ttu-id="9ea9c-124">VMImage 제안 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-124">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="9ea9c-125">이미지 제안을 얻으려면 Get-AzVMImageOffer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-125">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="9ea9c-126">-최신 Ername</span><span class="sxs-lookup"><span data-stu-id="9ea9c-126">-PublisherName</span></span>
<span data-ttu-id="9ea9c-127">VMImage의 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-127">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="9ea9c-128">이미지 게시자를 얻으려면 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-128">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="9ea9c-129">-Sku</span><span class="sxs-lookup"><span data-stu-id="9ea9c-129">-Skus</span></span>
<span data-ttu-id="9ea9c-130">VMImage SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-130">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="9ea9c-131">SKU를 얻으려면 Get-AzVMImageSku cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-131">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="9ea9c-132">-버전</span><span class="sxs-lookup"><span data-stu-id="9ea9c-132">-Version</span></span>
<span data-ttu-id="9ea9c-133">VMImage의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-133">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9ea9c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ea9c-134">CommonParameters</span></span>
<span data-ttu-id="9ea9c-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ea9c-136">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ea9c-137">입력</span><span class="sxs-lookup"><span data-stu-id="9ea9c-137">INPUTS</span></span>

### <span data-ttu-id="9ea9c-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9ea9c-138">System.String</span></span>

## <span data-ttu-id="9ea9c-139">출력</span><span class="sxs-lookup"><span data-stu-id="9ea9c-139">OUTPUTS</span></span>

### <span data-ttu-id="9ea9c-140">Microsoft. a \* PSVirtualMachineImage</span><span class="sxs-lookup"><span data-stu-id="9ea9c-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="9ea9c-141">Microsoft. a g m. a g m.</span><span class="sxs-lookup"><span data-stu-id="9ea9c-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="9ea9c-142">상속자</span><span class="sxs-lookup"><span data-stu-id="9ea9c-142">NOTES</span></span>

## <span data-ttu-id="9ea9c-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ea9c-143">RELATED LINKS</span></span>

[<span data-ttu-id="9ea9c-144">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9ea9c-144">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="9ea9c-145">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9ea9c-145">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="9ea9c-146">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9ea9c-146">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="9ea9c-147">저장-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9ea9c-147">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


