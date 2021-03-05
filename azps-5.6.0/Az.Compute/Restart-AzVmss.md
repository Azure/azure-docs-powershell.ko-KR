---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: a29e21bba3d04ca301d5f2bf3d2b5f9050fe9765
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994476"
---
# <span data-ttu-id="c9d76-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c9d76-101">Restart-AzVmss</span></span>

## <span data-ttu-id="c9d76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9d76-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d76-103">VMSS 내에서 VMSS 또는 가상 머신을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d76-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="c9d76-104">구문</span><span class="sxs-lookup"><span data-stu-id="c9d76-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9d76-105">설명</span><span class="sxs-lookup"><span data-stu-id="c9d76-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d76-106">다시 **시작-AzVmss** cmdlet은 VMSS(Virtual Machine Scale Set)를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d76-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="c9d76-107">이 cmdlet은 *InstanceId* 매개 변수를 사용하여 VMSS 내에서 특정 가상 머신을 다시 시작하는 데 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9d76-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="c9d76-108">예제</span><span class="sxs-lookup"><span data-stu-id="c9d76-108">EXAMPLES</span></span>

### <span data-ttu-id="c9d76-109">예제 1: VMSS 다시 시작</span><span class="sxs-lookup"><span data-stu-id="c9d76-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="c9d76-110">이 명령은 Group001이라는 리소스 그룹에 속하는 VMSS001이라는 VMSS를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d76-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="c9d76-111">예제 2: VMSS 내에서 특정 가상 머신 다시 시작</span><span class="sxs-lookup"><span data-stu-id="c9d76-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="c9d76-112">이 명령은 Group001이라는 리소스 그룹에 속하는 VMSS001이라는 VMSS에 인스턴스 ID가 1인 가상 머신을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d76-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="c9d76-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c9d76-113">PARAMETERS</span></span>

### <span data-ttu-id="c9d76-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9d76-114">-AsJob</span></span>
<span data-ttu-id="c9d76-115">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d76-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c9d76-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d76-116">-DefaultProfile</span></span>
<span data-ttu-id="c9d76-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9d76-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9d76-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c9d76-118">-InstanceId</span></span>
<span data-ttu-id="c9d76-119">문자열 배열로 다시 시작해야 하는 인스턴스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d76-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="c9d76-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9d76-120">-ResourceGroupName</span></span>
<span data-ttu-id="c9d76-121">VMSS의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d76-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="c9d76-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c9d76-122">-VMScaleSetName</span></span>
<span data-ttu-id="c9d76-123">이 cmdlet이 다시 시작하는 VMSS의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d76-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="c9d76-124">-확인</span><span class="sxs-lookup"><span data-stu-id="c9d76-124">-Confirm</span></span>
<span data-ttu-id="c9d76-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9d76-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9d76-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9d76-126">-WhatIf</span></span>
<span data-ttu-id="c9d76-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c9d76-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9d76-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9d76-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9d76-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d76-129">CommonParameters</span></span>
<span data-ttu-id="c9d76-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9d76-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d76-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9d76-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d76-132">입력</span><span class="sxs-lookup"><span data-stu-id="c9d76-132">INPUTS</span></span>

### <span data-ttu-id="c9d76-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c9d76-133">System.String</span></span>

### <span data-ttu-id="c9d76-134">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c9d76-134">System.String[]</span></span>

## <span data-ttu-id="c9d76-135">출력</span><span class="sxs-lookup"><span data-stu-id="c9d76-135">OUTPUTS</span></span>

### <span data-ttu-id="c9d76-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="c9d76-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="c9d76-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c9d76-137">NOTES</span></span>

## <span data-ttu-id="c9d76-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9d76-138">RELATED LINKS</span></span>

[<span data-ttu-id="c9d76-139">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c9d76-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="c9d76-140">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c9d76-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="c9d76-141">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c9d76-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="c9d76-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c9d76-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="c9d76-143">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c9d76-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="c9d76-144">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c9d76-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="c9d76-145">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="c9d76-145">Update-AzVmss</span></span>](./Update-AzVmss.md)


