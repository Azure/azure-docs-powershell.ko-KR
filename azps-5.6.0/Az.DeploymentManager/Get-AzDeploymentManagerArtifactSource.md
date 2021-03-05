---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 819fb3427ae59291c6b6d78a9ce93ee4e519ee13
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966368"
---
# <span data-ttu-id="68c63-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="68c63-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="68c63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68c63-102">SYNOPSIS</span></span>

<span data-ttu-id="68c63-103">아티팩트 원본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68c63-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="68c63-104">구문</span><span class="sxs-lookup"><span data-stu-id="68c63-104">SYNTAX</span></span>

### <span data-ttu-id="68c63-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="68c63-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68c63-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="68c63-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68c63-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="68c63-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68c63-108">설명</span><span class="sxs-lookup"><span data-stu-id="68c63-108">DESCRIPTION</span></span>
<span data-ttu-id="68c63-109">**Get-AzDeploymentManagerArtifactSource** cmdlet은 아티팩트 원본을 얻게 하여 해당 아티팩트 원본을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="68c63-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="68c63-110">이름 및 리소스 그룹 이름으로 아티팩트 원본을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="68c63-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="68c63-111">또는 ArtifactSource 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68c63-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="68c63-112">예제</span><span class="sxs-lookup"><span data-stu-id="68c63-112">EXAMPLES</span></span>

### <span data-ttu-id="68c63-113">예제 1: 아티팩트 원본 얻기</span><span class="sxs-lookup"><span data-stu-id="68c63-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="68c63-114">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource라는 아티팩트 원본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68c63-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="68c63-115">예제 2: 리소스 식별자를 사용하여 아티팩트 원본을 얻다</span><span class="sxs-lookup"><span data-stu-id="68c63-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="68c63-116">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource라는 아티팩트 원본을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="68c63-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="68c63-117">예제 3: 개체가 반환한 개체를 사용하여 아티팩트 원본을 New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="68c63-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="68c63-118">이 명령은 이름 및 ResourceGroup이 각각 이름 및 ResourceGroupName 속성과 일치하는 아티팩트 원본을 $artifactSourceObject 합니다.</span><span class="sxs-lookup"><span data-stu-id="68c63-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="68c63-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="68c63-119">PARAMETERS</span></span>

### <span data-ttu-id="68c63-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68c63-120">-DefaultProfile</span></span>
<span data-ttu-id="68c63-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68c63-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68c63-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68c63-122">-InputObject</span></span>
<span data-ttu-id="68c63-123">아티팩트 원본 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="68c63-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="68c63-124">-Name</span><span class="sxs-lookup"><span data-stu-id="68c63-124">-Name</span></span>
<span data-ttu-id="68c63-125">아티팩트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68c63-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="68c63-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68c63-126">-ResourceGroupName</span></span>
<span data-ttu-id="68c63-127">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="68c63-127">The resource group.</span></span>

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

### <span data-ttu-id="68c63-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68c63-128">-ResourceId</span></span>
<span data-ttu-id="68c63-129">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="68c63-129">The resource identifier.</span></span>

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

### <span data-ttu-id="68c63-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68c63-130">CommonParameters</span></span>
<span data-ttu-id="68c63-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="68c63-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68c63-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68c63-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68c63-133">입력</span><span class="sxs-lookup"><span data-stu-id="68c63-133">INPUTS</span></span>

### <span data-ttu-id="68c63-134">System.String</span><span class="sxs-lookup"><span data-stu-id="68c63-134">System.String</span></span>

### <span data-ttu-id="68c63-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="68c63-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="68c63-136">출력</span><span class="sxs-lookup"><span data-stu-id="68c63-136">OUTPUTS</span></span>

### <span data-ttu-id="68c63-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="68c63-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="68c63-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="68c63-138">NOTES</span></span>

## <span data-ttu-id="68c63-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68c63-139">RELATED LINKS</span></span>
