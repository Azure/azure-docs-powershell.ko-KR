---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 93837ff6618523f71fdd2b0a3b933b50892af429
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044623"
---
# <span data-ttu-id="f0a19-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="f0a19-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="f0a19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0a19-102">SYNOPSIS</span></span>
<span data-ttu-id="f0a19-103">가상 컴퓨터에서 마켓플레이스 계획 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a19-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="f0a19-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0a19-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0a19-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f0a19-105">DESCRIPTION</span></span>
<span data-ttu-id="f0a19-106">**AzVMPlan** cmdlet은 가상 컴퓨터에 대 한 Azure 마켓플레이스 계획 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a19-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="f0a19-107">명령줄을 통해 마켓플레이스 이미지를 배포 하기 전에 프로그래밍 방식 액세스를 사용 하도록 설정 하거나 Azure 포털을 사용 하 여 가상 컴퓨터를 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a19-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="f0a19-108">예제의</span><span class="sxs-lookup"><span data-stu-id="f0a19-108">EXAMPLES</span></span>

## <span data-ttu-id="f0a19-109">변수</span><span class="sxs-lookup"><span data-stu-id="f0a19-109">PARAMETERS</span></span>

### <span data-ttu-id="f0a19-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0a19-110">-DefaultProfile</span></span>
<span data-ttu-id="f0a19-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f0a19-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0a19-112">-이름</span><span class="sxs-lookup"><span data-stu-id="f0a19-112">-Name</span></span>
<span data-ttu-id="f0a19-113">Marketplace에서 이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a19-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="f0a19-114">이것은 Get-AzVMImageSku cmdlet에서 반환 되는 값과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a19-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="f0a19-115">이미지 정보를 찾는 방법에 대 한 자세한 내용은 PowerShell 및 Azure CLI를 사용 하 여 Azure 가상 컴퓨터 이미지 탐색 및 선택 https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) Microsoft azure 설명서)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f0a19-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="f0a19-116">-제품</span><span class="sxs-lookup"><span data-stu-id="f0a19-116">-Product</span></span>
<span data-ttu-id="f0a19-117">Marketplace에서 이미지의 제품을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a19-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="f0a19-118">이 정보는 **imageReference** 요소의 **제공** 값과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f0a19-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="f0a19-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="f0a19-119">-PromotionCode</span></span>
<span data-ttu-id="f0a19-120">프로 모션 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a19-120">Specifies a promotion code.</span></span>

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

### <span data-ttu-id="f0a19-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f0a19-121">-Publisher</span></span>
<span data-ttu-id="f0a19-122">이미지의 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a19-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="f0a19-123">Get-AzVMImagePublisher cmdlet을 사용 하 여이 정보를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0a19-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="f0a19-124">-VM</span><span class="sxs-lookup"><span data-stu-id="f0a19-124">-VM</span></span>
<span data-ttu-id="f0a19-125">마켓플레이스 계획을 설정할 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a19-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="f0a19-126">Get-AzVM cmdlet을 사용 하 여 가상 컴퓨터 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0a19-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="f0a19-127">New-AzVMConfig cmdlet을 사용 하 여 가상 컴퓨터 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0a19-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="f0a19-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0a19-128">CommonParameters</span></span>
<span data-ttu-id="f0a19-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a19-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0a19-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f0a19-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0a19-131">입력</span><span class="sxs-lookup"><span data-stu-id="f0a19-131">INPUTS</span></span>

### <span data-ttu-id="f0a19-132">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a19-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="f0a19-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f0a19-133">System.String</span></span>

## <span data-ttu-id="f0a19-134">출력</span><span class="sxs-lookup"><span data-stu-id="f0a19-134">OUTPUTS</span></span>

### <span data-ttu-id="f0a19-135">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0a19-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="f0a19-136">상속자</span><span class="sxs-lookup"><span data-stu-id="f0a19-136">NOTES</span></span>

## <span data-ttu-id="f0a19-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0a19-137">RELATED LINKS</span></span>

[<span data-ttu-id="f0a19-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="f0a19-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="f0a19-139">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f0a19-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="f0a19-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f0a19-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="f0a19-141">새로운 AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="f0a19-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
