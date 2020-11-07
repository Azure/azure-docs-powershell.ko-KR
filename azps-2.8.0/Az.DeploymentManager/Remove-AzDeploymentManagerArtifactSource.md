---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 1977fca9843c00d80d398a1dcd0bb967883cb5eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696652"
---
# <span data-ttu-id="9527c-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="9527c-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="9527c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9527c-102">SYNOPSIS</span></span>
<span data-ttu-id="9527c-103">지정 된 아티팩트 원본을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9527c-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="9527c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9527c-104">SYNTAX</span></span>

### <span data-ttu-id="9527c-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9527c-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9527c-106">리소스</span><span class="sxs-lookup"><span data-stu-id="9527c-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9527c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9527c-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9527c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9527c-108">DESCRIPTION</span></span>
<span data-ttu-id="9527c-109">**AzDeploymentManagerArtifactSource** cmdlet은 아티팩트 원본을 삭제 하 고 해당 이름 및 리소스 그룹 이름을 기준으로 아티팩트 원본을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9527c-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="9527c-110">또는 ArtifactSource 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9527c-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="9527c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9527c-111">EXAMPLES</span></span>

### <span data-ttu-id="9527c-112">예제 1: 아티팩트 원본 삭제</span><span class="sxs-lookup"><span data-stu-id="9527c-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="9527c-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="9527c-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="9527c-114">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource 이라는 아티팩트 원본을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9527c-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="9527c-115">예제 2: 리소스 식별자를 사용 하 여 아티팩트 원본 삭제</span><span class="sxs-lookup"><span data-stu-id="9527c-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="9527c-116">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource 이라는 아티팩트 원본을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9527c-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="9527c-117">예제 3: 개체를 사용 하 여 아티팩트 원본 삭제</span><span class="sxs-lookup"><span data-stu-id="9527c-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="9527c-118">이 명령은 name 및 ResourceGroup이 $artifactSourceObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 아티팩트 원본을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9527c-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="9527c-119">변수</span><span class="sxs-lookup"><span data-stu-id="9527c-119">PARAMETERS</span></span>

### <span data-ttu-id="9527c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9527c-120">-DefaultProfile</span></span>
<span data-ttu-id="9527c-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9527c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9527c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9527c-122">-InputObject</span></span>
<span data-ttu-id="9527c-123">제거할 아티팩트 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="9527c-123">The artifact source to be removed.</span></span>

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

### <span data-ttu-id="9527c-124">-이름</span><span class="sxs-lookup"><span data-stu-id="9527c-124">-Name</span></span>
<span data-ttu-id="9527c-125">아티팩트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9527c-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="9527c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9527c-126">-PassThru</span></span>
<span data-ttu-id="9527c-127">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="9527c-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9527c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9527c-128">-ResourceGroupName</span></span>
<span data-ttu-id="9527c-129">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="9527c-129">The resource group.</span></span>

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

### <span data-ttu-id="9527c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9527c-130">-ResourceId</span></span>
<span data-ttu-id="9527c-131">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9527c-131">The resource identifier.</span></span>

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

### <span data-ttu-id="9527c-132">-확인</span><span class="sxs-lookup"><span data-stu-id="9527c-132">-Confirm</span></span>
<span data-ttu-id="9527c-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9527c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9527c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9527c-134">-WhatIf</span></span>
<span data-ttu-id="9527c-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9527c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9527c-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9527c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9527c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9527c-137">CommonParameters</span></span>
<span data-ttu-id="9527c-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9527c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9527c-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9527c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9527c-140">입력</span><span class="sxs-lookup"><span data-stu-id="9527c-140">INPUTS</span></span>

### <span data-ttu-id="9527c-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9527c-141">System.String</span></span>

### <span data-ttu-id="9527c-142">Microsoft Azure.. i m a 관리자. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="9527c-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="9527c-143">출력</span><span class="sxs-lookup"><span data-stu-id="9527c-143">OUTPUTS</span></span>

### <span data-ttu-id="9527c-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9527c-144">System.Boolean</span></span>

## <span data-ttu-id="9527c-145">상속자</span><span class="sxs-lookup"><span data-stu-id="9527c-145">NOTES</span></span>

## <span data-ttu-id="9527c-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9527c-146">RELATED LINKS</span></span>
