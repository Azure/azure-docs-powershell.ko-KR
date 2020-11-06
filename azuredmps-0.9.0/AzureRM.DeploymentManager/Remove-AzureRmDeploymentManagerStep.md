---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 3abceb6c3c270378c911036967698f459cbe063a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523164"
---
# <span data-ttu-id="0158f-101">Remove-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="0158f-101">Remove-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="0158f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0158f-102">SYNOPSIS</span></span>
<span data-ttu-id="0158f-103">단계를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0158f-103">Deletes a step.</span></span>

## <span data-ttu-id="0158f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0158f-104">SYNTAX</span></span>

### <span data-ttu-id="0158f-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="0158f-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0158f-106">리소스</span><span class="sxs-lookup"><span data-stu-id="0158f-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0158f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="0158f-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0158f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0158f-108">DESCRIPTION</span></span>
<span data-ttu-id="0158f-109">**제거-AzureRmDeploymentManagerStep** cmdlet은 단계를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0158f-109">The **Remove-AzureRmDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="0158f-110">단계별 이름과 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0158f-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="0158f-111">또는 Step 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0158f-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="0158f-112">예제의</span><span class="sxs-lookup"><span data-stu-id="0158f-112">EXAMPLES</span></span>
### <span data-ttu-id="0158f-113">예제 1: 단계 제거</span><span class="sxs-lookup"><span data-stu-id="0158f-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="0158f-114">이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep 이라는 단계를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0158f-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="0158f-115">예제 2: 리소스 식별자를 사용 하 여 단계 제거</span><span class="sxs-lookup"><span data-stu-id="0158f-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="0158f-116">이 명령은 ContosoResourceGroup에서 ContosoService1WaitStep 이라는 단계를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0158f-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="0158f-117">예제 3: New-AzureRmDeploymentManagerStep에서 반환 된 개체를 사용 하 여 단계 제거</span><span class="sxs-lookup"><span data-stu-id="0158f-117">Example 3: Remove a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="0158f-118">이 명령은 name 및 ResourceGroup이 $stepObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 단계를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="0158f-118">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="0158f-119">변수</span><span class="sxs-lookup"><span data-stu-id="0158f-119">PARAMETERS</span></span>

### <span data-ttu-id="0158f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0158f-120">-DefaultProfile</span></span>
<span data-ttu-id="0158f-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0158f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0158f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0158f-122">-Force</span></span>
<span data-ttu-id="0158f-123">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0158f-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0158f-124">-이름</span><span class="sxs-lookup"><span data-stu-id="0158f-124">-Name</span></span>
<span data-ttu-id="0158f-125">단계의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0158f-125">The name of the step.</span></span>

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

### <span data-ttu-id="0158f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0158f-126">-PassThru</span></span>
<span data-ttu-id="0158f-127">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="0158f-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0158f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0158f-128">-ResourceGroupName</span></span>
<span data-ttu-id="0158f-129">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="0158f-129">The resource group.</span></span>

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

### <span data-ttu-id="0158f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0158f-130">-ResourceId</span></span>
<span data-ttu-id="0158f-131">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0158f-131">The resource identifier.</span></span>

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

### <span data-ttu-id="0158f-132">-단계</span><span class="sxs-lookup"><span data-stu-id="0158f-132">-Step</span></span>
<span data-ttu-id="0158f-133">제거할 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="0158f-133">The step to be removed.</span></span>

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

### <span data-ttu-id="0158f-134">-확인</span><span class="sxs-lookup"><span data-stu-id="0158f-134">-Confirm</span></span>
<span data-ttu-id="0158f-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0158f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0158f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0158f-136">-WhatIf</span></span>
<span data-ttu-id="0158f-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0158f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0158f-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0158f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0158f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0158f-139">CommonParameters</span></span>
<span data-ttu-id="0158f-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0158f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0158f-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0158f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0158f-142">입력</span><span class="sxs-lookup"><span data-stu-id="0158f-142">INPUTS</span></span>

### <span data-ttu-id="0158f-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0158f-143">System.String</span></span>

### <span data-ttu-id="0158f-144">PSStepResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="0158f-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="0158f-145">출력</span><span class="sxs-lookup"><span data-stu-id="0158f-145">OUTPUTS</span></span>

### <span data-ttu-id="0158f-146">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0158f-146">System.Boolean</span></span>

## <span data-ttu-id="0158f-147">상속자</span><span class="sxs-lookup"><span data-stu-id="0158f-147">NOTES</span></span>

## <span data-ttu-id="0158f-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0158f-148">RELATED LINKS</span></span>
