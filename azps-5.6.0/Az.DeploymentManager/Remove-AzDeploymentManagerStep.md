---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 96f5f9e3dd0390d714b0ee7a74b3f585b46dcc1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966304"
---
# <span data-ttu-id="82a64-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="82a64-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="82a64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82a64-102">SYNOPSIS</span></span>
<span data-ttu-id="82a64-103">단계를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="82a64-103">Deletes the step.</span></span>

## <span data-ttu-id="82a64-104">구문</span><span class="sxs-lookup"><span data-stu-id="82a64-104">SYNTAX</span></span>

### <span data-ttu-id="82a64-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="82a64-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82a64-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="82a64-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82a64-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="82a64-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82a64-108">설명</span><span class="sxs-lookup"><span data-stu-id="82a64-108">DESCRIPTION</span></span>
<span data-ttu-id="82a64-109">**Remove-AzDeploymentManagerStep** cmdlet은 단계를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="82a64-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="82a64-110">해당 이름 및 리소스 그룹 이름으로 단계를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="82a64-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="82a64-111">또는 단계 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82a64-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="82a64-112">예제</span><span class="sxs-lookup"><span data-stu-id="82a64-112">EXAMPLES</span></span>

### <span data-ttu-id="82a64-113">예제 1: 단계 제거</span><span class="sxs-lookup"><span data-stu-id="82a64-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="82a64-114">이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep이라는 단계를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="82a64-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="82a64-115">예제 2: 리소스 식별자를 사용하여 단계 제거</span><span class="sxs-lookup"><span data-stu-id="82a64-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="82a64-116">이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep이라는 단계를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="82a64-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="82a64-117">예제 3: 개체가 반환한 개체를 사용하여 단계를 New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="82a64-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="82a64-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="82a64-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="82a64-119">이 명령은 이름과 ResourceGroup이 각각 해당 명령의 이름 및 ResourceGroupName 속성과 일치하는 $stepObject 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="82a64-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="82a64-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="82a64-120">PARAMETERS</span></span>

### <span data-ttu-id="82a64-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82a64-121">-DefaultProfile</span></span>
<span data-ttu-id="82a64-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82a64-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82a64-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82a64-123">-InputObject</span></span>
<span data-ttu-id="82a64-124">제거할 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="82a64-124">The step to be removed.</span></span>

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

### <span data-ttu-id="82a64-125">-Name</span><span class="sxs-lookup"><span data-stu-id="82a64-125">-Name</span></span>
<span data-ttu-id="82a64-126">단계의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82a64-126">The name of the step.</span></span>

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

### <span data-ttu-id="82a64-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82a64-127">-PassThru</span></span>
<span data-ttu-id="82a64-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="82a64-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="82a64-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82a64-129">-ResourceGroupName</span></span>
<span data-ttu-id="82a64-130">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="82a64-130">The resource group.</span></span>

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

### <span data-ttu-id="82a64-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82a64-131">-ResourceId</span></span>
<span data-ttu-id="82a64-132">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="82a64-132">The resource identifier.</span></span>

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

### <span data-ttu-id="82a64-133">-확인</span><span class="sxs-lookup"><span data-stu-id="82a64-133">-Confirm</span></span>
<span data-ttu-id="82a64-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="82a64-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82a64-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82a64-135">-WhatIf</span></span>
<span data-ttu-id="82a64-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="82a64-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82a64-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82a64-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82a64-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a64-138">CommonParameters</span></span>
<span data-ttu-id="82a64-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82a64-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a64-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82a64-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a64-141">입력</span><span class="sxs-lookup"><span data-stu-id="82a64-141">INPUTS</span></span>

### <span data-ttu-id="82a64-142">System.String</span><span class="sxs-lookup"><span data-stu-id="82a64-142">System.String</span></span>

### <span data-ttu-id="82a64-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="82a64-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="82a64-144">출력</span><span class="sxs-lookup"><span data-stu-id="82a64-144">OUTPUTS</span></span>

### <span data-ttu-id="82a64-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="82a64-145">System.Boolean</span></span>

## <span data-ttu-id="82a64-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82a64-146">NOTES</span></span>

## <span data-ttu-id="82a64-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82a64-147">RELATED LINKS</span></span>
