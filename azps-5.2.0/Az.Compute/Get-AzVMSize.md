---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: e9ed9350b8ffdd93dd83843ee083c90bac786edd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369468"
---
# <span data-ttu-id="42d89-101">Get-AzVMSize</span><span class="sxs-lookup"><span data-stu-id="42d89-101">Get-AzVMSize</span></span>

## <span data-ttu-id="42d89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42d89-102">SYNOPSIS</span></span>
<span data-ttu-id="42d89-103">사용 가능한 가상 머신 크기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="42d89-103">Gets available virtual machine sizes.</span></span>

## <span data-ttu-id="42d89-104">구문</span><span class="sxs-lookup"><span data-stu-id="42d89-104">SYNTAX</span></span>

### <span data-ttu-id="42d89-105">ListVirtualMachineSizeParamSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="42d89-105">ListVirtualMachineSizeParamSet (Default)</span></span>
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42d89-106">ListAvailableSizesForAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="42d89-106">ListAvailableSizesForAvailabilitySet</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42d89-107">ListAvailableSizesForVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="42d89-107">ListAvailableSizesForVirtualMachine</span></span>
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42d89-108">설명</span><span class="sxs-lookup"><span data-stu-id="42d89-108">DESCRIPTION</span></span>
<span data-ttu-id="42d89-109">**Get-AzVMSize** cmdlet은 사용 가능한 가상 머신 크기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="42d89-109">The **Get-AzVMSize** cmdlet gets available virtual machine sizes.</span></span>

## <span data-ttu-id="42d89-110">예제</span><span class="sxs-lookup"><span data-stu-id="42d89-110">EXAMPLES</span></span>

### <span data-ttu-id="42d89-111">예제 1: 위치에 대한 가상 머신 크기 얻기</span><span class="sxs-lookup"><span data-stu-id="42d89-111">Example 1: Get virtual machine sizes for a location</span></span>
```
PS C:\> Get-AzVMSize -Location "Central US"
```

<span data-ttu-id="42d89-112">이 명령은 지정된 위치에 있는 가상 머신에 사용 가능한 크기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="42d89-112">This command gets the available sizes for virtual machines in the specified location.</span></span>

### <span data-ttu-id="42d89-113">예제 2: 가용성 집합의 크기 확인</span><span class="sxs-lookup"><span data-stu-id="42d89-113">Example 2: Get sizes for an availability set</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

<span data-ttu-id="42d89-114">이 명령은 AvailabilitySet17이라는 가용성 집합에 배포할 수 있는 가상 머신에 사용 가능한 크기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="42d89-114">This command gets available sizes for virtual machines that you can deploy in the availability set named AvailabilitySet17.</span></span>

### <span data-ttu-id="42d89-115">예제 3: 기존 가상 머신의 크기 얻기</span><span class="sxs-lookup"><span data-stu-id="42d89-115">Example 3: Get sizes for an existing virtual machine</span></span>
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

<span data-ttu-id="42d89-116">이 명령은 VirtualMachine12라는 기존 가상 머신에 사용 가능한 크기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="42d89-116">This command gets available sizes for the existing virtual machine named VirtualMachine12.</span></span>
<span data-ttu-id="42d89-117">이 명령에서 얻을 수 있는 크기로 이 가상 머신의 크기를조정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42d89-117">You can resize this virtual machine to the sizes that this command gets.</span></span>

## <span data-ttu-id="42d89-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42d89-118">PARAMETERS</span></span>

### <span data-ttu-id="42d89-119">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="42d89-119">-AvailabilitySetName</span></span>
<span data-ttu-id="42d89-120">이 cmdlet이 사용 가능한 가상 머신 크기를 얻을 가용성 집합의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42d89-120">Specifies the name of the Availability Set for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="42d89-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d89-121">-DefaultProfile</span></span>
<span data-ttu-id="42d89-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42d89-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42d89-123">-Location</span><span class="sxs-lookup"><span data-stu-id="42d89-123">-Location</span></span>
<span data-ttu-id="42d89-124">이 cmdlet에서 사용 가능한 가상 머신 크기를 얻을 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42d89-124">Specifies the location for which this cmdlet gets the available virtual machine sizes.</span></span>

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

### <span data-ttu-id="42d89-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42d89-125">-ResourceGroupName</span></span>
<span data-ttu-id="42d89-126">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42d89-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="42d89-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="42d89-127">-VMName</span></span>
<span data-ttu-id="42d89-128">이 cmdlet이 크기 조정에 사용할 수 있는 가상 머신 크기를 얻을 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42d89-128">Specifies the name of the virtual machine that this cmdlet gets the available virtual machine sizes for resizing.</span></span>

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

### <span data-ttu-id="42d89-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d89-129">CommonParameters</span></span>
<span data-ttu-id="42d89-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42d89-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d89-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="42d89-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d89-132">입력</span><span class="sxs-lookup"><span data-stu-id="42d89-132">INPUTS</span></span>

### <span data-ttu-id="42d89-133">System.String</span><span class="sxs-lookup"><span data-stu-id="42d89-133">System.String</span></span>

## <span data-ttu-id="42d89-134">출력</span><span class="sxs-lookup"><span data-stu-id="42d89-134">OUTPUTS</span></span>

### <span data-ttu-id="42d89-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="42d89-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineSize</span></span>

## <span data-ttu-id="42d89-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="42d89-136">NOTES</span></span>

## <span data-ttu-id="42d89-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42d89-137">RELATED LINKS</span></span>

[<span data-ttu-id="42d89-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="42d89-138">Get-AzVM</span></span>](./Get-AzVM.md)


