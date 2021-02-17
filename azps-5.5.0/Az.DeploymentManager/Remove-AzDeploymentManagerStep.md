---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 5e4af2ef006e51cee135dd642bcae7282940e8be
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198012"
---
# <span data-ttu-id="25b14-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="25b14-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="25b14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25b14-102">SYNOPSIS</span></span>
<span data-ttu-id="25b14-103">단계를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="25b14-103">Deletes the step.</span></span>

## <span data-ttu-id="25b14-104">구문</span><span class="sxs-lookup"><span data-stu-id="25b14-104">SYNTAX</span></span>

### <span data-ttu-id="25b14-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="25b14-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25b14-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="25b14-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25b14-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="25b14-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25b14-108">설명</span><span class="sxs-lookup"><span data-stu-id="25b14-108">DESCRIPTION</span></span>
<span data-ttu-id="25b14-109">**Remove-AzDeploymentManagerStep** cmdlet은 단계를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="25b14-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="25b14-110">해당 이름 및 리소스 그룹 이름으로 단계를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="25b14-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="25b14-111">또는 단계 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25b14-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="25b14-112">예제</span><span class="sxs-lookup"><span data-stu-id="25b14-112">EXAMPLES</span></span>

### <span data-ttu-id="25b14-113">예제 1: 단계 제거</span><span class="sxs-lookup"><span data-stu-id="25b14-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="25b14-114">이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep이라는 단계를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="25b14-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="25b14-115">예제 2: 리소스 식별자를 사용하여 단계 제거</span><span class="sxs-lookup"><span data-stu-id="25b14-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="25b14-116">이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep이라는 단계를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="25b14-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="25b14-117">예제 3: 사용자 계정에서 반환된 개체를 사용하여 New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="25b14-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="25b14-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="25b14-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="25b14-119">이 명령은 이름 및 ResourceGroup이 각각 이름 및 ResourceGroupName 속성과 일치하는 단계를 $stepObject 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="25b14-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="25b14-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25b14-120">PARAMETERS</span></span>

### <span data-ttu-id="25b14-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b14-121">-DefaultProfile</span></span>
<span data-ttu-id="25b14-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25b14-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25b14-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25b14-123">-InputObject</span></span>
<span data-ttu-id="25b14-124">제거할 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="25b14-124">The step to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25b14-125">-Name</span><span class="sxs-lookup"><span data-stu-id="25b14-125">-Name</span></span>
<span data-ttu-id="25b14-126">단계의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25b14-126">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b14-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25b14-127">-PassThru</span></span>
<span data-ttu-id="25b14-128">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="25b14-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="25b14-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25b14-129">-ResourceGroupName</span></span>
<span data-ttu-id="25b14-130">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="25b14-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25b14-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25b14-131">-ResourceId</span></span>
<span data-ttu-id="25b14-132">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="25b14-132">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b14-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25b14-133">-Confirm</span></span>
<span data-ttu-id="25b14-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="25b14-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25b14-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25b14-135">-WhatIf</span></span>
<span data-ttu-id="25b14-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="25b14-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25b14-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25b14-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25b14-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b14-138">CommonParameters</span></span>
<span data-ttu-id="25b14-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="25b14-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b14-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="25b14-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b14-141">입력</span><span class="sxs-lookup"><span data-stu-id="25b14-141">INPUTS</span></span>

### <span data-ttu-id="25b14-142">System.String</span><span class="sxs-lookup"><span data-stu-id="25b14-142">System.String</span></span>

### <span data-ttu-id="25b14-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="25b14-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="25b14-144">출력</span><span class="sxs-lookup"><span data-stu-id="25b14-144">OUTPUTS</span></span>

### <span data-ttu-id="25b14-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25b14-145">System.Boolean</span></span>

## <span data-ttu-id="25b14-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="25b14-146">NOTES</span></span>

## <span data-ttu-id="25b14-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25b14-147">RELATED LINKS</span></span>
