---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 2ff37cec23499afb0a0bb14069dc4e694f4440f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971435"
---
# <span data-ttu-id="e2e28-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e2e28-101">Start-AzVmss</span></span>

## <span data-ttu-id="e2e28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2e28-102">SYNOPSIS</span></span>
<span data-ttu-id="e2e28-103">VMSS 또는 VMSS 내의 가상 머신 집합을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e28-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="e2e28-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2e28-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2e28-105">설명</span><span class="sxs-lookup"><span data-stu-id="e2e28-105">DESCRIPTION</span></span>
<span data-ttu-id="e2e28-106">**Start-AzVmss** cmdlet은 VMSS(Virtual Machine Scale Set) 내의 모든 가상 머신 또는 가상 머신 집합을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e28-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="e2e28-107">*InstanceId* 매개 변수를 사용하여 가상 머신 집합을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2e28-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="e2e28-108">예제</span><span class="sxs-lookup"><span data-stu-id="e2e28-108">EXAMPLES</span></span>

### <span data-ttu-id="e2e28-109">예제 1: VMSS 내에서 특정 가상 머신 집합 시작</span><span class="sxs-lookup"><span data-stu-id="e2e28-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="e2e28-110">이 명령은 ContosoVMSS라는 VMSS에 속하는 인스턴스 ID 문자열 배열에 의해 지정된 특정 가상 머신 집합을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e28-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="e2e28-111">예제 2: VMSS 내의 모든 가상 머신 시작</span><span class="sxs-lookup"><span data-stu-id="e2e28-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="e2e28-112">이 명령은 ContosoVMSS라는 VMSS에 속하는 모든 가상 머신을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e28-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="e2e28-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e2e28-113">PARAMETERS</span></span>

### <span data-ttu-id="e2e28-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2e28-114">-AsJob</span></span>
<span data-ttu-id="e2e28-115">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e28-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e2e28-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2e28-116">-DefaultProfile</span></span>
<span data-ttu-id="e2e28-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2e28-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2e28-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e2e28-118">-InstanceId</span></span>
<span data-ttu-id="e2e28-119">cmdlet이 시작하는 인스턴스의 ID 또는 ID를 문자열 배열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e28-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="e2e28-120">예를 들어: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="e2e28-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="e2e28-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2e28-121">-ResourceGroupName</span></span>
<span data-ttu-id="e2e28-122">VMSS의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e28-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="e2e28-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e2e28-123">-VMScaleSetName</span></span>
<span data-ttu-id="e2e28-124">이 cmdlet이 가상 머신을 시작하는 VMSS의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e28-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="e2e28-125">-확인</span><span class="sxs-lookup"><span data-stu-id="e2e28-125">-Confirm</span></span>
<span data-ttu-id="e2e28-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2e28-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e28-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2e28-127">-WhatIf</span></span>
<span data-ttu-id="e2e28-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2e28-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2e28-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2e28-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2e28-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2e28-130">CommonParameters</span></span>
<span data-ttu-id="e2e28-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2e28-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2e28-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2e28-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2e28-133">입력</span><span class="sxs-lookup"><span data-stu-id="e2e28-133">INPUTS</span></span>

### <span data-ttu-id="e2e28-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e2e28-134">System.String</span></span>

### <span data-ttu-id="e2e28-135">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e2e28-135">System.String[]</span></span>

## <span data-ttu-id="e2e28-136">출력</span><span class="sxs-lookup"><span data-stu-id="e2e28-136">OUTPUTS</span></span>

### <span data-ttu-id="e2e28-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e2e28-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e2e28-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2e28-138">NOTES</span></span>

## <span data-ttu-id="e2e28-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2e28-139">RELATED LINKS</span></span>

[<span data-ttu-id="e2e28-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e2e28-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="e2e28-141">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e2e28-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="e2e28-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e2e28-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="e2e28-143">다시 시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e2e28-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="e2e28-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e2e28-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="e2e28-145">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e2e28-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="e2e28-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e2e28-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


