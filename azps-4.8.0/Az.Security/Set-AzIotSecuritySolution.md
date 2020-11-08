---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 30b6979be7f3aae23bec5d1ca45d48d4dd2290f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204353"
---
# <span data-ttu-id="ae0d3-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="ae0d3-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="ae0d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae0d3-102">SYNOPSIS</span></span>
<span data-ttu-id="ae0d3-103">IoT security 솔루션 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="ae0d3-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="ae0d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae0d3-104">SYNTAX</span></span>

### <span data-ttu-id="ae0d3-105">ResourceGroupLevelResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="ae0d3-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae0d3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ae0d3-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae0d3-107">리소스</span><span class="sxs-lookup"><span data-stu-id="ae0d3-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae0d3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ae0d3-108">DESCRIPTION</span></span>
<span data-ttu-id="ae0d3-109">Set-AzIotSecuritySolution cmdlet은 특정 iot 보안 솔루션을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="ae0d3-110">IoT security 솔루션은 iot 디바이스 및 iot hub의 보안 데이터 및 이벤트를 수집 하 여 위협을 방지 하 고 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="ae0d3-111">Iot 보안 솔루션의 이름은 iot hub의 이름과 동일 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="ae0d3-112">예제의</span><span class="sxs-lookup"><span data-stu-id="ae0d3-112">EXAMPLES</span></span>

### <span data-ttu-id="ae0d3-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="ae0d3-113">Example 1</span></span>
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

<span data-ttu-id="ae0d3-114">"/Subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" 리소스 id를 사용 하 여 IoT hub에 대 한 새 iot 보안 솔루션 "MySample" 만들기 (솔루션의 이름은 IoT hub의 이름과 동일 해야 합니다.)</span><span class="sxs-lookup"><span data-stu-id="ae0d3-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="ae0d3-115">변수</span><span class="sxs-lookup"><span data-stu-id="ae0d3-115">PARAMETERS</span></span>

### <span data-ttu-id="ae0d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae0d3-116">-DefaultProfile</span></span>
<span data-ttu-id="ae0d3-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae0d3-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="ae0d3-118">-DisabledDataSource</span></span>
<span data-ttu-id="ae0d3-119">데이터 원본을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-119">Disabled data sources.</span></span>

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

### <span data-ttu-id="ae0d3-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ae0d3-120">-DisplayName</span></span>
<span data-ttu-id="ae0d3-121">표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-121">Display name.</span></span>

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

### <span data-ttu-id="ae0d3-122">-사용</span><span class="sxs-lookup"><span data-stu-id="ae0d3-122">-Enabled</span></span>
<span data-ttu-id="ae0d3-123">상태.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-123">Status .</span></span>

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

### <span data-ttu-id="ae0d3-124">-Export</span><span class="sxs-lookup"><span data-stu-id="ae0d3-124">-Export</span></span>
<span data-ttu-id="ae0d3-125">데이터 내보내기</span><span class="sxs-lookup"><span data-stu-id="ae0d3-125">Export data.</span></span>

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

### <span data-ttu-id="ae0d3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae0d3-126">-InputObject</span></span>
<span data-ttu-id="ae0d3-127">입력 개체</span><span class="sxs-lookup"><span data-stu-id="ae0d3-127">Input Object.</span></span>

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

### <span data-ttu-id="ae0d3-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="ae0d3-128">-IotHub</span></span>
<span data-ttu-id="ae0d3-129">Iot hub.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-129">Iot hubs.</span></span>

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

### <span data-ttu-id="ae0d3-130">-위치</span><span class="sxs-lookup"><span data-stu-id="ae0d3-130">-Location</span></span>
<span data-ttu-id="ae0d3-131">Location.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-131">Location.</span></span>

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

### <span data-ttu-id="ae0d3-132">-이름</span><span class="sxs-lookup"><span data-stu-id="ae0d3-132">-Name</span></span>
<span data-ttu-id="ae0d3-133">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-133">Resource name.</span></span>

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

### <span data-ttu-id="ae0d3-134">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae0d3-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="ae0d3-135">권장 구성.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-135">Recommendations configuration.</span></span>

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

### <span data-ttu-id="ae0d3-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae0d3-136">-ResourceGroupName</span></span>
<span data-ttu-id="ae0d3-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-137">Resource group name.</span></span>

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

### <span data-ttu-id="ae0d3-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae0d3-138">-ResourceId</span></span>
<span data-ttu-id="ae0d3-139">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="ae0d3-140">태그</span><span class="sxs-lookup"><span data-stu-id="ae0d3-140">-Tag</span></span>
<span data-ttu-id="ae0d3-141">태그도.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-141">Tags.</span></span>

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

### <span data-ttu-id="ae0d3-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="ae0d3-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="ae0d3-143">마스크 되지 않은 ip 로깅 상태</span><span class="sxs-lookup"><span data-stu-id="ae0d3-143">Unmasked ip logging status.</span></span>

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

### <span data-ttu-id="ae0d3-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="ae0d3-144">-UserDefinedResource</span></span>
<span data-ttu-id="ae0d3-145">사용자가 정의한 리소스.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-145">User defined resources.</span></span>

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

### <span data-ttu-id="ae0d3-146">-작업 영역</span><span class="sxs-lookup"><span data-stu-id="ae0d3-146">-Workspace</span></span>
<span data-ttu-id="ae0d3-147">작업 영역 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-147">Workspace ID.</span></span>

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

### <span data-ttu-id="ae0d3-148">-확인</span><span class="sxs-lookup"><span data-stu-id="ae0d3-148">-Confirm</span></span>
<span data-ttu-id="ae0d3-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae0d3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae0d3-150">-WhatIf</span></span>
<span data-ttu-id="ae0d3-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae0d3-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae0d3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae0d3-153">CommonParameters</span></span>
<span data-ttu-id="ae0d3-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae0d3-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae0d3-156">입력</span><span class="sxs-lookup"><span data-stu-id="ae0d3-156">INPUTS</span></span>

### <span data-ttu-id="ae0d3-157">Microsoft. Azure. .Prootsecuritysecuritysolutions 솔루션.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="ae0d3-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ae0d3-158">System.String</span></span>

### <span data-ttu-id="ae0d3-159">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="ae0d3-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ae0d3-160">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="ae0d3-160">System.String[]</span></span>

### <span data-ttu-id="ae0d3-161">Microsoft. Azure. IPSUserDefinedResources Securitysolutions.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="ae0d3-162">PSRecommendationConfiguration []-IotSecuritySolutions을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="ae0d3-163">출력</span><span class="sxs-lookup"><span data-stu-id="ae0d3-163">OUTPUTS</span></span>

### <span data-ttu-id="ae0d3-164">Microsoft. Azure. .Prootsecuritysecuritysolutions 솔루션.</span><span class="sxs-lookup"><span data-stu-id="ae0d3-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="ae0d3-165">상속자</span><span class="sxs-lookup"><span data-stu-id="ae0d3-165">NOTES</span></span>

## <span data-ttu-id="ae0d3-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae0d3-166">RELATED LINKS</span></span>
