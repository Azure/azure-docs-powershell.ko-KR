---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: 4828471d684e82d67a10bed7340cc560e843210a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047796"
---
# <span data-ttu-id="1a6f5-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="1a6f5-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="1a6f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a6f5-102">SYNOPSIS</span></span>
<span data-ttu-id="1a6f5-103">서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-103">Deletes the service..</span></span> <span data-ttu-id="1a6f5-104">서비스를 삭제 하기 전에 서비스 아래에 만든 모든 서비스 단위를 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="1a6f5-105">구문과</span><span class="sxs-lookup"><span data-stu-id="1a6f5-105">SYNTAX</span></span>

### <span data-ttu-id="1a6f5-106">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1a6f5-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a6f5-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="1a6f5-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a6f5-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="1a6f5-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a6f5-109">리소스</span><span class="sxs-lookup"><span data-stu-id="1a6f5-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a6f5-110">InputObject</span><span class="sxs-lookup"><span data-stu-id="1a6f5-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a6f5-111">설명은</span><span class="sxs-lookup"><span data-stu-id="1a6f5-111">DESCRIPTION</span></span>
<span data-ttu-id="1a6f5-112">**AzDeploymentManagerService** cmdlet은 서비스 토폴로지에서 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="1a6f5-113">서비스를 이름, 서비스 토폴로지, 그리고 리소스 그룹 이름으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="1a6f5-114">또는 서비스 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="1a6f5-115">예제의</span><span class="sxs-lookup"><span data-stu-id="1a6f5-115">EXAMPLES</span></span>

### <span data-ttu-id="1a6f5-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="1a6f5-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="1a6f5-117">이 명령은 ContosoResourceGroup의 ContosoServiceTopology 이라는 서비스 토폴로지에서 ContosoService1 이라는 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="1a6f5-118">예제 2: 리소스 식별자를 사용 하 여 서비스 삭제</span><span class="sxs-lookup"><span data-stu-id="1a6f5-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="1a6f5-119">이 명령은 ContosoResourceGroup의 ContosoServiceTopology 이라는 서비스 토폴로지에서 ContosoService1 이라는 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="1a6f5-120">예제 3: 서비스 개체를 사용 하 여 서비스 삭제</span><span class="sxs-lookup"><span data-stu-id="1a6f5-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="1a6f5-121">이 명령은 이름을 가진 서비스를 삭제 하 고, 서비스 토폴로지 이름 및 ResourceGroup이 $serviceObject의 Name, ServiceTopologyName 및 ResourceGroupName 속성과 각각 일치 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="1a6f5-122">변수</span><span class="sxs-lookup"><span data-stu-id="1a6f5-122">PARAMETERS</span></span>

### <span data-ttu-id="1a6f5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a6f5-123">-DefaultProfile</span></span>
<span data-ttu-id="1a6f5-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a6f5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a6f5-125">-InputObject</span></span>
<span data-ttu-id="1a6f5-126">서비스 개체.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-126">Service object.</span></span>

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

### <span data-ttu-id="1a6f5-127">-이름</span><span class="sxs-lookup"><span data-stu-id="1a6f5-127">-Name</span></span>
<span data-ttu-id="1a6f5-128">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-128">The name of the service.</span></span>

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

### <span data-ttu-id="1a6f5-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a6f5-129">-PassThru</span></span>
<span data-ttu-id="1a6f5-130">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="1a6f5-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1a6f5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a6f5-131">-ResourceGroupName</span></span>
<span data-ttu-id="1a6f5-132">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="1a6f5-132">The resource group.</span></span>

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

### <span data-ttu-id="1a6f5-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a6f5-133">-ResourceId</span></span>
<span data-ttu-id="1a6f5-134">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-134">The resource identifier.</span></span>

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

### <span data-ttu-id="1a6f5-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="1a6f5-135">-ServiceTopologyName</span></span>
<span data-ttu-id="1a6f5-136">서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="1a6f5-137">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="1a6f5-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="1a6f5-138">서비스를 만들어야 하는 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-138">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="1a6f5-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="1a6f5-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="1a6f5-140">서비스를 만들어야 하는 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-140">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="1a6f5-141">-확인</span><span class="sxs-lookup"><span data-stu-id="1a6f5-141">-Confirm</span></span>
<span data-ttu-id="1a6f5-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a6f5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a6f5-143">-WhatIf</span></span>
<span data-ttu-id="1a6f5-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a6f5-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a6f5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a6f5-146">CommonParameters</span></span>
<span data-ttu-id="1a6f5-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a6f5-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1a6f5-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a6f5-149">입력</span><span class="sxs-lookup"><span data-stu-id="1a6f5-149">INPUTS</span></span>

### <span data-ttu-id="1a6f5-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1a6f5-150">System.String</span></span>

### <span data-ttu-id="1a6f5-151">Microsoft. Azure. PSServiceResource 명령)</span><span class="sxs-lookup"><span data-stu-id="1a6f5-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="1a6f5-152">출력</span><span class="sxs-lookup"><span data-stu-id="1a6f5-152">OUTPUTS</span></span>

### <span data-ttu-id="1a6f5-153">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1a6f5-153">System.Boolean</span></span>

## <span data-ttu-id="1a6f5-154">상속자</span><span class="sxs-lookup"><span data-stu-id="1a6f5-154">NOTES</span></span>

## <span data-ttu-id="1a6f5-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a6f5-155">RELATED LINKS</span></span>
