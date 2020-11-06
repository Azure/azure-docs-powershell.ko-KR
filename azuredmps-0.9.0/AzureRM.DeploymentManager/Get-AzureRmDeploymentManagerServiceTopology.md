---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: f5e0b1e0b2e85eb3c17a53b0108e853535712db1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524096"
---
# <span data-ttu-id="3bbff-101">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="3bbff-101">Get-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="3bbff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bbff-102">SYNOPSIS</span></span>
<span data-ttu-id="3bbff-103">서비스 토폴로지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3bbff-103">Gets a service topology.</span></span>

## <span data-ttu-id="3bbff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3bbff-104">SYNTAX</span></span>

### <span data-ttu-id="3bbff-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3bbff-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bbff-106">리소스</span><span class="sxs-lookup"><span data-stu-id="3bbff-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bbff-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="3bbff-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bbff-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3bbff-108">DESCRIPTION</span></span>
<span data-ttu-id="3bbff-109">**Get-AzureRmDeploymentManagerServiceTopology** cmdlet은 서비스 토폴로지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3bbff-109">The **Get-AzureRmDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="3bbff-110">이 개체를 로컬로 수정한 다음 Set-AzureRmDeploymentManagerServiceTopology cmdlet을 사용 하 여 토폴로지에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3bbff-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzureRmDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="3bbff-111">이름 및 리소스 그룹 이름을 기준으로 서비스 토폴로지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bbff-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="3bbff-112">또는 ServiceTopology 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3bbff-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="3bbff-113">예제의</span><span class="sxs-lookup"><span data-stu-id="3bbff-113">EXAMPLES</span></span>

### <span data-ttu-id="3bbff-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="3bbff-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="3bbff-115">이 명령은 ContosoResourceGroup에 ContosoServiceTopology 이라는 서비스 토폴로지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3bbff-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="3bbff-116">예제 2: 리소스 식별자를 사용 하 여 서비스 토폴로지 가져오기</span><span class="sxs-lookup"><span data-stu-id="3bbff-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="3bbff-117">이 명령은 ContosoResourceGroup에 ContosoServiceTopology 이라는 서비스 토폴로지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3bbff-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="3bbff-118">예제 3: 서비스 토폴로지 개체를 사용 하 여 서비스 토폴로지 가져오기</span><span class="sxs-lookup"><span data-stu-id="3bbff-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="3bbff-119">이 명령은 name 및 ResourceGroup이 $serviceTopologyObject의 Name 및 ResourceGroupName 속성과 각각 일치 하는 서비스 토폴로지를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3bbff-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="3bbff-120">변수</span><span class="sxs-lookup"><span data-stu-id="3bbff-120">PARAMETERS</span></span>

### <span data-ttu-id="3bbff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bbff-121">-DefaultProfile</span></span>
<span data-ttu-id="3bbff-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3bbff-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bbff-123">-이름</span><span class="sxs-lookup"><span data-stu-id="3bbff-123">-Name</span></span>
<span data-ttu-id="3bbff-124">서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3bbff-124">The name of the service topology.</span></span>

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

### <span data-ttu-id="3bbff-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bbff-125">-ResourceGroupName</span></span>
<span data-ttu-id="3bbff-126">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="3bbff-126">The resource group.</span></span>

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

### <span data-ttu-id="3bbff-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bbff-127">-ResourceId</span></span>
<span data-ttu-id="3bbff-128">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3bbff-128">The resource identifier.</span></span>

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

### <span data-ttu-id="3bbff-129">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="3bbff-129">-ServiceTopology</span></span>
<span data-ttu-id="3bbff-130">서비스 토폴로지 리소스 개체</span><span class="sxs-lookup"><span data-stu-id="3bbff-130">Service topology resource object.</span></span>

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

### <span data-ttu-id="3bbff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bbff-131">CommonParameters</span></span>
<span data-ttu-id="3bbff-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bbff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bbff-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bbff-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bbff-134">입력</span><span class="sxs-lookup"><span data-stu-id="3bbff-134">INPUTS</span></span>

### <span data-ttu-id="3bbff-135">않아야</span><span class="sxs-lookup"><span data-stu-id="3bbff-135">None</span></span>

## <span data-ttu-id="3bbff-136">출력</span><span class="sxs-lookup"><span data-stu-id="3bbff-136">OUTPUTS</span></span>

### <span data-ttu-id="3bbff-137">PSServiceTopologyResource-. m i 매니저.</span><span class="sxs-lookup"><span data-stu-id="3bbff-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="3bbff-138">상속자</span><span class="sxs-lookup"><span data-stu-id="3bbff-138">NOTES</span></span>

## <span data-ttu-id="3bbff-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3bbff-139">RELATED LINKS</span></span>

[<span data-ttu-id="3bbff-140">새로운 AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="3bbff-140">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="3bbff-141">제거-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="3bbff-141">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="3bbff-142">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="3bbff-142">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)