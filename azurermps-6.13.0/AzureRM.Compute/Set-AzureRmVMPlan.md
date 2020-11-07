---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMPlan.md
ms.openlocfilehash: c09ef052807ab09059e9f5a2822aac4e5616175c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702621"
---
# <span data-ttu-id="8254a-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="8254a-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="8254a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8254a-102">SYNOPSIS</span></span>
<span data-ttu-id="8254a-103">가상 컴퓨터에서 마켓플레이스 계획 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8254a-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8254a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8254a-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8254a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8254a-105">DESCRIPTION</span></span>
<span data-ttu-id="8254a-106">**AzureRmVMPlan** cmdlet은 가상 컴퓨터에 대 한 Azure 마켓플레이스 계획 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8254a-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="8254a-107">명령줄을 통해 마켓플레이스 이미지를 배포 하기 전에 프로그래밍 방식 액세스를 사용 하도록 설정 하거나 Azure 포털을 사용 하 여 가상 컴퓨터를 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8254a-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="8254a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="8254a-108">EXAMPLES</span></span>

## <span data-ttu-id="8254a-109">변수</span><span class="sxs-lookup"><span data-stu-id="8254a-109">PARAMETERS</span></span>

### <span data-ttu-id="8254a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8254a-110">-DefaultProfile</span></span>
<span data-ttu-id="8254a-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8254a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8254a-112">-이름</span><span class="sxs-lookup"><span data-stu-id="8254a-112">-Name</span></span>
<span data-ttu-id="8254a-113">Marketplace에서 이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8254a-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="8254a-114">이것은 Get-AzureRmVMImageSku cmdlet에서 반환 되는 값과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="8254a-114">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="8254a-115">이미지 정보를 찾는 방법에 대 한 자세한 내용은 PowerShell 및 Azure CLI를 사용 하 여 Azure 가상 컴퓨터 이미지 탐색 및 선택 https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) Microsoft azure 설명서)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8254a-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="8254a-116">-제품</span><span class="sxs-lookup"><span data-stu-id="8254a-116">-Product</span></span>
<span data-ttu-id="8254a-117">Marketplace에서 이미지의 제품을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8254a-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="8254a-118">이 정보는 **imageReference** 요소의 **제공** 값과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8254a-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="8254a-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="8254a-119">-PromotionCode</span></span>
<span data-ttu-id="8254a-120">프로 모션 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8254a-120">Specifies a promotion code.</span></span>

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

### <span data-ttu-id="8254a-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8254a-121">-Publisher</span></span>
<span data-ttu-id="8254a-122">이미지의 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8254a-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="8254a-123">Get-AzureRmVMImagePublisher cmdlet을 사용 하 여이 정보를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8254a-123">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="8254a-124">-VM</span><span class="sxs-lookup"><span data-stu-id="8254a-124">-VM</span></span>
<span data-ttu-id="8254a-125">마켓플레이스 계획을 설정할 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8254a-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="8254a-126">Get-AzureRmVM cmdlet을 사용 하 여 가상 컴퓨터 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8254a-126">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="8254a-127">New-AzureRmVMConfig cmdlet을 사용 하 여 가상 컴퓨터 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8254a-127">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="8254a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8254a-128">CommonParameters</span></span>
<span data-ttu-id="8254a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8254a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8254a-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8254a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8254a-131">입력</span><span class="sxs-lookup"><span data-stu-id="8254a-131">INPUTS</span></span>

### <span data-ttu-id="8254a-132">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="8254a-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="8254a-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8254a-133">System.String</span></span>

## <span data-ttu-id="8254a-134">출력</span><span class="sxs-lookup"><span data-stu-id="8254a-134">OUTPUTS</span></span>

### <span data-ttu-id="8254a-135">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="8254a-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="8254a-136">상속자</span><span class="sxs-lookup"><span data-stu-id="8254a-136">NOTES</span></span>

## <span data-ttu-id="8254a-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8254a-137">RELATED LINKS</span></span>

[<span data-ttu-id="8254a-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8254a-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="8254a-139">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8254a-139">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="8254a-140">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="8254a-140">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="8254a-141">새로운 AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="8254a-141">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
