---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: d3716d18bc883d5407ee4acf3fa43960b63e7cd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980683"
---
# <span data-ttu-id="42661-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="42661-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="42661-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42661-102">SYNOPSIS</span></span>
<span data-ttu-id="42661-103">서비스 토폴로지가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="42661-103">Deletes the service topology.</span></span> <span data-ttu-id="42661-104">서비스 토폴로지 아래에서 만든 모든 서비스는 서비스 토폴로지 삭제 전에 삭제해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="42661-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="42661-105">구문</span><span class="sxs-lookup"><span data-stu-id="42661-105">SYNTAX</span></span>

### <span data-ttu-id="42661-106">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="42661-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42661-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="42661-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42661-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="42661-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42661-109">설명</span><span class="sxs-lookup"><span data-stu-id="42661-109">DESCRIPTION</span></span>
<span data-ttu-id="42661-110">**Remove-AzDeploymentManagerServiceTopology** cmdlet은 서비스 토폴로지가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="42661-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="42661-111">서비스 토폴로지의 이름 및 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42661-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="42661-112">또는 ServiceTopology 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42661-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="42661-113">예제</span><span class="sxs-lookup"><span data-stu-id="42661-113">EXAMPLES</span></span>

### <span data-ttu-id="42661-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="42661-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="42661-115">이 명령은 ContosoResourceGroup에서 ContosoServiceTopology라는 서비스 토폴로지가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="42661-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="42661-116">예제 2: 리소스 식별자를 사용하여 서비스 토폴로지 삭제</span><span class="sxs-lookup"><span data-stu-id="42661-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="42661-117">이 명령은 ContosoResourceGroup에서 ContosoServiceTopology라는 서비스 토폴로지가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="42661-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="42661-118">예제 3: 서비스 토폴로지 개체를 사용하여 서비스 토폴로지 삭제</span><span class="sxs-lookup"><span data-stu-id="42661-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="42661-119">이 명령은 이름 및 ResourceGroup이 각각 해당 서비스의 이름 및 ResourceGroupName 속성과 일치하는 서비스 토폴로지 $serviceTopologyObject 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="42661-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="42661-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="42661-120">PARAMETERS</span></span>

### <span data-ttu-id="42661-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42661-121">-DefaultProfile</span></span>
<span data-ttu-id="42661-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42661-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42661-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42661-123">-InputObject</span></span>
<span data-ttu-id="42661-124">제거할 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="42661-124">The resource to be removed.</span></span>

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

### <span data-ttu-id="42661-125">-Name</span><span class="sxs-lookup"><span data-stu-id="42661-125">-Name</span></span>
<span data-ttu-id="42661-126">서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42661-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="42661-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42661-127">-PassThru</span></span>
<span data-ttu-id="42661-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="42661-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="42661-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42661-129">-ResourceGroupName</span></span>
<span data-ttu-id="42661-130">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="42661-130">The resource group.</span></span>

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

### <span data-ttu-id="42661-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42661-131">-ResourceId</span></span>
<span data-ttu-id="42661-132">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="42661-132">The resource identifier.</span></span>

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

### <span data-ttu-id="42661-133">-확인</span><span class="sxs-lookup"><span data-stu-id="42661-133">-Confirm</span></span>
<span data-ttu-id="42661-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="42661-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42661-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42661-135">-WhatIf</span></span>
<span data-ttu-id="42661-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="42661-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42661-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42661-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42661-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42661-138">CommonParameters</span></span>
<span data-ttu-id="42661-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42661-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42661-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42661-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42661-141">입력</span><span class="sxs-lookup"><span data-stu-id="42661-141">INPUTS</span></span>

### <span data-ttu-id="42661-142">System.String</span><span class="sxs-lookup"><span data-stu-id="42661-142">System.String</span></span>

### <span data-ttu-id="42661-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="42661-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="42661-144">출력</span><span class="sxs-lookup"><span data-stu-id="42661-144">OUTPUTS</span></span>

### <span data-ttu-id="42661-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="42661-145">System.Boolean</span></span>

## <span data-ttu-id="42661-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="42661-146">NOTES</span></span>

## <span data-ttu-id="42661-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42661-147">RELATED LINKS</span></span>
