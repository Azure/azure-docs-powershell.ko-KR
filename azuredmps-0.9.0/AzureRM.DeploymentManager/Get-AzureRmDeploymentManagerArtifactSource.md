---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: baf5059d3a952e90422f3e16d83634291aa87614
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701782"
---
# <span data-ttu-id="32c20-101">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="32c20-101">Get-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="32c20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32c20-102">SYNOPSIS</span></span>
<span data-ttu-id="32c20-103">아티팩트 소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32c20-103">Gets an artifact source.</span></span>

## <span data-ttu-id="32c20-104">구문과</span><span class="sxs-lookup"><span data-stu-id="32c20-104">SYNTAX</span></span>

### <span data-ttu-id="32c20-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="32c20-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32c20-106">리소스</span><span class="sxs-lookup"><span data-stu-id="32c20-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="32c20-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="32c20-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32c20-108">설명은</span><span class="sxs-lookup"><span data-stu-id="32c20-108">DESCRIPTION</span></span>
<span data-ttu-id="32c20-109">**Get-AzureRmDeploymentManagerArtifactSource** cmdlet은 아티팩트 원본을 가져오고 해당 아티팩트 소스를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="32c20-109">The **Get-AzureRmDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="32c20-110">아티팩트 원본에 이름 및 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32c20-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="32c20-111">또는 ArtifactSource 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32c20-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

<span data-ttu-id="32c20-112">이 개체를 로컬로 수정한 다음 Set-AzureRmDeploymentManagerArtifactSource cmdlet을 사용 하 여 아티팩트 원본에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32c20-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerArtifactSource cmdlet.</span></span>

## <span data-ttu-id="32c20-113">예제의</span><span class="sxs-lookup"><span data-stu-id="32c20-113">EXAMPLES</span></span>

### <span data-ttu-id="32c20-114">예제 1: 아티팩트 원본 가져오기</span><span class="sxs-lookup"><span data-stu-id="32c20-114">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="32c20-115">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource 이라는 아티팩트 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32c20-115">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="32c20-116">예제 2: 리소스 식별자를 사용 하 여 아티팩트 원본 가져오기</span><span class="sxs-lookup"><span data-stu-id="32c20-116">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="32c20-117">이 명령은 ContosoResourceGroup에서 ContosoArtifactSource 이라는 아티팩트 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32c20-117">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="32c20-118">예제 3: New-AzureRmDeploymentManagerArtifactSource에서 반환 된 개체를 사용 하 여 아티팩트 원본 가져오기</span><span class="sxs-lookup"><span data-stu-id="32c20-118">Example 3: Get an artifact source using an object returned by New-AzureRmDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="32c20-119">이 명령은 name 및 ResourceGroup이 $artifactSourceObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 아티팩트 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="32c20-119">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="32c20-120">변수</span><span class="sxs-lookup"><span data-stu-id="32c20-120">PARAMETERS</span></span>

### <span data-ttu-id="32c20-121">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="32c20-121">-ArtifactSource</span></span>
<span data-ttu-id="32c20-122">아티팩트 원본 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="32c20-122">Artifact Source object.</span></span>

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

### <span data-ttu-id="32c20-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32c20-123">-DefaultProfile</span></span>
<span data-ttu-id="32c20-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32c20-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32c20-125">-이름</span><span class="sxs-lookup"><span data-stu-id="32c20-125">-Name</span></span>
<span data-ttu-id="32c20-126">아티팩트 원본의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32c20-126">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32c20-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32c20-127">-ResourceGroupName</span></span>
<span data-ttu-id="32c20-128">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="32c20-128">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32c20-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32c20-129">-ResourceId</span></span>
<span data-ttu-id="32c20-130">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="32c20-130">The resource identifier.</span></span>

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

### <span data-ttu-id="32c20-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32c20-131">CommonParameters</span></span>
<span data-ttu-id="32c20-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32c20-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32c20-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32c20-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32c20-134">입력</span><span class="sxs-lookup"><span data-stu-id="32c20-134">INPUTS</span></span>

### <span data-ttu-id="32c20-135">않아야</span><span class="sxs-lookup"><span data-stu-id="32c20-135">None</span></span>

## <span data-ttu-id="32c20-136">출력</span><span class="sxs-lookup"><span data-stu-id="32c20-136">OUTPUTS</span></span>

### <span data-ttu-id="32c20-137">Microsoft Azure.. i m a 관리자. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="32c20-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="32c20-138">상속자</span><span class="sxs-lookup"><span data-stu-id="32c20-138">NOTES</span></span>

## <span data-ttu-id="32c20-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32c20-139">RELATED LINKS</span></span>

[<span data-ttu-id="32c20-140">새로운 AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="32c20-140">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="32c20-141">제거-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="32c20-141">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="32c20-142">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="32c20-142">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)