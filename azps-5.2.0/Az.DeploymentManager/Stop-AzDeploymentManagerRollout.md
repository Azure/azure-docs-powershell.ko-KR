---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: cd59cd39fb2834bed2162a257905fea643c0a767
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333549"
---
# <span data-ttu-id="28a62-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="28a62-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="28a62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28a62-102">SYNOPSIS</span></span>
<span data-ttu-id="28a62-103">롤아웃을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-103">Stops the rollout.</span></span>

## <span data-ttu-id="28a62-104">구문</span><span class="sxs-lookup"><span data-stu-id="28a62-104">SYNTAX</span></span>

### <span data-ttu-id="28a62-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="28a62-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28a62-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="28a62-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28a62-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="28a62-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28a62-108">설명</span><span class="sxs-lookup"><span data-stu-id="28a62-108">DESCRIPTION</span></span>
<span data-ttu-id="28a62-109">**Stop-AzDeploymentManagerRollout** cmdlet은 진행 중인 롤아웃을 중지하고 롤아웃의 현재 상태를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="28a62-110">이름 및 리소스 그룹 이름으로 롤아웃을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="28a62-111">또는 Rollout 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="28a62-112">롤아웃이 중지된 후 다시 시작하거나 다시 시작할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="28a62-113">새 롤아웃만 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="28a62-114">예제</span><span class="sxs-lookup"><span data-stu-id="28a62-114">EXAMPLES</span></span>

### <span data-ttu-id="28a62-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="28a62-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="28a62-116">이 명령은 ContosoResourceGroup에서 ContosoRollout이라는 롤아웃을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="28a62-117">예제 2: 리소스 식별자를 사용하여 롤아웃 중지</span><span class="sxs-lookup"><span data-stu-id="28a62-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="28a62-118">이 명령은 ContosoResourceGroup에서 ContosoRollout이라는 롤아웃을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="28a62-119">예제 3: 롤아웃 개체를 사용하여 롤아웃을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="28a62-120">이 명령은 이름 및 ResourceGroup이 각각 이름 및 ResourceGroupName 속성과 일치하는 롤아웃을 $rolloutObject 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="28a62-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28a62-121">PARAMETERS</span></span>

### <span data-ttu-id="28a62-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a62-122">-DefaultProfile</span></span>
<span data-ttu-id="28a62-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28a62-124">-Force</span><span class="sxs-lookup"><span data-stu-id="28a62-124">-Force</span></span>
<span data-ttu-id="28a62-125">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="28a62-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28a62-126">-InputObject</span></span>
<span data-ttu-id="28a62-127">제거할 롤아웃입니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="28a62-128">-Name</span><span class="sxs-lookup"><span data-stu-id="28a62-128">-Name</span></span>
<span data-ttu-id="28a62-129">롤아웃의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="28a62-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28a62-130">-ResourceGroupName</span></span>
<span data-ttu-id="28a62-131">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-131">The resource group.</span></span>

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

### <span data-ttu-id="28a62-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28a62-132">-ResourceId</span></span>
<span data-ttu-id="28a62-133">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-133">The resource identifier.</span></span>

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

### <span data-ttu-id="28a62-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28a62-134">-Confirm</span></span>
<span data-ttu-id="28a62-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28a62-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28a62-136">-WhatIf</span></span>
<span data-ttu-id="28a62-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="28a62-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28a62-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28a62-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a62-139">CommonParameters</span></span>
<span data-ttu-id="28a62-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="28a62-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a62-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="28a62-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a62-142">입력</span><span class="sxs-lookup"><span data-stu-id="28a62-142">INPUTS</span></span>

### <span data-ttu-id="28a62-143">System.String</span><span class="sxs-lookup"><span data-stu-id="28a62-143">System.String</span></span>

### <span data-ttu-id="28a62-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="28a62-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="28a62-145">출력</span><span class="sxs-lookup"><span data-stu-id="28a62-145">OUTPUTS</span></span>

### <span data-ttu-id="28a62-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="28a62-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="28a62-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="28a62-147">NOTES</span></span>

## <span data-ttu-id="28a62-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28a62-148">RELATED LINKS</span></span>
