---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 8e5e2c25f69d6e61c21a0f616f49079710c2d5db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492075"
---
# <span data-ttu-id="6160f-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="6160f-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="6160f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6160f-102">SYNOPSIS</span></span>
<span data-ttu-id="6160f-103">롤아웃을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6160f-103">Deletes the rollout.</span></span>

## <span data-ttu-id="6160f-104">구문</span><span class="sxs-lookup"><span data-stu-id="6160f-104">SYNTAX</span></span>

### <span data-ttu-id="6160f-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="6160f-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6160f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6160f-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6160f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6160f-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6160f-108">설명</span><span class="sxs-lookup"><span data-stu-id="6160f-108">DESCRIPTION</span></span>
<span data-ttu-id="6160f-109">**Remove-AzDeploymentManagerRollout** cmdlet은 터미널 상태의 롤아웃을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6160f-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="6160f-110">이름 및 리소스 그룹 이름으로 롤아웃을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6160f-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="6160f-111">또는 Rollout 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6160f-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="6160f-112">예제</span><span class="sxs-lookup"><span data-stu-id="6160f-112">EXAMPLES</span></span>

### <span data-ttu-id="6160f-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="6160f-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="6160f-114">이 명령은 ContosoResourceGroup에서 ContosoRollout이라는 롤아웃을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6160f-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="6160f-115">예제 2: 리소스 식별자를 사용하여 롤아웃 삭제</span><span class="sxs-lookup"><span data-stu-id="6160f-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="6160f-116">이 명령은 ContosoResourceGroup에서 ContosoRollout이라는 롤아웃을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6160f-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="6160f-117">예제 3: 롤아웃 개체를 사용하여 롤아웃을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6160f-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="6160f-118">이 명령은 이름과 ResourceGroup이 각각 이름 및 ResourceGroupName 속성과 일치하는 롤아웃을 $rolloutObject 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="6160f-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="6160f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6160f-119">PARAMETERS</span></span>

### <span data-ttu-id="6160f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6160f-120">-DefaultProfile</span></span>
<span data-ttu-id="6160f-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6160f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6160f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6160f-122">-InputObject</span></span>
<span data-ttu-id="6160f-123">제거할 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="6160f-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="6160f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6160f-124">-Name</span></span>
<span data-ttu-id="6160f-125">롤아웃의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6160f-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="6160f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6160f-126">-PassThru</span></span>
<span data-ttu-id="6160f-127">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="6160f-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6160f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6160f-128">-ResourceGroupName</span></span>
<span data-ttu-id="6160f-129">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="6160f-129">The resource group.</span></span>

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

### <span data-ttu-id="6160f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6160f-130">-ResourceId</span></span>
<span data-ttu-id="6160f-131">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6160f-131">The resource identifier.</span></span>

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

### <span data-ttu-id="6160f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6160f-132">-Confirm</span></span>
<span data-ttu-id="6160f-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6160f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6160f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6160f-134">-WhatIf</span></span>
<span data-ttu-id="6160f-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6160f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6160f-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6160f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6160f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6160f-137">CommonParameters</span></span>
<span data-ttu-id="6160f-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6160f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6160f-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6160f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6160f-140">입력</span><span class="sxs-lookup"><span data-stu-id="6160f-140">INPUTS</span></span>

### <span data-ttu-id="6160f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6160f-141">System.String</span></span>

### <span data-ttu-id="6160f-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="6160f-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="6160f-143">출력</span><span class="sxs-lookup"><span data-stu-id="6160f-143">OUTPUTS</span></span>

### <span data-ttu-id="6160f-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6160f-144">System.Boolean</span></span>

## <span data-ttu-id="6160f-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6160f-145">NOTES</span></span>

## <span data-ttu-id="6160f-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6160f-146">RELATED LINKS</span></span>
