---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 607e094a03d43704057af80266a6f9f2b669d3b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696665"
---
# <span data-ttu-id="76fa0-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="76fa0-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="76fa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="76fa0-103">서비스 단위를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-103">Gets the service unit.</span></span>

## <span data-ttu-id="76fa0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="76fa0-104">SYNTAX</span></span>

### <span data-ttu-id="76fa0-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="76fa0-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fa0-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="76fa0-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fa0-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="76fa0-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> [-ServiceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fa0-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="76fa0-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76fa0-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="76fa0-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76fa0-110">리소스</span><span class="sxs-lookup"><span data-stu-id="76fa0-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="76fa0-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="76fa0-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ServiceUnitObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76fa0-112">설명은</span><span class="sxs-lookup"><span data-stu-id="76fa0-112">DESCRIPTION</span></span>
<span data-ttu-id="76fa0-113">**Get-AzDeploymentManagerServiceUnit** cmdlet은 서비스에서 서비스 단위를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="76fa0-114">서비스 단위를 이름, 정의 된 서비스, 서비스 토폴로지 이름 및 리소스 그룹 이름을 기준으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="76fa0-115">또는 ServiceUnit 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="76fa0-116">이 개체를 로컬로 수정한 다음 Set-AzDeploymentManagerServiceUnit cmdlet을 사용 하 여 서비스 단위에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="76fa0-117">예제의</span><span class="sxs-lookup"><span data-stu-id="76fa0-117">EXAMPLES</span></span>

### <span data-ttu-id="76fa0-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="76fa0-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="76fa0-119">이 명령은 ContosoResourceGroup에서 ContosoServiceTopology 이라는 서비스 토폴로지의 서비스 ContosoService1 아래에 ContosoService1Storage 이라는 서비스 단위를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="76fa0-120">예제 2: 리소스 식별자를 사용 하 여 서비스 단위 가져오기</span><span class="sxs-lookup"><span data-stu-id="76fa0-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="76fa0-121">이 명령은 ContosoResourceGroup에서 ContosoServiceTopology 이라는 서비스 토폴로지의 서비스 ContosoService1 아래에 ContosoService1Storage 이라는 서비스 단위를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="76fa0-122">예제 3: 서비스 단위 개체를 사용 하 여 서비스 단위 가져오기</span><span class="sxs-lookup"><span data-stu-id="76fa0-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="76fa0-123">이 명령은 이름, 서비스 이름, 서비스 토폴로지 이름 및 ResourceGroup이 $serviceUnitObject의 Name, ServiceName, ServiceTopologyName 및 ResourceGroupName 속성과 각각 일치 하는 서비스 단위를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="76fa0-124">변수</span><span class="sxs-lookup"><span data-stu-id="76fa0-124">PARAMETERS</span></span>

### <span data-ttu-id="76fa0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76fa0-125">-DefaultProfile</span></span>
<span data-ttu-id="76fa0-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76fa0-127">-이름</span><span class="sxs-lookup"><span data-stu-id="76fa0-127">-Name</span></span>
<span data-ttu-id="76fa0-128">서비스 단위의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-128">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fa0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76fa0-129">-ResourceGroupName</span></span>
<span data-ttu-id="76fa0-130">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="76fa0-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fa0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76fa0-131">-ResourceId</span></span>
<span data-ttu-id="76fa0-132">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-132">The resource identifier.</span></span>

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

### <span data-ttu-id="76fa0-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="76fa0-133">-ServiceName</span></span>
<span data-ttu-id="76fa0-134">서비스 단위를 포함 하는 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-134">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="76fa0-135">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="76fa0-135">-ServiceObject</span></span>
<span data-ttu-id="76fa0-136">서비스 단위를 만들 서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-136">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="76fa0-137">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="76fa0-137">-ServiceResourceId</span></span>
<span data-ttu-id="76fa0-138">서비스 단위를 만들 서비스 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-138">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="76fa0-139">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="76fa0-139">-ServiceTopologyName</span></span>
<span data-ttu-id="76fa0-140">서비스 단위를 포함 하는 서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-140">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="76fa0-141">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="76fa0-141">-ServiceTopologyObject</span></span>
<span data-ttu-id="76fa0-142">서비스 단위를 만들 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-142">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="76fa0-143">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="76fa0-143">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="76fa0-144">서비스 단위를 만들 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-144">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="76fa0-145">-Service사업부 개체</span><span class="sxs-lookup"><span data-stu-id="76fa0-145">-ServiceUnitObject</span></span>
<span data-ttu-id="76fa0-146">서비스 단위 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-146">Service unit resource object.</span></span>

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

### <span data-ttu-id="76fa0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76fa0-147">CommonParameters</span></span>
<span data-ttu-id="76fa0-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="76fa0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76fa0-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76fa0-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76fa0-150">입력</span><span class="sxs-lookup"><span data-stu-id="76fa0-150">INPUTS</span></span>

### <span data-ttu-id="76fa0-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="76fa0-151">System.String</span></span>

### <span data-ttu-id="76fa0-152">Microsoft. Azure. Psservicemanager 리소스</span><span class="sxs-lookup"><span data-stu-id="76fa0-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="76fa0-153">출력</span><span class="sxs-lookup"><span data-stu-id="76fa0-153">OUTPUTS</span></span>

### <span data-ttu-id="76fa0-154">Microsoft. Azure. Psservicemanager 리소스</span><span class="sxs-lookup"><span data-stu-id="76fa0-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="76fa0-155">상속자</span><span class="sxs-lookup"><span data-stu-id="76fa0-155">NOTES</span></span>

## <span data-ttu-id="76fa0-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76fa0-156">RELATED LINKS</span></span>
