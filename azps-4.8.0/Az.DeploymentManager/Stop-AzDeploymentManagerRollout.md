---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: cd59cd39fb2834bed2162a257905fea643c0a767
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212804"
---
# <span data-ttu-id="feaf2-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="feaf2-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="feaf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feaf2-102">SYNOPSIS</span></span>
<span data-ttu-id="feaf2-103">출시를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-103">Stops the rollout.</span></span>

## <span data-ttu-id="feaf2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="feaf2-104">SYNTAX</span></span>

### <span data-ttu-id="feaf2-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="feaf2-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feaf2-106">리소스</span><span class="sxs-lookup"><span data-stu-id="feaf2-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feaf2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="feaf2-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="feaf2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="feaf2-108">DESCRIPTION</span></span>
<span data-ttu-id="feaf2-109">**AzDeploymentManagerRollout** cmdlet은 진행 중인 출시를 중지 하 고 롤아웃의 현재 상태를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="feaf2-110">이름 및 리소스 그룹 이름을 기준으로 출시를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="feaf2-111">또는 롤아웃 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="feaf2-112">롤아웃이 중지 되 면 다시 시작 하거나 다시 시작할 수 없다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="feaf2-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="feaf2-113">새 출시만 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="feaf2-114">예제의</span><span class="sxs-lookup"><span data-stu-id="feaf2-114">EXAMPLES</span></span>

### <span data-ttu-id="feaf2-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="feaf2-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="feaf2-116">이 명령은 ContosoResourceGroup에서 ContosoRollout 이라는 출시를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="feaf2-117">예제 2: 리소스 식별자를 사용 하 여 출시 중지</span><span class="sxs-lookup"><span data-stu-id="feaf2-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="feaf2-118">이 명령은 ContosoResourceGroup에서 ContosoRollout 이라는 출시를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="feaf2-119">예제 3: 롤아웃 개체를 사용 하 여 출시를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="feaf2-120">이 명령은 이름 및 ResourceGroup이 $rolloutObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 롤아웃을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="feaf2-121">변수</span><span class="sxs-lookup"><span data-stu-id="feaf2-121">PARAMETERS</span></span>

### <span data-ttu-id="feaf2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feaf2-122">-DefaultProfile</span></span>
<span data-ttu-id="feaf2-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="feaf2-124">-Force</span><span class="sxs-lookup"><span data-stu-id="feaf2-124">-Force</span></span>
<span data-ttu-id="feaf2-125">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="feaf2-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="feaf2-126">-InputObject</span></span>
<span data-ttu-id="feaf2-127">제거할 롤아웃입니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="feaf2-128">-이름</span><span class="sxs-lookup"><span data-stu-id="feaf2-128">-Name</span></span>
<span data-ttu-id="feaf2-129">롤아웃 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="feaf2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feaf2-130">-ResourceGroupName</span></span>
<span data-ttu-id="feaf2-131">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="feaf2-131">The resource group.</span></span>

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

### <span data-ttu-id="feaf2-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="feaf2-132">-ResourceId</span></span>
<span data-ttu-id="feaf2-133">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-133">The resource identifier.</span></span>

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

### <span data-ttu-id="feaf2-134">-확인</span><span class="sxs-lookup"><span data-stu-id="feaf2-134">-Confirm</span></span>
<span data-ttu-id="feaf2-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feaf2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feaf2-136">-WhatIf</span></span>
<span data-ttu-id="feaf2-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="feaf2-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feaf2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feaf2-139">CommonParameters</span></span>
<span data-ttu-id="feaf2-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="feaf2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feaf2-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="feaf2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feaf2-142">입력</span><span class="sxs-lookup"><span data-stu-id="feaf2-142">INPUTS</span></span>

### <span data-ttu-id="feaf2-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="feaf2-143">System.String</span></span>

### <span data-ttu-id="feaf2-144">Microsoft. Azure. PSRollout. 모델. a 배포</span><span class="sxs-lookup"><span data-stu-id="feaf2-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="feaf2-145">출력</span><span class="sxs-lookup"><span data-stu-id="feaf2-145">OUTPUTS</span></span>

### <span data-ttu-id="feaf2-146">Microsoft. Azure. PSRollout. 모델. a 배포</span><span class="sxs-lookup"><span data-stu-id="feaf2-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="feaf2-147">상속자</span><span class="sxs-lookup"><span data-stu-id="feaf2-147">NOTES</span></span>

## <span data-ttu-id="feaf2-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="feaf2-148">RELATED LINKS</span></span>
