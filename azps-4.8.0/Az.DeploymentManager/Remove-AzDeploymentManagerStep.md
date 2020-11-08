---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 5e4af2ef006e51cee135dd642bcae7282940e8be
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047793"
---
# <span data-ttu-id="b4981-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="b4981-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="b4981-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4981-102">SYNOPSIS</span></span>
<span data-ttu-id="b4981-103">단계를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4981-103">Deletes the step.</span></span>

## <span data-ttu-id="b4981-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4981-104">SYNTAX</span></span>

### <span data-ttu-id="b4981-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b4981-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4981-106">리소스</span><span class="sxs-lookup"><span data-stu-id="b4981-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4981-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b4981-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4981-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b4981-108">DESCRIPTION</span></span>
<span data-ttu-id="b4981-109">**제거-AzDeploymentManagerStep** cmdlet은 단계를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4981-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="b4981-110">단계별 이름과 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4981-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="b4981-111">또는 Step 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b4981-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="b4981-112">예제의</span><span class="sxs-lookup"><span data-stu-id="b4981-112">EXAMPLES</span></span>

### <span data-ttu-id="b4981-113">예제 1: 단계 제거</span><span class="sxs-lookup"><span data-stu-id="b4981-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="b4981-114">이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep 이라는 단계를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4981-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b4981-115">예제 2: 리소스 식별자를 사용 하 여 단계 제거</span><span class="sxs-lookup"><span data-stu-id="b4981-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="b4981-116">이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep 이라는 단계를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4981-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b4981-117">예제 3: New-AzDeploymentManagerStep에서 반환 된 개체를 사용 하 여 단계 제거</span><span class="sxs-lookup"><span data-stu-id="b4981-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="b4981-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="b4981-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="b4981-119">이 명령은 name 및 ResourceGroup이 $stepObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 단계를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4981-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="b4981-120">변수</span><span class="sxs-lookup"><span data-stu-id="b4981-120">PARAMETERS</span></span>

### <span data-ttu-id="b4981-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4981-121">-DefaultProfile</span></span>
<span data-ttu-id="b4981-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b4981-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4981-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4981-123">-InputObject</span></span>
<span data-ttu-id="b4981-124">제거할 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="b4981-124">The step to be removed.</span></span>

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

### <span data-ttu-id="b4981-125">-이름</span><span class="sxs-lookup"><span data-stu-id="b4981-125">-Name</span></span>
<span data-ttu-id="b4981-126">단계의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4981-126">The name of the step.</span></span>

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

### <span data-ttu-id="b4981-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4981-127">-PassThru</span></span>
<span data-ttu-id="b4981-128">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="b4981-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b4981-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4981-129">-ResourceGroupName</span></span>
<span data-ttu-id="b4981-130">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="b4981-130">The resource group.</span></span>

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

### <span data-ttu-id="b4981-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4981-131">-ResourceId</span></span>
<span data-ttu-id="b4981-132">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b4981-132">The resource identifier.</span></span>

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

### <span data-ttu-id="b4981-133">-확인</span><span class="sxs-lookup"><span data-stu-id="b4981-133">-Confirm</span></span>
<span data-ttu-id="b4981-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4981-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4981-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4981-135">-WhatIf</span></span>
<span data-ttu-id="b4981-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b4981-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4981-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4981-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4981-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4981-138">CommonParameters</span></span>
<span data-ttu-id="b4981-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4981-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4981-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4981-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4981-141">입력</span><span class="sxs-lookup"><span data-stu-id="b4981-141">INPUTS</span></span>

### <span data-ttu-id="b4981-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b4981-142">System.String</span></span>

### <span data-ttu-id="b4981-143">PSStepResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="b4981-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="b4981-144">출력</span><span class="sxs-lookup"><span data-stu-id="b4981-144">OUTPUTS</span></span>

### <span data-ttu-id="b4981-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b4981-145">System.Boolean</span></span>

## <span data-ttu-id="b4981-146">상속자</span><span class="sxs-lookup"><span data-stu-id="b4981-146">NOTES</span></span>

## <span data-ttu-id="b4981-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4981-147">RELATED LINKS</span></span>
