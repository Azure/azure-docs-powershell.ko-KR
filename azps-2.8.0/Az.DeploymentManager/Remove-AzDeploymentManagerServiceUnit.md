---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 3ba27cf26ccc555ea79a2b46100bee6be7e3c7fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696643"
---
# <span data-ttu-id="92b0c-101">Remove-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="92b0c-101">Remove-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="92b0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="92b0c-103">서비스 단위를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-103">Deletes the service unit.</span></span>

## <span data-ttu-id="92b0c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="92b0c-104">SYNTAX</span></span>

### <span data-ttu-id="92b0c-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="92b0c-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b0c-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="92b0c-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b0c-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="92b0c-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b0c-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="92b0c-108">ByServiceObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b0c-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="92b0c-109">ByServiceResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b0c-110">리소스</span><span class="sxs-lookup"><span data-stu-id="92b0c-110">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b0c-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="92b0c-111">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92b0c-112">설명은</span><span class="sxs-lookup"><span data-stu-id="92b0c-112">DESCRIPTION</span></span>
<span data-ttu-id="92b0c-113">**AzDeploymentManagerServiceUnit** cmdlet은 서비스에서 서비스 단위를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-113">The **Remove-AzDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="92b0c-114">서비스 단위를 이름, 정의 된 서비스, 서비스 토폴로지 이름 및 리소스 그룹 이름을 기준으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="92b0c-115">또는 ServiceUnit 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="92b0c-116">예제의</span><span class="sxs-lookup"><span data-stu-id="92b0c-116">EXAMPLES</span></span>

### <span data-ttu-id="92b0c-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="92b0c-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="92b0c-118">이 명령은 ContosoResourceGroup에서 ContosoServiceTopology 이라는 서비스 토폴로지의 서비스 ContosoService1 아래에 있는 ContosoService1Storage 이라는 서비스 단위를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="92b0c-119">예제 2: 리소스 식별자를 사용 하 여 서비스 단위 삭제</span><span class="sxs-lookup"><span data-stu-id="92b0c-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="92b0c-120">이 명령은 ContosoResourceGroup에서 ContosoServiceTopology 이라는 서비스 토폴로지의 서비스 ContosoService1 아래에 ContosoService1Storage 이라는 서비스 단위를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="92b0c-121">예제 3: 서비스 단위 개체를 사용 하 여 서비스 단위를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="92b0c-122">이 명령은 이름, 서비스 이름, 서비스 토폴로지 이름 및 ResourceGroup이 $serviceUnitObject의 Name, ServiceName, ServiceTopologyName 및 ResourceGroupName 속성과 각각 일치 하는 서비스 단위를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="92b0c-123">변수</span><span class="sxs-lookup"><span data-stu-id="92b0c-123">PARAMETERS</span></span>

### <span data-ttu-id="92b0c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b0c-124">-DefaultProfile</span></span>
<span data-ttu-id="92b0c-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92b0c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92b0c-126">-InputObject</span></span>
<span data-ttu-id="92b0c-127">서비스 단위 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-127">Service unit resource object.</span></span>

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

### <span data-ttu-id="92b0c-128">-이름</span><span class="sxs-lookup"><span data-stu-id="92b0c-128">-Name</span></span>
<span data-ttu-id="92b0c-129">서비스 단위의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-129">The name of the service unit.</span></span>

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

### <span data-ttu-id="92b0c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92b0c-130">-PassThru</span></span>
<span data-ttu-id="92b0c-131">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="92b0c-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="92b0c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92b0c-132">-ResourceGroupName</span></span>
<span data-ttu-id="92b0c-133">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="92b0c-133">The resource group.</span></span>

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

### <span data-ttu-id="92b0c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="92b0c-134">-ResourceId</span></span>
<span data-ttu-id="92b0c-135">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-135">The resource identifier.</span></span>

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

### <span data-ttu-id="92b0c-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="92b0c-136">-ServiceName</span></span>
<span data-ttu-id="92b0c-137">서비스 단위를 포함 하는 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-137">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="92b0c-138">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="92b0c-138">-ServiceObject</span></span>
<span data-ttu-id="92b0c-139">서비스 단위를 만들 서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-139">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="92b0c-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="92b0c-140">-ServiceResourceId</span></span>
<span data-ttu-id="92b0c-141">서비스 단위를 만들 서비스 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-141">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="92b0c-142">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="92b0c-142">-ServiceTopologyName</span></span>
<span data-ttu-id="92b0c-143">서비스 단위를 포함 하는 서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-143">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="92b0c-144">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="92b0c-144">-ServiceTopologyObject</span></span>
<span data-ttu-id="92b0c-145">서비스 단위를 만들 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-145">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="92b0c-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="92b0c-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="92b0c-147">서비스 단위를 만들 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-147">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="92b0c-148">-확인</span><span class="sxs-lookup"><span data-stu-id="92b0c-148">-Confirm</span></span>
<span data-ttu-id="92b0c-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92b0c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92b0c-150">-WhatIf</span></span>
<span data-ttu-id="92b0c-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92b0c-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92b0c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b0c-153">CommonParameters</span></span>
<span data-ttu-id="92b0c-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="92b0c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b0c-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92b0c-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b0c-156">입력</span><span class="sxs-lookup"><span data-stu-id="92b0c-156">INPUTS</span></span>

### <span data-ttu-id="92b0c-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="92b0c-157">System.String</span></span>

### <span data-ttu-id="92b0c-158">Microsoft. Azure. Psservicemanager 리소스</span><span class="sxs-lookup"><span data-stu-id="92b0c-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="92b0c-159">출력</span><span class="sxs-lookup"><span data-stu-id="92b0c-159">OUTPUTS</span></span>

### <span data-ttu-id="92b0c-160">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="92b0c-160">System.Boolean</span></span>

## <span data-ttu-id="92b0c-161">상속자</span><span class="sxs-lookup"><span data-stu-id="92b0c-161">NOTES</span></span>

## <span data-ttu-id="92b0c-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92b0c-162">RELATED LINKS</span></span>
