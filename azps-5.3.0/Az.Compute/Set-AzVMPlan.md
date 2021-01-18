---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 93837ff6618523f71fdd2b0a3b933b50892af429
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495910"
---
# <span data-ttu-id="5f0c7-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="5f0c7-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="5f0c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f0c7-102">SYNOPSIS</span></span>
<span data-ttu-id="5f0c7-103">가상 머신에서 Marketplace 계획 정보를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="5f0c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="5f0c7-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f0c7-105">설명</span><span class="sxs-lookup"><span data-stu-id="5f0c7-105">DESCRIPTION</span></span>
<span data-ttu-id="5f0c7-106">**Set-AzVMPlan** cmdlet은 가상 머신에 대한 Azure Marketplace 계획 정보를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="5f0c7-107">명령줄을 통해 Marketplace 이미지를 배포하려면 먼저 프로그래밍 액세스를 사용하도록 설정해야 합니다. 또는 Azure Portal을 사용하여 가상 머신을 배포해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="5f0c7-108">예제</span><span class="sxs-lookup"><span data-stu-id="5f0c7-108">EXAMPLES</span></span>

## <span data-ttu-id="5f0c7-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f0c7-109">PARAMETERS</span></span>

### <span data-ttu-id="5f0c7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f0c7-110">-DefaultProfile</span></span>
<span data-ttu-id="5f0c7-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f0c7-112">-Name</span><span class="sxs-lookup"><span data-stu-id="5f0c7-112">-Name</span></span>
<span data-ttu-id="5f0c7-113">Marketplace에서 이미지의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="5f0c7-114">이는 Get-AzVMImageSku cmdlet에서 반환되는 동일한 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="5f0c7-115">이미지 정보를 찾는 방법에 대한 자세한 내용은 PowerShell 및 Azure CLI(Microsoft Azure 설명서)를 사용하여 Azure Virtual Machine 이미지의 검색 및 선택을 https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="5f0c7-116">-Product</span><span class="sxs-lookup"><span data-stu-id="5f0c7-116">-Product</span></span>
<span data-ttu-id="5f0c7-117">Marketplace의 이미지 제품을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="5f0c7-118">**imageReference** 요소의 **제품** 값과 동일한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="5f0c7-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="5f0c7-119">-PromotionCode</span></span>
<span data-ttu-id="5f0c7-120">프로모션 코드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-120">Specifies a promotion code.</span></span>

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

### <span data-ttu-id="5f0c7-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="5f0c7-121">-Publisher</span></span>
<span data-ttu-id="5f0c7-122">이미지의 게시자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="5f0c7-123">이 정보는 다음 cmdlet을 사용하여 Get-AzVMImagePublisher 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="5f0c7-124">-VM</span><span class="sxs-lookup"><span data-stu-id="5f0c7-124">-VM</span></span>
<span data-ttu-id="5f0c7-125">Marketplace 계획을 설정할 가상 머신 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="5f0c7-126">가상 머신 개체를 Get-AzVM cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="5f0c7-127">New-AzVMConfig cmdlet을 사용하여 가상 머신 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="5f0c7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f0c7-128">CommonParameters</span></span>
<span data-ttu-id="5f0c7-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f0c7-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5f0c7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f0c7-131">입력</span><span class="sxs-lookup"><span data-stu-id="5f0c7-131">INPUTS</span></span>

### <span data-ttu-id="5f0c7-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5f0c7-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="5f0c7-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5f0c7-133">System.String</span></span>

## <span data-ttu-id="5f0c7-134">출력</span><span class="sxs-lookup"><span data-stu-id="5f0c7-134">OUTPUTS</span></span>

### <span data-ttu-id="5f0c7-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5f0c7-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5f0c7-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5f0c7-136">NOTES</span></span>

## <span data-ttu-id="5f0c7-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f0c7-137">RELATED LINKS</span></span>

[<span data-ttu-id="5f0c7-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="5f0c7-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="5f0c7-139">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="5f0c7-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="5f0c7-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="5f0c7-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="5f0c7-141">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="5f0c7-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
