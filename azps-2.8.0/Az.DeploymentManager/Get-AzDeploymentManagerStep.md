---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: eb0c7db4706aacfba4010632422869f0dca54694
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696663"
---
# <span data-ttu-id="214b7-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="214b7-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="214b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="214b7-102">SYNOPSIS</span></span>
<span data-ttu-id="214b7-103">단계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="214b7-103">Gets the step.</span></span>

## <span data-ttu-id="214b7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="214b7-104">SYNTAX</span></span>

### <span data-ttu-id="214b7-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="214b7-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="214b7-106">리소스</span><span class="sxs-lookup"><span data-stu-id="214b7-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="214b7-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="214b7-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="214b7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="214b7-108">DESCRIPTION</span></span>
<span data-ttu-id="214b7-109">**Get-AzDeploymentManagerStep** cmdlet은 단계를 가져오고 해당 단계를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="214b7-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="214b7-110">해당 이름 및 리소스 그룹 이름으로 단계를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="214b7-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="214b7-111">또는 Step 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="214b7-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="214b7-112">이 개체를 로컬로 수정한 다음 Set-AzDeploymentManagerStep cmdlet을 사용 하 여 아티팩트 원본에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="214b7-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="214b7-113">예제의</span><span class="sxs-lookup"><span data-stu-id="214b7-113">EXAMPLES</span></span>

### <span data-ttu-id="214b7-114">예제 1: 단계 가져오기</span><span class="sxs-lookup"><span data-stu-id="214b7-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="214b7-115">이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep 이라는 단계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="214b7-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="214b7-116">예제 2: 리소스 식별자를 사용 하 여 단계 가져오기</span><span class="sxs-lookup"><span data-stu-id="214b7-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="214b7-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="214b7-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="214b7-118">이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep 이라는 단계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="214b7-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="214b7-119">예제 3: New-AzDeploymentManagerStep에서 반환 된 개체를 사용 하 여 단계 가져오기</span><span class="sxs-lookup"><span data-stu-id="214b7-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="214b7-120">이 명령은 name 및 ResourceGroup이 $stepObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 단계를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="214b7-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="214b7-121">변수</span><span class="sxs-lookup"><span data-stu-id="214b7-121">PARAMETERS</span></span>

### <span data-ttu-id="214b7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214b7-122">-DefaultProfile</span></span>
<span data-ttu-id="214b7-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="214b7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="214b7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="214b7-124">-InputObject</span></span>
<span data-ttu-id="214b7-125">단계 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="214b7-125">The step resource object.</span></span>

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

### <span data-ttu-id="214b7-126">-이름</span><span class="sxs-lookup"><span data-stu-id="214b7-126">-Name</span></span>
<span data-ttu-id="214b7-127">단계의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="214b7-127">The name of the step.</span></span>

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

### <span data-ttu-id="214b7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="214b7-128">-ResourceGroupName</span></span>
<span data-ttu-id="214b7-129">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="214b7-129">The resource group.</span></span>

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

### <span data-ttu-id="214b7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="214b7-130">-ResourceId</span></span>
<span data-ttu-id="214b7-131">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="214b7-131">The resource identifier.</span></span>

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

### <span data-ttu-id="214b7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214b7-132">CommonParameters</span></span>
<span data-ttu-id="214b7-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="214b7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214b7-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="214b7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214b7-135">입력</span><span class="sxs-lookup"><span data-stu-id="214b7-135">INPUTS</span></span>

### <span data-ttu-id="214b7-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="214b7-136">System.String</span></span>

### <span data-ttu-id="214b7-137">PSStepResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="214b7-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="214b7-138">출력</span><span class="sxs-lookup"><span data-stu-id="214b7-138">OUTPUTS</span></span>

### <span data-ttu-id="214b7-139">PSStepResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="214b7-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="214b7-140">상속자</span><span class="sxs-lookup"><span data-stu-id="214b7-140">NOTES</span></span>

## <span data-ttu-id="214b7-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="214b7-141">RELATED LINKS</span></span>
