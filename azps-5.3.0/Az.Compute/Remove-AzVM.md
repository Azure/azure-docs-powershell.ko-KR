---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 6e733bfecea9a054bbab3794ca61778894c613fe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495989"
---
# <span data-ttu-id="71222-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="71222-101">Remove-AzVM</span></span>

## <span data-ttu-id="71222-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71222-102">SYNOPSIS</span></span>
<span data-ttu-id="71222-103">Azure에서 가상 머신을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="71222-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="71222-104">구문</span><span class="sxs-lookup"><span data-stu-id="71222-104">SYNTAX</span></span>

### <span data-ttu-id="71222-105">ResourceGroupNameParameterSetName(기본값)</span><span class="sxs-lookup"><span data-stu-id="71222-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71222-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="71222-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71222-107">설명</span><span class="sxs-lookup"><span data-stu-id="71222-107">DESCRIPTION</span></span>
<span data-ttu-id="71222-108">**Remove-AzVM** cmdlet은 Azure에서 가상 머신을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="71222-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="71222-109">예제</span><span class="sxs-lookup"><span data-stu-id="71222-109">EXAMPLES</span></span>

### <span data-ttu-id="71222-110">예제 1: 가상 머신 제거</span><span class="sxs-lookup"><span data-stu-id="71222-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="71222-111">이 명령은 리소스 그룹 ResourceGroup11에서 VirtualMachine07이라는 가상 머신을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="71222-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="71222-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71222-112">PARAMETERS</span></span>

### <span data-ttu-id="71222-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71222-113">-AsJob</span></span>
<span data-ttu-id="71222-114">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="71222-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="71222-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71222-115">-DefaultProfile</span></span>
<span data-ttu-id="71222-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71222-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71222-117">-Force</span><span class="sxs-lookup"><span data-stu-id="71222-117">-Force</span></span>
<span data-ttu-id="71222-118">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="71222-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="71222-119">-Id</span><span class="sxs-lookup"><span data-stu-id="71222-119">-Id</span></span>
<span data-ttu-id="71222-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71222-120">The resource group name.</span></span>

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

### <span data-ttu-id="71222-121">-Name</span><span class="sxs-lookup"><span data-stu-id="71222-121">-Name</span></span>
<span data-ttu-id="71222-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71222-122">The resource name.</span></span>

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

### <span data-ttu-id="71222-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="71222-123">-NoWait</span></span>
<span data-ttu-id="71222-124">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="71222-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="71222-125">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71222-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="71222-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71222-126">-ResourceGroupName</span></span>
<span data-ttu-id="71222-127">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71222-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="71222-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71222-128">-Confirm</span></span>
<span data-ttu-id="71222-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="71222-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71222-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71222-130">-WhatIf</span></span>
<span data-ttu-id="71222-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="71222-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71222-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71222-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71222-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71222-133">CommonParameters</span></span>
<span data-ttu-id="71222-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71222-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71222-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="71222-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71222-136">입력</span><span class="sxs-lookup"><span data-stu-id="71222-136">INPUTS</span></span>

### <span data-ttu-id="71222-137">System.String</span><span class="sxs-lookup"><span data-stu-id="71222-137">System.String</span></span>

## <span data-ttu-id="71222-138">출력</span><span class="sxs-lookup"><span data-stu-id="71222-138">OUTPUTS</span></span>

### <span data-ttu-id="71222-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="71222-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="71222-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="71222-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="71222-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="71222-141">NOTES</span></span>

## <span data-ttu-id="71222-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71222-142">RELATED LINKS</span></span>

[<span data-ttu-id="71222-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="71222-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="71222-144">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="71222-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="71222-145">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="71222-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="71222-146">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="71222-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="71222-147">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="71222-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="71222-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="71222-148">Update-AzVM</span></span>](./Update-AzVM.md)


