---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: ee0f1f855f4f24e3672606bfedc000452ce6040d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696646"
---
# <span data-ttu-id="5a4fa-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="5a4fa-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="5a4fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a4fa-102">SYNOPSIS</span></span>
<span data-ttu-id="5a4fa-103">서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-103">Deletes the service..</span></span> <span data-ttu-id="5a4fa-104">서비스를 삭제 하기 전에 서비스 아래에 만든 모든 서비스 단위를 삭제 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="5a4fa-105">구문과</span><span class="sxs-lookup"><span data-stu-id="5a4fa-105">SYNTAX</span></span>

### <span data-ttu-id="5a4fa-106">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="5a4fa-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5a4fa-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="5a4fa-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a4fa-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="5a4fa-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a4fa-109">리소스</span><span class="sxs-lookup"><span data-stu-id="5a4fa-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a4fa-110">InputObject</span><span class="sxs-lookup"><span data-stu-id="5a4fa-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a4fa-111">설명은</span><span class="sxs-lookup"><span data-stu-id="5a4fa-111">DESCRIPTION</span></span>
<span data-ttu-id="5a4fa-112">**AzDeploymentManagerService** cmdlet은 서비스 토폴로지에서 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="5a4fa-113">서비스를 이름, 서비스 토폴로지, 그리고 리소스 그룹 이름으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="5a4fa-114">또는 서비스 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="5a4fa-115">예제의</span><span class="sxs-lookup"><span data-stu-id="5a4fa-115">EXAMPLES</span></span>

### <span data-ttu-id="5a4fa-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="5a4fa-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="5a4fa-117">이 명령은 ContosoResourceGroup의 ContosoServiceTopology 이라는 서비스 토폴로지에서 ContosoService1 이라는 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="5a4fa-118">예제 2: 리소스 식별자를 사용 하 여 서비스 삭제</span><span class="sxs-lookup"><span data-stu-id="5a4fa-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="5a4fa-119">이 명령은 ContosoResourceGroup의 ContosoServiceTopology 이라는 서비스 토폴로지에서 ContosoService1 이라는 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="5a4fa-120">예제 3: 서비스 개체를 사용 하 여 서비스 삭제</span><span class="sxs-lookup"><span data-stu-id="5a4fa-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="5a4fa-121">이 명령은 이름을 가진 서비스를 삭제 하 고, 서비스 토폴로지 이름 및 ResourceGroup이 $serviceObject의 Name, ServiceTopologyName 및 ResourceGroupName 속성과 각각 일치 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="5a4fa-122">변수</span><span class="sxs-lookup"><span data-stu-id="5a4fa-122">PARAMETERS</span></span>

### <span data-ttu-id="5a4fa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a4fa-123">-DefaultProfile</span></span>
<span data-ttu-id="5a4fa-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a4fa-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a4fa-125">-InputObject</span></span>
<span data-ttu-id="5a4fa-126">서비스 개체.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-126">Service object.</span></span>

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

### <span data-ttu-id="5a4fa-127">-이름</span><span class="sxs-lookup"><span data-stu-id="5a4fa-127">-Name</span></span>
<span data-ttu-id="5a4fa-128">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-128">The name of the service.</span></span>

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

### <span data-ttu-id="5a4fa-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a4fa-129">-PassThru</span></span>
<span data-ttu-id="5a4fa-130">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="5a4fa-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5a4fa-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a4fa-131">-ResourceGroupName</span></span>
<span data-ttu-id="5a4fa-132">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="5a4fa-132">The resource group.</span></span>

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

### <span data-ttu-id="5a4fa-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a4fa-133">-ResourceId</span></span>
<span data-ttu-id="5a4fa-134">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-134">The resource identifier.</span></span>

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

### <span data-ttu-id="5a4fa-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="5a4fa-135">-ServiceTopologyName</span></span>
<span data-ttu-id="5a4fa-136">서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="5a4fa-137">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="5a4fa-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="5a4fa-138">서비스를 만들어야 하는 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-138">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="5a4fa-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="5a4fa-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="5a4fa-140">서비스를 만들어야 하는 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-140">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="5a4fa-141">-확인</span><span class="sxs-lookup"><span data-stu-id="5a4fa-141">-Confirm</span></span>
<span data-ttu-id="5a4fa-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a4fa-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a4fa-143">-WhatIf</span></span>
<span data-ttu-id="5a4fa-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a4fa-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a4fa-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a4fa-146">CommonParameters</span></span>
<span data-ttu-id="5a4fa-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a4fa-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a4fa-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a4fa-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a4fa-149">입력</span><span class="sxs-lookup"><span data-stu-id="5a4fa-149">INPUTS</span></span>

### <span data-ttu-id="5a4fa-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5a4fa-150">System.String</span></span>

### <span data-ttu-id="5a4fa-151">Microsoft. Azure. PSServiceResource 명령)</span><span class="sxs-lookup"><span data-stu-id="5a4fa-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="5a4fa-152">출력</span><span class="sxs-lookup"><span data-stu-id="5a4fa-152">OUTPUTS</span></span>

### <span data-ttu-id="5a4fa-153">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="5a4fa-153">System.Boolean</span></span>

## <span data-ttu-id="5a4fa-154">상속자</span><span class="sxs-lookup"><span data-stu-id="5a4fa-154">NOTES</span></span>

## <span data-ttu-id="5a4fa-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a4fa-155">RELATED LINKS</span></span>