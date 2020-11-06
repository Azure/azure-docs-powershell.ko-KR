---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: f329468dce9c520eb647bb0d927ba91de64a5c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523079"
---
# <span data-ttu-id="8d9d1-101">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="8d9d1-101">Remove-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="8d9d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d9d1-102">SYNOPSIS</span></span>
<span data-ttu-id="8d9d1-103">출시를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-103">Deletes a rollout.</span></span>

## <span data-ttu-id="8d9d1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d9d1-104">SYNTAX</span></span>

### <span data-ttu-id="8d9d1-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8d9d1-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d9d1-106">리소스</span><span class="sxs-lookup"><span data-stu-id="8d9d1-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d9d1-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="8d9d1-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d9d1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8d9d1-108">DESCRIPTION</span></span>
<span data-ttu-id="8d9d1-109">**AzureRmDeploymentManagerRollout** cmdlet은 터미널 상태에서 롤아웃을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-109">The **Remove-AzureRmDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="8d9d1-110">이름 및 리소스 그룹 이름을 기준으로 출시를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="8d9d1-111">또는 롤아웃 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="8d9d1-112">예제의</span><span class="sxs-lookup"><span data-stu-id="8d9d1-112">EXAMPLES</span></span>

### <span data-ttu-id="8d9d1-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="8d9d1-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="8d9d1-114">이 명령은 ContosoResourceGroup에서 ContosoRollout 이라는 롤아웃을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="8d9d1-115">예제 2: 리소스 식별자를 사용 하 여 롤아웃 삭제</span><span class="sxs-lookup"><span data-stu-id="8d9d1-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="8d9d1-116">이 명령은 ContosoResourceGroup에서 ContosoRollout 이라는 롤아웃을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="8d9d1-117">예제 3: 롤아웃 개체를 사용 하 여 출시를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="8d9d1-118">이 명령은 이름 및 ResourceGroup이 $rolloutObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 롤아웃을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="8d9d1-119">변수</span><span class="sxs-lookup"><span data-stu-id="8d9d1-119">PARAMETERS</span></span>

### <span data-ttu-id="8d9d1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d9d1-120">-DefaultProfile</span></span>
<span data-ttu-id="8d9d1-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d9d1-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8d9d1-122">-Force</span></span>
<span data-ttu-id="8d9d1-123">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8d9d1-124">-이름</span><span class="sxs-lookup"><span data-stu-id="8d9d1-124">-Name</span></span>
<span data-ttu-id="8d9d1-125">롤아웃 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="8d9d1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d9d1-126">-PassThru</span></span>
<span data-ttu-id="8d9d1-127">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="8d9d1-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8d9d1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d9d1-128">-ResourceGroupName</span></span>
<span data-ttu-id="8d9d1-129">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="8d9d1-129">The resource group.</span></span>

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

### <span data-ttu-id="8d9d1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d9d1-130">-ResourceId</span></span>
<span data-ttu-id="8d9d1-131">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-131">The resource identifier.</span></span>

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

### <span data-ttu-id="8d9d1-132">-출시</span><span class="sxs-lookup"><span data-stu-id="8d9d1-132">-Rollout</span></span>
<span data-ttu-id="8d9d1-133">제거할 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="8d9d1-134">-확인</span><span class="sxs-lookup"><span data-stu-id="8d9d1-134">-Confirm</span></span>
<span data-ttu-id="8d9d1-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d9d1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d9d1-136">-WhatIf</span></span>
<span data-ttu-id="8d9d1-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d9d1-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d9d1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d9d1-139">CommonParameters</span></span>
<span data-ttu-id="8d9d1-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d9d1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d9d1-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d9d1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d9d1-142">입력</span><span class="sxs-lookup"><span data-stu-id="8d9d1-142">INPUTS</span></span>

### <span data-ttu-id="8d9d1-143">Microsoft. Azure. PSRollout. 모델. a 배포</span><span class="sxs-lookup"><span data-stu-id="8d9d1-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="8d9d1-144">출력</span><span class="sxs-lookup"><span data-stu-id="8d9d1-144">OUTPUTS</span></span>

### <span data-ttu-id="8d9d1-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8d9d1-145">System.Boolean</span></span>

## <span data-ttu-id="8d9d1-146">상속자</span><span class="sxs-lookup"><span data-stu-id="8d9d1-146">NOTES</span></span>

## <span data-ttu-id="8d9d1-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d9d1-147">RELATED LINKS</span></span>

[<span data-ttu-id="8d9d1-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="8d9d1-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="8d9d1-149">중지-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="8d9d1-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="8d9d1-150">다시 시작-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="8d9d1-150">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)