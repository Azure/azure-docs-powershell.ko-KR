---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/restart-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: ee1ef6e5b8bcee4af1d3aef67767269042c552df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523852"
---
# <span data-ttu-id="1ac13-101">Restart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="1ac13-101">Restart-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="1ac13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ac13-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac13-103">실패 한 배포를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-103">Restart a failed rollout.</span></span>

## <span data-ttu-id="1ac13-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1ac13-104">SYNTAX</span></span>

### <span data-ttu-id="1ac13-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1ac13-105">Interactive (Default)</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ac13-106">리소스</span><span class="sxs-lookup"><span data-stu-id="1ac13-106">ResourceId</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ac13-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="1ac13-107">InputObject</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ac13-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1ac13-108">DESCRIPTION</span></span>
<span data-ttu-id="1ac13-109">**AzureRmDeploymentManagerRollout** cmdlet은 실패 한 롤아웃을 다시 시작 하 고 롤아웃 진행 상황에 대 한 모든 세부 정보를 사용 하 여 해당 롤아웃을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-109">The **Restart-AzureRmDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="1ac13-110">이름 및 리소스 그룹 이름을 기준으로 출시를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="1ac13-111">또는 롤아웃 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="1ac13-112">선택적 매개 변수 SkipSucceeded는 이전 출시의 모든 성공 단계를 건너뛸 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="1ac13-113">예제의</span><span class="sxs-lookup"><span data-stu-id="1ac13-113">EXAMPLES</span></span>

### <span data-ttu-id="1ac13-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="1ac13-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="1ac13-115">이 명령은 ContosoResourceGroup에서 ContosoRollout 이라는 롤아웃을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="1ac13-116">SkipSucceeded 플래그는 이미 성공적으로 실행 된 모든 단계가 생략 되어야 하 고, 롤아웃이 마지막으로 실패 한 위치에서 실행을 계속 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="1ac13-117">예제 2: 리소스 식별자를 사용 하 여 출시 다시 시작</span><span class="sxs-lookup"><span data-stu-id="1ac13-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="1ac13-118">이 명령은 ContosoResourceGroup에서 ContosoRollout 이라는 롤아웃을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="1ac13-119">예제 3: 롤아웃 개체를 사용 하 여 출시를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="1ac13-120">이 명령은 이름 및 ResourceGroup이 $rolloutObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 롤아웃을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="1ac13-121">변수</span><span class="sxs-lookup"><span data-stu-id="1ac13-121">PARAMETERS</span></span>

### <span data-ttu-id="1ac13-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac13-122">-DefaultProfile</span></span>
<span data-ttu-id="1ac13-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac13-124">-이름</span><span class="sxs-lookup"><span data-stu-id="1ac13-124">-Name</span></span>
<span data-ttu-id="1ac13-125">롤아웃 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-125">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac13-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ac13-126">-ResourceGroupName</span></span>
<span data-ttu-id="1ac13-127">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="1ac13-127">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac13-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ac13-128">-ResourceId</span></span>
<span data-ttu-id="1ac13-129">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-129">The resource identifier.</span></span>

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

### <span data-ttu-id="1ac13-130">-출시</span><span class="sxs-lookup"><span data-stu-id="1ac13-130">-Rollout</span></span>
<span data-ttu-id="1ac13-131">제거할 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-131">The resource to be removed.</span></span>

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

### <span data-ttu-id="1ac13-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="1ac13-132">-SkipSucceeded</span></span>
<span data-ttu-id="1ac13-133">이전 출시 실행에 성공한 단계를 건너뛰십시오.</span><span class="sxs-lookup"><span data-stu-id="1ac13-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="1ac13-134">-확인</span><span class="sxs-lookup"><span data-stu-id="1ac13-134">-Confirm</span></span>
<span data-ttu-id="1ac13-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ac13-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ac13-136">-WhatIf</span></span>
<span data-ttu-id="1ac13-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ac13-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ac13-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac13-139">CommonParameters</span></span>
<span data-ttu-id="1ac13-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ac13-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac13-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ac13-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac13-142">입력</span><span class="sxs-lookup"><span data-stu-id="1ac13-142">INPUTS</span></span>

### <span data-ttu-id="1ac13-143">Microsoft. Azure. PSRollout. 모델. a 배포</span><span class="sxs-lookup"><span data-stu-id="1ac13-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="1ac13-144">출력</span><span class="sxs-lookup"><span data-stu-id="1ac13-144">OUTPUTS</span></span>

### <span data-ttu-id="1ac13-145">Microsoft. Azure. PSRollout. 모델. a 배포</span><span class="sxs-lookup"><span data-stu-id="1ac13-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="1ac13-146">상속자</span><span class="sxs-lookup"><span data-stu-id="1ac13-146">NOTES</span></span>

## <span data-ttu-id="1ac13-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ac13-147">RELATED LINKS</span></span>

[<span data-ttu-id="1ac13-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="1ac13-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="1ac13-149">중지-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="1ac13-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="1ac13-150">제거-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="1ac13-150">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)