---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 5b330b2f20fb0611d4bfdea37756b4d62e3bbd69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196521"
---
# <span data-ttu-id="f016c-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f016c-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="f016c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f016c-102">SYNOPSIS</span></span>

<span data-ttu-id="f016c-103">아티팩트 원본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f016c-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="f016c-104">구문</span><span class="sxs-lookup"><span data-stu-id="f016c-104">SYNTAX</span></span>

### <span data-ttu-id="f016c-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="f016c-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f016c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f016c-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f016c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f016c-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f016c-108">설명</span><span class="sxs-lookup"><span data-stu-id="f016c-108">DESCRIPTION</span></span>
<span data-ttu-id="f016c-109">**Get-AzDeploymentManagerArtifactSource** cmdlet은 아티팩트 원본을 얻게 하여 해당 아티팩트 원본을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f016c-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="f016c-110">이름 및 리소스 그룹 이름으로 아티팩트 원본을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f016c-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="f016c-111">또는 ArtifactSource 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f016c-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="f016c-112">예제</span><span class="sxs-lookup"><span data-stu-id="f016c-112">EXAMPLES</span></span>

### <span data-ttu-id="f016c-113">예제 1: 아티팩트 원본을 얻게</span><span class="sxs-lookup"><span data-stu-id="f016c-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="f016c-114">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource라는 아티팩트 원본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f016c-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="f016c-115">예제 2: 리소스 식별자를 사용하여 아티팩트 원본을 얻다</span><span class="sxs-lookup"><span data-stu-id="f016c-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="f016c-116">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource라는 아티팩트 원본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f016c-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="f016c-117">예제 3: 개체에서 반환된 개체를 사용하여 아티팩트 원본을 New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f016c-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="f016c-118">이 명령은 이름과 ResourceGroup이 각각 이름 및 ResourceGroupName 속성과 일치하는 아티팩트 원본을 $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="f016c-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="f016c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f016c-119">PARAMETERS</span></span>

### <span data-ttu-id="f016c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f016c-120">-DefaultProfile</span></span>
<span data-ttu-id="f016c-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f016c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f016c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f016c-122">-InputObject</span></span>
<span data-ttu-id="f016c-123">아티팩트 원본 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f016c-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="f016c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f016c-124">-Name</span></span>
<span data-ttu-id="f016c-125">아티팩트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f016c-125">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f016c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f016c-126">-ResourceGroupName</span></span>
<span data-ttu-id="f016c-127">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="f016c-127">The resource group.</span></span>

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

### <span data-ttu-id="f016c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f016c-128">-ResourceId</span></span>
<span data-ttu-id="f016c-129">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f016c-129">The resource identifier.</span></span>

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

### <span data-ttu-id="f016c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f016c-130">CommonParameters</span></span>
<span data-ttu-id="f016c-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f016c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f016c-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f016c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f016c-133">입력</span><span class="sxs-lookup"><span data-stu-id="f016c-133">INPUTS</span></span>

### <span data-ttu-id="f016c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f016c-134">System.String</span></span>

### <span data-ttu-id="f016c-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f016c-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="f016c-136">출력</span><span class="sxs-lookup"><span data-stu-id="f016c-136">OUTPUTS</span></span>

### <span data-ttu-id="f016c-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="f016c-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="f016c-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f016c-138">NOTES</span></span>

## <span data-ttu-id="f016c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f016c-139">RELATED LINKS</span></span>
