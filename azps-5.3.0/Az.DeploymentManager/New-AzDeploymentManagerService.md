---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: aec721a3676a6b4510c7fe0eccf5badc4f9ccce2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493087"
---
# <span data-ttu-id="fe433-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="fe433-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="fe433-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe433-102">SYNOPSIS</span></span>
<span data-ttu-id="fe433-103">지정된 서비스 토폴로지 아래에 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="fe433-104">구문</span><span class="sxs-lookup"><span data-stu-id="fe433-104">SYNTAX</span></span>

### <span data-ttu-id="fe433-105">대화형(기본값)</span><span class="sxs-lookup"><span data-stu-id="fe433-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe433-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="fe433-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe433-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="fe433-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe433-108">설명</span><span class="sxs-lookup"><span data-stu-id="fe433-108">DESCRIPTION</span></span>
<span data-ttu-id="fe433-109">**New-AzDeploymentManagerService** cmdlet은 서비스 토폴로지 아래에 서비스를 만들고 해당 서비스를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="fe433-110">해당 이름, 있는 서비스 토폴로지 및 리소스 그룹 이름으로 서비스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="fe433-111">cmdlet은 서비스 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="fe433-112">이 개체를 로컬로 수정한 다음, Set-AzDeploymentManagerService cmdlet을 사용하여 서비스에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="fe433-113">예제</span><span class="sxs-lookup"><span data-stu-id="fe433-113">EXAMPLES</span></span>

### <span data-ttu-id="fe433-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="fe433-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="fe433-115">리소스 그룹 ContosoResourceGroup의 서비스 토폴로지 ContosoServiceTopology에서 이름이 ContosoService1인 새 서비스를 미국 중부 위치에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="fe433-116">TargetLocation 속성은 지정된 구독에서 ContosoService1 서비스를 미국 동부 지역에 배포해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="fe433-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe433-117">PARAMETERS</span></span>

### <span data-ttu-id="fe433-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe433-118">-DefaultProfile</span></span>
<span data-ttu-id="fe433-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe433-120">-Location</span><span class="sxs-lookup"><span data-stu-id="fe433-120">-Location</span></span>
<span data-ttu-id="fe433-121">서비스 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-121">The location of the service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe433-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fe433-122">-Name</span></span>
<span data-ttu-id="fe433-123">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-123">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe433-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe433-124">-ResourceGroupName</span></span>
<span data-ttu-id="fe433-125">리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-125">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe433-126">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="fe433-126">-ServiceTopologyId</span></span>
<span data-ttu-id="fe433-127">서비스를 만들어야 하는 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-127">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="fe433-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="fe433-128">-ServiceTopologyName</span></span>
<span data-ttu-id="fe433-129">이 서비스가 속한 서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-129">The name of the service topology this service belongs to.</span></span>

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

### <span data-ttu-id="fe433-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="fe433-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="fe433-131">서비스를 만들어야 하는 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-131">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="fe433-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="fe433-132">-Tag</span></span>
<span data-ttu-id="fe433-133">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe433-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="fe433-134">-TargetLocation</span></span>
<span data-ttu-id="fe433-135">서비스에서 리소스를 배포할 위치를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-135">Determines the location where resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe433-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe433-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="fe433-137">서비스에서 리소스를 배포할 구독을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe433-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe433-138">-Confirm</span></span>
<span data-ttu-id="fe433-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe433-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe433-140">-WhatIf</span></span>
<span data-ttu-id="fe433-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fe433-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe433-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe433-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe433-143">CommonParameters</span></span>
<span data-ttu-id="fe433-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fe433-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe433-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fe433-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe433-146">입력</span><span class="sxs-lookup"><span data-stu-id="fe433-146">INPUTS</span></span>

### <span data-ttu-id="fe433-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fe433-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fe433-148">출력</span><span class="sxs-lookup"><span data-stu-id="fe433-148">OUTPUTS</span></span>

### <span data-ttu-id="fe433-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="fe433-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="fe433-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fe433-150">NOTES</span></span>

## <span data-ttu-id="fe433-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe433-151">RELATED LINKS</span></span>
