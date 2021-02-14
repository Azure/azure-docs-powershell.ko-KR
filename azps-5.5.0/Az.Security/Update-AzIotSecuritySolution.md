---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Update-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
ms.openlocfilehash: ba84bccc92b58b7f8a21812e2f1599bbc9679d38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201772"
---
# <span data-ttu-id="daf7b-101">Update-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="daf7b-101">Update-AzIotSecuritySolution</span></span>

## <span data-ttu-id="daf7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daf7b-102">SYNOPSIS</span></span>
<span data-ttu-id="daf7b-103">IoT 보안 솔루션에서 하나 이상의 속성 업데이트: 태그, 권장 사항 구성, 사용자 정의 리소스</span><span class="sxs-lookup"><span data-stu-id="daf7b-103">Update one or more of the following properties in IoT security solution: tags, recommendation configuration, user defined resources</span></span>

## <span data-ttu-id="daf7b-104">구문</span><span class="sxs-lookup"><span data-stu-id="daf7b-104">SYNTAX</span></span>

### <span data-ttu-id="daf7b-105">ResourceGroupLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="daf7b-105">ResourceGroupLevelResource (Default)</span></span>
```
Update-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daf7b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="daf7b-106">ResourceId</span></span>
```
Update-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daf7b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="daf7b-107">InputObject</span></span>
```
Update-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daf7b-108">설명</span><span class="sxs-lookup"><span data-stu-id="daf7b-108">DESCRIPTION</span></span>
<span data-ttu-id="daf7b-109">이 Update-AzIotSecuritySolution cmdlet은 태그, 권장 사항 구성, 사용자 정의 리소스와 같은 특정 IoT 보안 솔루션에서 하나 이상의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="daf7b-109">The Update-AzIotSecuritySolution cmdlet updayes one or more of the following properties in a specific IoT security solution: tags, recommendation configuration, user defined resources.</span></span>
<span data-ttu-id="daf7b-110">지정된 속성만 iot 보안 솔루션 내에서 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="daf7b-110">Only the specified properties will be updated inside the iot security solution.</span></span>
<span data-ttu-id="daf7b-111">IoT 보안 솔루션은 위협을 방지하고 검색할 수 있도록 IoT 디바이스 및 IoT Hub에서 보안 데이터 및 이벤트를 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="daf7b-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="daf7b-112">예제</span><span class="sxs-lookup"><span data-stu-id="daf7b-112">EXAMPLES</span></span>

### <span data-ttu-id="daf7b-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="daf7b-113">Example 1</span></span>
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

<span data-ttu-id="daf7b-114">권장 구성 및 사용자 정의 리소스로 리소스 그룹 "MyResourceGroup"에서 iot 보안 솔루션 "MySample"을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="daf7b-114">Update iot security solution "MySample" from resource group "MyResourceGroup" with recommendation configuration and user defined resources</span></span>

## <span data-ttu-id="daf7b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="daf7b-115">PARAMETERS</span></span>

### <span data-ttu-id="daf7b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf7b-116">-DefaultProfile</span></span>
<span data-ttu-id="daf7b-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="daf7b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daf7b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="daf7b-118">-InputObject</span></span>
<span data-ttu-id="daf7b-119">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="daf7b-119">Input Object.</span></span>

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

### <span data-ttu-id="daf7b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="daf7b-120">-Name</span></span>
<span data-ttu-id="daf7b-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="daf7b-121">Resource name.</span></span>

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

### <span data-ttu-id="daf7b-122">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="daf7b-122">-RecommendationsConfiguration</span></span>
<span data-ttu-id="daf7b-123">권장 사항 구성.</span><span class="sxs-lookup"><span data-stu-id="daf7b-123">Recommendations configuration.</span></span>

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

### <span data-ttu-id="daf7b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daf7b-124">-ResourceGroupName</span></span>
<span data-ttu-id="daf7b-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="daf7b-125">Resource group name.</span></span>

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

### <span data-ttu-id="daf7b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="daf7b-126">-ResourceId</span></span>
<span data-ttu-id="daf7b-127">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="daf7b-127">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="daf7b-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="daf7b-128">-Tag</span></span>
<span data-ttu-id="daf7b-129">태그.</span><span class="sxs-lookup"><span data-stu-id="daf7b-129">Tags.</span></span>

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

### <span data-ttu-id="daf7b-130">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="daf7b-130">-UserDefinedResource</span></span>
<span data-ttu-id="daf7b-131">사용자 정의 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="daf7b-131">User defined resources.</span></span>

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

### <span data-ttu-id="daf7b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="daf7b-132">-Confirm</span></span>
<span data-ttu-id="daf7b-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="daf7b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daf7b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daf7b-134">-WhatIf</span></span>
<span data-ttu-id="daf7b-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="daf7b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daf7b-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="daf7b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daf7b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf7b-137">CommonParameters</span></span>
<span data-ttu-id="daf7b-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="daf7b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf7b-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="daf7b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf7b-140">입력</span><span class="sxs-lookup"><span data-stu-id="daf7b-140">INPUTS</span></span>

### <span data-ttu-id="daf7b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="daf7b-141">System.String</span></span>

### <span data-ttu-id="daf7b-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="daf7b-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="daf7b-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="daf7b-143">System.Collections.Hashtable</span></span>

### <span data-ttu-id="daf7b-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="daf7b-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="daf7b-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="daf7b-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="daf7b-146">출력</span><span class="sxs-lookup"><span data-stu-id="daf7b-146">OUTPUTS</span></span>

### <span data-ttu-id="daf7b-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="daf7b-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="daf7b-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="daf7b-148">NOTES</span></span>

## <span data-ttu-id="daf7b-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="daf7b-149">RELATED LINKS</span></span>
