---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: aec721a3676a6b4510c7fe0eccf5badc4f9ccce2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304973"
---
# <span data-ttu-id="6a5a8-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="6a5a8-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="6a5a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a5a8-102">SYNOPSIS</span></span>
<span data-ttu-id="6a5a8-103">지정 된 서비스 토폴로지 아래에 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="6a5a8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6a5a8-104">SYNTAX</span></span>

### <span data-ttu-id="6a5a8-105">대화형 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6a5a8-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a5a8-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="6a5a8-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a5a8-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="6a5a8-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a5a8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6a5a8-108">DESCRIPTION</span></span>
<span data-ttu-id="6a5a8-109">**AzDeploymentManagerService** cmdlet은 서비스 토폴로지 아래에 서비스를 만들고 해당 서비스를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="6a5a8-110">서비스를 이름, 서비스 토폴로지, 그리고 리소스 그룹 이름으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="6a5a8-111">Cmdlet은 서비스 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="6a5a8-112">이 개체를 로컬로 수정한 다음 Set-AzDeploymentManagerService cmdlet을 사용 하 여 서비스에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="6a5a8-113">예제의</span><span class="sxs-lookup"><span data-stu-id="6a5a8-113">EXAMPLES</span></span>

### <span data-ttu-id="6a5a8-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="6a5a8-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="6a5a8-115">중앙 미국에 있는 리소스 그룹 ContosoResourceGroup의 서비스 토폴로지 ContosoServiceTopology에서 이름이 ContosoService1 인 새 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="6a5a8-116">TargetLocation 속성은 서비스 ContosoService1 지정 된 구독의 동부 US 지역에 배포 되어야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="6a5a8-117">변수</span><span class="sxs-lookup"><span data-stu-id="6a5a8-117">PARAMETERS</span></span>

### <span data-ttu-id="6a5a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a5a8-118">-DefaultProfile</span></span>
<span data-ttu-id="6a5a8-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a5a8-120">-위치</span><span class="sxs-lookup"><span data-stu-id="6a5a8-120">-Location</span></span>
<span data-ttu-id="6a5a8-121">서비스 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-121">The location of the service resource.</span></span>

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

### <span data-ttu-id="6a5a8-122">-이름</span><span class="sxs-lookup"><span data-stu-id="6a5a8-122">-Name</span></span>
<span data-ttu-id="6a5a8-123">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-123">The name of the service.</span></span>

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

### <span data-ttu-id="6a5a8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a5a8-124">-ResourceGroupName</span></span>
<span data-ttu-id="6a5a8-125">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="6a5a8-125">The resource group.</span></span>

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

### <span data-ttu-id="6a5a8-126">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="6a5a8-126">-ServiceTopologyId</span></span>
<span data-ttu-id="6a5a8-127">서비스를 만들어야 하는 서비스 토폴로지 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-127">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="6a5a8-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="6a5a8-128">-ServiceTopologyName</span></span>
<span data-ttu-id="6a5a8-129">이 서비스가 속한 서비스 토폴로지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-129">The name of the service topology this service belongs to.</span></span>

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

### <span data-ttu-id="6a5a8-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="6a5a8-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="6a5a8-131">서비스를 만들어야 하는 서비스 토폴로지 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-131">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="6a5a8-132">태그</span><span class="sxs-lookup"><span data-stu-id="6a5a8-132">-Tag</span></span>
<span data-ttu-id="6a5a8-133">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="6a5a8-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="6a5a8-134">-TargetLocation</span></span>
<span data-ttu-id="6a5a8-135">서비스의 리소스가 배포 되는 위치를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-135">Determines the location where resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="6a5a8-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a5a8-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="6a5a8-137">서비스에 속한 리소스가 배포 되는 구독을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="6a5a8-138">-확인</span><span class="sxs-lookup"><span data-stu-id="6a5a8-138">-Confirm</span></span>
<span data-ttu-id="6a5a8-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a5a8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a5a8-140">-WhatIf</span></span>
<span data-ttu-id="6a5a8-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a5a8-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a5a8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a5a8-143">CommonParameters</span></span>
<span data-ttu-id="6a5a8-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a5a8-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6a5a8-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a5a8-146">입력</span><span class="sxs-lookup"><span data-stu-id="6a5a8-146">INPUTS</span></span>

### <span data-ttu-id="6a5a8-147">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="6a5a8-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6a5a8-148">출력</span><span class="sxs-lookup"><span data-stu-id="6a5a8-148">OUTPUTS</span></span>

### <span data-ttu-id="6a5a8-149">Microsoft. Azure. PSServiceResource 명령)</span><span class="sxs-lookup"><span data-stu-id="6a5a8-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="6a5a8-150">상속자</span><span class="sxs-lookup"><span data-stu-id="6a5a8-150">NOTES</span></span>

## <span data-ttu-id="6a5a8-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a5a8-151">RELATED LINKS</span></span>
