---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTenantDeployment.md
ms.openlocfilehash: 2417e152b2672d70425e5425a29c1901bfa29313
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354806"
---
# <span data-ttu-id="a0010-101">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="a0010-101">Remove-AzTenantDeployment</span></span>

## <span data-ttu-id="a0010-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0010-102">SYNOPSIS</span></span>
<span data-ttu-id="a0010-103">테넌트 범위 및 모든 관련 작업에서 배포를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a0010-103">Removes a deployment at tenant scope and any associated operations</span></span>

## <span data-ttu-id="a0010-104">구문</span><span class="sxs-lookup"><span data-stu-id="a0010-104">SYNTAX</span></span>

### <span data-ttu-id="a0010-105">RemoveByDeploymentName(기본값)</span><span class="sxs-lookup"><span data-stu-id="a0010-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzTenantDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0010-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="a0010-106">RemoveByDeploymentId</span></span>
```
Remove-AzTenantDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0010-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="a0010-107">RemoveByInputObject</span></span>
```
Remove-AzTenantDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0010-108">설명</span><span class="sxs-lookup"><span data-stu-id="a0010-108">DESCRIPTION</span></span>
<span data-ttu-id="a0010-109">**Remove-AzTenantDeployment** cmdlet은 현재 테넌트 범위 및 연결된 작업에서 Azure 배포를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a0010-109">The **Remove-AzTenantDeployment** cmdlet removes an Azure deployment at the current tenant scope and any associated operations.</span></span>

## <span data-ttu-id="a0010-110">예제</span><span class="sxs-lookup"><span data-stu-id="a0010-110">EXAMPLES</span></span>

### <span data-ttu-id="a0010-111">예제 1: 지정한 이름의 배포 제거</span><span class="sxs-lookup"><span data-stu-id="a0010-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzTenantDeployment -Name "RolesDeployment"
```

<span data-ttu-id="a0010-112">이 명령은 현재 테넌트 범위에서 배포 "RolesDeployment"를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a0010-112">This command removes the deployment "RolesDeployment" at the current tenant scope.</span></span>

### <span data-ttu-id="a0010-113">예제 2: 배포를 사용하여 제거</span><span class="sxs-lookup"><span data-stu-id="a0010-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "RolesDeployment" | Remove-AzTenantDeployment
```

<span data-ttu-id="a0010-114">이 명령은 현재 테넌트 범위에서 배포 "RolesDeployment"를 구하고 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a0010-114">This command gets the deployment "RolesDeployment" at the current tenant scope and removes it.</span></span>

## <span data-ttu-id="a0010-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0010-115">PARAMETERS</span></span>

### <span data-ttu-id="a0010-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0010-116">-AsJob</span></span>
<span data-ttu-id="a0010-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a0010-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0010-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0010-118">-DefaultProfile</span></span>
<span data-ttu-id="a0010-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0010-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0010-120">-Id</span><span class="sxs-lookup"><span data-stu-id="a0010-120">-Id</span></span>
<span data-ttu-id="a0010-121">배포의 정식 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a0010-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="a0010-122">예: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="a0010-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="a0010-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0010-123">-InputObject</span></span>
<span data-ttu-id="a0010-124">배포 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a0010-124">The deployment object.</span></span>

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

### <span data-ttu-id="a0010-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a0010-125">-Name</span></span>
<span data-ttu-id="a0010-126">배포의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0010-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="a0010-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0010-127">-PassThru</span></span>
<span data-ttu-id="a0010-128">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="a0010-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a0010-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="a0010-129">-Pre</span></span>
<span data-ttu-id="a0010-130">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a0010-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a0010-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0010-131">-Confirm</span></span>
<span data-ttu-id="a0010-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0010-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0010-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0010-133">-WhatIf</span></span>
<span data-ttu-id="a0010-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a0010-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0010-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a0010-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0010-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0010-136">CommonParameters</span></span>
<span data-ttu-id="a0010-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a0010-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0010-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a0010-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0010-139">입력</span><span class="sxs-lookup"><span data-stu-id="a0010-139">INPUTS</span></span>

### <span data-ttu-id="a0010-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSD</span><span class="sxs-lookup"><span data-stu-id="a0010-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="a0010-141">출력</span><span class="sxs-lookup"><span data-stu-id="a0010-141">OUTPUTS</span></span>

### <span data-ttu-id="a0010-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a0010-142">System.Boolean</span></span>

## <span data-ttu-id="a0010-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a0010-143">NOTES</span></span>

## <span data-ttu-id="a0010-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0010-144">RELATED LINKS</span></span>
