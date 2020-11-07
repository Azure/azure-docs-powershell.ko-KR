---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: fbcb93ec75dc0e136c1c18743a8686f7642ef02f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696670"
---
# <span data-ttu-id="9b4b7-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="9b4b7-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="9b4b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b4b7-102">SYNOPSIS</span></span>
<span data-ttu-id="9b4b7-103">출시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-103">Gets the rollout.</span></span>

## <span data-ttu-id="9b4b7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b4b7-104">SYNTAX</span></span>

### <span data-ttu-id="9b4b7-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9b4b7-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b4b7-106">리소스</span><span class="sxs-lookup"><span data-stu-id="9b4b7-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b4b7-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9b4b7-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b4b7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9b4b7-108">DESCRIPTION</span></span>
<span data-ttu-id="9b4b7-109">**AzDeploymentManagerRollout** cmdlet은 롤아웃을 가져오고, 롤아웃 진행 상황에 대 한 모든 세부 정보를 사용 하 여 해당 롤아웃을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="9b4b7-110">이름 및 리소스 그룹 이름을 기준으로 출시를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="9b4b7-111">또는 롤아웃 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="9b4b7-112">반환 되는 출시 개체에는 서비스, 서비스 단위, 배포 된 작업 및 진행 중인 단계가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="9b4b7-113">아직 배포 되지 않은 항목이 응답에 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="9b4b7-114">예제의</span><span class="sxs-lookup"><span data-stu-id="9b4b7-114">EXAMPLES</span></span>

### <span data-ttu-id="9b4b7-115">예제 1 출시 준비</span><span class="sxs-lookup"><span data-stu-id="9b4b7-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="9b4b7-116">이 명령은 ContosoResourceGroup에 ContosoRollout 이라는 롤아웃을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="9b4b7-117">예제 2 롤아웃 세부 정보 가져오기 및 표시</span><span class="sxs-lookup"><span data-stu-id="9b4b7-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="9b4b7-118">이 명령은 ContosoResourceGroup에 ContosoRollout 이라는 롤아웃을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="9b4b7-119">-Verbose 스위치는 모든 롤아웃 세부 정보를 계층적으로 표시 합니다. 롤아웃에 대 한 전체적인 보기를 위해 각 단계의 서비스, ServiceUnits 및 각 단계에 대 한 컨텍스트 정보를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="9b4b7-120">예제 3: 리소스 식별자를 사용 하 여 롤아웃 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b4b7-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="9b4b7-121">이 명령은 ContosoResourceGroup에 ContosoRollout 이라는 롤아웃을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="9b4b7-122">예제 4: 롤아웃 개체를 사용 하 여 출시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="9b4b7-123">이 명령은 이름 및 ResourceGroup이 $rolloutObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 롤아웃을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="9b4b7-124">변수</span><span class="sxs-lookup"><span data-stu-id="9b4b7-124">PARAMETERS</span></span>

### <span data-ttu-id="9b4b7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b4b7-125">-DefaultProfile</span></span>
<span data-ttu-id="9b4b7-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b4b7-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b4b7-127">-InputObject</span></span>
<span data-ttu-id="9b4b7-128">개체를 출시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-128">Rollout object.</span></span>

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

### <span data-ttu-id="9b4b7-129">-이름</span><span class="sxs-lookup"><span data-stu-id="9b4b7-129">-Name</span></span>
<span data-ttu-id="9b4b7-130">롤아웃 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="9b4b7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b4b7-131">-ResourceGroupName</span></span>
<span data-ttu-id="9b4b7-132">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="9b4b7-132">The resource group.</span></span>

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

### <span data-ttu-id="9b4b7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b4b7-133">-ResourceId</span></span>
<span data-ttu-id="9b4b7-134">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-134">The resource identifier.</span></span>

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

### <span data-ttu-id="9b4b7-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="9b4b7-135">-RetryAttempt</span></span>
<span data-ttu-id="9b4b7-136">롤아웃을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-136">The retry attempt of the rollout.</span></span>

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

### <span data-ttu-id="9b4b7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b4b7-137">CommonParameters</span></span>
<span data-ttu-id="9b4b7-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b4b7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b4b7-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b4b7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b4b7-140">입력</span><span class="sxs-lookup"><span data-stu-id="9b4b7-140">INPUTS</span></span>

### <span data-ttu-id="9b4b7-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9b4b7-141">System.String</span></span>

### <span data-ttu-id="9b4b7-142">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="9b4b7-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9b4b7-143">Microsoft. Azure. PSRollout. 모델. a 배포</span><span class="sxs-lookup"><span data-stu-id="9b4b7-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="9b4b7-144">출력</span><span class="sxs-lookup"><span data-stu-id="9b4b7-144">OUTPUTS</span></span>

### <span data-ttu-id="9b4b7-145">Microsoft. Azure. PSRollout. 모델. a 배포</span><span class="sxs-lookup"><span data-stu-id="9b4b7-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="9b4b7-146">상속자</span><span class="sxs-lookup"><span data-stu-id="9b4b7-146">NOTES</span></span>

## <span data-ttu-id="9b4b7-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b4b7-147">RELATED LINKS</span></span>