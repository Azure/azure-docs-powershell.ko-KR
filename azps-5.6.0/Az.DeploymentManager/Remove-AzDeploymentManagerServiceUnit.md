---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: db7291f143abc5305f79f6b41310a5526c9fbb3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966315"
---
# <span data-ttu-id="535fa-101">Remove-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="535fa-101">Remove-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="535fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="535fa-102">SYNOPSIS</span></span>
<span data-ttu-id="535fa-103">서비스 단위를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-103">Deletes the service unit.</span></span>

## <span data-ttu-id="535fa-104">구문</span><span class="sxs-lookup"><span data-stu-id="535fa-104">SYNTAX</span></span>

### <span data-ttu-id="535fa-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="535fa-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="535fa-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="535fa-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="535fa-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="535fa-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="535fa-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="535fa-108">ByServiceObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="535fa-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="535fa-109">ByServiceResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="535fa-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="535fa-110">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="535fa-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="535fa-111">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="535fa-112">설명</span><span class="sxs-lookup"><span data-stu-id="535fa-112">DESCRIPTION</span></span>
<span data-ttu-id="535fa-113">**Remove-AzDeploymentManagerServiceUnit** cmdlet은 서비스에서 서비스 단위를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-113">The **Remove-AzDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="535fa-114">서비스 단위의 이름, 정의된 서비스, 서비스 토폴로지 이름 및 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="535fa-115">또는 ServiceUnit 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="535fa-116">예제</span><span class="sxs-lookup"><span data-stu-id="535fa-116">EXAMPLES</span></span>

### <span data-ttu-id="535fa-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="535fa-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="535fa-118">이 명령은 ContosoResourceGroup의 ContosoServiceTopology라는 서비스 토폴로지에서 ContosoService1 서비스 아래에 ContosoService1Storage라는 서비스 단위를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="535fa-119">예제 2: 리소스 식별자를 사용하여 서비스 단위를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="535fa-120">이 명령은 ContosoResourceGroup의 ContosoServiceTopology라는 서비스 토폴로지에서 ContosoService1 서비스 아래에 ContosoService1Storage라는 서비스 단위를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="535fa-121">예제 3: 서비스 단위 개체를 사용하여 서비스 단위를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="535fa-122">이 명령은 이름, 서비스 이름, 서비스 토폴로지 이름 및 ResourceGroup이 각각 서비스의 이름, ServiceName, ServiceTopologyName 및 ResourceGroupName 속성과 일치하는 서비스 $serviceUnitObject 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="535fa-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="535fa-123">PARAMETERS</span></span>

### <span data-ttu-id="535fa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="535fa-124">-DefaultProfile</span></span>
<span data-ttu-id="535fa-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="535fa-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="535fa-126">-InputObject</span></span>
<span data-ttu-id="535fa-127">서비스 단위 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-127">Service unit resource object.</span></span>

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

### <span data-ttu-id="535fa-128">-Name</span><span class="sxs-lookup"><span data-stu-id="535fa-128">-Name</span></span>
<span data-ttu-id="535fa-129">서비스 단위의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-129">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535fa-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="535fa-130">-PassThru</span></span>
<span data-ttu-id="535fa-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="535fa-131">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535fa-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="535fa-132">-ResourceGroupName</span></span>
<span data-ttu-id="535fa-133">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-133">The resource group.</span></span>

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

### <span data-ttu-id="535fa-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="535fa-134">-ResourceId</span></span>
<span data-ttu-id="535fa-135">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-135">The resource identifier.</span></span>

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

### <span data-ttu-id="535fa-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="535fa-136">-ServiceName</span></span>
<span data-ttu-id="535fa-137">서비스 단위의 일부인 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-137">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="535fa-138">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="535fa-138">-ServiceObject</span></span>
<span data-ttu-id="535fa-139">서비스 단위를 만들어야 하는 서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-139">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="535fa-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="535fa-140">-ServiceResourceId</span></span>
<span data-ttu-id="535fa-141">서비스 단위를 만들어야 하는 서비스 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-141">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="535fa-142">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="535fa-142">-ServiceTopologyName</span></span>
<span data-ttu-id="535fa-143">서비스 단위의 일부인 서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-143">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="535fa-144">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="535fa-144">-ServiceTopologyObject</span></span>
<span data-ttu-id="535fa-145">서비스 단위를 만들어야 하는 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-145">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="535fa-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="535fa-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="535fa-147">서비스 단위를 만들어야 하는 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-147">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="535fa-148">-확인</span><span class="sxs-lookup"><span data-stu-id="535fa-148">-Confirm</span></span>
<span data-ttu-id="535fa-149">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535fa-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="535fa-150">-WhatIf</span></span>
<span data-ttu-id="535fa-151">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="535fa-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="535fa-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="535fa-153">CommonParameters</span></span>
<span data-ttu-id="535fa-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="535fa-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="535fa-155">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="535fa-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="535fa-156">입력</span><span class="sxs-lookup"><span data-stu-id="535fa-156">INPUTS</span></span>

### <span data-ttu-id="535fa-157">System.String</span><span class="sxs-lookup"><span data-stu-id="535fa-157">System.String</span></span>

### <span data-ttu-id="535fa-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="535fa-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="535fa-159">출력</span><span class="sxs-lookup"><span data-stu-id="535fa-159">OUTPUTS</span></span>

### <span data-ttu-id="535fa-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="535fa-160">System.Boolean</span></span>

## <span data-ttu-id="535fa-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="535fa-161">NOTES</span></span>

## <span data-ttu-id="535fa-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="535fa-162">RELATED LINKS</span></span>
