---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387486"
---
# <span data-ttu-id="e7869-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="e7869-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="e7869-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7869-102">SYNOPSIS</span></span>
<span data-ttu-id="e7869-103">롤아웃을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-103">Gets the rollout.</span></span>

## <span data-ttu-id="e7869-104">구문</span><span class="sxs-lookup"><span data-stu-id="e7869-104">SYNTAX</span></span>

### <span data-ttu-id="e7869-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="e7869-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7869-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7869-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7869-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e7869-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7869-108">설명</span><span class="sxs-lookup"><span data-stu-id="e7869-108">DESCRIPTION</span></span>
<span data-ttu-id="e7869-109">**Get-AzDeploymentManagerRollout** cmdlet은 롤아웃을 구하고 롤아웃 진행률에 대한 모든 세부 정보가 있는 해당 롤아웃을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="e7869-110">이름 및 리소스 그룹 이름으로 롤아웃을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="e7869-111">또는 Rollout 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="e7869-112">반환된 롤아웃 개체에는 배포된 서비스, 서비스 단위 및 단계 및 진행 중 단계가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="e7869-113">아직 배포되지 않은 것은 응답에 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="e7869-114">예제</span><span class="sxs-lookup"><span data-stu-id="e7869-114">EXAMPLES</span></span>

### <span data-ttu-id="e7869-115">예제 1 롤아웃하기</span><span class="sxs-lookup"><span data-stu-id="e7869-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="e7869-116">이 명령은 ContosoResourceGroup에서 ContosoRollout이라는 롤아웃을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="e7869-117">예제 2 롤아웃 세부 정보 표시</span><span class="sxs-lookup"><span data-stu-id="e7869-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="e7869-118">이 명령은 ContosoResourceGroup에서 ContosoRollout이라는 롤아웃을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="e7869-119">-Verbose 스위치는 모든 롤아웃 세부 정보를 계층적으로 표시됩니다. 서비스, ServiceUnits 및 각 ServiceUnit의 단계 및 롤아웃의 전체적인 보기에 대한 각 단계에 대한 상황별 정보를 보여 줄 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="e7869-120">예제 3: 리소스 식별자를 사용하여 롤아웃하기</span><span class="sxs-lookup"><span data-stu-id="e7869-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="e7869-121">이 명령은 ContosoResourceGroup에서 ContosoRollout이라는 롤아웃을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e7869-122">예제 4: 롤아웃 개체를 사용하여 롤아웃합니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="e7869-123">이 명령은 이름과 ResourceGroup이 각각 이름 및 ResourceGroupName 속성과 일치하는 롤아웃을 $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="e7869-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="e7869-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7869-124">PARAMETERS</span></span>

### <span data-ttu-id="e7869-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7869-125">-DefaultProfile</span></span>
<span data-ttu-id="e7869-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7869-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7869-127">-InputObject</span></span>
<span data-ttu-id="e7869-128">롤아웃 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-128">Rollout object.</span></span>

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

### <span data-ttu-id="e7869-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e7869-129">-Name</span></span>
<span data-ttu-id="e7869-130">롤아웃의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-130">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7869-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7869-131">-ResourceGroupName</span></span>
<span data-ttu-id="e7869-132">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-132">The resource group.</span></span>

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

### <span data-ttu-id="e7869-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7869-133">-ResourceId</span></span>
<span data-ttu-id="e7869-134">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-134">The resource identifier.</span></span>

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

### <span data-ttu-id="e7869-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="e7869-135">-RetryAttempt</span></span>
<span data-ttu-id="e7869-136">롤아웃의 재시도 시도입니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-136">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7869-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7869-137">CommonParameters</span></span>
<span data-ttu-id="e7869-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e7869-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7869-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e7869-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7869-140">입력</span><span class="sxs-lookup"><span data-stu-id="e7869-140">INPUTS</span></span>

### <span data-ttu-id="e7869-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e7869-141">System.String</span></span>

### <span data-ttu-id="e7869-142">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e7869-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e7869-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="e7869-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="e7869-144">출력</span><span class="sxs-lookup"><span data-stu-id="e7869-144">OUTPUTS</span></span>

### <span data-ttu-id="e7869-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="e7869-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="e7869-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e7869-146">NOTES</span></span>

## <span data-ttu-id="e7869-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7869-147">RELATED LINKS</span></span>
