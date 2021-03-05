---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 4eea328b83b4d4ad70ba755e4875168b6b35ecb7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013744"
---
# <span data-ttu-id="51dca-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="51dca-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="51dca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51dca-102">SYNOPSIS</span></span>
<span data-ttu-id="51dca-103">VMImage SKUS를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51dca-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="51dca-104">구문</span><span class="sxs-lookup"><span data-stu-id="51dca-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51dca-105">설명</span><span class="sxs-lookup"><span data-stu-id="51dca-105">DESCRIPTION</span></span>
<span data-ttu-id="51dca-106">**Get-AzVMImageSku** cmdlet은 VMImage SKU를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51dca-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="51dca-107">예제</span><span class="sxs-lookup"><span data-stu-id="51dca-107">EXAMPLES</span></span>

### <span data-ttu-id="51dca-108">예제 1: VMImage SKUS를 얻다</span><span class="sxs-lookup"><span data-stu-id="51dca-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="51dca-109">이 명령은 지정된 게시자 및 제품용 SKUS를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51dca-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="51dca-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="51dca-110">PARAMETERS</span></span>

### <span data-ttu-id="51dca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51dca-111">-DefaultProfile</span></span>
<span data-ttu-id="51dca-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51dca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51dca-113">-Location</span><span class="sxs-lookup"><span data-stu-id="51dca-113">-Location</span></span>
<span data-ttu-id="51dca-114">VMImage의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51dca-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="51dca-115">-제품</span><span class="sxs-lookup"><span data-stu-id="51dca-115">-Offer</span></span>
<span data-ttu-id="51dca-116">VMImage 제품 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51dca-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="51dca-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="51dca-117">-PublisherName</span></span>
<span data-ttu-id="51dca-118">VMImage의 게시자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="51dca-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="51dca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51dca-119">CommonParameters</span></span>
<span data-ttu-id="51dca-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="51dca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51dca-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51dca-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51dca-122">입력</span><span class="sxs-lookup"><span data-stu-id="51dca-122">INPUTS</span></span>

### <span data-ttu-id="51dca-123">System.String</span><span class="sxs-lookup"><span data-stu-id="51dca-123">System.String</span></span>

## <span data-ttu-id="51dca-124">출력</span><span class="sxs-lookup"><span data-stu-id="51dca-124">OUTPUTS</span></span>

### <span data-ttu-id="51dca-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="51dca-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="51dca-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="51dca-126">NOTES</span></span>

## <span data-ttu-id="51dca-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51dca-127">RELATED LINKS</span></span>

[<span data-ttu-id="51dca-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="51dca-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="51dca-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="51dca-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="51dca-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="51dca-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="51dca-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="51dca-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


