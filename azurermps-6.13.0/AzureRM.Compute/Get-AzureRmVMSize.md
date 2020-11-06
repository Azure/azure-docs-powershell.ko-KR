---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: 9aca04a3b8bbccccd2950be30f0f13287997bcfb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532093"
---
# <span data-ttu-id="966ce-101">Get-AzureRmVMSize</span><span class="sxs-lookup"><span data-stu-id="966ce-101">Get-AzureRmVMSize</span></span>

## <span data-ttu-id="966ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="966ce-102">SYNOPSIS</span></span>
<span data-ttu-id="966ce-103">사용할 수 있는 가상 컴퓨터 크기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="966ce-103">Gets available virtual machine sizes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="966ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="966ce-104">SYNTAX</span></span>

### <span data-ttu-id="966ce-105">ListVirtualMachineSizeParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="966ce-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzureRmVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="966ce-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="966ce-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="966ce-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="966ce-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="966ce-108">설명은</span><span class="sxs-lookup"><span data-stu-id="966ce-108">DESCRIPTION</span></span>
<span data-ttu-id="966ce-109">**Get-AzureRmVMSize** cmdlet은 사용 가능한 가상 컴퓨터 크기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="966ce-109">The **Get-AzureRmVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="966ce-110">예제의</span><span class="sxs-lookup"><span data-stu-id="966ce-110">EXAMPLES</span></span>

### <span data-ttu-id="966ce-111">예제 1: 위치에 대 한 가상 컴퓨터 크기 가져오기</span><span class="sxs-lookup"><span data-stu-id="966ce-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

<span data-ttu-id="966ce-112">이 명령은 지정 된 위치에서 가상 컴퓨터에 사용할 수 있는 크기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="966ce-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="966ce-113">예제 2: 가용성 집합의 크기 가져오기</span><span class="sxs-lookup"><span data-stu-id="966ce-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="966ce-114">이 명령은 AvailabilitySet17 이라는 가용성 집합에 배포할 수 있는 가상 컴퓨터에 사용할 수 있는 크기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="966ce-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="966ce-115">예제 3: 기존 가상 컴퓨터의 크기 가져오기</span><span class="sxs-lookup"><span data-stu-id="966ce-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="966ce-116">이 명령은 VirtualMachine12 이라는 기존 가상 컴퓨터에 대해 사용 가능한 크기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="966ce-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="966ce-117">이 명령이 가져오는 크기에 맞게이 가상 컴퓨터의 크기를 조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="966ce-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="966ce-118">변수</span><span class="sxs-lookup"><span data-stu-id="966ce-118">PARAMETERS</span></span>

### <span data-ttu-id="966ce-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="966ce-119">-AvailabilitySetName</span></span>
<span data-ttu-id="966ce-120">이 cmdlet에서 사용 가능한 가상 컴퓨터 크기를 가져오는 가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="966ce-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="966ce-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="966ce-121">-DefaultProfile</span></span>
<span data-ttu-id="966ce-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="966ce-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="966ce-123">-위치</span><span class="sxs-lookup"><span data-stu-id="966ce-123">-Location</span></span>
<span data-ttu-id="966ce-124">이 cmdlet이 사용 가능한 가상 컴퓨터 크기를 가져오는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="966ce-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="966ce-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="966ce-125">-ResourceGroupName</span></span>
<span data-ttu-id="966ce-126">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="966ce-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="966ce-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="966ce-127">-VMName</span></span>
<span data-ttu-id="966ce-128">이 cmdlet이 크기를 조정할 수 있는 가상 컴퓨터 크기를 가져오는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="966ce-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="966ce-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="966ce-129">CommonParameters</span></span>
<span data-ttu-id="966ce-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="966ce-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="966ce-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="966ce-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="966ce-132">입력</span><span class="sxs-lookup"><span data-stu-id="966ce-132">INPUTS</span></span>

### <span data-ttu-id="966ce-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="966ce-133">System.String</span></span>

## <span data-ttu-id="966ce-134">출력</span><span class="sxs-lookup"><span data-stu-id="966ce-134">OUTPUTS</span></span>

### <span data-ttu-id="966ce-135">PSVirtualMachineSize를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="966ce-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="966ce-136">상속자</span><span class="sxs-lookup"><span data-stu-id="966ce-136">NOTES</span></span>

## <span data-ttu-id="966ce-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="966ce-137">RELATED LINKS</span></span>

[<span data-ttu-id="966ce-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="966ce-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


