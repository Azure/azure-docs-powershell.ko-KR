---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: 4828471d684e82d67a10bed7340cc560e843210a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387360"
---
# <span data-ttu-id="8efc8-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="8efc8-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="8efc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8efc8-102">SYNOPSIS</span></span>
<span data-ttu-id="8efc8-103">서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-103">Deletes the service..</span></span> <span data-ttu-id="8efc8-104">서비스에서 만든 모든 서비스 단위는 서비스를 삭제하기 전에 삭제해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="8efc8-105">구문</span><span class="sxs-lookup"><span data-stu-id="8efc8-105">SYNTAX</span></span>

### <span data-ttu-id="8efc8-106">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="8efc8-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8efc8-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="8efc8-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8efc8-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="8efc8-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8efc8-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8efc8-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8efc8-110">InputObject</span><span class="sxs-lookup"><span data-stu-id="8efc8-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8efc8-111">설명</span><span class="sxs-lookup"><span data-stu-id="8efc8-111">DESCRIPTION</span></span>
<span data-ttu-id="8efc8-112">**Remove-AzDeploymentManagerService** cmdlet은 서비스 토폴로지에서 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="8efc8-113">해당 이름, 있는 서비스 토폴로지 및 리소스 그룹 이름으로 서비스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="8efc8-114">또는 서비스 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="8efc8-115">예제</span><span class="sxs-lookup"><span data-stu-id="8efc8-115">EXAMPLES</span></span>

### <span data-ttu-id="8efc8-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="8efc8-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="8efc8-117">이 명령은 ContosoResourceGroup의 ContosoServiceTopology라는 서비스 토폴로지에서 ContosoService1이라는 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="8efc8-118">예제 2: 리소스 식별자를 사용하여 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="8efc8-119">이 명령은 ContosoResourceGroup의 ContosoServiceTopology라는 서비스 토폴로지에서 ContosoService1이라는 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="8efc8-120">예제 3: 서비스 개체를 사용하여 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="8efc8-121">이 명령은 이름, 서비스 토폴로지 이름 및 ResourceGroup이 각각 이름, ServiceTopologyName 및 ResourceGroupName 속성과 일치하는 서비스를 $serviceObject 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="8efc8-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8efc8-122">PARAMETERS</span></span>

### <span data-ttu-id="8efc8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8efc8-123">-DefaultProfile</span></span>
<span data-ttu-id="8efc8-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8efc8-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8efc8-125">-InputObject</span></span>
<span data-ttu-id="8efc8-126">서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-126">Service object.</span></span>

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

### <span data-ttu-id="8efc8-127">-Name</span><span class="sxs-lookup"><span data-stu-id="8efc8-127">-Name</span></span>
<span data-ttu-id="8efc8-128">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-128">The name of the service.</span></span>

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

### <span data-ttu-id="8efc8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8efc8-129">-PassThru</span></span>
<span data-ttu-id="8efc8-130">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="8efc8-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8efc8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8efc8-131">-ResourceGroupName</span></span>
<span data-ttu-id="8efc8-132">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-132">The resource group.</span></span>

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

### <span data-ttu-id="8efc8-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8efc8-133">-ResourceId</span></span>
<span data-ttu-id="8efc8-134">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-134">The resource identifier.</span></span>

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

### <span data-ttu-id="8efc8-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="8efc8-135">-ServiceTopologyName</span></span>
<span data-ttu-id="8efc8-136">서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="8efc8-137">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="8efc8-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="8efc8-138">서비스를 만들어야 하는 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-138">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="8efc8-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="8efc8-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="8efc8-140">서비스를 만들어야 하는 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-140">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="8efc8-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8efc8-141">-Confirm</span></span>
<span data-ttu-id="8efc8-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8efc8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8efc8-143">-WhatIf</span></span>
<span data-ttu-id="8efc8-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8efc8-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8efc8-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8efc8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8efc8-146">CommonParameters</span></span>
<span data-ttu-id="8efc8-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8efc8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8efc8-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8efc8-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8efc8-149">입력</span><span class="sxs-lookup"><span data-stu-id="8efc8-149">INPUTS</span></span>

### <span data-ttu-id="8efc8-150">System.String</span><span class="sxs-lookup"><span data-stu-id="8efc8-150">System.String</span></span>

### <span data-ttu-id="8efc8-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="8efc8-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="8efc8-152">출력</span><span class="sxs-lookup"><span data-stu-id="8efc8-152">OUTPUTS</span></span>

### <span data-ttu-id="8efc8-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8efc8-153">System.Boolean</span></span>

## <span data-ttu-id="8efc8-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8efc8-154">NOTES</span></span>

## <span data-ttu-id="8efc8-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8efc8-155">RELATED LINKS</span></span>
