---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 33847b9a86d5fa39511102e964f8f2a63fce6960
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210072"
---
# <span data-ttu-id="9440c-101">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="9440c-101">Get-AzVmssVM</span></span>

## <span data-ttu-id="9440c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9440c-102">SYNOPSIS</span></span>
<span data-ttu-id="9440c-103">VMSS 가상 머신의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-103">Gets the properties of a VMSS virtual machine.</span></span>

## <span data-ttu-id="9440c-104">구문</span><span class="sxs-lookup"><span data-stu-id="9440c-104">SYNTAX</span></span>

### <span data-ttu-id="9440c-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="9440c-105">DefaultParameter (Default)</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9440c-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="9440c-106">FriendMethod</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9440c-107">설명</span><span class="sxs-lookup"><span data-stu-id="9440c-107">DESCRIPTION</span></span>
<span data-ttu-id="9440c-108">**Get-AzVmssVM** cmdlet은 VMSS(Virtual Machine Scale Set) 가상 머신의 모델 보기 및 인스턴스 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-108">The **Get-AzVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="9440c-109">모델 보기는 가상 머신의 사용자 지정 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="9440c-110">인스턴스 보기는 가상 머신의 인스턴스 수준 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="9440c-111">가상 *머신의* 인스턴스 보기만 얻게 하는 상태 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="9440c-112">예제</span><span class="sxs-lookup"><span data-stu-id="9440c-112">EXAMPLES</span></span>

### <span data-ttu-id="9440c-113">예제 1: VMSS 가상 머신의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="9440c-114">이 명령은 Group001이라는 리소스 그룹에 속하는 VMSS001이라는 VMSS 가상 머신의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="9440c-115">이 명령은 *InstanceView* 스위치 매개 변수를 지정하지 않습니다. cmdlet은 가상 머신의 모델 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="9440c-116">예제 2: VMSS 가상 머신의 모델 보기 속성 보기</span><span class="sxs-lookup"><span data-stu-id="9440c-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="9440c-117">이 명령은 Group002라는 리소스 그룹에 속하는 VMSS004라는 VMSS 가상 머신의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="9440c-118">이 명령은 모델 보기를 $ID 변수에 저장된 인스턴스 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="9440c-119">예제 3: VMSS 가상 머신의 인스턴스 보기 속성 얻음</span><span class="sxs-lookup"><span data-stu-id="9440c-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="9440c-120">이 명령은 Group002라는 리소스 그룹에 속하는 VMSS004라는 VMSS 가상 머신의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="9440c-121">이 명령은 *InstanceView* 스위치 매개 변수를 지정하기 때문에 cmdlet은 가상 머신의 인스턴스 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="9440c-122">이 명령은 인스턴스 보기를 $ID 변수에 저장된 인스턴스 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="9440c-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9440c-123">PARAMETERS</span></span>

### <span data-ttu-id="9440c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9440c-124">-DefaultProfile</span></span>
<span data-ttu-id="9440c-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9440c-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="9440c-126">-InstanceId</span></span>
<span data-ttu-id="9440c-127">모델 보기를 얻을 인스턴스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-127">Specifies the instance ID for which to get the model view.</span></span>

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

### <span data-ttu-id="9440c-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="9440c-128">-InstanceView</span></span>
<span data-ttu-id="9440c-129">이 cmdlet이 가상 머신의 인스턴스 보기만 얻게 된다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9440c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9440c-130">-ResourceGroupName</span></span>
<span data-ttu-id="9440c-131">VMSS의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9440c-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9440c-132">-VMScaleSetName</span></span>
<span data-ttu-id="9440c-133">VMSS의 이름 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9440c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9440c-134">CommonParameters</span></span>
<span data-ttu-id="9440c-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9440c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9440c-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9440c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9440c-137">입력</span><span class="sxs-lookup"><span data-stu-id="9440c-137">INPUTS</span></span>

### <span data-ttu-id="9440c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="9440c-138">System.String</span></span>

## <span data-ttu-id="9440c-139">출력</span><span class="sxs-lookup"><span data-stu-id="9440c-139">OUTPUTS</span></span>

### <span data-ttu-id="9440c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="9440c-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="9440c-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9440c-141">NOTES</span></span>

## <span data-ttu-id="9440c-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9440c-142">RELATED LINKS</span></span>

[<span data-ttu-id="9440c-143">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="9440c-143">Set-AzVmssVM</span></span>](./Set-AzVmssVM.md)

[<span data-ttu-id="9440c-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9440c-144">Get-AzVmss</span></span>](./Get-AzVmss.md)


