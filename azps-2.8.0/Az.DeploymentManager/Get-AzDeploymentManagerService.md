---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: 3dda11ec4fddde67a3ae4300f884290831ac28ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696672"
---
# <span data-ttu-id="3f155-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="3f155-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="3f155-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f155-102">SYNOPSIS</span></span>
<span data-ttu-id="3f155-103">서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3f155-103">Gets the service.</span></span>

## <span data-ttu-id="3f155-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f155-104">SYNTAX</span></span>

### <span data-ttu-id="3f155-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3f155-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f155-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="3f155-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f155-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="3f155-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f155-108">리소스</span><span class="sxs-lookup"><span data-stu-id="3f155-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f155-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="3f155-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f155-110">설명은</span><span class="sxs-lookup"><span data-stu-id="3f155-110">DESCRIPTION</span></span>
<span data-ttu-id="3f155-111">**AzDeploymentManagerService** cmdlet은 서비스 토폴로지에서 서비스를 가져오고 해당 서비스를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f155-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="3f155-112">서비스를 이름, 서비스 토폴로지, 그리고 리소스 그룹 이름으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f155-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="3f155-113">또는 서비스 개체 또는 ResourceId를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3f155-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="3f155-114">이 개체를 로컬로 수정한 다음 Set-AzDeploymentManagerService cmdlet을 사용 하 여 서비스에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3f155-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="3f155-115">예제의</span><span class="sxs-lookup"><span data-stu-id="3f155-115">EXAMPLES</span></span>

### <span data-ttu-id="3f155-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="3f155-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="3f155-117">이 명령은 ContosoResourceGroup의 ContosoServiceTopology 라는 서비스 토폴로지에서 ContosoService1 이라는 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3f155-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="3f155-118">예제 2: 리소스 식별자를 사용 하 여 서비스 가져오기</span><span class="sxs-lookup"><span data-stu-id="3f155-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="3f155-119">이 명령은 ContosoResourceGroup의 ContosoServiceTopology 라는 서비스 토폴로지에서 ContosoService1 이라는 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3f155-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="3f155-120">예제 3: 서비스 개체를 사용 하 여 서비스 가져오기</span><span class="sxs-lookup"><span data-stu-id="3f155-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="3f155-121">이 명령은 이름, 서비스 토폴로지 이름 및 ResourceGroup이 $serviceObject의 Name, ServiceTopologyName 및 ResourceGroupName 속성과 각각 일치 하는 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3f155-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="3f155-122">변수</span><span class="sxs-lookup"><span data-stu-id="3f155-122">PARAMETERS</span></span>

### <span data-ttu-id="3f155-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f155-123">-DefaultProfile</span></span>
<span data-ttu-id="3f155-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f155-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f155-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f155-125">-InputObject</span></span>
<span data-ttu-id="3f155-126">서비스 개체.</span><span class="sxs-lookup"><span data-stu-id="3f155-126">Service object.</span></span>

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

### <span data-ttu-id="3f155-127">-이름</span><span class="sxs-lookup"><span data-stu-id="3f155-127">-Name</span></span>
<span data-ttu-id="3f155-128">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f155-128">The name of the service.</span></span>

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

### <span data-ttu-id="3f155-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f155-129">-ResourceGroupName</span></span>
<span data-ttu-id="3f155-130">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="3f155-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f155-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f155-131">-ResourceId</span></span>
<span data-ttu-id="3f155-132">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3f155-132">The resource identifier.</span></span>

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

### <span data-ttu-id="3f155-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="3f155-133">-ServiceTopologyName</span></span>
<span data-ttu-id="3f155-134">서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f155-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="3f155-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="3f155-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="3f155-136">서비스를 만들어야 하는 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3f155-136">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="3f155-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="3f155-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="3f155-138">서비스를 만들어야 하는 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3f155-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="3f155-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f155-139">CommonParameters</span></span>
<span data-ttu-id="3f155-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f155-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f155-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f155-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f155-142">입력</span><span class="sxs-lookup"><span data-stu-id="3f155-142">INPUTS</span></span>

### <span data-ttu-id="3f155-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3f155-143">System.String</span></span>

### <span data-ttu-id="3f155-144">Microsoft. Azure. PSServiceResource 명령)</span><span class="sxs-lookup"><span data-stu-id="3f155-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="3f155-145">출력</span><span class="sxs-lookup"><span data-stu-id="3f155-145">OUTPUTS</span></span>

### <span data-ttu-id="3f155-146">Microsoft. Azure. PSServiceResource 명령)</span><span class="sxs-lookup"><span data-stu-id="3f155-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="3f155-147">상속자</span><span class="sxs-lookup"><span data-stu-id="3f155-147">NOTES</span></span>

## <span data-ttu-id="3f155-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f155-148">RELATED LINKS</span></span>
