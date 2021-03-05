---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 1ac6f9b17f954361d95e6855a618c7dbbf3d20f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001787"
---
# <span data-ttu-id="cd233-101">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="cd233-101">Get-AzVmssVM</span></span>

## <span data-ttu-id="cd233-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd233-102">SYNOPSIS</span></span>
<span data-ttu-id="cd233-103">VMSS 가상 머신의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-103">Gets the properties of a VMSS virtual machine.</span></span>

## <span data-ttu-id="cd233-104">구문</span><span class="sxs-lookup"><span data-stu-id="cd233-104">SYNTAX</span></span>

### <span data-ttu-id="cd233-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="cd233-105">DefaultParameter (Default)</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd233-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="cd233-106">FriendMethod</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd233-107">설명</span><span class="sxs-lookup"><span data-stu-id="cd233-107">DESCRIPTION</span></span>
<span data-ttu-id="cd233-108">**Get-AzVmssVM** cmdlet은 VMSS(Virtual Machine Scale Set) 가상 머신의 모델 보기 및 인스턴스 보기를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-108">The **Get-AzVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="cd233-109">모델 보기는 가상 머신의 사용자 지정 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="cd233-110">인스턴스 보기는 가상 머신의 인스턴스 수준 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="cd233-111">상태 매개 *변수를* 지정하여 가상 머신의 인스턴스 보기만 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="cd233-112">예제</span><span class="sxs-lookup"><span data-stu-id="cd233-112">EXAMPLES</span></span>

### <span data-ttu-id="cd233-113">예제 1: VMSS 가상 머신의 속성 얻음</span><span class="sxs-lookup"><span data-stu-id="cd233-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="cd233-114">이 명령은 Group001이라는 리소스 그룹에 속하는 VMSS001이라는 VMSS 가상 머신의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="cd233-115">명령은 *InstanceView* 스위치 매개 변수를 지정하지 않습니다. cmdlet은 가상 머신의 모델 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="cd233-116">예제 2: VMSS 가상 머신의 모델 보기 속성 얻음</span><span class="sxs-lookup"><span data-stu-id="cd233-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="cd233-117">이 명령은 Group002라는 리소스 그룹에 속하는 VMSS004라는 VMSS 가상 머신의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="cd233-118">명령은 모델 보기를 얻을 수 $ID 변수에 저장된 인스턴스 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="cd233-119">예제 3: VMSS 가상 머신의 인스턴스 보기 속성 얻음</span><span class="sxs-lookup"><span data-stu-id="cd233-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="cd233-120">이 명령은 Group002라는 리소스 그룹에 속하는 VMSS004라는 VMSS 가상 머신의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="cd233-121">명령은 *InstanceView* 스위치 매개 변수를 지정하기 때문에 cmdlet은 가상 머신의 인스턴스 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="cd233-122">명령은 인스턴스 보기를 얻을 수 있는 $ID 변수에 저장된 인스턴스 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="cd233-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cd233-123">PARAMETERS</span></span>

### <span data-ttu-id="cd233-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd233-124">-DefaultProfile</span></span>
<span data-ttu-id="cd233-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd233-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="cd233-126">-InstanceId</span></span>
<span data-ttu-id="cd233-127">모델 보기를 얻을 인스턴스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-127">Specifies the instance ID for which to get the model view.</span></span>

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

### <span data-ttu-id="cd233-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="cd233-128">-InstanceView</span></span>
<span data-ttu-id="cd233-129">이 cmdlet은 가상 머신의 인스턴스 보기만 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="cd233-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd233-130">-ResourceGroupName</span></span>
<span data-ttu-id="cd233-131">VMSS의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="cd233-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cd233-132">-VMScaleSetName</span></span>
<span data-ttu-id="cd233-133">VMSS의 이름을 종으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-133">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="cd233-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd233-134">CommonParameters</span></span>
<span data-ttu-id="cd233-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cd233-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd233-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd233-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd233-137">입력</span><span class="sxs-lookup"><span data-stu-id="cd233-137">INPUTS</span></span>

### <span data-ttu-id="cd233-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cd233-138">System.String</span></span>

## <span data-ttu-id="cd233-139">출력</span><span class="sxs-lookup"><span data-stu-id="cd233-139">OUTPUTS</span></span>

### <span data-ttu-id="cd233-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="cd233-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="cd233-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cd233-141">NOTES</span></span>

## <span data-ttu-id="cd233-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd233-142">RELATED LINKS</span></span>

[<span data-ttu-id="cd233-143">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="cd233-143">Set-AzVmssVM</span></span>](./Set-AzVmssVM.md)

[<span data-ttu-id="cd233-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cd233-144">Get-AzVmss</span></span>](./Get-AzVmss.md)


