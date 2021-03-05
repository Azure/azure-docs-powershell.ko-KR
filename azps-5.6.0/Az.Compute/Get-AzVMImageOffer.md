---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: 94556ce0b78b90ae9c418aee175f090e9209adb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013808"
---
# <span data-ttu-id="a9778-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="a9778-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="a9778-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9778-102">SYNOPSIS</span></span>
<span data-ttu-id="a9778-103">VMImage 제품 형식을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9778-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="a9778-104">구문</span><span class="sxs-lookup"><span data-stu-id="a9778-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9778-105">설명</span><span class="sxs-lookup"><span data-stu-id="a9778-105">DESCRIPTION</span></span>
<span data-ttu-id="a9778-106">**Get-AzVMImageOffer** cmdlet은 VMImage 제품 형식을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9778-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="a9778-107">예제</span><span class="sxs-lookup"><span data-stu-id="a9778-107">EXAMPLES</span></span>

### <span data-ttu-id="a9778-108">예제 1: 퍼블리셔에 대한 제품 유형 얻기</span><span class="sxs-lookup"><span data-stu-id="a9778-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="a9778-109">이 명령은 미국 중부 지역의 지정된 게시자에 대한 제품 형식을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a9778-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="a9778-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a9778-110">PARAMETERS</span></span>

### <span data-ttu-id="a9778-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9778-111">-DefaultProfile</span></span>
<span data-ttu-id="a9778-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9778-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9778-113">-Location</span><span class="sxs-lookup"><span data-stu-id="a9778-113">-Location</span></span>
<span data-ttu-id="a9778-114">VMImage의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9778-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="a9778-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="a9778-115">-PublisherName</span></span>
<span data-ttu-id="a9778-116">VMImage의 게시자의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a9778-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="a9778-117">퍼블리셔를 얻지 위해 Get-AzVMImagePublisher cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9778-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="a9778-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9778-118">CommonParameters</span></span>
<span data-ttu-id="a9778-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a9778-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9778-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9778-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9778-121">입력</span><span class="sxs-lookup"><span data-stu-id="a9778-121">INPUTS</span></span>

### <span data-ttu-id="a9778-122">System.String</span><span class="sxs-lookup"><span data-stu-id="a9778-122">System.String</span></span>

## <span data-ttu-id="a9778-123">출력</span><span class="sxs-lookup"><span data-stu-id="a9778-123">OUTPUTS</span></span>

### <span data-ttu-id="a9778-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="a9778-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="a9778-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a9778-125">NOTES</span></span>

## <span data-ttu-id="a9778-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9778-126">RELATED LINKS</span></span>

[<span data-ttu-id="a9778-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a9778-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="a9778-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="a9778-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="a9778-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="a9778-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="a9778-130">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a9778-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


