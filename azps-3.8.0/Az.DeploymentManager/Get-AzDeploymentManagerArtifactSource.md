---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 5b330b2f20fb0611d4bfdea37756b4d62e3bbd69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044406"
---
# <span data-ttu-id="aa28b-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="aa28b-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="aa28b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa28b-102">SYNOPSIS</span></span>

<span data-ttu-id="aa28b-103">아티팩트 소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aa28b-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="aa28b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aa28b-104">SYNTAX</span></span>

### <span data-ttu-id="aa28b-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="aa28b-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa28b-106">리소스</span><span class="sxs-lookup"><span data-stu-id="aa28b-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="aa28b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="aa28b-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa28b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="aa28b-108">DESCRIPTION</span></span>
<span data-ttu-id="aa28b-109">**Get-AzDeploymentManagerArtifactSource** cmdlet은 아티팩트 원본을 가져오고 해당 아티팩트 소스를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa28b-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="aa28b-110">아티팩트 원본에 이름 및 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa28b-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="aa28b-111">또는 ArtifactSource 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa28b-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="aa28b-112">예제의</span><span class="sxs-lookup"><span data-stu-id="aa28b-112">EXAMPLES</span></span>

### <span data-ttu-id="aa28b-113">예제 1: 아티팩트 원본 가져오기</span><span class="sxs-lookup"><span data-stu-id="aa28b-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="aa28b-114">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource 이라는 아티팩트 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aa28b-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="aa28b-115">예제 2: 리소스 식별자를 사용 하 여 아티팩트 원본 가져오기</span><span class="sxs-lookup"><span data-stu-id="aa28b-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="aa28b-116">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource 이라는 아티팩트 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aa28b-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="aa28b-117">예제 3: New-AzDeploymentManagerArtifactSource에서 반환 된 개체를 사용 하 여 아티팩트 원본 가져오기</span><span class="sxs-lookup"><span data-stu-id="aa28b-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="aa28b-118">이 명령은 name 및 ResourceGroup이 $artifactSourceObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 아티팩트 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="aa28b-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="aa28b-119">변수</span><span class="sxs-lookup"><span data-stu-id="aa28b-119">PARAMETERS</span></span>

### <span data-ttu-id="aa28b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa28b-120">-DefaultProfile</span></span>
<span data-ttu-id="aa28b-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aa28b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa28b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa28b-122">-InputObject</span></span>
<span data-ttu-id="aa28b-123">아티팩트 원본 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="aa28b-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="aa28b-124">-이름</span><span class="sxs-lookup"><span data-stu-id="aa28b-124">-Name</span></span>
<span data-ttu-id="aa28b-125">아티팩트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aa28b-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="aa28b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa28b-126">-ResourceGroupName</span></span>
<span data-ttu-id="aa28b-127">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="aa28b-127">The resource group.</span></span>

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

### <span data-ttu-id="aa28b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa28b-128">-ResourceId</span></span>
<span data-ttu-id="aa28b-129">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="aa28b-129">The resource identifier.</span></span>

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

### <span data-ttu-id="aa28b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa28b-130">CommonParameters</span></span>
<span data-ttu-id="aa28b-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa28b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa28b-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aa28b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa28b-133">입력</span><span class="sxs-lookup"><span data-stu-id="aa28b-133">INPUTS</span></span>

### <span data-ttu-id="aa28b-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aa28b-134">System.String</span></span>

### <span data-ttu-id="aa28b-135">Microsoft Azure.. i m a 관리자. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="aa28b-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="aa28b-136">출력</span><span class="sxs-lookup"><span data-stu-id="aa28b-136">OUTPUTS</span></span>

### <span data-ttu-id="aa28b-137">Microsoft Azure.. i m a 관리자. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="aa28b-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="aa28b-138">상속자</span><span class="sxs-lookup"><span data-stu-id="aa28b-138">NOTES</span></span>

## <span data-ttu-id="aa28b-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa28b-139">RELATED LINKS</span></span>
