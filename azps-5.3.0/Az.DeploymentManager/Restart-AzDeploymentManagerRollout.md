---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: ba7b62d42764f5098868e6a15eb073cb6b898e82
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494601"
---
# <span data-ttu-id="61770-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="61770-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="61770-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61770-102">SYNOPSIS</span></span>
<span data-ttu-id="61770-103">실패한 롤아웃을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="61770-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="61770-104">구문</span><span class="sxs-lookup"><span data-stu-id="61770-104">SYNTAX</span></span>

### <span data-ttu-id="61770-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="61770-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61770-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="61770-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61770-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="61770-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61770-108">설명</span><span class="sxs-lookup"><span data-stu-id="61770-108">DESCRIPTION</span></span>
<span data-ttu-id="61770-109">**Restart-AzDeploymentManagerRollout** cmdlet은 실패한 롤아웃을 다시 시작하고 롤아웃 진행률에 대한 모든 세부 정보가 있는 해당 롤아웃을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="61770-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="61770-110">이름 및 리소스 그룹 이름으로 롤아웃을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="61770-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="61770-111">또는 Rollout 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61770-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="61770-112">SkipSucceeded 선택적 매개 변수를 사용하면 롤아웃의 이전 실행에서 성공한 모든 단계를 건너뛸 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61770-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="61770-113">예제</span><span class="sxs-lookup"><span data-stu-id="61770-113">EXAMPLES</span></span>

### <span data-ttu-id="61770-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="61770-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="61770-115">이 명령은 ContosoResourceGroup에서 ContosoRollout이라는 롤아웃을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="61770-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="61770-116">SkipSucceeded 플래그는 이미 실행된 모든 단계를 건너뛰고 롤아웃이 마지막으로 실패한 위치부터 실행을 계속해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="61770-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="61770-117">예제 2: 리소스 식별자를 사용하여 롤아웃 다시 시작</span><span class="sxs-lookup"><span data-stu-id="61770-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="61770-118">이 명령은 ContosoResourceGroup에서 ContosoRollout이라는 롤아웃을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="61770-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="61770-119">예제 3: 롤아웃 개체를 사용하여 롤아웃을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="61770-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="61770-120">이 명령은 이름과 ResourceGroup이 각각 이름 및 ResourceGroupName 속성과 일치하는 롤아웃을 $rolloutObject 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="61770-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="61770-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61770-121">PARAMETERS</span></span>

### <span data-ttu-id="61770-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61770-122">-DefaultProfile</span></span>
<span data-ttu-id="61770-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="61770-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61770-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61770-124">-InputObject</span></span>
<span data-ttu-id="61770-125">제거할 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="61770-125">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61770-126">-Name</span><span class="sxs-lookup"><span data-stu-id="61770-126">-Name</span></span>
<span data-ttu-id="61770-127">롤아웃의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61770-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="61770-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61770-128">-ResourceGroupName</span></span>
<span data-ttu-id="61770-129">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="61770-129">The resource group.</span></span>

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

### <span data-ttu-id="61770-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61770-130">-ResourceId</span></span>
<span data-ttu-id="61770-131">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="61770-131">The resource identifier.</span></span>

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

### <span data-ttu-id="61770-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="61770-132">-SkipSucceeded</span></span>
<span data-ttu-id="61770-133">롤아웃의 이전 실행에서 성공한 단계를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="61770-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="61770-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61770-134">-Confirm</span></span>
<span data-ttu-id="61770-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="61770-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61770-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61770-136">-WhatIf</span></span>
<span data-ttu-id="61770-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="61770-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61770-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61770-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61770-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61770-139">CommonParameters</span></span>
<span data-ttu-id="61770-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="61770-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61770-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61770-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61770-142">입력</span><span class="sxs-lookup"><span data-stu-id="61770-142">INPUTS</span></span>

### <span data-ttu-id="61770-143">System.String</span><span class="sxs-lookup"><span data-stu-id="61770-143">System.String</span></span>

### <span data-ttu-id="61770-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="61770-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="61770-145">출력</span><span class="sxs-lookup"><span data-stu-id="61770-145">OUTPUTS</span></span>

### <span data-ttu-id="61770-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="61770-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="61770-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="61770-147">NOTES</span></span>

## <span data-ttu-id="61770-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61770-148">RELATED LINKS</span></span>
