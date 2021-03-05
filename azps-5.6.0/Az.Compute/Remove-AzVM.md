---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: d5ce1af197575f96fd21f5355c0edfb98e3b181f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978768"
---
# <span data-ttu-id="c93d1-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="c93d1-101">Remove-AzVM</span></span>

## <span data-ttu-id="c93d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c93d1-102">SYNOPSIS</span></span>
<span data-ttu-id="c93d1-103">Azure에서 가상 머신을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c93d1-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="c93d1-104">구문</span><span class="sxs-lookup"><span data-stu-id="c93d1-104">SYNTAX</span></span>

### <span data-ttu-id="c93d1-105">ResourceGroupNameParameterSetName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c93d1-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c93d1-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="c93d1-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c93d1-107">설명</span><span class="sxs-lookup"><span data-stu-id="c93d1-107">DESCRIPTION</span></span>
<span data-ttu-id="c93d1-108">**Remove-AzVM** cmdlet은 Azure에서 가상 머신을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c93d1-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="c93d1-109">예제</span><span class="sxs-lookup"><span data-stu-id="c93d1-109">EXAMPLES</span></span>

### <span data-ttu-id="c93d1-110">예제 1: 가상 머신 제거</span><span class="sxs-lookup"><span data-stu-id="c93d1-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="c93d1-111">이 명령은 리소스 그룹 ResourceGroup11에서 VirtualMachine07이라는 가상 머신을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c93d1-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="c93d1-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c93d1-112">PARAMETERS</span></span>

### <span data-ttu-id="c93d1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c93d1-113">-AsJob</span></span>
<span data-ttu-id="c93d1-114">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="c93d1-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c93d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c93d1-115">-DefaultProfile</span></span>
<span data-ttu-id="c93d1-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c93d1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c93d1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c93d1-117">-Force</span></span>
<span data-ttu-id="c93d1-118">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c93d1-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c93d1-119">-Id</span><span class="sxs-lookup"><span data-stu-id="c93d1-119">-Id</span></span>
<span data-ttu-id="c93d1-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c93d1-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c93d1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c93d1-121">-Name</span></span>
<span data-ttu-id="c93d1-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c93d1-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c93d1-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c93d1-123">-NoWait</span></span>
<span data-ttu-id="c93d1-124">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c93d1-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="c93d1-125">작업이 성공적으로 완료된지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c93d1-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="c93d1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c93d1-126">-ResourceGroupName</span></span>
<span data-ttu-id="c93d1-127">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c93d1-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c93d1-128">-확인</span><span class="sxs-lookup"><span data-stu-id="c93d1-128">-Confirm</span></span>
<span data-ttu-id="c93d1-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c93d1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c93d1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c93d1-130">-WhatIf</span></span>
<span data-ttu-id="c93d1-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c93d1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c93d1-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c93d1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c93d1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c93d1-133">CommonParameters</span></span>
<span data-ttu-id="c93d1-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c93d1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c93d1-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c93d1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c93d1-136">입력</span><span class="sxs-lookup"><span data-stu-id="c93d1-136">INPUTS</span></span>

### <span data-ttu-id="c93d1-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c93d1-137">System.String</span></span>

## <span data-ttu-id="c93d1-138">출력</span><span class="sxs-lookup"><span data-stu-id="c93d1-138">OUTPUTS</span></span>

### <span data-ttu-id="c93d1-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="c93d1-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="c93d1-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c93d1-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c93d1-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c93d1-141">NOTES</span></span>

## <span data-ttu-id="c93d1-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c93d1-142">RELATED LINKS</span></span>

[<span data-ttu-id="c93d1-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c93d1-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="c93d1-144">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="c93d1-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="c93d1-145">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="c93d1-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="c93d1-146">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="c93d1-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="c93d1-147">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="c93d1-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="c93d1-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="c93d1-148">Update-AzVM</span></span>](./Update-AzVM.md)


