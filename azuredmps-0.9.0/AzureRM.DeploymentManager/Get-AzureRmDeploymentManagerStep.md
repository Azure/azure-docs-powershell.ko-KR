---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: bd17ee5dd653ee66daf014c57661b3787c04b06f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523183"
---
# <span data-ttu-id="bea4d-101">Get-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="bea4d-101">Get-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="bea4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bea4d-102">SYNOPSIS</span></span>
<span data-ttu-id="bea4d-103">배포 단계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bea4d-103">Gets the deployment step.</span></span>

## <span data-ttu-id="bea4d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bea4d-104">SYNTAX</span></span>

### <span data-ttu-id="bea4d-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="bea4d-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bea4d-106">리소스</span><span class="sxs-lookup"><span data-stu-id="bea4d-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bea4d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="bea4d-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bea4d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bea4d-108">DESCRIPTION</span></span>
<span data-ttu-id="bea4d-109">**Get-AzureRmDeploymentManagerStep** cmdlet은 단계를 가져오고 해당 단계를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bea4d-109">The **Get-AzureRmDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="bea4d-110">해당 이름 및 리소스 그룹 이름으로 단계를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bea4d-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="bea4d-111">또는 Step 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bea4d-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="bea4d-112">이 개체를 로컬로 수정한 다음 Set-AzureRmDeploymentManagerStep cmdlet을 사용 하 여 아티팩트 원본에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bea4d-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="bea4d-113">예제의</span><span class="sxs-lookup"><span data-stu-id="bea4d-113">EXAMPLES</span></span>

### <span data-ttu-id="bea4d-114">예제 1: 단계 가져오기</span><span class="sxs-lookup"><span data-stu-id="bea4d-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="bea4d-115">이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep 이라는 단계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bea4d-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="bea4d-116">예제 2: 리소스 식별자를 사용 하 여 단계 가져오기</span><span class="sxs-lookup"><span data-stu-id="bea4d-116">Example 2: Get a step using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="bea4d-117">이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep 이라는 단계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bea4d-117">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="bea4d-118">예제 3: New-AzureRmDeploymentManagerStep에서 반환 된 개체를 사용 하 여 단계 가져오기</span><span class="sxs-lookup"><span data-stu-id="bea4d-118">Example 3: Get a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="bea4d-119">이 명령은 name 및 ResourceGroup이 $stepObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 단계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bea4d-119">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>


## <span data-ttu-id="bea4d-120">변수</span><span class="sxs-lookup"><span data-stu-id="bea4d-120">PARAMETERS</span></span>

### <span data-ttu-id="bea4d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea4d-121">-DefaultProfile</span></span>
<span data-ttu-id="bea4d-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bea4d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bea4d-123">-이름</span><span class="sxs-lookup"><span data-stu-id="bea4d-123">-Name</span></span>
<span data-ttu-id="bea4d-124">단계의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bea4d-124">The name of the step.</span></span>

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

### <span data-ttu-id="bea4d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea4d-125">-ResourceGroupName</span></span>
<span data-ttu-id="bea4d-126">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="bea4d-126">The resource group.</span></span>

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

### <span data-ttu-id="bea4d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bea4d-127">-ResourceId</span></span>
<span data-ttu-id="bea4d-128">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bea4d-128">The resource identifier.</span></span>

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

### <span data-ttu-id="bea4d-129">-단계</span><span class="sxs-lookup"><span data-stu-id="bea4d-129">-Step</span></span>
<span data-ttu-id="bea4d-130">단계 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bea4d-130">The step resource object.</span></span>

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

### <span data-ttu-id="bea4d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea4d-131">CommonParameters</span></span>
<span data-ttu-id="bea4d-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bea4d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bea4d-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bea4d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea4d-134">입력</span><span class="sxs-lookup"><span data-stu-id="bea4d-134">INPUTS</span></span>

### <span data-ttu-id="bea4d-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bea4d-135">System.String</span></span>

### <span data-ttu-id="bea4d-136">PSStepResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="bea4d-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="bea4d-137">출력</span><span class="sxs-lookup"><span data-stu-id="bea4d-137">OUTPUTS</span></span>

### <span data-ttu-id="bea4d-138">PSStepResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="bea4d-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="bea4d-139">상속자</span><span class="sxs-lookup"><span data-stu-id="bea4d-139">NOTES</span></span>

## <span data-ttu-id="bea4d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bea4d-140">RELATED LINKS</span></span>
