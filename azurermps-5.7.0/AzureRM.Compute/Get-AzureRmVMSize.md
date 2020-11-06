---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: d75ff7f549ddb1efd9f5640b9b2d634449faa21c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531101"
---
# <span data-ttu-id="e02ce-101">Get-AzureRmVMSize</span><span class="sxs-lookup"><span data-stu-id="e02ce-101">Get-AzureRmVMSize</span></span>

## <span data-ttu-id="e02ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e02ce-102">SYNOPSIS</span></span>
<span data-ttu-id="e02ce-103">사용할 수 있는 가상 컴퓨터 크기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e02ce-103">Gets available virtual machine sizes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e02ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e02ce-104">SYNTAX</span></span>

### <span data-ttu-id="e02ce-105">ListVirtualMachineSizeParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e02ce-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzureRmVMSize [-Location] <String> [<CommonParameters>]
```

### <span data-ttu-id="e02ce-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e02ce-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="e02ce-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e02ce-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [<CommonParameters>]
```

## <span data-ttu-id="e02ce-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e02ce-108">DESCRIPTION</span></span>
<span data-ttu-id="e02ce-109">**Get-AzureRmVMSize** cmdlet은 사용 가능한 가상 컴퓨터 크기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e02ce-109">The **Get-AzureRmVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="e02ce-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e02ce-110">EXAMPLES</span></span>

### <span data-ttu-id="e02ce-111">예제 1: 위치에 대 한 가상 컴퓨터 크기 가져오기</span><span class="sxs-lookup"><span data-stu-id="e02ce-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

<span data-ttu-id="e02ce-112">이 명령은 지정 된 위치에서 가상 컴퓨터에 사용할 수 있는 크기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e02ce-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="e02ce-113">예제 2: 가용성 집합의 크기 가져오기</span><span class="sxs-lookup"><span data-stu-id="e02ce-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="e02ce-114">이 명령은 AvailabilitySet17 이라는 가용성 집합에 배포할 수 있는 가상 컴퓨터에 사용할 수 있는 크기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e02ce-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="e02ce-115">예제 3: 기존 가상 컴퓨터의 크기 가져오기</span><span class="sxs-lookup"><span data-stu-id="e02ce-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="e02ce-116">이 명령은 VirtualMachine12 이라는 기존 가상 컴퓨터에 대해 사용 가능한 크기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e02ce-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="e02ce-117">이 명령이 가져오는 크기에 맞게이 가상 컴퓨터의 크기를 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e02ce-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="e02ce-118">변수</span><span class="sxs-lookup"><span data-stu-id="e02ce-118">PARAMETERS</span></span>

### <span data-ttu-id="e02ce-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="e02ce-119">-AvailabilitySetName</span></span>
<span data-ttu-id="e02ce-120">이 cmdlet에서 사용 가능한 가상 컴퓨터 크기를 가져오는 가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e02ce-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02ce-121">-위치</span><span class="sxs-lookup"><span data-stu-id="e02ce-121">-Location</span></span>
<span data-ttu-id="e02ce-122">이 cmdlet이 사용 가능한 가상 컴퓨터 크기를 가져오는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e02ce-122">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02ce-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e02ce-123">-ResourceGroupName</span></span>
<span data-ttu-id="e02ce-124">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e02ce-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02ce-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="e02ce-125">-VMName</span></span>
<span data-ttu-id="e02ce-126">이 cmdlet이 크기를 조정할 수 있는 가상 컴퓨터 크기를 가져오는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e02ce-126">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02ce-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02ce-127">CommonParameters</span></span>
<span data-ttu-id="e02ce-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e02ce-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02ce-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e02ce-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02ce-130">입력</span><span class="sxs-lookup"><span data-stu-id="e02ce-130">INPUTS</span></span>

### <span data-ttu-id="e02ce-131">않아야</span><span class="sxs-lookup"><span data-stu-id="e02ce-131">None</span></span>
<span data-ttu-id="e02ce-132">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e02ce-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e02ce-133">출력</span><span class="sxs-lookup"><span data-stu-id="e02ce-133">OUTPUTS</span></span>

## <span data-ttu-id="e02ce-134">상속자</span><span class="sxs-lookup"><span data-stu-id="e02ce-134">NOTES</span></span>

## <span data-ttu-id="e02ce-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e02ce-135">RELATED LINKS</span></span>

[<span data-ttu-id="e02ce-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e02ce-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


