---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: fa9dc4f8234e9c6e709d59f3945b05eeceef4316
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186084"
---
# <span data-ttu-id="2f66d-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="2f66d-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="2f66d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f66d-102">SYNOPSIS</span></span>
<span data-ttu-id="2f66d-103">지정된 아티팩트 원본을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="2f66d-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="2f66d-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f66d-104">SYNTAX</span></span>

### <span data-ttu-id="2f66d-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="2f66d-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f66d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f66d-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f66d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2f66d-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f66d-108">설명</span><span class="sxs-lookup"><span data-stu-id="2f66d-108">DESCRIPTION</span></span>
<span data-ttu-id="2f66d-109">**Remove-AzDeploymentManagerArtifactSource** cmdlet은 아티팩트 원본을 삭제하고 이름 및 리소스 그룹 이름으로 아티팩트 원본을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f66d-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="2f66d-110">또는 ArtifactSource 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2f66d-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="2f66d-111">예제</span><span class="sxs-lookup"><span data-stu-id="2f66d-111">EXAMPLES</span></span>

### <span data-ttu-id="2f66d-112">예제 1: 아티팩트 원본 삭제</span><span class="sxs-lookup"><span data-stu-id="2f66d-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="2f66d-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="2f66d-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="2f66d-114">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource라는 아티팩트 원본을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="2f66d-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="2f66d-115">예제 2: 리소스 식별자를 사용하여 아티팩트 원본 삭제</span><span class="sxs-lookup"><span data-stu-id="2f66d-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="2f66d-116">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource라는 아티팩트 원본을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="2f66d-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="2f66d-117">예제 3: 개체를 사용하여 아티팩트 원본 삭제</span><span class="sxs-lookup"><span data-stu-id="2f66d-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="2f66d-118">이 명령은 이름과 ResourceGroup이 각각 이름 및 ResourceGroupName 속성과 일치하는 아티팩트 원본을 $artifactSourceObject 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="2f66d-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="2f66d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f66d-119">PARAMETERS</span></span>

### <span data-ttu-id="2f66d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f66d-120">-DefaultProfile</span></span>
<span data-ttu-id="2f66d-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f66d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f66d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f66d-122">-InputObject</span></span>
<span data-ttu-id="2f66d-123">제거할 아티팩트 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="2f66d-123">The artifact source to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f66d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2f66d-124">-Name</span></span>
<span data-ttu-id="2f66d-125">아티팩트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f66d-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="2f66d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f66d-126">-PassThru</span></span>
<span data-ttu-id="2f66d-127">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="2f66d-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2f66d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f66d-128">-ResourceGroupName</span></span>
<span data-ttu-id="2f66d-129">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="2f66d-129">The resource group.</span></span>

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

### <span data-ttu-id="2f66d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f66d-130">-ResourceId</span></span>
<span data-ttu-id="2f66d-131">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2f66d-131">The resource identifier.</span></span>

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

### <span data-ttu-id="2f66d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f66d-132">-Confirm</span></span>
<span data-ttu-id="2f66d-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f66d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f66d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f66d-134">-WhatIf</span></span>
<span data-ttu-id="2f66d-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2f66d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f66d-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f66d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f66d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f66d-137">CommonParameters</span></span>
<span data-ttu-id="2f66d-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f66d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f66d-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2f66d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f66d-140">입력</span><span class="sxs-lookup"><span data-stu-id="2f66d-140">INPUTS</span></span>

### <span data-ttu-id="2f66d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2f66d-141">System.String</span></span>

### <span data-ttu-id="2f66d-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="2f66d-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="2f66d-143">출력</span><span class="sxs-lookup"><span data-stu-id="2f66d-143">OUTPUTS</span></span>

### <span data-ttu-id="2f66d-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2f66d-144">System.Boolean</span></span>

## <span data-ttu-id="2f66d-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f66d-145">NOTES</span></span>

## <span data-ttu-id="2f66d-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f66d-146">RELATED LINKS</span></span>
