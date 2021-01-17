---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: cf2f8f011803deb4649b8c7d1550c421c9e62017
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490299"
---
# <span data-ttu-id="1a17a-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="1a17a-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="1a17a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a17a-102">SYNOPSIS</span></span>
<span data-ttu-id="1a17a-103">관리 그룹 및 모든 관련 작업에서 배포를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1a17a-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="1a17a-104">구문</span><span class="sxs-lookup"><span data-stu-id="1a17a-104">SYNTAX</span></span>

### <span data-ttu-id="1a17a-105">RemoveByDeploymentName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1a17a-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a17a-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="1a17a-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a17a-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="1a17a-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a17a-108">설명</span><span class="sxs-lookup"><span data-stu-id="1a17a-108">DESCRIPTION</span></span>
<span data-ttu-id="1a17a-109">**Remove-AzManagementGroupDeployment** cmdlet은 관리 그룹 및 연결된 작업에서 Azure 배포를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1a17a-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="1a17a-110">예제</span><span class="sxs-lookup"><span data-stu-id="1a17a-110">EXAMPLES</span></span>

### <span data-ttu-id="1a17a-111">예제 1: 지정한 이름의 배포 제거</span><span class="sxs-lookup"><span data-stu-id="1a17a-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="1a17a-112">이 명령은 관리 그룹 "myMG"에서 "RolesDeployment" 배포를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1a17a-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="1a17a-113">예제 2: 배포를 사용하여 제거</span><span class="sxs-lookup"><span data-stu-id="1a17a-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="1a17a-114">이 명령은 관리 그룹 "myMG"에서 배포 "RolesDeployment"를 사용하여 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1a17a-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="1a17a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a17a-115">PARAMETERS</span></span>

### <span data-ttu-id="1a17a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a17a-116">-AsJob</span></span>
<span data-ttu-id="1a17a-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1a17a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a17a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a17a-118">-DefaultProfile</span></span>
<span data-ttu-id="1a17a-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a17a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a17a-120">-Id</span><span class="sxs-lookup"><span data-stu-id="1a17a-120">-Id</span></span>
<span data-ttu-id="1a17a-121">배포의 정식 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1a17a-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="1a17a-122">예: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="1a17a-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="1a17a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a17a-123">-InputObject</span></span>
<span data-ttu-id="1a17a-124">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1a17a-124">The deployment object.</span></span>

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

### <span data-ttu-id="1a17a-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="1a17a-125">-ManagementGroupId</span></span>
<span data-ttu-id="1a17a-126">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1a17a-126">The management group id.</span></span>

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

### <span data-ttu-id="1a17a-127">-Name</span><span class="sxs-lookup"><span data-stu-id="1a17a-127">-Name</span></span>
<span data-ttu-id="1a17a-128">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a17a-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="1a17a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a17a-129">-PassThru</span></span>
<span data-ttu-id="1a17a-130">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="1a17a-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="1a17a-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="1a17a-131">-Pre</span></span>
<span data-ttu-id="1a17a-132">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1a17a-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1a17a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a17a-133">-Confirm</span></span>
<span data-ttu-id="1a17a-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a17a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a17a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a17a-135">-WhatIf</span></span>
<span data-ttu-id="1a17a-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1a17a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a17a-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a17a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a17a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a17a-138">CommonParameters</span></span>
<span data-ttu-id="1a17a-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1a17a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a17a-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1a17a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a17a-141">입력</span><span class="sxs-lookup"><span data-stu-id="1a17a-141">INPUTS</span></span>

### <span data-ttu-id="1a17a-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="1a17a-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="1a17a-143">출력</span><span class="sxs-lookup"><span data-stu-id="1a17a-143">OUTPUTS</span></span>

### <span data-ttu-id="1a17a-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1a17a-144">System.Boolean</span></span>

## <span data-ttu-id="1a17a-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1a17a-145">NOTES</span></span>

## <span data-ttu-id="1a17a-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a17a-146">RELATED LINKS</span></span>
