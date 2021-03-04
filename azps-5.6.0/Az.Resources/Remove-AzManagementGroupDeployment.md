---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: 06f3dec483c2c8b5e1730cb1046f927d6d38a7f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967691"
---
# <span data-ttu-id="b68df-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b68df-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="b68df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b68df-102">SYNOPSIS</span></span>
<span data-ttu-id="b68df-103">관리 그룹 및 관련 작업에서 배포를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b68df-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="b68df-104">구문</span><span class="sxs-lookup"><span data-stu-id="b68df-104">SYNTAX</span></span>

### <span data-ttu-id="b68df-105">RemoveByDeploymentName(기본값)</span><span class="sxs-lookup"><span data-stu-id="b68df-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b68df-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="b68df-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b68df-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="b68df-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b68df-108">설명</span><span class="sxs-lookup"><span data-stu-id="b68df-108">DESCRIPTION</span></span>
<span data-ttu-id="b68df-109">**Remove-AzManagementGroupDeployment** cmdlet은 관리 그룹 및 연결된 작업에서 Azure 배포를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b68df-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="b68df-110">예제</span><span class="sxs-lookup"><span data-stu-id="b68df-110">EXAMPLES</span></span>

### <span data-ttu-id="b68df-111">예제 1: 지정한 이름으로 배포 제거</span><span class="sxs-lookup"><span data-stu-id="b68df-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="b68df-112">이 명령은 관리 그룹 "myMG"에서 배포 "RolesDeployment"를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b68df-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="b68df-113">예제 2: 배포를 시작하고 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b68df-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="b68df-114">이 명령은 관리 그룹 "myMG"에서 "RolesDeployment"를 배포하고 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b68df-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="b68df-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b68df-115">PARAMETERS</span></span>

### <span data-ttu-id="b68df-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b68df-116">-AsJob</span></span>
<span data-ttu-id="b68df-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b68df-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b68df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b68df-118">-DefaultProfile</span></span>
<span data-ttu-id="b68df-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b68df-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b68df-120">-Id</span><span class="sxs-lookup"><span data-stu-id="b68df-120">-Id</span></span>
<span data-ttu-id="b68df-121">배포의 완전히 자격을 갖춘 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b68df-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="b68df-122">예제: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="b68df-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="b68df-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b68df-123">-InputObject</span></span>
<span data-ttu-id="b68df-124">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b68df-124">The deployment object.</span></span>

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

### <span data-ttu-id="b68df-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b68df-125">-ManagementGroupId</span></span>
<span data-ttu-id="b68df-126">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b68df-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b68df-127">-Name</span><span class="sxs-lookup"><span data-stu-id="b68df-127">-Name</span></span>
<span data-ttu-id="b68df-128">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b68df-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b68df-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b68df-129">-PassThru</span></span>
<span data-ttu-id="b68df-130">{{ Fill PassThru 설명 }}</span><span class="sxs-lookup"><span data-stu-id="b68df-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b68df-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="b68df-131">-Pre</span></span>
<span data-ttu-id="b68df-132">설정하면 cmdlet이 사용할 버전을 자동으로 결정할 때 미리 릴리스 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b68df-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b68df-133">-확인</span><span class="sxs-lookup"><span data-stu-id="b68df-133">-Confirm</span></span>
<span data-ttu-id="b68df-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b68df-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b68df-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b68df-135">-WhatIf</span></span>
<span data-ttu-id="b68df-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b68df-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b68df-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b68df-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b68df-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b68df-138">CommonParameters</span></span>
<span data-ttu-id="b68df-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b68df-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b68df-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b68df-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b68df-141">입력</span><span class="sxs-lookup"><span data-stu-id="b68df-141">INPUTS</span></span>

### <span data-ttu-id="b68df-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDMicrosoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="b68df-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="b68df-143">출력</span><span class="sxs-lookup"><span data-stu-id="b68df-143">OUTPUTS</span></span>

### <span data-ttu-id="b68df-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b68df-144">System.Boolean</span></span>

## <span data-ttu-id="b68df-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b68df-145">NOTES</span></span>

## <span data-ttu-id="b68df-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b68df-146">RELATED LINKS</span></span>
