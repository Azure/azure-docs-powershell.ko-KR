---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387451"
---
# <span data-ttu-id="fdf1d-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="fdf1d-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="fdf1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdf1d-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf1d-103">서비스 토폴로지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdf1d-103">Gets the service topology.</span></span>

## <span data-ttu-id="fdf1d-104">구문</span><span class="sxs-lookup"><span data-stu-id="fdf1d-104">SYNTAX</span></span>

### <span data-ttu-id="fdf1d-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="fdf1d-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdf1d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdf1d-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fdf1d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="fdf1d-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdf1d-108">설명</span><span class="sxs-lookup"><span data-stu-id="fdf1d-108">DESCRIPTION</span></span>
<span data-ttu-id="fdf1d-109">**Get-AzDeploymentManagerServiceTopology** cmdlet은 서비스 토폴로지가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdf1d-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="fdf1d-110">이 개체를 로컬로 수정한 다음, Set-AzDeploymentManagerServiceTopology cmdlet을 사용하여 토폴로지에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdf1d-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="fdf1d-111">서비스 토폴로지의 이름 및 리소스 그룹 이름으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf1d-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="fdf1d-112">또는 ServiceTopology 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdf1d-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="fdf1d-113">예제</span><span class="sxs-lookup"><span data-stu-id="fdf1d-113">EXAMPLES</span></span>

### <span data-ttu-id="fdf1d-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="fdf1d-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="fdf1d-115">이 명령은 ContosoResourceGroup에서 ContosoServiceTopology라는 서비스 토폴로지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdf1d-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="fdf1d-116">예제 2: 리소스 식별자를 사용하여 서비스 토폴로지 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fdf1d-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="fdf1d-117">이 명령은 ContosoResourceGroup에서 ContosoServiceTopology라는 서비스 토폴로지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdf1d-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="fdf1d-118">예제 3: 서비스 토폴로지 개체를 사용하여 서비스 토폴로지 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fdf1d-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="fdf1d-119">이 명령은 이름 및 ResourceGroup이 각각 이름 및 ResourceGroupName 속성과 일치하는 서비스 토폴로지 $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="fdf1d-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="fdf1d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fdf1d-120">PARAMETERS</span></span>

### <span data-ttu-id="fdf1d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf1d-121">-DefaultProfile</span></span>
<span data-ttu-id="fdf1d-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fdf1d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdf1d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdf1d-123">-InputObject</span></span>
<span data-ttu-id="fdf1d-124">서비스 토폴로지 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fdf1d-124">Service topology resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf1d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fdf1d-125">-Name</span></span>
<span data-ttu-id="fdf1d-126">서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fdf1d-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="fdf1d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdf1d-127">-ResourceGroupName</span></span>
<span data-ttu-id="fdf1d-128">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="fdf1d-128">The resource group.</span></span>

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

### <span data-ttu-id="fdf1d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdf1d-129">-ResourceId</span></span>
<span data-ttu-id="fdf1d-130">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fdf1d-130">The resource identifier.</span></span>

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

### <span data-ttu-id="fdf1d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf1d-131">CommonParameters</span></span>
<span data-ttu-id="fdf1d-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fdf1d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf1d-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fdf1d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf1d-134">입력</span><span class="sxs-lookup"><span data-stu-id="fdf1d-134">INPUTS</span></span>

### <span data-ttu-id="fdf1d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="fdf1d-135">System.String</span></span>

### <span data-ttu-id="fdf1d-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="fdf1d-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="fdf1d-137">출력</span><span class="sxs-lookup"><span data-stu-id="fdf1d-137">OUTPUTS</span></span>

### <span data-ttu-id="fdf1d-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="fdf1d-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="fdf1d-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fdf1d-139">NOTES</span></span>

## <span data-ttu-id="fdf1d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fdf1d-140">RELATED LINKS</span></span>
