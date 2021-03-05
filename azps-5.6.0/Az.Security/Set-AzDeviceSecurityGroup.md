---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
ms.openlocfilehash: 19f610cb4b17e32e88ddb85b01d6de82926b7eba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993482"
---
# <span data-ttu-id="341f4-101">Set-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="341f4-101">Set-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="341f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="341f4-102">SYNOPSIS</span></span>
<span data-ttu-id="341f4-103">디바이스 보안 그룹 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="341f4-103">Create or update device security group</span></span>

## <span data-ttu-id="341f4-104">구문</span><span class="sxs-lookup"><span data-stu-id="341f4-104">SYNTAX</span></span>

### <span data-ttu-id="341f4-105">ResourceIdLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="341f4-105">ResourceIdLevelResource (Default)</span></span>
```
Set-AzDeviceSecurityGroup -Name <String> -HubResourceId <String>
 [-ThresholdRule <PSThresholdCustomAlertRule[]>] [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>]
 [-AllowlistRule <PSAllowlistCustomAlertRule[]>] [-DenylistRule <PSDenylistCustomAlertRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="341f4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="341f4-106">InputObject</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -InputObject <PSDeviceSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="341f4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="341f4-107">ResourceId</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="341f4-108">설명</span><span class="sxs-lookup"><span data-stu-id="341f4-108">DESCRIPTION</span></span>
<span data-ttu-id="341f4-109">Set-AzDeviceSecurityGroup cmdlet은 iot 보안 솔루션에 정의된 디바이스 보안 그룹을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="341f4-109">The Set-AzDeviceSecurityGroup cmdlet creates or updates a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="341f4-110">예제</span><span class="sxs-lookup"><span data-stu-id="341f4-110">EXAMPLES</span></span>

### <span data-ttu-id="341f4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="341f4-111">Example 1</span></span>
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

<span data-ttu-id="341f4-112">규칙 형식 "ActiveConnectionsNotInAllowedRange"를 사용하여 IoT Hub "/subscriptions/XXXXXXXX-XXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/providers/Microsoft.Devices/IotHubs/MyHub"에서 기존 디바이스 보안 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="341f4-112">Update existing device security group from IoT Hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" with rule type "ActiveConnectionsNotInAllowedRange"</span></span>

## <span data-ttu-id="341f4-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="341f4-113">PARAMETERS</span></span>

### <span data-ttu-id="341f4-114">-AllowlistRule</span><span class="sxs-lookup"><span data-stu-id="341f4-114">-AllowlistRule</span></span>
<span data-ttu-id="341f4-115">목록 규칙을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="341f4-115">Allow list rules.</span></span>

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

### <span data-ttu-id="341f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="341f4-116">-DefaultProfile</span></span>
<span data-ttu-id="341f4-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="341f4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="341f4-118">-DenylistRule</span><span class="sxs-lookup"><span data-stu-id="341f4-118">-DenylistRule</span></span>
<span data-ttu-id="341f4-119">목록 규칙을 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="341f4-119">Deny list rules.</span></span>

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

### <span data-ttu-id="341f4-120">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="341f4-120">-HubResourceId</span></span>
<span data-ttu-id="341f4-121">IoT Hub 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="341f4-121">IoT Hub resource Id.</span></span>

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

### <span data-ttu-id="341f4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="341f4-122">-InputObject</span></span>
<span data-ttu-id="341f4-123">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="341f4-123">Input Object.</span></span>

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

### <span data-ttu-id="341f4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="341f4-124">-Name</span></span>
<span data-ttu-id="341f4-125">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="341f4-125">Resource name.</span></span>

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

### <span data-ttu-id="341f4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="341f4-126">-ResourceId</span></span>
<span data-ttu-id="341f4-127">명령을 호출할 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="341f4-127">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="341f4-128">-ThresholdRule</span><span class="sxs-lookup"><span data-stu-id="341f4-128">-ThresholdRule</span></span>
<span data-ttu-id="341f4-129">임계값 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="341f4-129">Threshold rules.</span></span>

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

### <span data-ttu-id="341f4-130">-TimeWindowRule</span><span class="sxs-lookup"><span data-stu-id="341f4-130">-TimeWindowRule</span></span>
<span data-ttu-id="341f4-131">시간 창 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="341f4-131">Time window rules.</span></span>

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

### <span data-ttu-id="341f4-132">-확인</span><span class="sxs-lookup"><span data-stu-id="341f4-132">-Confirm</span></span>
<span data-ttu-id="341f4-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="341f4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="341f4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="341f4-134">-WhatIf</span></span>
<span data-ttu-id="341f4-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="341f4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="341f4-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="341f4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="341f4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="341f4-137">CommonParameters</span></span>
<span data-ttu-id="341f4-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="341f4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="341f4-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="341f4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="341f4-140">입력</span><span class="sxs-lookup"><span data-stu-id="341f4-140">INPUTS</span></span>

### <span data-ttu-id="341f4-141">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="341f4-141">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span></span>

### <span data-ttu-id="341f4-142">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="341f4-142">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span></span>

### <span data-ttu-id="341f4-143">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="341f4-143">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span></span>

### <span data-ttu-id="341f4-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDEnylistCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="341f4-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]</span></span>

### <span data-ttu-id="341f4-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="341f4-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="341f4-146">System.String</span><span class="sxs-lookup"><span data-stu-id="341f4-146">System.String</span></span>

## <span data-ttu-id="341f4-147">출력</span><span class="sxs-lookup"><span data-stu-id="341f4-147">OUTPUTS</span></span>

### <span data-ttu-id="341f4-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="341f4-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="341f4-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="341f4-149">NOTES</span></span>

## <span data-ttu-id="341f4-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="341f4-150">RELATED LINKS</span></span>
