---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 2910afe209a83e07e65cc04b9ffa371fe4ed72d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966352"
---
# <span data-ttu-id="2a484-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="2a484-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="2a484-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a484-102">SYNOPSIS</span></span>
<span data-ttu-id="2a484-103">서비스 단위를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-103">Gets the service unit.</span></span>

## <span data-ttu-id="2a484-104">구문</span><span class="sxs-lookup"><span data-stu-id="2a484-104">SYNTAX</span></span>

### <span data-ttu-id="2a484-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="2a484-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a484-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="2a484-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a484-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="2a484-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a484-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="2a484-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a484-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="2a484-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a484-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a484-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a484-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="2a484-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a484-112">설명</span><span class="sxs-lookup"><span data-stu-id="2a484-112">DESCRIPTION</span></span>
<span data-ttu-id="2a484-113">**Get-AzDeploymentManagerServiceUnit** cmdlet은 서비스 단위를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="2a484-114">서비스 단위의 이름, 정의된 서비스, 서비스 토폴로지 이름 및 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="2a484-115">또는 ServiceUnit 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="2a484-116">이 개체를 로컬로 수정한 다음, cmdlet을 사용하여 서비스 단위에 Set-AzDeploymentManagerServiceUnit 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="2a484-117">예제</span><span class="sxs-lookup"><span data-stu-id="2a484-117">EXAMPLES</span></span>

### <span data-ttu-id="2a484-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="2a484-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="2a484-119">이 명령은 ContosoResourceGroup의 ContosoServiceTopology라는 서비스 토폴로지에서 ContosoService1 서비스 아래에 ContosoService1Storage라는 서비스 단위를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2a484-120">예제 2: 리소스 식별자를 사용하여 서비스 단위를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="2a484-121">이 명령은 ContosoResourceGroup의 ContosoServiceTopology라는 서비스 토폴로지에서 ContosoService1 서비스 아래에 ContosoService1Storage라는 서비스 단위를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2a484-122">예제 3: 서비스 단위 개체를 사용하여 서비스 단위를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="2a484-123">이 명령은 이름, 서비스 이름, 서비스 토폴로지 이름 및 ResourceGroup이 각각 서비스의 이름, ServiceName, ServiceTopologyName 및 ResourceGroupName 속성과 일치하는 $serviceUnitObject 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="2a484-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2a484-124">PARAMETERS</span></span>

### <span data-ttu-id="2a484-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a484-125">-DefaultProfile</span></span>
<span data-ttu-id="2a484-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a484-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a484-127">-InputObject</span></span>
<span data-ttu-id="2a484-128">서비스 단위 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-128">Service unit resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a484-129">-Name</span><span class="sxs-lookup"><span data-stu-id="2a484-129">-Name</span></span>
<span data-ttu-id="2a484-130">서비스 단위의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-130">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a484-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a484-131">-ResourceGroupName</span></span>
<span data-ttu-id="2a484-132">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-132">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a484-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a484-133">-ResourceId</span></span>
<span data-ttu-id="2a484-134">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-134">The resource identifier.</span></span>

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

### <span data-ttu-id="2a484-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2a484-135">-ServiceName</span></span>
<span data-ttu-id="2a484-136">서비스 단위의 일부인 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-136">The name of the service the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a484-137">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="2a484-137">-ServiceObject</span></span>
<span data-ttu-id="2a484-138">서비스 단위를 만들어야 하는 서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-138">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a484-139">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="2a484-139">-ServiceResourceId</span></span>
<span data-ttu-id="2a484-140">서비스 단위를 만들어야 하는 서비스 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-140">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a484-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="2a484-141">-ServiceTopologyName</span></span>
<span data-ttu-id="2a484-142">서비스 단위의 일부인 서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="2a484-143">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="2a484-143">-ServiceTopologyObject</span></span>
<span data-ttu-id="2a484-144">서비스 단위를 만들어야 하는 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-144">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a484-145">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="2a484-145">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="2a484-146">서비스 단위를 만들어야 하는 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-146">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a484-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a484-147">CommonParameters</span></span>
<span data-ttu-id="2a484-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2a484-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a484-149">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a484-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a484-150">입력</span><span class="sxs-lookup"><span data-stu-id="2a484-150">INPUTS</span></span>

### <span data-ttu-id="2a484-151">System.String</span><span class="sxs-lookup"><span data-stu-id="2a484-151">System.String</span></span>

### <span data-ttu-id="2a484-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="2a484-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="2a484-153">출력</span><span class="sxs-lookup"><span data-stu-id="2a484-153">OUTPUTS</span></span>

### <span data-ttu-id="2a484-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="2a484-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="2a484-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2a484-155">NOTES</span></span>

## <span data-ttu-id="2a484-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a484-156">RELATED LINKS</span></span>
