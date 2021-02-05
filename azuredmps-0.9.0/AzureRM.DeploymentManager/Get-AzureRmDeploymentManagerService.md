---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4a91c2f8fdda1d2cda7c75f0cf7cfab165701f3d
ms.sourcegitcommit: e57be0da5162efeb0a01f396e2343dd137920063
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2021
ms.locfileid: "99572108"
---
# <span data-ttu-id="b66f0-101">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="b66f0-101">Get-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="b66f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b66f0-102">SYNOPSIS</span></span>
<span data-ttu-id="b66f0-103">서비스 토폴로지에서 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-103">Gets a service in a service topology.</span></span>

## <span data-ttu-id="b66f0-104">구문</span><span class="sxs-lookup"><span data-stu-id="b66f0-104">SYNTAX</span></span>

### <span data-ttu-id="b66f0-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="b66f0-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b66f0-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="b66f0-106">ByServiceTopologyObject</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b66f0-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="b66f0-107">ByServiceTopologyResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b66f0-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b66f0-108">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b66f0-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="b66f0-109">InputObject</span></span>
```
Get-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b66f0-110">설명</span><span class="sxs-lookup"><span data-stu-id="b66f0-110">DESCRIPTION</span></span>
<span data-ttu-id="b66f0-111">**Get-AzureRmDeploymentManagerService** cmdlet은 서비스 토폴로지에서 서비스를 반환하고 해당 서비스를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-111">The **Get-AzureRmDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="b66f0-112">해당 이름, 있는 서비스 토폴로지 및 리소스 그룹 이름으로 서비스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="b66f0-113">또는 서비스 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="b66f0-114">이 개체를 로컬로 수정한 다음, Set-AzureRmDeploymentManagerService cmdlet을 사용하여 서비스에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="b66f0-115">예제</span><span class="sxs-lookup"><span data-stu-id="b66f0-115">EXAMPLES</span></span>

### <span data-ttu-id="b66f0-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="b66f0-116">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="b66f0-117">이 명령은 ContosoResourceGroup의 ContosoServiceTopology라는 서비스 토폴로지에서 ContosoService1이라는 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="b66f0-118">예제 2: 리소스 식별자를 사용하여 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="b66f0-119">이 명령은 ContosoResourceGroup의 ContosoServiceTopology라는 서비스 토폴로지에서 ContosoService1이라는 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="b66f0-120">예제 3: 서비스 개체를 사용하여 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="b66f0-121">이 명령은 이름, 서비스 토폴로지 이름 및 ResourceGroup이 각각 이름, ServiceTopologyName 및 ResourceGroupName 속성과 일치하는 서비스를 $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="b66f0-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="b66f0-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b66f0-122">PARAMETERS</span></span>

### <span data-ttu-id="b66f0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b66f0-123">-DefaultProfile</span></span>
<span data-ttu-id="b66f0-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b66f0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b66f0-125">-Name</span></span>
<span data-ttu-id="b66f0-126">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-126">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b66f0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b66f0-127">-ResourceGroupName</span></span>
<span data-ttu-id="b66f0-128">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-128">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b66f0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b66f0-129">-ResourceId</span></span>
<span data-ttu-id="b66f0-130">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-130">The resource identifier.</span></span>

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

### <span data-ttu-id="b66f0-131">-Service</span><span class="sxs-lookup"><span data-stu-id="b66f0-131">-Service</span></span>
<span data-ttu-id="b66f0-132">서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-132">Service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b66f0-133">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="b66f0-133">-ServiceTopology</span></span>
<span data-ttu-id="b66f0-134">서비스를 만들어야 하는 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-134">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b66f0-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="b66f0-135">-ServiceTopologyName</span></span>
<span data-ttu-id="b66f0-136">서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="b66f0-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="b66f0-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="b66f0-138">서비스를 만들어야 하는 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-138">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b66f0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b66f0-139">CommonParameters</span></span>
<span data-ttu-id="b66f0-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b66f0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b66f0-141">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b66f0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b66f0-142">입력</span><span class="sxs-lookup"><span data-stu-id="b66f0-142">INPUTS</span></span>

### <span data-ttu-id="b66f0-143">없음</span><span class="sxs-lookup"><span data-stu-id="b66f0-143">None</span></span>

## <span data-ttu-id="b66f0-144">출력</span><span class="sxs-lookup"><span data-stu-id="b66f0-144">OUTPUTS</span></span>

### <span data-ttu-id="b66f0-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="b66f0-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="b66f0-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b66f0-146">NOTES</span></span>

## <span data-ttu-id="b66f0-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b66f0-147">RELATED LINKS</span></span>

[<span data-ttu-id="b66f0-148">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="b66f0-148">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="b66f0-149">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="b66f0-149">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="b66f0-150">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="b66f0-150">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)
