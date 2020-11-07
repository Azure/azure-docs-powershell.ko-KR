---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 54cccbedc45977505b10526d4806b64c8118380e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701011"
---
# <span data-ttu-id="b89a1-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b89a1-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="b89a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b89a1-102">SYNOPSIS</span></span>

<span data-ttu-id="b89a1-103">아티팩트 소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b89a1-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="b89a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b89a1-104">SYNTAX</span></span>

### <span data-ttu-id="b89a1-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b89a1-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b89a1-106">리소스</span><span class="sxs-lookup"><span data-stu-id="b89a1-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b89a1-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b89a1-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b89a1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b89a1-108">DESCRIPTION</span></span>
<span data-ttu-id="b89a1-109">**Get-AzDeploymentManagerArtifactSource** cmdlet은 아티팩트 원본을 가져오고 해당 아티팩트 소스를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b89a1-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="b89a1-110">아티팩트 원본에 이름 및 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b89a1-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="b89a1-111">또는 ArtifactSource 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b89a1-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="b89a1-112">예제의</span><span class="sxs-lookup"><span data-stu-id="b89a1-112">EXAMPLES</span></span>

### <span data-ttu-id="b89a1-113">예제 1: 아티팩트 원본 가져오기</span><span class="sxs-lookup"><span data-stu-id="b89a1-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="b89a1-114">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource 이라는 아티팩트 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b89a1-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b89a1-115">예제 2: 리소스 식별자를 사용 하 여 아티팩트 원본 가져오기</span><span class="sxs-lookup"><span data-stu-id="b89a1-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="b89a1-116">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource 이라는 아티팩트 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b89a1-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b89a1-117">예제 3: New-AzDeploymentManagerArtifactSource에서 반환 된 개체를 사용 하 여 아티팩트 원본 가져오기</span><span class="sxs-lookup"><span data-stu-id="b89a1-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="b89a1-118">이 명령은 name 및 ResourceGroup이 $artifactSourceObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 아티팩트 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b89a1-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="b89a1-119">변수</span><span class="sxs-lookup"><span data-stu-id="b89a1-119">PARAMETERS</span></span>

### <span data-ttu-id="b89a1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b89a1-120">-DefaultProfile</span></span>
<span data-ttu-id="b89a1-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b89a1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b89a1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b89a1-122">-InputObject</span></span>
<span data-ttu-id="b89a1-123">아티팩트 원본 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b89a1-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="b89a1-124">-이름</span><span class="sxs-lookup"><span data-stu-id="b89a1-124">-Name</span></span>
<span data-ttu-id="b89a1-125">아티팩트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b89a1-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="b89a1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b89a1-126">-ResourceGroupName</span></span>
<span data-ttu-id="b89a1-127">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="b89a1-127">The resource group.</span></span>

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

### <span data-ttu-id="b89a1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b89a1-128">-ResourceId</span></span>
<span data-ttu-id="b89a1-129">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b89a1-129">The resource identifier.</span></span>

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

### <span data-ttu-id="b89a1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b89a1-130">CommonParameters</span></span>
<span data-ttu-id="b89a1-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b89a1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b89a1-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b89a1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b89a1-133">입력</span><span class="sxs-lookup"><span data-stu-id="b89a1-133">INPUTS</span></span>

### <span data-ttu-id="b89a1-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b89a1-134">System.String</span></span>

### <span data-ttu-id="b89a1-135">Microsoft Azure.. i m a 관리자. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b89a1-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="b89a1-136">출력</span><span class="sxs-lookup"><span data-stu-id="b89a1-136">OUTPUTS</span></span>

### <span data-ttu-id="b89a1-137">Microsoft Azure.. i m a 관리자. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b89a1-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="b89a1-138">상속자</span><span class="sxs-lookup"><span data-stu-id="b89a1-138">NOTES</span></span>

## <span data-ttu-id="b89a1-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b89a1-139">RELATED LINKS</span></span>
