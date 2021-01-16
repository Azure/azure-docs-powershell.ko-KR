---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: 3f2b09e047a4a7e39efe6f0f1724776f14a90d2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355574"
---
# <span data-ttu-id="3dd6d-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="3dd6d-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="3dd6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dd6d-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd6d-103">배포 및 관련 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="3dd6d-104">구문</span><span class="sxs-lookup"><span data-stu-id="3dd6d-104">SYNTAX</span></span>

### <span data-ttu-id="3dd6d-105">RemoveByDeploymentName(기본값)</span><span class="sxs-lookup"><span data-stu-id="3dd6d-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dd6d-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="3dd6d-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dd6d-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="3dd6d-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dd6d-108">설명</span><span class="sxs-lookup"><span data-stu-id="3dd6d-108">DESCRIPTION</span></span>
<span data-ttu-id="3dd6d-109">**Remove-AzDeployment** cmdlet은 구독 범위 및 연결된 작업에서 Azure 배포를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="3dd6d-110">예제</span><span class="sxs-lookup"><span data-stu-id="3dd6d-110">EXAMPLES</span></span>

### <span data-ttu-id="3dd6d-111">예제 1: 지정한 이름의 배포 제거</span><span class="sxs-lookup"><span data-stu-id="3dd6d-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="3dd6d-112">이 명령은 현재 구독 범위에서 배포 "RolesDeployment"를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="3dd6d-113">예제 2: 배포를 사용하여 제거</span><span class="sxs-lookup"><span data-stu-id="3dd6d-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="3dd6d-114">이 명령은 현재 구독 범위에서 배포 "RolesDeployment"를 얻게 하여 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="3dd6d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dd6d-115">PARAMETERS</span></span>

### <span data-ttu-id="3dd6d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3dd6d-116">-AsJob</span></span>
<span data-ttu-id="3dd6d-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3dd6d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3dd6d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd6d-118">-DefaultProfile</span></span>
<span data-ttu-id="3dd6d-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dd6d-120">-Id</span><span class="sxs-lookup"><span data-stu-id="3dd6d-120">-Id</span></span>
<span data-ttu-id="3dd6d-121">배포의 정식 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="3dd6d-122">예: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="3dd6d-122">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dd6d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3dd6d-123">-InputObject</span></span>
<span data-ttu-id="3dd6d-124">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd6d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="3dd6d-125">-Name</span></span>
<span data-ttu-id="3dd6d-126">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dd6d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3dd6d-127">-PassThru</span></span>
<span data-ttu-id="3dd6d-128">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="3dd6d-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3dd6d-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="3dd6d-129">-Pre</span></span>
<span data-ttu-id="3dd6d-130">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3dd6d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dd6d-131">-Confirm</span></span>
<span data-ttu-id="3dd6d-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dd6d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dd6d-133">-WhatIf</span></span>
<span data-ttu-id="3dd6d-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3dd6d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dd6d-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dd6d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd6d-136">CommonParameters</span></span>
<span data-ttu-id="3dd6d-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd6d-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd6d-139">입력</span><span class="sxs-lookup"><span data-stu-id="3dd6d-139">INPUTS</span></span>

### <span data-ttu-id="3dd6d-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="3dd6d-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="3dd6d-141">출력</span><span class="sxs-lookup"><span data-stu-id="3dd6d-141">OUTPUTS</span></span>

### <span data-ttu-id="3dd6d-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3dd6d-142">System.Boolean</span></span>

## <span data-ttu-id="3dd6d-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3dd6d-143">NOTES</span></span>

## <span data-ttu-id="3dd6d-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3dd6d-144">RELATED LINKS</span></span>
