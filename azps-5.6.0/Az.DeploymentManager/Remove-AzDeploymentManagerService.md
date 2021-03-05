---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: 284e568e1748c8bf6da3c5d43c27acb046be6172
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980688"
---
# <span data-ttu-id="560d5-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="560d5-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="560d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="560d5-102">SYNOPSIS</span></span>
<span data-ttu-id="560d5-103">서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-103">Deletes the service..</span></span> <span data-ttu-id="560d5-104">서비스에서 만든 모든 서비스 단위는 서비스를 삭제하기 전에 삭제해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="560d5-105">구문</span><span class="sxs-lookup"><span data-stu-id="560d5-105">SYNTAX</span></span>

### <span data-ttu-id="560d5-106">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="560d5-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="560d5-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="560d5-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="560d5-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="560d5-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="560d5-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="560d5-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="560d5-110">InputObject</span><span class="sxs-lookup"><span data-stu-id="560d5-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="560d5-111">설명</span><span class="sxs-lookup"><span data-stu-id="560d5-111">DESCRIPTION</span></span>
<span data-ttu-id="560d5-112">**Remove-AzDeploymentManagerService** cmdlet은 서비스 토폴로지에서 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="560d5-113">해당 이름, 에 있는 서비스 토폴로지 및 리소스 그룹 이름으로 서비스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="560d5-114">또는 Service 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="560d5-115">예제</span><span class="sxs-lookup"><span data-stu-id="560d5-115">EXAMPLES</span></span>

### <span data-ttu-id="560d5-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="560d5-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="560d5-117">이 명령은 ContosoResourceGroup의 ContosoServiceTopology라는 서비스 토폴로지에서 ContosoService1이라는 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="560d5-118">예제 2: 리소스 식별자를 사용하여 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="560d5-119">이 명령은 ContosoResourceGroup의 ContosoServiceTopology라는 서비스 토폴로지에서 ContosoService1이라는 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="560d5-120">예제 3: 서비스 개체를 사용하여 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="560d5-121">이 명령은 이름, 서비스 토폴로지 이름 및 ResourceGroup이 각각 서비스의 이름, ServiceTopologyName 및 ResourceGroupName 속성과 일치하는 서비스를 $serviceObject 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="560d5-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="560d5-122">PARAMETERS</span></span>

### <span data-ttu-id="560d5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="560d5-123">-DefaultProfile</span></span>
<span data-ttu-id="560d5-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="560d5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="560d5-125">-InputObject</span></span>
<span data-ttu-id="560d5-126">서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-126">Service object.</span></span>

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

### <span data-ttu-id="560d5-127">-Name</span><span class="sxs-lookup"><span data-stu-id="560d5-127">-Name</span></span>
<span data-ttu-id="560d5-128">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="560d5-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="560d5-129">-PassThru</span></span>
<span data-ttu-id="560d5-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="560d5-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="560d5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="560d5-131">-ResourceGroupName</span></span>
<span data-ttu-id="560d5-132">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-132">The resource group.</span></span>

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

### <span data-ttu-id="560d5-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="560d5-133">-ResourceId</span></span>
<span data-ttu-id="560d5-134">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-134">The resource identifier.</span></span>

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

### <span data-ttu-id="560d5-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="560d5-135">-ServiceTopologyName</span></span>
<span data-ttu-id="560d5-136">서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="560d5-137">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="560d5-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="560d5-138">서비스를 만들어야 하는 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-138">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="560d5-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="560d5-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="560d5-140">서비스를 만들어야 하는 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-140">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="560d5-141">-확인</span><span class="sxs-lookup"><span data-stu-id="560d5-141">-Confirm</span></span>
<span data-ttu-id="560d5-142">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="560d5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="560d5-143">-WhatIf</span></span>
<span data-ttu-id="560d5-144">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="560d5-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="560d5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="560d5-146">CommonParameters</span></span>
<span data-ttu-id="560d5-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="560d5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="560d5-148">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="560d5-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="560d5-149">입력</span><span class="sxs-lookup"><span data-stu-id="560d5-149">INPUTS</span></span>

### <span data-ttu-id="560d5-150">System.String</span><span class="sxs-lookup"><span data-stu-id="560d5-150">System.String</span></span>

### <span data-ttu-id="560d5-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="560d5-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="560d5-152">출력</span><span class="sxs-lookup"><span data-stu-id="560d5-152">OUTPUTS</span></span>

### <span data-ttu-id="560d5-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="560d5-153">System.Boolean</span></span>

## <span data-ttu-id="560d5-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="560d5-154">NOTES</span></span>

## <span data-ttu-id="560d5-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="560d5-155">RELATED LINKS</span></span>
