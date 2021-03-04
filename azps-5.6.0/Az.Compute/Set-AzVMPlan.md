---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 9d3897b52d59c85caac3f68b9904878f14014606
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004555"
---
# <span data-ttu-id="42f39-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="42f39-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="42f39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42f39-102">SYNOPSIS</span></span>
<span data-ttu-id="42f39-103">가상 머신에서 Marketplace 계획 정보를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="42f39-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="42f39-104">구문</span><span class="sxs-lookup"><span data-stu-id="42f39-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42f39-105">설명</span><span class="sxs-lookup"><span data-stu-id="42f39-105">DESCRIPTION</span></span>
<span data-ttu-id="42f39-106">**Set-AzVMPlan** cmdlet은 가상 머신에 대한 Azure Marketplace 계획 정보를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="42f39-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="42f39-107">명령줄을 통해 Marketplace 이미지를 배포하기 전에 프로그래밍식 액세스를 사용하도록 설정해야 합니다. 또는 Azure Portal을 사용하여 가상 머신을 배포해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42f39-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="42f39-108">예제</span><span class="sxs-lookup"><span data-stu-id="42f39-108">EXAMPLES</span></span>

## <span data-ttu-id="42f39-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="42f39-109">PARAMETERS</span></span>

### <span data-ttu-id="42f39-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f39-110">-DefaultProfile</span></span>
<span data-ttu-id="42f39-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42f39-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42f39-112">-Name</span><span class="sxs-lookup"><span data-stu-id="42f39-112">-Name</span></span>
<span data-ttu-id="42f39-113">Marketplace에서 이미지의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42f39-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="42f39-114">이 값은 cmdlet에서 반환되는 Get-AzVMImageSku 값입니다.</span><span class="sxs-lookup"><span data-stu-id="42f39-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="42f39-115">이미지 정보를 찾는 방법에 대한 자세한 내용은 PowerShell 및 Azure CLI(Microsoft Azure 설명서)를 사용하여 Azure Virtual Machine 이미지의 검색 및 선택을 https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="42f39-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42f39-116">-Product</span><span class="sxs-lookup"><span data-stu-id="42f39-116">-Product</span></span>
<span data-ttu-id="42f39-117">Marketplace에서 이미지의 제품을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42f39-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="42f39-118">이는 **imageReference** 요소의 **제품** 값과 동일한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="42f39-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42f39-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="42f39-119">-PromotionCode</span></span>
<span data-ttu-id="42f39-120">프로모션 코드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42f39-120">Specifies a promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42f39-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="42f39-121">-Publisher</span></span>
<span data-ttu-id="42f39-122">이미지의 게시자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42f39-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="42f39-123">이 정보는 cmdlet을 사용하여 Get-AzVMImagePublisher 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42f39-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42f39-124">-VM</span><span class="sxs-lookup"><span data-stu-id="42f39-124">-VM</span></span>
<span data-ttu-id="42f39-125">Marketplace 계획을 설정할 가상 머신 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42f39-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="42f39-126">가상 머신 개체를 Get-AzVM cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42f39-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="42f39-127">New-AzVMConfig cmdlet을 사용하여 가상 머신 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42f39-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42f39-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f39-128">CommonParameters</span></span>
<span data-ttu-id="42f39-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42f39-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f39-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42f39-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f39-131">입력</span><span class="sxs-lookup"><span data-stu-id="42f39-131">INPUTS</span></span>

### <span data-ttu-id="42f39-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="42f39-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="42f39-133">System.String</span><span class="sxs-lookup"><span data-stu-id="42f39-133">System.String</span></span>

## <span data-ttu-id="42f39-134">출력</span><span class="sxs-lookup"><span data-stu-id="42f39-134">OUTPUTS</span></span>

### <span data-ttu-id="42f39-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="42f39-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="42f39-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="42f39-136">NOTES</span></span>

## <span data-ttu-id="42f39-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42f39-137">RELATED LINKS</span></span>

[<span data-ttu-id="42f39-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="42f39-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="42f39-139">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="42f39-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="42f39-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="42f39-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="42f39-141">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="42f39-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
