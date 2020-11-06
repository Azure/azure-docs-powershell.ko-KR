---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 21d0b4f7feec5b32ff732f880924becddd84db73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93522928"
---
# <span data-ttu-id="ad402-101">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="ad402-101">Get-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="ad402-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad402-102">SYNOPSIS</span></span>
<span data-ttu-id="ad402-103">출시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad402-103">Gets a rollout.</span></span>

## <span data-ttu-id="ad402-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad402-104">SYNTAX</span></span>

### <span data-ttu-id="ad402-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ad402-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [[-RetryAttempt] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad402-106">리소스</span><span class="sxs-lookup"><span data-stu-id="ad402-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad402-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ad402-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ad402-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ad402-108">DESCRIPTION</span></span>
<span data-ttu-id="ad402-109">**AzureRmDeploymentManagerRollout** cmdlet은 롤아웃을 가져오고, 롤아웃 진행 상황에 대 한 모든 세부 정보를 사용 하 여 해당 롤아웃을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad402-109">The **Get-AzureRmDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="ad402-110">이름 및 리소스 그룹 이름을 기준으로 출시를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad402-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="ad402-111">또는 롤아웃 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad402-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="ad402-112">예제의</span><span class="sxs-lookup"><span data-stu-id="ad402-112">EXAMPLES</span></span>

### <span data-ttu-id="ad402-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="ad402-113">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="ad402-114">이 명령은 ContosoResourceGroup에 ContosoRollout 이라는 롤아웃을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad402-114">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ad402-115">예제 2: 리소스 식별자를 사용 하 여 롤아웃 가져오기</span><span class="sxs-lookup"><span data-stu-id="ad402-115">Example 2: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="ad402-116">이 명령은 ContosoResourceGroup에 ContosoRollout 이라는 롤아웃을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad402-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ad402-117">예제 3: 롤아웃 개체를 사용 하 여 출시를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad402-117">Example 3: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="ad402-118">이 명령은 이름 및 ResourceGroup이 $rolloutObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 롤아웃을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ad402-118">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="ad402-119">변수</span><span class="sxs-lookup"><span data-stu-id="ad402-119">PARAMETERS</span></span>

### <span data-ttu-id="ad402-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad402-120">-DefaultProfile</span></span>
<span data-ttu-id="ad402-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad402-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad402-122">-이름</span><span class="sxs-lookup"><span data-stu-id="ad402-122">-Name</span></span>
<span data-ttu-id="ad402-123">롤아웃 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad402-123">The name of the rollout.</span></span>

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

### <span data-ttu-id="ad402-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad402-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad402-125">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="ad402-125">The resource group.</span></span>

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

### <span data-ttu-id="ad402-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad402-126">-ResourceId</span></span>
<span data-ttu-id="ad402-127">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ad402-127">The resource identifier.</span></span>

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

### <span data-ttu-id="ad402-128">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="ad402-128">-RetryAttempt</span></span>
<span data-ttu-id="ad402-129">롤아웃을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad402-129">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad402-130">-출시</span><span class="sxs-lookup"><span data-stu-id="ad402-130">-Rollout</span></span>
<span data-ttu-id="ad402-131">개체를 출시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad402-131">Rollout object.</span></span>

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

### <span data-ttu-id="ad402-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad402-132">CommonParameters</span></span>
<span data-ttu-id="ad402-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad402-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad402-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad402-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad402-135">입력</span><span class="sxs-lookup"><span data-stu-id="ad402-135">INPUTS</span></span>

### <span data-ttu-id="ad402-136">않아야</span><span class="sxs-lookup"><span data-stu-id="ad402-136">None</span></span>

## <span data-ttu-id="ad402-137">출력</span><span class="sxs-lookup"><span data-stu-id="ad402-137">OUTPUTS</span></span>

### <span data-ttu-id="ad402-138">Microsoft. Azure. PSRollout. 모델. a 배포</span><span class="sxs-lookup"><span data-stu-id="ad402-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="ad402-139">상속자</span><span class="sxs-lookup"><span data-stu-id="ad402-139">NOTES</span></span>

## <span data-ttu-id="ad402-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad402-140">RELATED LINKS</span></span>

[<span data-ttu-id="ad402-141">중지-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="ad402-141">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="ad402-142">다시 시작-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="ad402-142">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="ad402-143">제거-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="ad402-143">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)