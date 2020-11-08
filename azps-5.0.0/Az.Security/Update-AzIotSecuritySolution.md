---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Update-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
ms.openlocfilehash: ba84bccc92b58b7f8a21812e2f1599bbc9679d38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216180"
---
# <span data-ttu-id="69bf3-101">Update-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="69bf3-101">Update-AzIotSecuritySolution</span></span>

## <span data-ttu-id="69bf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="69bf3-103">IoT security 솔루션에서 다음 속성 중 하나 이상을 업데이트: 태그, 권장 구성, 사용자 정의 리소스</span><span class="sxs-lookup"><span data-stu-id="69bf3-103">Update one or more of the following properties in IoT security solution: tags, recommendation configuration, user defined resources</span></span>

## <span data-ttu-id="69bf3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69bf3-104">SYNTAX</span></span>

### <span data-ttu-id="69bf3-105">ResourceGroupLevelResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="69bf3-105">ResourceGroupLevelResource (Default)</span></span>
```
Update-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69bf3-106">리소스</span><span class="sxs-lookup"><span data-stu-id="69bf3-106">ResourceId</span></span>
```
Update-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69bf3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="69bf3-107">InputObject</span></span>
```
Update-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69bf3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="69bf3-108">DESCRIPTION</span></span>
<span data-ttu-id="69bf3-109">특정 IoT 보안 솔루션에서 Update-AzIotSecuritySolution cmdlet updayes는 태그, 권장 구성, 사용자 정의 리소스 중 하나 이상을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="69bf3-109">The Update-AzIotSecuritySolution cmdlet updayes one or more of the following properties in a specific IoT security solution: tags, recommendation configuration, user defined resources.</span></span>
<span data-ttu-id="69bf3-110">지정 된 속성만 iot security 솔루션 내에서 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="69bf3-110">Only the specified properties will be updated inside the iot security solution.</span></span>
<span data-ttu-id="69bf3-111">IoT security 솔루션은 iot 디바이스 및 iot hub의 보안 데이터 및 이벤트를 수집 하 여 위협을 방지 하 고 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="69bf3-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="69bf3-112">예제의</span><span class="sxs-lookup"><span data-stu-id="69bf3-112">EXAMPLES</span></span>

### <span data-ttu-id="69bf3-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="69bf3-113">Example 1</span></span>
```powershell
PS C:\> $RecConfig = New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_OpenPorts" -Enabled $false
PS C:\> $UserDefinedResource = New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")   
PS C:\> Update-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -RecommendationsConfiguration @($RecConfig) -UserDefinedResource $UserDefinedResource

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "westus"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
    QuerySubscriptions: ["XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"]
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_OpenPorts"
    Name: "Device has open port"
    Status: "Disabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
}]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
```

<span data-ttu-id="69bf3-114">권장 구성 및 사용자 정의 리소스를 사용 하 여 "MyResourceGroup" 리소스 그룹에서 iot security 솔루션 "MySample"을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="69bf3-114">Update iot security solution "MySample" from resource group "MyResourceGroup" with recommendation configuration and user defined resources</span></span>

## <span data-ttu-id="69bf3-115">변수</span><span class="sxs-lookup"><span data-stu-id="69bf3-115">PARAMETERS</span></span>

### <span data-ttu-id="69bf3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69bf3-116">-DefaultProfile</span></span>
<span data-ttu-id="69bf3-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69bf3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69bf3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69bf3-118">-InputObject</span></span>
<span data-ttu-id="69bf3-119">입력 개체</span><span class="sxs-lookup"><span data-stu-id="69bf3-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69bf3-120">-이름</span><span class="sxs-lookup"><span data-stu-id="69bf3-120">-Name</span></span>
<span data-ttu-id="69bf3-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69bf3-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bf3-122">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="69bf3-122">-RecommendationsConfiguration</span></span>
<span data-ttu-id="69bf3-123">권장 구성.</span><span class="sxs-lookup"><span data-stu-id="69bf3-123">Recommendations configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bf3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69bf3-124">-ResourceGroupName</span></span>
<span data-ttu-id="69bf3-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69bf3-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bf3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69bf3-126">-ResourceId</span></span>
<span data-ttu-id="69bf3-127">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="69bf3-127">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69bf3-128">태그</span><span class="sxs-lookup"><span data-stu-id="69bf3-128">-Tag</span></span>
<span data-ttu-id="69bf3-129">태그도.</span><span class="sxs-lookup"><span data-stu-id="69bf3-129">Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bf3-130">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="69bf3-130">-UserDefinedResource</span></span>
<span data-ttu-id="69bf3-131">사용자가 정의한 리소스.</span><span class="sxs-lookup"><span data-stu-id="69bf3-131">User defined resources.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bf3-132">-확인</span><span class="sxs-lookup"><span data-stu-id="69bf3-132">-Confirm</span></span>
<span data-ttu-id="69bf3-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="69bf3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69bf3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69bf3-134">-WhatIf</span></span>
<span data-ttu-id="69bf3-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="69bf3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69bf3-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69bf3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69bf3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69bf3-137">CommonParameters</span></span>
<span data-ttu-id="69bf3-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69bf3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69bf3-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69bf3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69bf3-140">입력</span><span class="sxs-lookup"><span data-stu-id="69bf3-140">INPUTS</span></span>

### <span data-ttu-id="69bf3-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="69bf3-141">System.String</span></span>

### <span data-ttu-id="69bf3-142">Microsoft. Azure. .Prootsecuritysecuritysolutions 솔루션.</span><span class="sxs-lookup"><span data-stu-id="69bf3-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="69bf3-143">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="69bf3-143">System.Collections.Hashtable</span></span>

### <span data-ttu-id="69bf3-144">Microsoft. Azure. IPSUserDefinedResources Securitysolutions.</span><span class="sxs-lookup"><span data-stu-id="69bf3-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="69bf3-145">PSRecommendationConfiguration []-IotSecuritySolutions을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69bf3-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="69bf3-146">출력</span><span class="sxs-lookup"><span data-stu-id="69bf3-146">OUTPUTS</span></span>

### <span data-ttu-id="69bf3-147">Microsoft. Azure. .Prootsecuritysecuritysolutions 솔루션.</span><span class="sxs-lookup"><span data-stu-id="69bf3-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="69bf3-148">상속자</span><span class="sxs-lookup"><span data-stu-id="69bf3-148">NOTES</span></span>

## <span data-ttu-id="69bf3-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69bf3-149">RELATED LINKS</span></span>
