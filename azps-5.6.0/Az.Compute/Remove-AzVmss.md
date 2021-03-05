---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: 2ed7be0cf790a596a2a2fc9b23c0e6aa50f67623
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998886"
---
# <span data-ttu-id="78523-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="78523-101">Remove-AzVmss</span></span>

## <span data-ttu-id="78523-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78523-102">SYNOPSIS</span></span>
<span data-ttu-id="78523-103">VMSS 내에 있는 VMSS 또는 가상 머신을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="78523-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="78523-104">구문</span><span class="sxs-lookup"><span data-stu-id="78523-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78523-105">설명</span><span class="sxs-lookup"><span data-stu-id="78523-105">DESCRIPTION</span></span>
<span data-ttu-id="78523-106">**Remove-AzVmss** cmdlet은 Azure에서 VMSS(Virtual Machine Scale Set)를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="78523-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="78523-107">이 cmdlet을 사용하여 VMSS 내에서 특정 가상 머신을 제거할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78523-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="78523-108">*InstanceId* 매개 변수를 사용하여 VMSS 내에서 특정 가상 머신을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="78523-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="78523-109">예제</span><span class="sxs-lookup"><span data-stu-id="78523-109">EXAMPLES</span></span>

### <span data-ttu-id="78523-110">예제 1: VMSS 제거</span><span class="sxs-lookup"><span data-stu-id="78523-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="78523-111">이 명령은 Group001이라는 리소스 그룹에 속하는 VMScaleSet001이라는 VMSS를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="78523-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="78523-112">예제 2: VMSS 내에서 가상 머신 제거</span><span class="sxs-lookup"><span data-stu-id="78523-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="78523-113">이 명령은 Group002라는 리소스 그룹에 속하는 VMScaleSet002라는 VMSS에서 인스턴스 ID 3이 있는 가상 머신을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="78523-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="78523-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="78523-114">PARAMETERS</span></span>

### <span data-ttu-id="78523-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78523-115">-AsJob</span></span>
<span data-ttu-id="78523-116">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="78523-116">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78523-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78523-117">-DefaultProfile</span></span>
<span data-ttu-id="78523-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78523-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78523-119">-Force</span><span class="sxs-lookup"><span data-stu-id="78523-119">-Force</span></span>
<span data-ttu-id="78523-120">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="78523-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78523-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="78523-121">-InstanceId</span></span>
<span data-ttu-id="78523-122">문자열 배열로 시작해야 하는 인스턴스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78523-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="78523-123">예를 들어: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="78523-123">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78523-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78523-124">-ResourceGroupName</span></span>
<span data-ttu-id="78523-125">VMSS가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78523-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78523-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="78523-126">-VMScaleSetName</span></span>
<span data-ttu-id="78523-127">이 cmdlet에서 제거하는 VMSS의 이름을 종으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="78523-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="78523-128">*InstanceId* 매개 변수를 지정하면 cmdlet은 이 매개 변수에 의해 명명된 VMSS에서 지정된 가상 머신을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="78523-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78523-129">-확인</span><span class="sxs-lookup"><span data-stu-id="78523-129">-Confirm</span></span>
<span data-ttu-id="78523-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="78523-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78523-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78523-131">-WhatIf</span></span>
<span data-ttu-id="78523-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="78523-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78523-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78523-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78523-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78523-134">CommonParameters</span></span>
<span data-ttu-id="78523-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="78523-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78523-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78523-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78523-137">입력</span><span class="sxs-lookup"><span data-stu-id="78523-137">INPUTS</span></span>

### <span data-ttu-id="78523-138">System.String</span><span class="sxs-lookup"><span data-stu-id="78523-138">System.String</span></span>

### <span data-ttu-id="78523-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="78523-139">System.String[]</span></span>

## <span data-ttu-id="78523-140">출력</span><span class="sxs-lookup"><span data-stu-id="78523-140">OUTPUTS</span></span>

### <span data-ttu-id="78523-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="78523-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="78523-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="78523-142">NOTES</span></span>

## <span data-ttu-id="78523-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78523-143">RELATED LINKS</span></span>

[<span data-ttu-id="78523-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="78523-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="78523-145">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="78523-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="78523-146">다시 시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="78523-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="78523-147">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="78523-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="78523-148">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="78523-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="78523-149">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="78523-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="78523-150">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="78523-150">Update-AzVmss</span></span>](./Update-AzVmss.md)


