---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
ms.openlocfilehash: 269d333c9b74ed0e3e959ef609531bcea41b724c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208256"
---
# <span data-ttu-id="5d261-101">Set-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5d261-101">Set-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="5d261-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d261-102">SYNOPSIS</span></span>
<span data-ttu-id="5d261-103">디바이스 보안 그룹 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d261-103">Create or update device security group</span></span>

## <span data-ttu-id="5d261-104">구문</span><span class="sxs-lookup"><span data-stu-id="5d261-104">SYNTAX</span></span>

### <span data-ttu-id="5d261-105">ResourceIdLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="5d261-105">ResourceIdLevelResource (Default)</span></span>
```
Set-AzDeviceSecurityGroup -Name <String> -HubResourceId <String>
 [-ThresholdRule <PSThresholdCustomAlertRule[]>] [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>]
 [-AllowlistRule <PSAllowlistCustomAlertRule[]>] [-DenylistRule <PSDenylistCustomAlertRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d261-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5d261-106">InputObject</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -InputObject <PSDeviceSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d261-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d261-107">ResourceId</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d261-108">설명</span><span class="sxs-lookup"><span data-stu-id="5d261-108">DESCRIPTION</span></span>
<span data-ttu-id="5d261-109">이 Set-AzDeviceSecurityGroup cmdlet은 iot 보안 솔루션에 정의된 디바이스 보안 그룹을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5d261-109">The Set-AzDeviceSecurityGroup cmdlet creates or updates a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="5d261-110">예제</span><span class="sxs-lookup"><span data-stu-id="5d261-110">EXAMPLES</span></span>

### <span data-ttu-id="5d261-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5d261-111">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> $TimeWindowRule = New-AzDeviceSecurityGroupTimeWindowRuleObject -Type "ActiveConnectionsNotInAllowedRange" -Enabled $true 
-MaxThreshold 30 -MinThreshold 0 -TimeWindowSize $TimeWindowSize
PS C:\> Set-AzDeviceSecurityGroup -Name "MySecurityGroup" 
-HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 
-TimeWindowRule $TimeWindowRules

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: true
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT5M"
            }]
AllowlistRules: [
            {
              RuleType": "ConnectionToIpNotAllowed",
              DisplayName: "Outbound connection to an ip that isn't allowed"
              Description: "Get an alert when an outbound connection is created between your device and an ip that isn't allowed"
              IsEnabled: false
              ValueType: "IpCidr"
              AllowlistValues: []
            },
            {
              RuleType: "LocalUserNotAllowed"
              DisplayName: "Login by a local user that isn't allowed"
              Description: "Get an alert when a local user that isn't allowed logins to the device"
              IsEnabled: false
              ValueType: "String"
              AllowlistValues: []
            }]
DenylistRules: []
```

<span data-ttu-id="5d261-112">IoT Hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXXX-XXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"에서 규칙 유형 "ActiveConnectionsNotInAllowedRange"로 기존 디바이스 보안 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5d261-112">Update existing device security group from IoT Hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" with rule type "ActiveConnectionsNotInAllowedRange"</span></span>

## <span data-ttu-id="5d261-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d261-113">PARAMETERS</span></span>

### <span data-ttu-id="5d261-114">-AllowlistRule</span><span class="sxs-lookup"><span data-stu-id="5d261-114">-AllowlistRule</span></span>
<span data-ttu-id="5d261-115">목록 규칙을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="5d261-115">Allow list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d261-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d261-116">-DefaultProfile</span></span>
<span data-ttu-id="5d261-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d261-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d261-118">-DenylistRule</span><span class="sxs-lookup"><span data-stu-id="5d261-118">-DenylistRule</span></span>
<span data-ttu-id="5d261-119">목록 규칙을 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="5d261-119">Deny list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d261-120">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="5d261-120">-HubResourceId</span></span>
<span data-ttu-id="5d261-121">IoT Hub 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5d261-121">IoT Hub resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d261-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d261-122">-InputObject</span></span>
<span data-ttu-id="5d261-123">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5d261-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d261-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5d261-124">-Name</span></span>
<span data-ttu-id="5d261-125">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d261-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d261-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d261-126">-ResourceId</span></span>
<span data-ttu-id="5d261-127">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5d261-127">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="5d261-128">-ThresholdRule</span><span class="sxs-lookup"><span data-stu-id="5d261-128">-ThresholdRule</span></span>
<span data-ttu-id="5d261-129">임계값 규칙.</span><span class="sxs-lookup"><span data-stu-id="5d261-129">Threshold rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d261-130">-TimeWindowRule</span><span class="sxs-lookup"><span data-stu-id="5d261-130">-TimeWindowRule</span></span>
<span data-ttu-id="5d261-131">기간 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="5d261-131">Time window rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d261-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d261-132">-Confirm</span></span>
<span data-ttu-id="5d261-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d261-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d261-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d261-134">-WhatIf</span></span>
<span data-ttu-id="5d261-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5d261-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d261-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d261-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d261-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d261-137">CommonParameters</span></span>
<span data-ttu-id="5d261-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d261-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d261-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5d261-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d261-140">입력</span><span class="sxs-lookup"><span data-stu-id="5d261-140">INPUTS</span></span>

### <span data-ttu-id="5d261-141">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="5d261-141">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span></span>

### <span data-ttu-id="5d261-142">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="5d261-142">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span></span>

### <span data-ttu-id="5d261-143">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="5d261-143">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span></span>

### <span data-ttu-id="5d261-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="5d261-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]</span></span>

### <span data-ttu-id="5d261-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5d261-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="5d261-146">System.String</span><span class="sxs-lookup"><span data-stu-id="5d261-146">System.String</span></span>

## <span data-ttu-id="5d261-147">출력</span><span class="sxs-lookup"><span data-stu-id="5d261-147">OUTPUTS</span></span>

### <span data-ttu-id="5d261-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5d261-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="5d261-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5d261-149">NOTES</span></span>

## <span data-ttu-id="5d261-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d261-150">RELATED LINKS</span></span>
