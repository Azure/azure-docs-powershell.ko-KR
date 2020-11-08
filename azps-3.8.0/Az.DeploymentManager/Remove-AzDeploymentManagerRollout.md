---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 8e5e2c25f69d6e61c21a0f616f49079710c2d5db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044400"
---
# <span data-ttu-id="7b668-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7b668-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="7b668-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b668-102">SYNOPSIS</span></span>
<span data-ttu-id="7b668-103">출시를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b668-103">Deletes the rollout.</span></span>

## <span data-ttu-id="7b668-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7b668-104">SYNTAX</span></span>

### <span data-ttu-id="7b668-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="7b668-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b668-106">리소스</span><span class="sxs-lookup"><span data-stu-id="7b668-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b668-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7b668-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b668-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7b668-108">DESCRIPTION</span></span>
<span data-ttu-id="7b668-109">**AzDeploymentManagerRollout** cmdlet은 터미널 상태에서 롤아웃을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b668-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="7b668-110">이름 및 리소스 그룹 이름을 기준으로 출시를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b668-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="7b668-111">또는 롤아웃 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b668-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="7b668-112">예제의</span><span class="sxs-lookup"><span data-stu-id="7b668-112">EXAMPLES</span></span>

### <span data-ttu-id="7b668-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="7b668-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="7b668-114">이 명령은 ContosoResourceGroup에서 ContosoRollout 이라는 롤아웃을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b668-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7b668-115">예제 2: 리소스 식별자를 사용 하 여 롤아웃 삭제</span><span class="sxs-lookup"><span data-stu-id="7b668-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="7b668-116">이 명령은 ContosoResourceGroup에서 ContosoRollout 이라는 롤아웃을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b668-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7b668-117">예제 3: 롤아웃 개체를 사용 하 여 출시를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b668-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="7b668-118">이 명령은 이름 및 ResourceGroup이 $rolloutObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 롤아웃을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b668-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="7b668-119">변수</span><span class="sxs-lookup"><span data-stu-id="7b668-119">PARAMETERS</span></span>

### <span data-ttu-id="7b668-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b668-120">-DefaultProfile</span></span>
<span data-ttu-id="7b668-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b668-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b668-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b668-122">-InputObject</span></span>
<span data-ttu-id="7b668-123">제거할 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="7b668-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="7b668-124">-이름</span><span class="sxs-lookup"><span data-stu-id="7b668-124">-Name</span></span>
<span data-ttu-id="7b668-125">롤아웃 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b668-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="7b668-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b668-126">-PassThru</span></span>
<span data-ttu-id="7b668-127">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="7b668-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7b668-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b668-128">-ResourceGroupName</span></span>
<span data-ttu-id="7b668-129">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="7b668-129">The resource group.</span></span>

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

### <span data-ttu-id="7b668-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b668-130">-ResourceId</span></span>
<span data-ttu-id="7b668-131">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7b668-131">The resource identifier.</span></span>

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

### <span data-ttu-id="7b668-132">-확인</span><span class="sxs-lookup"><span data-stu-id="7b668-132">-Confirm</span></span>
<span data-ttu-id="7b668-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b668-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b668-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b668-134">-WhatIf</span></span>
<span data-ttu-id="7b668-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b668-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b668-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b668-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b668-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b668-137">CommonParameters</span></span>
<span data-ttu-id="7b668-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b668-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b668-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7b668-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b668-140">입력</span><span class="sxs-lookup"><span data-stu-id="7b668-140">INPUTS</span></span>

### <span data-ttu-id="7b668-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7b668-141">System.String</span></span>

### <span data-ttu-id="7b668-142">Microsoft. Azure. PSRollout. 모델. a 배포</span><span class="sxs-lookup"><span data-stu-id="7b668-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7b668-143">출력</span><span class="sxs-lookup"><span data-stu-id="7b668-143">OUTPUTS</span></span>

### <span data-ttu-id="7b668-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7b668-144">System.Boolean</span></span>

## <span data-ttu-id="7b668-145">상속자</span><span class="sxs-lookup"><span data-stu-id="7b668-145">NOTES</span></span>

## <span data-ttu-id="7b668-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b668-146">RELATED LINKS</span></span>
