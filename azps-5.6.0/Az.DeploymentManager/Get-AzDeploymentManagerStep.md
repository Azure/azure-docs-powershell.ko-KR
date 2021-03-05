---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: 5bf59cb766d82e2fc50bdc75c0a072e2b8d17a69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966347"
---
# <span data-ttu-id="bb77e-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="bb77e-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="bb77e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb77e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb77e-103">단계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb77e-103">Gets the step.</span></span>

## <span data-ttu-id="bb77e-104">구문</span><span class="sxs-lookup"><span data-stu-id="bb77e-104">SYNTAX</span></span>

### <span data-ttu-id="bb77e-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="bb77e-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb77e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb77e-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb77e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="bb77e-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb77e-108">설명</span><span class="sxs-lookup"><span data-stu-id="bb77e-108">DESCRIPTION</span></span>
<span data-ttu-id="bb77e-109">**Get-AzDeploymentManagerStep** cmdlet은 단계를 시작하고 해당 단계를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bb77e-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="bb77e-110">해당 이름 및 리소스 그룹 이름으로 단계를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bb77e-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="bb77e-111">또는 단계 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb77e-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="bb77e-112">이 개체를 로컬로 수정한 다음, cmdlet을 사용하여 아티팩트 원본에 Set-AzDeploymentManagerStep 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb77e-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="bb77e-113">예제</span><span class="sxs-lookup"><span data-stu-id="bb77e-113">EXAMPLES</span></span>

### <span data-ttu-id="bb77e-114">예제 1: 단계 시작</span><span class="sxs-lookup"><span data-stu-id="bb77e-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="bb77e-115">이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep이라는 단계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb77e-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="bb77e-116">예제 2: 리소스 식별자를 사용하여 단계 시작</span><span class="sxs-lookup"><span data-stu-id="bb77e-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="bb77e-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="bb77e-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="bb77e-118">이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep이라는 단계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb77e-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="bb77e-119">예제 3: 개체가 반환한 개체를 사용하여 단계 New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="bb77e-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="bb77e-120">이 명령은 이름과 ResourceGroup이 각각 해당 명령의 이름 및 ResourceGroupName 속성과 일치하는 $stepObject 를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bb77e-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="bb77e-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bb77e-121">PARAMETERS</span></span>

### <span data-ttu-id="bb77e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb77e-122">-DefaultProfile</span></span>
<span data-ttu-id="bb77e-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb77e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb77e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb77e-124">-InputObject</span></span>
<span data-ttu-id="bb77e-125">단계 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bb77e-125">The step resource object.</span></span>

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

### <span data-ttu-id="bb77e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="bb77e-126">-Name</span></span>
<span data-ttu-id="bb77e-127">단계의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bb77e-127">The name of the step.</span></span>

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

### <span data-ttu-id="bb77e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb77e-128">-ResourceGroupName</span></span>
<span data-ttu-id="bb77e-129">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="bb77e-129">The resource group.</span></span>

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

### <span data-ttu-id="bb77e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb77e-130">-ResourceId</span></span>
<span data-ttu-id="bb77e-131">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bb77e-131">The resource identifier.</span></span>

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

### <span data-ttu-id="bb77e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb77e-132">CommonParameters</span></span>
<span data-ttu-id="bb77e-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bb77e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb77e-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb77e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb77e-135">입력</span><span class="sxs-lookup"><span data-stu-id="bb77e-135">INPUTS</span></span>

### <span data-ttu-id="bb77e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bb77e-136">System.String</span></span>

### <span data-ttu-id="bb77e-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="bb77e-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="bb77e-138">출력</span><span class="sxs-lookup"><span data-stu-id="bb77e-138">OUTPUTS</span></span>

### <span data-ttu-id="bb77e-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="bb77e-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="bb77e-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bb77e-140">NOTES</span></span>

## <span data-ttu-id="bb77e-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb77e-141">RELATED LINKS</span></span>
