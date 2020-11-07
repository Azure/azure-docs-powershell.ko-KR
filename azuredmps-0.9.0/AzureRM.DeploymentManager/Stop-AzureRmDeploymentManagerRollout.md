---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/stop-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 3c4f221fc00187c4faea2dbcc1a5014822c476c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701704"
---
# <span data-ttu-id="9583f-101">Stop-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="9583f-101">Stop-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="9583f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9583f-102">SYNOPSIS</span></span>
<span data-ttu-id="9583f-103">진행 중인 출시를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-103">Stops a rollout in progress.</span></span>

## <span data-ttu-id="9583f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9583f-104">SYNTAX</span></span>

### <span data-ttu-id="9583f-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9583f-105">Interactive (Default)</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9583f-106">리소스</span><span class="sxs-lookup"><span data-stu-id="9583f-106">ResourceId</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9583f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9583f-107">InputObject</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9583f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9583f-108">DESCRIPTION</span></span>
<span data-ttu-id="9583f-109">**AzureRmDeploymentManagerRollout** cmdlet은 진행 중인 출시를 중지 하 고 롤아웃의 현재 상태를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-109">The **Stop-AzureRmDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="9583f-110">이름 및 리소스 그룹 이름을 기준으로 출시를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="9583f-111">또는 롤아웃 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="9583f-112">롤아웃이 중지 되 면 다시 시작 하거나 다시 시작할 수 없다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="9583f-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="9583f-113">새 출시만 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="9583f-114">예제의</span><span class="sxs-lookup"><span data-stu-id="9583f-114">EXAMPLES</span></span>

### <span data-ttu-id="9583f-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="9583f-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="9583f-116">이 명령은 ContosoResourceGroup에서 ContosoRollout 이라는 출시를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="9583f-117">예제 2: 리소스 식별자를 사용 하 여 출시 중지</span><span class="sxs-lookup"><span data-stu-id="9583f-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="9583f-118">이 명령은 ContosoResourceGroup에서 ContosoRollout 이라는 출시를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="9583f-119">예제 3: 롤아웃 개체를 사용 하 여 출시를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="9583f-120">이 명령은 이름 및 ResourceGroup이 $rolloutObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 롤아웃을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="9583f-121">변수</span><span class="sxs-lookup"><span data-stu-id="9583f-121">PARAMETERS</span></span>

### <span data-ttu-id="9583f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9583f-122">-DefaultProfile</span></span>
<span data-ttu-id="9583f-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9583f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9583f-124">-Force</span></span>
<span data-ttu-id="9583f-125">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9583f-126">-이름</span><span class="sxs-lookup"><span data-stu-id="9583f-126">-Name</span></span>
<span data-ttu-id="9583f-127">롤아웃 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="9583f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9583f-128">-ResourceGroupName</span></span>
<span data-ttu-id="9583f-129">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="9583f-129">The resource group.</span></span>

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

### <span data-ttu-id="9583f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9583f-130">-ResourceId</span></span>
<span data-ttu-id="9583f-131">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-131">The resource identifier.</span></span>

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

### <span data-ttu-id="9583f-132">-출시</span><span class="sxs-lookup"><span data-stu-id="9583f-132">-Rollout</span></span>
<span data-ttu-id="9583f-133">제거할 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="9583f-134">-확인</span><span class="sxs-lookup"><span data-stu-id="9583f-134">-Confirm</span></span>
<span data-ttu-id="9583f-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9583f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9583f-136">-WhatIf</span></span>
<span data-ttu-id="9583f-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9583f-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9583f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9583f-139">CommonParameters</span></span>
<span data-ttu-id="9583f-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9583f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9583f-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9583f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9583f-142">입력</span><span class="sxs-lookup"><span data-stu-id="9583f-142">INPUTS</span></span>

### <span data-ttu-id="9583f-143">Microsoft. Azure. PSRollout. 모델. a 배포</span><span class="sxs-lookup"><span data-stu-id="9583f-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="9583f-144">출력</span><span class="sxs-lookup"><span data-stu-id="9583f-144">OUTPUTS</span></span>

### <span data-ttu-id="9583f-145">Microsoft. Azure. PSRollout. 모델. a 배포</span><span class="sxs-lookup"><span data-stu-id="9583f-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="9583f-146">상속자</span><span class="sxs-lookup"><span data-stu-id="9583f-146">NOTES</span></span>

## <span data-ttu-id="9583f-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9583f-147">RELATED LINKS</span></span>

[<span data-ttu-id="9583f-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="9583f-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="9583f-149">다시 시작-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="9583f-149">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="9583f-150">제거-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="9583f-150">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)