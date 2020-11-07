---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
ms.openlocfilehash: c6c17978840fd5c446d7d89350f1792091a5cffa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702158"
---
# <span data-ttu-id="11c71-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="11c71-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="11c71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11c71-102">SYNOPSIS</span></span>
<span data-ttu-id="11c71-103">가상 컴퓨터에서 마켓플레이스 계획 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c71-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11c71-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11c71-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [<CommonParameters>]
```

## <span data-ttu-id="11c71-105">설명은</span><span class="sxs-lookup"><span data-stu-id="11c71-105">DESCRIPTION</span></span>
<span data-ttu-id="11c71-106">**AzureRmVMPlan** cmdlet은 가상 컴퓨터에 대 한 Azure 마켓플레이스 계획 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c71-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="11c71-107">명령줄을 통해 마켓플레이스 이미지를 배포 하기 전에 프로그래밍 방식 액세스를 사용 하도록 설정 하거나 Azure 포털을 사용 하 여 가상 컴퓨터를 배포 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c71-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="11c71-108">예제의</span><span class="sxs-lookup"><span data-stu-id="11c71-108">EXAMPLES</span></span>

## <span data-ttu-id="11c71-109">변수</span><span class="sxs-lookup"><span data-stu-id="11c71-109">PARAMETERS</span></span>

### <span data-ttu-id="11c71-110">-이름</span><span class="sxs-lookup"><span data-stu-id="11c71-110">-Name</span></span>
<span data-ttu-id="11c71-111">Marketplace에서 이미지의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c71-111">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="11c71-112">이것은 Get-AzureRmVMImageSku cmdlet에서 반환 되는 값과 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c71-112">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="11c71-113">이미지 정보를 찾는 방법에 대 한 자세한 내용은 PowerShell을 사용 하 여 [Azure 가상 컴퓨터 이미지 탐색 및 선택 및](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) Microsoft azure 설명서에서 azure CLI를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="11c71-113">For more information about how to find image information, see [Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLI](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c71-114">-제품</span><span class="sxs-lookup"><span data-stu-id="11c71-114">-Product</span></span>
<span data-ttu-id="11c71-115">Marketplace에서 이미지의 제품을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c71-115">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="11c71-116">이 정보는 **imageReference** 요소의 **제공** 값과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="11c71-116">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c71-117">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="11c71-117">-PromotionCode</span></span>
<span data-ttu-id="11c71-118">프로 모션 코드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c71-118">Specifies a promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c71-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="11c71-119">-Publisher</span></span>
<span data-ttu-id="11c71-120">이미지의 게시자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c71-120">Specifies the publisher of the image.</span></span>
<span data-ttu-id="11c71-121">Get-AzureRmVMImagePublisher cmdlet을 사용 하 여이 정보를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11c71-121">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c71-122">-VM</span><span class="sxs-lookup"><span data-stu-id="11c71-122">-VM</span></span>
<span data-ttu-id="11c71-123">마켓플레이스 계획을 설정할 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c71-123">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="11c71-124">Get-AzureRmVM cmdlet을 사용 하 여 가상 컴퓨터 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11c71-124">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="11c71-125">New-AzureRmVMConfig cmdlet을 사용 하 여 가상 컴퓨터 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11c71-125">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11c71-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c71-126">CommonParameters</span></span>
<span data-ttu-id="11c71-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c71-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c71-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11c71-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c71-129">입력</span><span class="sxs-lookup"><span data-stu-id="11c71-129">INPUTS</span></span>

### <span data-ttu-id="11c71-130">않아야</span><span class="sxs-lookup"><span data-stu-id="11c71-130">None</span></span>
<span data-ttu-id="11c71-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11c71-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="11c71-132">출력</span><span class="sxs-lookup"><span data-stu-id="11c71-132">OUTPUTS</span></span>

## <span data-ttu-id="11c71-133">상속자</span><span class="sxs-lookup"><span data-stu-id="11c71-133">NOTES</span></span>

## <span data-ttu-id="11c71-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11c71-134">RELATED LINKS</span></span>

[<span data-ttu-id="11c71-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="11c71-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="11c71-136">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="11c71-136">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="11c71-137">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="11c71-137">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="11c71-138">새로운 AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="11c71-138">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
