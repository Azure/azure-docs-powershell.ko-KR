---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 30b6979be7f3aae23bec5d1ca45d48d4dd2290f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208253"
---
# <span data-ttu-id="d2e19-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d2e19-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="d2e19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2e19-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e19-103">IoT 보안 솔루션 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="d2e19-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="d2e19-104">구문</span><span class="sxs-lookup"><span data-stu-id="d2e19-104">SYNTAX</span></span>

### <span data-ttu-id="d2e19-105">ResourceGroupLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="d2e19-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2e19-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d2e19-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2e19-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2e19-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2e19-108">설명</span><span class="sxs-lookup"><span data-stu-id="d2e19-108">DESCRIPTION</span></span>
<span data-ttu-id="d2e19-109">이 Set-AzIotSecuritySolution cmdlet은 특정 iot 보안 솔루션을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e19-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="d2e19-110">IoT 보안 솔루션은 위협을 방지하고 검색할 수 있도록 IoT 디바이스 및 IoT Hub에서 보안 데이터 및 이벤트를 수집합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e19-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="d2e19-111">iot 보안 솔루션의 이름은 iot 허브의 이름과 동일해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e19-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="d2e19-112">예제</span><span class="sxs-lookup"><span data-stu-id="d2e19-112">EXAMPLES</span></span>

### <span data-ttu-id="d2e19-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="d2e19-113">Example 1</span></span>
```powershell
PS C:\> $Workspace = "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.OperationalInsights/workspaces/IoTHubWorkspace"
PS C:\> $IotHubs = @("/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample")
PS C:\> Set-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -Location "West US" 
-Workspace $Workspace -DisplayName "MySample" -Enabled $true -IotHub $IotHubs

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
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="d2e19-114">리소스 ID "/subscriptions/XXXXXXXX-XXXXX-XXXXX-XXXXX-XXXXX-XXXXXXXXXX"를 사용하여 IoT Hub용 새 IoT Hub용 IoT Hub용 "MySample" 보안 솔루션 만들기XXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (솔루션의 이름은 IoT Hub의 이름과 동일해야 합니다.)</span><span class="sxs-lookup"><span data-stu-id="d2e19-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="d2e19-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2e19-115">PARAMETERS</span></span>

### <span data-ttu-id="d2e19-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e19-116">-DefaultProfile</span></span>
<span data-ttu-id="d2e19-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e19-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2e19-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="d2e19-118">-DisabledDataSource</span></span>
<span data-ttu-id="d2e19-119">비활성화된 데이터 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e19-119">Disabled data sources.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e19-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d2e19-120">-DisplayName</span></span>
<span data-ttu-id="d2e19-121">표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e19-121">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e19-122">-Enabled</span><span class="sxs-lookup"><span data-stu-id="d2e19-122">-Enabled</span></span>
<span data-ttu-id="d2e19-123">상태.</span><span class="sxs-lookup"><span data-stu-id="d2e19-123">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e19-124">-Export</span><span class="sxs-lookup"><span data-stu-id="d2e19-124">-Export</span></span>
<span data-ttu-id="d2e19-125">데이터를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2e19-125">Export data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e19-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2e19-126">-InputObject</span></span>
<span data-ttu-id="d2e19-127">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e19-127">Input Object.</span></span>

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

### <span data-ttu-id="d2e19-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="d2e19-128">-IotHub</span></span>
<span data-ttu-id="d2e19-129">Iot Hubs.</span><span class="sxs-lookup"><span data-stu-id="d2e19-129">Iot hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e19-130">-Location</span><span class="sxs-lookup"><span data-stu-id="d2e19-130">-Location</span></span>
<span data-ttu-id="d2e19-131">위치.</span><span class="sxs-lookup"><span data-stu-id="d2e19-131">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e19-132">-Name</span><span class="sxs-lookup"><span data-stu-id="d2e19-132">-Name</span></span>
<span data-ttu-id="d2e19-133">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e19-133">Resource name.</span></span>

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

### <span data-ttu-id="d2e19-134">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2e19-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="d2e19-135">권장 사항 구성.</span><span class="sxs-lookup"><span data-stu-id="d2e19-135">Recommendations configuration.</span></span>

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

### <span data-ttu-id="d2e19-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e19-136">-ResourceGroupName</span></span>
<span data-ttu-id="d2e19-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e19-137">Resource group name.</span></span>

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

### <span data-ttu-id="d2e19-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2e19-138">-ResourceId</span></span>
<span data-ttu-id="d2e19-139">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e19-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="d2e19-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="d2e19-140">-Tag</span></span>
<span data-ttu-id="d2e19-141">태그.</span><span class="sxs-lookup"><span data-stu-id="d2e19-141">Tags.</span></span>

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

### <span data-ttu-id="d2e19-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="d2e19-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="d2e19-143">마스킹되지 않은 IP 로깅 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e19-143">Unmasked ip logging status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e19-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="d2e19-144">-UserDefinedResource</span></span>
<span data-ttu-id="d2e19-145">사용자 정의 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e19-145">User defined resources.</span></span>

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

### <span data-ttu-id="d2e19-146">-Workspace</span><span class="sxs-lookup"><span data-stu-id="d2e19-146">-Workspace</span></span>
<span data-ttu-id="d2e19-147">작업 영역 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d2e19-147">Workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e19-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2e19-148">-Confirm</span></span>
<span data-ttu-id="d2e19-149">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2e19-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2e19-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2e19-150">-WhatIf</span></span>
<span data-ttu-id="d2e19-151">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d2e19-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2e19-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2e19-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2e19-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e19-153">CommonParameters</span></span>
<span data-ttu-id="d2e19-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d2e19-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e19-155">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d2e19-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e19-156">입력</span><span class="sxs-lookup"><span data-stu-id="d2e19-156">INPUTS</span></span>

### <span data-ttu-id="d2e19-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d2e19-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="d2e19-158">System.String</span><span class="sxs-lookup"><span data-stu-id="d2e19-158">System.String</span></span>

### <span data-ttu-id="d2e19-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d2e19-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d2e19-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d2e19-160">System.String[]</span></span>

### <span data-ttu-id="d2e19-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="d2e19-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="d2e19-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="d2e19-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="d2e19-163">출력</span><span class="sxs-lookup"><span data-stu-id="d2e19-163">OUTPUTS</span></span>

### <span data-ttu-id="d2e19-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d2e19-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="d2e19-165">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d2e19-165">NOTES</span></span>

## <span data-ttu-id="d2e19-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2e19-166">RELATED LINKS</span></span>
