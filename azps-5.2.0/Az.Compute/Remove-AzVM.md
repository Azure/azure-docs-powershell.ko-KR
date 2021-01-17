---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 6e733bfecea9a054bbab3794ca61778894c613fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346317"
---
# <span data-ttu-id="6575a-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="6575a-101">Remove-AzVM</span></span>

## <span data-ttu-id="6575a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6575a-102">SYNOPSIS</span></span>
<span data-ttu-id="6575a-103">Azure에서 가상 머신을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6575a-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="6575a-104">구문</span><span class="sxs-lookup"><span data-stu-id="6575a-104">SYNTAX</span></span>

### <span data-ttu-id="6575a-105">ResourceGroupNameParameterSetName(기본값)</span><span class="sxs-lookup"><span data-stu-id="6575a-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6575a-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="6575a-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6575a-107">설명</span><span class="sxs-lookup"><span data-stu-id="6575a-107">DESCRIPTION</span></span>
<span data-ttu-id="6575a-108">**Remove-AzVM** cmdlet은 Azure에서 가상 머신을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6575a-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="6575a-109">예제</span><span class="sxs-lookup"><span data-stu-id="6575a-109">EXAMPLES</span></span>

### <span data-ttu-id="6575a-110">예제 1: 가상 머신 제거</span><span class="sxs-lookup"><span data-stu-id="6575a-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="6575a-111">이 명령은 리소스 그룹 ResourceGroup11에서 VirtualMachine07이라는 가상 머신을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6575a-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="6575a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6575a-112">PARAMETERS</span></span>

### <span data-ttu-id="6575a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6575a-113">-AsJob</span></span>
<span data-ttu-id="6575a-114">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="6575a-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6575a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6575a-115">-DefaultProfile</span></span>
<span data-ttu-id="6575a-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6575a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6575a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6575a-117">-Force</span></span>
<span data-ttu-id="6575a-118">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6575a-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6575a-119">-Id</span><span class="sxs-lookup"><span data-stu-id="6575a-119">-Id</span></span>
<span data-ttu-id="6575a-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6575a-120">The resource group name.</span></span>

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

### <span data-ttu-id="6575a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6575a-121">-Name</span></span>
<span data-ttu-id="6575a-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6575a-122">The resource name.</span></span>

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

### <span data-ttu-id="6575a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6575a-123">-NoWait</span></span>
<span data-ttu-id="6575a-124">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6575a-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="6575a-125">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6575a-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="6575a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6575a-126">-ResourceGroupName</span></span>
<span data-ttu-id="6575a-127">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6575a-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6575a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6575a-128">-Confirm</span></span>
<span data-ttu-id="6575a-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6575a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6575a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6575a-130">-WhatIf</span></span>
<span data-ttu-id="6575a-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6575a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6575a-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6575a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6575a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6575a-133">CommonParameters</span></span>
<span data-ttu-id="6575a-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6575a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6575a-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6575a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6575a-136">입력</span><span class="sxs-lookup"><span data-stu-id="6575a-136">INPUTS</span></span>

### <span data-ttu-id="6575a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6575a-137">System.String</span></span>

## <span data-ttu-id="6575a-138">출력</span><span class="sxs-lookup"><span data-stu-id="6575a-138">OUTPUTS</span></span>

### <span data-ttu-id="6575a-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="6575a-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="6575a-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6575a-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6575a-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6575a-141">NOTES</span></span>

## <span data-ttu-id="6575a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6575a-142">RELATED LINKS</span></span>

[<span data-ttu-id="6575a-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="6575a-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="6575a-144">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="6575a-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="6575a-145">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="6575a-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="6575a-146">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="6575a-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="6575a-147">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="6575a-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="6575a-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="6575a-148">Update-AzVM</span></span>](./Update-AzVM.md)


