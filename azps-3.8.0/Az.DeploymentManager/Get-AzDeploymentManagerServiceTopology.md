---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044394"
---
# <span data-ttu-id="cc982-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="cc982-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="cc982-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc982-102">SYNOPSIS</span></span>
<span data-ttu-id="cc982-103">서비스 토폴로지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc982-103">Gets the service topology.</span></span>

## <span data-ttu-id="cc982-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cc982-104">SYNTAX</span></span>

### <span data-ttu-id="cc982-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="cc982-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc982-106">리소스</span><span class="sxs-lookup"><span data-stu-id="cc982-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc982-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="cc982-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc982-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cc982-108">DESCRIPTION</span></span>
<span data-ttu-id="cc982-109">**Get-AzDeploymentManagerServiceTopology** cmdlet은 서비스 토폴로지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc982-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="cc982-110">이 개체를 로컬로 수정한 다음 Set-AzDeploymentManagerServiceTopology cmdlet을 사용 하 여 토폴로지에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc982-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="cc982-111">이름 및 리소스 그룹 이름을 기준으로 서비스 토폴로지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc982-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="cc982-112">또는 ServiceTopology 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc982-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="cc982-113">예제의</span><span class="sxs-lookup"><span data-stu-id="cc982-113">EXAMPLES</span></span>

### <span data-ttu-id="cc982-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="cc982-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="cc982-115">이 명령은 ContosoResourceGroup에 ContosoServiceTopology 이라는 서비스 토폴로지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc982-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="cc982-116">예제 2: 리소스 식별자를 사용 하 여 서비스 토폴로지 가져오기</span><span class="sxs-lookup"><span data-stu-id="cc982-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="cc982-117">이 명령은 ContosoResourceGroup에 ContosoServiceTopology 이라는 서비스 토폴로지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc982-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="cc982-118">예제 3: 서비스 토폴로지 개체를 사용 하 여 서비스 토폴로지 가져오기</span><span class="sxs-lookup"><span data-stu-id="cc982-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="cc982-119">이 명령은 name 및 ResourceGroup이 $serviceTopologyObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 서비스 토폴로지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="cc982-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="cc982-120">변수</span><span class="sxs-lookup"><span data-stu-id="cc982-120">PARAMETERS</span></span>

### <span data-ttu-id="cc982-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc982-121">-DefaultProfile</span></span>
<span data-ttu-id="cc982-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc982-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc982-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc982-123">-InputObject</span></span>
<span data-ttu-id="cc982-124">서비스 토폴로지 리소스 개체</span><span class="sxs-lookup"><span data-stu-id="cc982-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="cc982-125">-이름</span><span class="sxs-lookup"><span data-stu-id="cc982-125">-Name</span></span>
<span data-ttu-id="cc982-126">서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cc982-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="cc982-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc982-127">-ResourceGroupName</span></span>
<span data-ttu-id="cc982-128">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="cc982-128">The resource group.</span></span>

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

### <span data-ttu-id="cc982-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc982-129">-ResourceId</span></span>
<span data-ttu-id="cc982-130">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="cc982-130">The resource identifier.</span></span>

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

### <span data-ttu-id="cc982-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc982-131">CommonParameters</span></span>
<span data-ttu-id="cc982-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cc982-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc982-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cc982-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc982-134">입력</span><span class="sxs-lookup"><span data-stu-id="cc982-134">INPUTS</span></span>

### <span data-ttu-id="cc982-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cc982-135">System.String</span></span>

### <span data-ttu-id="cc982-136">PSServiceTopologyResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="cc982-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="cc982-137">출력</span><span class="sxs-lookup"><span data-stu-id="cc982-137">OUTPUTS</span></span>

### <span data-ttu-id="cc982-138">PSServiceTopologyResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="cc982-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="cc982-139">상속자</span><span class="sxs-lookup"><span data-stu-id="cc982-139">NOTES</span></span>

## <span data-ttu-id="cc982-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc982-140">RELATED LINKS</span></span>
