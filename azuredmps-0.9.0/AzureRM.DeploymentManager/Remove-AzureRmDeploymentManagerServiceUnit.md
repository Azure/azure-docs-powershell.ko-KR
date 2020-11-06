---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: 993b250b0c49efc448c0198c4e9a3aea29f77714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523855"
---
# <span data-ttu-id="b012a-101">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b012a-101">Remove-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="b012a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b012a-102">SYNOPSIS</span></span>
<span data-ttu-id="b012a-103">서비스 토폴로지에서 서비스의 서비스 단위를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-103">Deletes the service unit of a service in a service topology.</span></span>

## <span data-ttu-id="b012a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b012a-104">SYNTAX</span></span>

### <span data-ttu-id="b012a-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b012a-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b012a-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="b012a-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b012a-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="b012a-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b012a-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="b012a-108">ByServiceObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b012a-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="b012a-109">ByServiceResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b012a-110">리소스</span><span class="sxs-lookup"><span data-stu-id="b012a-110">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b012a-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="b012a-111">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b012a-112">설명은</span><span class="sxs-lookup"><span data-stu-id="b012a-112">DESCRIPTION</span></span>
<span data-ttu-id="b012a-113">**AzureRmDeploymentManagerServiceUnit** cmdlet은 서비스에서 서비스 단위를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-113">The **Remove-AzureRmDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="b012a-114">서비스 단위를 이름, 정의 된 서비스, 서비스 토폴로지 이름 및 리소스 그룹 이름을 기준으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="b012a-115">또는 ServiceUnit 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="b012a-116">예제의</span><span class="sxs-lookup"><span data-stu-id="b012a-116">EXAMPLES</span></span>

### <span data-ttu-id="b012a-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="b012a-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="b012a-118">이 명령은 ContosoResourceGroup에서 ContosoServiceTopology 이라는 서비스 토폴로지의 서비스 ContosoService1 아래에 있는 ContosoService1Storage 이라는 서비스 단위를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="b012a-119">예제 2: 리소스 식별자를 사용 하 여 서비스 단위 삭제</span><span class="sxs-lookup"><span data-stu-id="b012a-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="b012a-120">이 명령은 ContosoResourceGroup에서 ContosoServiceTopology 이라는 서비스 토폴로지의 서비스 ContosoService1 아래에 ContosoService1Storage 이라는 서비스 단위를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="b012a-121">예제 3: 서비스 단위 개체를 사용 하 여 서비스 단위를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="b012a-122">이 명령은 이름, 서비스 이름, 서비스 토폴로지 이름 및 ResourceGroup이 $serviceUnitObject의 Name, ServiceName, ServiceTopologyName 및 ResourceGroupName 속성과 각각 일치 하는 서비스 단위를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="b012a-123">변수</span><span class="sxs-lookup"><span data-stu-id="b012a-123">PARAMETERS</span></span>

### <span data-ttu-id="b012a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b012a-124">-DefaultProfile</span></span>
<span data-ttu-id="b012a-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b012a-126">-Force</span><span class="sxs-lookup"><span data-stu-id="b012a-126">-Force</span></span>
<span data-ttu-id="b012a-127">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b012a-128">-이름</span><span class="sxs-lookup"><span data-stu-id="b012a-128">-Name</span></span>
<span data-ttu-id="b012a-129">삭제할 서비스 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-129">The name of the service unit to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b012a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b012a-130">-PassThru</span></span>
<span data-ttu-id="b012a-131">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="b012a-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b012a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b012a-132">-ResourceGroupName</span></span>
<span data-ttu-id="b012a-133">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="b012a-133">The resource group.</span></span>

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

### <span data-ttu-id="b012a-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b012a-134">-ResourceId</span></span>
<span data-ttu-id="b012a-135">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-135">The resource identifier.</span></span>

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

### <span data-ttu-id="b012a-136">-서비스</span><span class="sxs-lookup"><span data-stu-id="b012a-136">-Service</span></span>
<span data-ttu-id="b012a-137">서비스 단위를 만들 서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-137">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="b012a-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b012a-138">-ServiceName</span></span>
<span data-ttu-id="b012a-139">서비스 단위가 속한 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-139">The name of the service the service unit belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b012a-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="b012a-140">-ServiceResourceId</span></span>
<span data-ttu-id="b012a-141">서비스 단위를 만들 서비스 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-141">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="b012a-142">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="b012a-142">-ServiceTopology</span></span>
<span data-ttu-id="b012a-143">서비스 단위를 만들 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-143">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="b012a-144">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="b012a-144">-ServiceTopologyName</span></span>
<span data-ttu-id="b012a-145">서비스 장치가 속한 서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-145">The name of the service topology the service unit belongs to.</span></span>

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

### <span data-ttu-id="b012a-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="b012a-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="b012a-147">서비스 단위를 만들 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-147">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="b012a-148">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b012a-148">-ServiceUnit</span></span>
<span data-ttu-id="b012a-149">제거할 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-149">The resource to be removed.</span></span>

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

### <span data-ttu-id="b012a-150">-확인</span><span class="sxs-lookup"><span data-stu-id="b012a-150">-Confirm</span></span>
<span data-ttu-id="b012a-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b012a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b012a-152">-WhatIf</span></span>
<span data-ttu-id="b012a-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b012a-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b012a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b012a-155">CommonParameters</span></span>
<span data-ttu-id="b012a-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b012a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b012a-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b012a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b012a-158">입력</span><span class="sxs-lookup"><span data-stu-id="b012a-158">INPUTS</span></span>

### <span data-ttu-id="b012a-159">Microsoft. Azure. Psservicemanager 리소스</span><span class="sxs-lookup"><span data-stu-id="b012a-159">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="b012a-160">출력</span><span class="sxs-lookup"><span data-stu-id="b012a-160">OUTPUTS</span></span>

### <span data-ttu-id="b012a-161">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b012a-161">System.Boolean</span></span>

## <span data-ttu-id="b012a-162">상속자</span><span class="sxs-lookup"><span data-stu-id="b012a-162">NOTES</span></span>

## <span data-ttu-id="b012a-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b012a-163">RELATED LINKS</span></span>

[<span data-ttu-id="b012a-164">새로운 AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b012a-164">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="b012a-165">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b012a-165">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="b012a-166">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="b012a-166">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)