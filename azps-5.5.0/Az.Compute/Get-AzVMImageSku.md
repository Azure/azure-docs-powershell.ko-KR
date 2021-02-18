---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2BBAC5B-A7B9-44DA-BE37-24D89E03BAB3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageSku.md
ms.openlocfilehash: 9b67d2973296f1a497f6e22ee2f35e9ff4580b6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181692"
---
# <span data-ttu-id="9b133-101">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9b133-101">Get-AzVMImageSku</span></span>

## <span data-ttu-id="9b133-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b133-102">SYNOPSIS</span></span>
<span data-ttu-id="9b133-103">VMImage SKUS를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9b133-103">Gets VMImage SKUs.</span></span>

## <span data-ttu-id="9b133-104">구문</span><span class="sxs-lookup"><span data-stu-id="9b133-104">SYNTAX</span></span>

```
Get-AzVMImageSku -Location <String> -PublisherName <String> -Offer <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b133-105">설명</span><span class="sxs-lookup"><span data-stu-id="9b133-105">DESCRIPTION</span></span>
<span data-ttu-id="9b133-106">**Get-AzVMImageSku** cmdlet은 VMImage SKU를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9b133-106">The **Get-AzVMImageSku** cmdlet gets VMImage SKUs.</span></span>

## <span data-ttu-id="9b133-107">예제</span><span class="sxs-lookup"><span data-stu-id="9b133-107">EXAMPLES</span></span>

### <span data-ttu-id="9b133-108">예제 1: VMImage SKUS를 얻게</span><span class="sxs-lookup"><span data-stu-id="9b133-108">Example 1: Get VMImage SKUs</span></span>
```
PS C:\> Get-AzVMImageSku -Location "Central US" -PublisherName "Fabrikam" -Offer "LinuxServer"
```

<span data-ttu-id="9b133-109">이 명령은 지정된 게시자 및 제안에 대한 SKUS를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9b133-109">This command gets the SKUs for the specified publisher and offer.</span></span>

## <span data-ttu-id="9b133-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b133-110">PARAMETERS</span></span>

### <span data-ttu-id="9b133-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b133-111">-DefaultProfile</span></span>
<span data-ttu-id="9b133-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b133-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b133-113">-Location</span><span class="sxs-lookup"><span data-stu-id="9b133-113">-Location</span></span>
<span data-ttu-id="9b133-114">VMImage의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b133-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="9b133-115">-Offer</span><span class="sxs-lookup"><span data-stu-id="9b133-115">-Offer</span></span>
<span data-ttu-id="9b133-116">VMImage 제안의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b133-116">Specifies the type of VMImage offer.</span></span>

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

### <span data-ttu-id="9b133-117">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9b133-117">-PublisherName</span></span>
<span data-ttu-id="9b133-118">VMImage의 게시자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b133-118">Specifies the publisher of a VMImage.</span></span>

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

### <span data-ttu-id="9b133-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b133-119">CommonParameters</span></span>
<span data-ttu-id="9b133-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9b133-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b133-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9b133-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b133-122">입력</span><span class="sxs-lookup"><span data-stu-id="9b133-122">INPUTS</span></span>

### <span data-ttu-id="9b133-123">System.String</span><span class="sxs-lookup"><span data-stu-id="9b133-123">System.String</span></span>

## <span data-ttu-id="9b133-124">출력</span><span class="sxs-lookup"><span data-stu-id="9b133-124">OUTPUTS</span></span>

### <span data-ttu-id="9b133-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span><span class="sxs-lookup"><span data-stu-id="9b133-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageSku</span></span>

## <span data-ttu-id="9b133-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9b133-126">NOTES</span></span>

## <span data-ttu-id="9b133-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b133-127">RELATED LINKS</span></span>

[<span data-ttu-id="9b133-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9b133-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="9b133-129">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9b133-129">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="9b133-130">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9b133-130">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="9b133-131">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9b133-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


