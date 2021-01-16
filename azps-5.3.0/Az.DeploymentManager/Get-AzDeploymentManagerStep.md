---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: 68bc2af69c3450f0c52c5613057ba4b2db211ee8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387465"
---
# <span data-ttu-id="e1552-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="e1552-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="e1552-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1552-102">SYNOPSIS</span></span>
<span data-ttu-id="e1552-103">단계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e1552-103">Gets the step.</span></span>

## <span data-ttu-id="e1552-104">구문</span><span class="sxs-lookup"><span data-stu-id="e1552-104">SYNTAX</span></span>

### <span data-ttu-id="e1552-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="e1552-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1552-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1552-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1552-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e1552-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1552-108">설명</span><span class="sxs-lookup"><span data-stu-id="e1552-108">DESCRIPTION</span></span>
<span data-ttu-id="e1552-109">**Get-AzDeploymentManagerStep** cmdlet은 단계를 얻게 하여 해당 단계를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e1552-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="e1552-110">해당 이름 및 리소스 그룹 이름으로 단계를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1552-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="e1552-111">또는 단계 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1552-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="e1552-112">이 개체를 로컬로 수정한 다음, Set-AzDeploymentManagerStep cmdlet을 사용하여 아티팩트 원본에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e1552-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="e1552-113">예제</span><span class="sxs-lookup"><span data-stu-id="e1552-113">EXAMPLES</span></span>

### <span data-ttu-id="e1552-114">예제 1: 단계하기</span><span class="sxs-lookup"><span data-stu-id="e1552-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="e1552-115">이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep이라는 단계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e1552-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="e1552-116">예제 2: 리소스 식별자를 사용하여 단계 얻기</span><span class="sxs-lookup"><span data-stu-id="e1552-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="e1552-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="e1552-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="e1552-118">이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep이라는 단계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e1552-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="e1552-119">예제 3: 개체가 반환한 개체를 사용하여 New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="e1552-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="e1552-120">이 명령은 이름과 ResourceGroup이 각각 이름 및 ResourceGroupName 속성과 일치하는 단계를 $stepObject.</span><span class="sxs-lookup"><span data-stu-id="e1552-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="e1552-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1552-121">PARAMETERS</span></span>

### <span data-ttu-id="e1552-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1552-122">-DefaultProfile</span></span>
<span data-ttu-id="e1552-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1552-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1552-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1552-124">-InputObject</span></span>
<span data-ttu-id="e1552-125">단계 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e1552-125">The step resource object.</span></span>

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

### <span data-ttu-id="e1552-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e1552-126">-Name</span></span>
<span data-ttu-id="e1552-127">단계의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1552-127">The name of the step.</span></span>

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

### <span data-ttu-id="e1552-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1552-128">-ResourceGroupName</span></span>
<span data-ttu-id="e1552-129">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="e1552-129">The resource group.</span></span>

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

### <span data-ttu-id="e1552-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1552-130">-ResourceId</span></span>
<span data-ttu-id="e1552-131">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e1552-131">The resource identifier.</span></span>

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

### <span data-ttu-id="e1552-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1552-132">CommonParameters</span></span>
<span data-ttu-id="e1552-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e1552-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1552-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e1552-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1552-135">입력</span><span class="sxs-lookup"><span data-stu-id="e1552-135">INPUTS</span></span>

### <span data-ttu-id="e1552-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e1552-136">System.String</span></span>

### <span data-ttu-id="e1552-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="e1552-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="e1552-138">출력</span><span class="sxs-lookup"><span data-stu-id="e1552-138">OUTPUTS</span></span>

### <span data-ttu-id="e1552-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="e1552-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="e1552-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e1552-140">NOTES</span></span>

## <span data-ttu-id="e1552-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1552-141">RELATED LINKS</span></span>
