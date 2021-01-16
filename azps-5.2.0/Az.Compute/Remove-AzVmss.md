---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: e02ddb83e40495fbcf729428a737f27e6665d765
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355401"
---
# <span data-ttu-id="91fe4-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="91fe4-101">Remove-AzVmss</span></span>

## <span data-ttu-id="91fe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="91fe4-103">VMSS 또는 VMSS 내에 있는 가상 머신을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="91fe4-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="91fe4-104">구문</span><span class="sxs-lookup"><span data-stu-id="91fe4-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91fe4-105">설명</span><span class="sxs-lookup"><span data-stu-id="91fe4-105">DESCRIPTION</span></span>
<span data-ttu-id="91fe4-106">**Remove-AzVmss** cmdlet은 Azure에서 VMSS(Virtual Machine Scale Set)를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="91fe4-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="91fe4-107">이 cmdlet을 사용하여 VMSS 내에서 특정 가상 머신을 제거할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91fe4-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="91fe4-108">*InstanceId* 매개 변수를 사용하여 VMSS 내에서 특정 가상 머신을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91fe4-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="91fe4-109">예제</span><span class="sxs-lookup"><span data-stu-id="91fe4-109">EXAMPLES</span></span>

### <span data-ttu-id="91fe4-110">예제 1: VMSS 제거</span><span class="sxs-lookup"><span data-stu-id="91fe4-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="91fe4-111">이 명령은 Group001이라는 리소스 그룹에 속하는 VMScaleSet001이라는 VMSS를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="91fe4-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="91fe4-112">예제 2: VMSS 내에서 가상 머신 제거</span><span class="sxs-lookup"><span data-stu-id="91fe4-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="91fe4-113">이 명령은 그룹002 리소스 그룹에 속하는 VMScaleSet002라는 VMSS에서 인스턴스 ID 3이 있는 가상 머신을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="91fe4-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="91fe4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91fe4-114">PARAMETERS</span></span>

### <span data-ttu-id="91fe4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91fe4-115">-AsJob</span></span>
<span data-ttu-id="91fe4-116">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="91fe4-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="91fe4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91fe4-117">-DefaultProfile</span></span>
<span data-ttu-id="91fe4-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91fe4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91fe4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="91fe4-119">-Force</span></span>
<span data-ttu-id="91fe4-120">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="91fe4-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="91fe4-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="91fe4-121">-InstanceId</span></span>
<span data-ttu-id="91fe4-122">문자열 배열로 시작해야 하는 인스턴스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91fe4-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="91fe4-123">예: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="91fe4-123">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="91fe4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91fe4-124">-ResourceGroupName</span></span>
<span data-ttu-id="91fe4-125">VMSS가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91fe4-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="91fe4-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="91fe4-126">-VMScaleSetName</span></span>
<span data-ttu-id="91fe4-127">이 cmdlet이 제거하는 VMSS의 이름 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="91fe4-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="91fe4-128">*InstanceId* 매개 변수를 지정하면 cmdlet은 이 매개 변수로 명명된 VMSS에서 지정된 가상 머신을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="91fe4-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="91fe4-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91fe4-129">-Confirm</span></span>
<span data-ttu-id="91fe4-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="91fe4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91fe4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91fe4-131">-WhatIf</span></span>
<span data-ttu-id="91fe4-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="91fe4-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91fe4-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91fe4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91fe4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91fe4-134">CommonParameters</span></span>
<span data-ttu-id="91fe4-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="91fe4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91fe4-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="91fe4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91fe4-137">입력</span><span class="sxs-lookup"><span data-stu-id="91fe4-137">INPUTS</span></span>

### <span data-ttu-id="91fe4-138">System.String</span><span class="sxs-lookup"><span data-stu-id="91fe4-138">System.String</span></span>

### <span data-ttu-id="91fe4-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="91fe4-139">System.String[]</span></span>

## <span data-ttu-id="91fe4-140">출력</span><span class="sxs-lookup"><span data-stu-id="91fe4-140">OUTPUTS</span></span>

### <span data-ttu-id="91fe4-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="91fe4-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="91fe4-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="91fe4-142">NOTES</span></span>

## <span data-ttu-id="91fe4-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91fe4-143">RELATED LINKS</span></span>

[<span data-ttu-id="91fe4-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="91fe4-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="91fe4-145">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="91fe4-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="91fe4-146">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="91fe4-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="91fe4-147">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="91fe4-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="91fe4-148">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="91fe4-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="91fe4-149">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="91fe4-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="91fe4-150">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="91fe4-150">Update-AzVmss</span></span>](./Update-AzVmss.md)


