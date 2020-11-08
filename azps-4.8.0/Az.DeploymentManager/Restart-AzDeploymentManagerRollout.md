---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: ba7b62d42764f5098868e6a15eb073cb6b898e82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212808"
---
# <span data-ttu-id="c94b0-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="c94b0-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="c94b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c94b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c94b0-103">실패 한 출시를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="c94b0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c94b0-104">SYNTAX</span></span>

### <span data-ttu-id="c94b0-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c94b0-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c94b0-106">리소스</span><span class="sxs-lookup"><span data-stu-id="c94b0-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c94b0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c94b0-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c94b0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c94b0-108">DESCRIPTION</span></span>
<span data-ttu-id="c94b0-109">**AzDeploymentManagerRollout** cmdlet은 실패 한 롤아웃을 다시 시작 하 고 롤아웃 진행 상황에 대 한 모든 세부 정보를 사용 하 여 해당 롤아웃을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="c94b0-110">이름 및 리소스 그룹 이름을 기준으로 출시를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="c94b0-111">또는 롤아웃 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="c94b0-112">선택적 매개 변수 SkipSucceeded는 이전 출시의 모든 성공 단계를 건너뛸 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="c94b0-113">예제의</span><span class="sxs-lookup"><span data-stu-id="c94b0-113">EXAMPLES</span></span>

### <span data-ttu-id="c94b0-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="c94b0-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="c94b0-115">이 명령은 ContosoResourceGroup에서 ContosoRollout 이라는 롤아웃을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="c94b0-116">SkipSucceeded 플래그는 이미 성공적으로 실행 된 모든 단계가 생략 되어야 하 고, 롤아웃이 마지막으로 실패 한 위치에서 실행을 계속 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="c94b0-117">예제 2: 리소스 식별자를 사용 하 여 출시 다시 시작</span><span class="sxs-lookup"><span data-stu-id="c94b0-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="c94b0-118">이 명령은 ContosoResourceGroup에서 ContosoRollout 이라는 롤아웃을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c94b0-119">예제 3: 롤아웃 개체를 사용 하 여 출시를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="c94b0-120">이 명령은 이름 및 ResourceGroup이 $rolloutObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 롤아웃을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="c94b0-121">변수</span><span class="sxs-lookup"><span data-stu-id="c94b0-121">PARAMETERS</span></span>

### <span data-ttu-id="c94b0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c94b0-122">-DefaultProfile</span></span>
<span data-ttu-id="c94b0-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c94b0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c94b0-124">-InputObject</span></span>
<span data-ttu-id="c94b0-125">제거할 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-125">The resource to be removed.</span></span>

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

### <span data-ttu-id="c94b0-126">-이름</span><span class="sxs-lookup"><span data-stu-id="c94b0-126">-Name</span></span>
<span data-ttu-id="c94b0-127">롤아웃 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="c94b0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c94b0-128">-ResourceGroupName</span></span>
<span data-ttu-id="c94b0-129">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="c94b0-129">The resource group.</span></span>

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

### <span data-ttu-id="c94b0-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c94b0-130">-ResourceId</span></span>
<span data-ttu-id="c94b0-131">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-131">The resource identifier.</span></span>

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

### <span data-ttu-id="c94b0-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="c94b0-132">-SkipSucceeded</span></span>
<span data-ttu-id="c94b0-133">이전 출시 실행에 성공한 단계를 건너뛰십시오.</span><span class="sxs-lookup"><span data-stu-id="c94b0-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="c94b0-134">-확인</span><span class="sxs-lookup"><span data-stu-id="c94b0-134">-Confirm</span></span>
<span data-ttu-id="c94b0-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c94b0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c94b0-136">-WhatIf</span></span>
<span data-ttu-id="c94b0-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c94b0-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c94b0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c94b0-139">CommonParameters</span></span>
<span data-ttu-id="c94b0-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c94b0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c94b0-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c94b0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c94b0-142">입력</span><span class="sxs-lookup"><span data-stu-id="c94b0-142">INPUTS</span></span>

### <span data-ttu-id="c94b0-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c94b0-143">System.String</span></span>

### <span data-ttu-id="c94b0-144">Microsoft. Azure. PSRollout. 모델. a 배포</span><span class="sxs-lookup"><span data-stu-id="c94b0-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="c94b0-145">출력</span><span class="sxs-lookup"><span data-stu-id="c94b0-145">OUTPUTS</span></span>

### <span data-ttu-id="c94b0-146">Microsoft. Azure. PSRollout. 모델. a 배포</span><span class="sxs-lookup"><span data-stu-id="c94b0-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="c94b0-147">상속자</span><span class="sxs-lookup"><span data-stu-id="c94b0-147">NOTES</span></span>

## <span data-ttu-id="c94b0-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c94b0-148">RELATED LINKS</span></span>
