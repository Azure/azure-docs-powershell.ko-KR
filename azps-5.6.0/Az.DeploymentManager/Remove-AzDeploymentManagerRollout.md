---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 3ade9bfd724a84e162c0cedd937f2255ebb5b6a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980699"
---
# <span data-ttu-id="3ef38-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="3ef38-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="3ef38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ef38-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef38-103">롤아웃을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3ef38-103">Deletes the rollout.</span></span>

## <span data-ttu-id="3ef38-104">구문</span><span class="sxs-lookup"><span data-stu-id="3ef38-104">SYNTAX</span></span>

### <span data-ttu-id="3ef38-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="3ef38-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ef38-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ef38-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ef38-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="3ef38-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ef38-108">설명</span><span class="sxs-lookup"><span data-stu-id="3ef38-108">DESCRIPTION</span></span>
<span data-ttu-id="3ef38-109">**Remove-AzDeploymentManagerRollout** cmdlet은 터미널 상태의 롤아웃을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3ef38-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="3ef38-110">해당 이름 및 리소스 그룹 이름으로 롤아웃을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ef38-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="3ef38-111">또는 롤아웃 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ef38-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="3ef38-112">예제</span><span class="sxs-lookup"><span data-stu-id="3ef38-112">EXAMPLES</span></span>

### <span data-ttu-id="3ef38-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="3ef38-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="3ef38-114">이 명령은 ContosoResourceGroup에서 ContosoRollout이라는 롤아웃을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3ef38-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="3ef38-115">예제 2: 리소스 식별자를 사용하여 롤아웃 삭제</span><span class="sxs-lookup"><span data-stu-id="3ef38-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="3ef38-116">이 명령은 ContosoResourceGroup에서 ContosoRollout이라는 롤아웃을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3ef38-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="3ef38-117">예제 3: 롤아웃 개체를 사용하여 롤아웃을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3ef38-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="3ef38-118">이 명령은 이름 및 ResourceGroup이 각각 해당 리소스의 이름 및 ResourceGroupName 속성과 일치하는 $rolloutObject 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3ef38-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="3ef38-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3ef38-119">PARAMETERS</span></span>

### <span data-ttu-id="3ef38-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ef38-120">-DefaultProfile</span></span>
<span data-ttu-id="3ef38-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ef38-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ef38-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ef38-122">-InputObject</span></span>
<span data-ttu-id="3ef38-123">제거할 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="3ef38-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="3ef38-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3ef38-124">-Name</span></span>
<span data-ttu-id="3ef38-125">롤아웃의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ef38-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="3ef38-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ef38-126">-PassThru</span></span>
<span data-ttu-id="3ef38-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3ef38-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3ef38-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ef38-128">-ResourceGroupName</span></span>
<span data-ttu-id="3ef38-129">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="3ef38-129">The resource group.</span></span>

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

### <span data-ttu-id="3ef38-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ef38-130">-ResourceId</span></span>
<span data-ttu-id="3ef38-131">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3ef38-131">The resource identifier.</span></span>

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

### <span data-ttu-id="3ef38-132">-확인</span><span class="sxs-lookup"><span data-stu-id="3ef38-132">-Confirm</span></span>
<span data-ttu-id="3ef38-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ef38-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ef38-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ef38-134">-WhatIf</span></span>
<span data-ttu-id="3ef38-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3ef38-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ef38-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ef38-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ef38-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef38-137">CommonParameters</span></span>
<span data-ttu-id="3ef38-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3ef38-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef38-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ef38-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef38-140">입력</span><span class="sxs-lookup"><span data-stu-id="3ef38-140">INPUTS</span></span>

### <span data-ttu-id="3ef38-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3ef38-141">System.String</span></span>

### <span data-ttu-id="3ef38-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="3ef38-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="3ef38-143">출력</span><span class="sxs-lookup"><span data-stu-id="3ef38-143">OUTPUTS</span></span>

### <span data-ttu-id="3ef38-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3ef38-144">System.Boolean</span></span>

## <span data-ttu-id="3ef38-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3ef38-145">NOTES</span></span>

## <span data-ttu-id="3ef38-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ef38-146">RELATED LINKS</span></span>
