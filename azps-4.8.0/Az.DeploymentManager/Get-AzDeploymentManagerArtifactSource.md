---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 5b330b2f20fb0611d4bfdea37756b4d62e3bbd69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048332"
---
# <span data-ttu-id="77c1d-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="77c1d-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="77c1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77c1d-102">SYNOPSIS</span></span>

<span data-ttu-id="77c1d-103">아티팩트 소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77c1d-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="77c1d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="77c1d-104">SYNTAX</span></span>

### <span data-ttu-id="77c1d-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="77c1d-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77c1d-106">리소스</span><span class="sxs-lookup"><span data-stu-id="77c1d-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77c1d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="77c1d-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77c1d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="77c1d-108">DESCRIPTION</span></span>
<span data-ttu-id="77c1d-109">**Get-AzDeploymentManagerArtifactSource** cmdlet은 아티팩트 원본을 가져오고 해당 아티팩트 소스를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="77c1d-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="77c1d-110">아티팩트 원본에 이름 및 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="77c1d-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="77c1d-111">또는 ArtifactSource 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="77c1d-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="77c1d-112">예제의</span><span class="sxs-lookup"><span data-stu-id="77c1d-112">EXAMPLES</span></span>

### <span data-ttu-id="77c1d-113">예제 1: 아티팩트 원본 가져오기</span><span class="sxs-lookup"><span data-stu-id="77c1d-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="77c1d-114">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource 이라는 아티팩트 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77c1d-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="77c1d-115">예제 2: 리소스 식별자를 사용 하 여 아티팩트 원본 가져오기</span><span class="sxs-lookup"><span data-stu-id="77c1d-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="77c1d-116">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource 이라는 아티팩트 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77c1d-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="77c1d-117">예제 3: New-AzDeploymentManagerArtifactSource에서 반환 된 개체를 사용 하 여 아티팩트 원본 가져오기</span><span class="sxs-lookup"><span data-stu-id="77c1d-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="77c1d-118">이 명령은 name 및 ResourceGroup이 $artifactSourceObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 아티팩트 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="77c1d-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="77c1d-119">변수</span><span class="sxs-lookup"><span data-stu-id="77c1d-119">PARAMETERS</span></span>

### <span data-ttu-id="77c1d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77c1d-120">-DefaultProfile</span></span>
<span data-ttu-id="77c1d-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77c1d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77c1d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77c1d-122">-InputObject</span></span>
<span data-ttu-id="77c1d-123">아티팩트 원본 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="77c1d-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="77c1d-124">-이름</span><span class="sxs-lookup"><span data-stu-id="77c1d-124">-Name</span></span>
<span data-ttu-id="77c1d-125">아티팩트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77c1d-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="77c1d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77c1d-126">-ResourceGroupName</span></span>
<span data-ttu-id="77c1d-127">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="77c1d-127">The resource group.</span></span>

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

### <span data-ttu-id="77c1d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77c1d-128">-ResourceId</span></span>
<span data-ttu-id="77c1d-129">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="77c1d-129">The resource identifier.</span></span>

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

### <span data-ttu-id="77c1d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77c1d-130">CommonParameters</span></span>
<span data-ttu-id="77c1d-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77c1d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77c1d-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="77c1d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77c1d-133">입력</span><span class="sxs-lookup"><span data-stu-id="77c1d-133">INPUTS</span></span>

### <span data-ttu-id="77c1d-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="77c1d-134">System.String</span></span>

### <span data-ttu-id="77c1d-135">Microsoft Azure.. i m a 관리자. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="77c1d-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="77c1d-136">출력</span><span class="sxs-lookup"><span data-stu-id="77c1d-136">OUTPUTS</span></span>

### <span data-ttu-id="77c1d-137">Microsoft Azure.. i m a 관리자. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="77c1d-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="77c1d-138">상속자</span><span class="sxs-lookup"><span data-stu-id="77c1d-138">NOTES</span></span>

## <span data-ttu-id="77c1d-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77c1d-139">RELATED LINKS</span></span>
