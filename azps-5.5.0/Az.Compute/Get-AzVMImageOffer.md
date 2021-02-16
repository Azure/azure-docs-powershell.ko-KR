---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: bd434bae36bc48d5c06bee1ed5fa77673ac426ec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199300"
---
# <span data-ttu-id="92913-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="92913-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="92913-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92913-102">SYNOPSIS</span></span>
<span data-ttu-id="92913-103">VMImage 제품 유형을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="92913-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="92913-104">구문</span><span class="sxs-lookup"><span data-stu-id="92913-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92913-105">설명</span><span class="sxs-lookup"><span data-stu-id="92913-105">DESCRIPTION</span></span>
<span data-ttu-id="92913-106">**Get-AzVMImageOffer** cmdlet은 VMImage 제품 유형을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="92913-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="92913-107">예제</span><span class="sxs-lookup"><span data-stu-id="92913-107">EXAMPLES</span></span>

### <span data-ttu-id="92913-108">예제 1: 게시자에 대한 제품 유형 얻기</span><span class="sxs-lookup"><span data-stu-id="92913-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="92913-109">이 명령은 미국 중부 지역의 지정된 게시자에 대한 제품 유형을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="92913-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="92913-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92913-110">PARAMETERS</span></span>

### <span data-ttu-id="92913-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92913-111">-DefaultProfile</span></span>
<span data-ttu-id="92913-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92913-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92913-113">-Location</span><span class="sxs-lookup"><span data-stu-id="92913-113">-Location</span></span>
<span data-ttu-id="92913-114">VMImage의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="92913-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="92913-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="92913-115">-PublisherName</span></span>
<span data-ttu-id="92913-116">VMImage의 게시자 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="92913-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="92913-117">게시자를 얻습니다. Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="92913-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="92913-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92913-118">CommonParameters</span></span>
<span data-ttu-id="92913-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="92913-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92913-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="92913-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92913-121">입력</span><span class="sxs-lookup"><span data-stu-id="92913-121">INPUTS</span></span>

### <span data-ttu-id="92913-122">System.String</span><span class="sxs-lookup"><span data-stu-id="92913-122">System.String</span></span>

## <span data-ttu-id="92913-123">출력</span><span class="sxs-lookup"><span data-stu-id="92913-123">OUTPUTS</span></span>

### <span data-ttu-id="92913-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="92913-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="92913-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="92913-125">NOTES</span></span>

## <span data-ttu-id="92913-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92913-126">RELATED LINKS</span></span>

[<span data-ttu-id="92913-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="92913-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="92913-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="92913-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="92913-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="92913-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="92913-130">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="92913-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


