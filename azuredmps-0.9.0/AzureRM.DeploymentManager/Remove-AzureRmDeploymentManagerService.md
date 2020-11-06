---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4b2cd4ef2dde674b10d51dc378578acbd13c4a7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523076"
---
# <span data-ttu-id="11377-101">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="11377-101">Remove-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="11377-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11377-102">SYNOPSIS</span></span>
<span data-ttu-id="11377-103">서비스 토폴로지에서 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="11377-103">Deletes a service in a service topology.</span></span>

## <span data-ttu-id="11377-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11377-104">SYNTAX</span></span>

### <span data-ttu-id="11377-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="11377-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11377-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="11377-106">ByServiceTopologyObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11377-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="11377-107">ByServiceTopologyResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11377-108">리소스</span><span class="sxs-lookup"><span data-stu-id="11377-108">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11377-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="11377-109">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11377-110">설명은</span><span class="sxs-lookup"><span data-stu-id="11377-110">DESCRIPTION</span></span>
<span data-ttu-id="11377-111">**AzureRmDeploymentManagerService** cmdlet은 서비스 토폴로지에서 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="11377-111">The **Remove-AzureRmDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="11377-112">서비스를 이름, 서비스 토폴로지, 그리고 리소스 그룹 이름으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11377-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="11377-113">또는 서비스 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11377-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="11377-114">예제의</span><span class="sxs-lookup"><span data-stu-id="11377-114">EXAMPLES</span></span>

### <span data-ttu-id="11377-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="11377-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="11377-116">이 명령은 ContosoResourceGroup의 ContosoServiceTopology 이라는 서비스 토폴로지에서 ContosoService1 이라는 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="11377-116">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="11377-117">예제 2: 리소스 식별자를 사용 하 여 서비스 삭제</span><span class="sxs-lookup"><span data-stu-id="11377-117">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="11377-118">이 명령은 ContosoResourceGroup의 ContosoServiceTopology 이라는 서비스 토폴로지에서 ContosoService1 이라는 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="11377-118">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="11377-119">예제 3: 서비스 개체를 사용 하 여 서비스 삭제</span><span class="sxs-lookup"><span data-stu-id="11377-119">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="11377-120">이 명령은 이름을 가진 서비스를 삭제 하 고, 서비스 토폴로지 이름 및 ResourceGroup이 $serviceObject의 Name, ServiceTopologyName 및 ResourceGroupName 속성과 각각 일치 합니다.</span><span class="sxs-lookup"><span data-stu-id="11377-120">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="11377-121">변수</span><span class="sxs-lookup"><span data-stu-id="11377-121">PARAMETERS</span></span>

### <span data-ttu-id="11377-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11377-122">-DefaultProfile</span></span>
<span data-ttu-id="11377-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11377-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11377-124">-Force</span><span class="sxs-lookup"><span data-stu-id="11377-124">-Force</span></span>
<span data-ttu-id="11377-125">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11377-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="11377-126">-이름</span><span class="sxs-lookup"><span data-stu-id="11377-126">-Name</span></span>
<span data-ttu-id="11377-127">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11377-127">The name of the service.</span></span>

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

### <span data-ttu-id="11377-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11377-128">-PassThru</span></span>
<span data-ttu-id="11377-129">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="11377-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="11377-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11377-130">-ResourceGroupName</span></span>
<span data-ttu-id="11377-131">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="11377-131">The resource group.</span></span>

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

### <span data-ttu-id="11377-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11377-132">-ResourceId</span></span>
<span data-ttu-id="11377-133">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="11377-133">The resource identifier.</span></span>

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

### <span data-ttu-id="11377-134">-서비스</span><span class="sxs-lookup"><span data-stu-id="11377-134">-Service</span></span>
<span data-ttu-id="11377-135">제거할 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="11377-135">The resource to be removed.</span></span>

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

### <span data-ttu-id="11377-136">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="11377-136">-ServiceTopology</span></span>
<span data-ttu-id="11377-137">서비스를 만들어야 하는 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="11377-137">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="11377-138">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="11377-138">-ServiceTopologyName</span></span>
<span data-ttu-id="11377-139">서비스가 속한 서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11377-139">The name of the service topology the service belongs to.</span></span>

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

### <span data-ttu-id="11377-140">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="11377-140">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="11377-141">서비스를 만들어야 하는 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="11377-141">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="11377-142">-확인</span><span class="sxs-lookup"><span data-stu-id="11377-142">-Confirm</span></span>
<span data-ttu-id="11377-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11377-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11377-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11377-144">-WhatIf</span></span>
<span data-ttu-id="11377-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="11377-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11377-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11377-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11377-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11377-147">CommonParameters</span></span>
<span data-ttu-id="11377-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11377-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11377-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11377-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11377-150">입력</span><span class="sxs-lookup"><span data-stu-id="11377-150">INPUTS</span></span>

### <span data-ttu-id="11377-151">Microsoft. Azure. PSServiceResource 명령)</span><span class="sxs-lookup"><span data-stu-id="11377-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="11377-152">출력</span><span class="sxs-lookup"><span data-stu-id="11377-152">OUTPUTS</span></span>

### <span data-ttu-id="11377-153">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="11377-153">System.Boolean</span></span>

## <span data-ttu-id="11377-154">상속자</span><span class="sxs-lookup"><span data-stu-id="11377-154">NOTES</span></span>

## <span data-ttu-id="11377-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11377-155">RELATED LINKS</span></span>

[<span data-ttu-id="11377-156">새로운 AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="11377-156">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="11377-157">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="11377-157">Get-AzureRmDeploymentManagerService</span></span>](./Get-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="11377-158">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="11377-158">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)