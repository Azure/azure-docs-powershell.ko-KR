---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
ms.openlocfilehash: 3d43407c9f7e58d7a5d29ef56412f6d38c5c957b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337509"
---
# <span data-ttu-id="58253-101">Get-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="58253-101">Get-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="58253-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58253-102">SYNOPSIS</span></span>
<span data-ttu-id="58253-103">디바이스 보안 그룹(IoT Hub 보안)</span><span class="sxs-lookup"><span data-stu-id="58253-103">Get device security group (IoT Hub security)</span></span>

## <span data-ttu-id="58253-104">구문</span><span class="sxs-lookup"><span data-stu-id="58253-104">SYNTAX</span></span>

### <span data-ttu-id="58253-105">ResourceIdScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="58253-105">ResourceIdScope (Default)</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58253-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="58253-106">ResourceIdLevelResource</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58253-107">설명</span><span class="sxs-lookup"><span data-stu-id="58253-107">DESCRIPTION</span></span>
<span data-ttu-id="58253-108">Get-AzDeviceSecurityGroup cmdlet은 iot 보안 솔루션에 정의된 디바이스 보안 그룹을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="58253-108">The Get-AzDeviceSecurityGroup cmdlet returns a device security group defined in iot security solution</span></span>

## <span data-ttu-id="58253-109">예제</span><span class="sxs-lookup"><span data-stu-id="58253-109">EXAMPLES</span></span>

### <span data-ttu-id="58253-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="58253-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" -Name "MySecurityGroup" 

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
            }
            {
              RuleType: "AmqpC2DMessagesNotInAllowedRange"
              DisplayName: "Number of cloud to device messages (AMQP protocol) is not in allowed range"
              Description: "Get an alert when the number of cloud to device messages (AMQP protocol) in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
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

<span data-ttu-id="58253-111">IoT Hub의 디바이스 보안 그룹 "/subscriptions/XXXXXXXXX-XXXXXX-XXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"를 사용하여 디바이스 보안 그룹 "MySecurityGroup"을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="58253-111">Get device security group "MySecurityGroup" in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

### <span data-ttu-id="58253-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="58253-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 

Array of security group items like the item returned in example 1
```

<span data-ttu-id="58253-113">IoT Hub에서 리소스 ID "/subscriptions/XXXXXXXX-XXXXXX-XXXXX-XXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"를 사용하여 디바이스 보안 그룹 목록을 확인합니다.</span><span class="sxs-lookup"><span data-stu-id="58253-113">Get list of device security group in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="58253-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58253-114">PARAMETERS</span></span>

### <span data-ttu-id="58253-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58253-115">-DefaultProfile</span></span>
<span data-ttu-id="58253-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58253-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58253-117">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="58253-117">-HubResourceId</span></span>
<span data-ttu-id="58253-118">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="58253-118">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="58253-119">-Name</span><span class="sxs-lookup"><span data-stu-id="58253-119">-Name</span></span>
<span data-ttu-id="58253-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58253-120">Resource name.</span></span>

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

### <span data-ttu-id="58253-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58253-121">CommonParameters</span></span>
<span data-ttu-id="58253-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="58253-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58253-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="58253-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58253-124">입력</span><span class="sxs-lookup"><span data-stu-id="58253-124">INPUTS</span></span>

### <span data-ttu-id="58253-125">없음</span><span class="sxs-lookup"><span data-stu-id="58253-125">None</span></span>

## <span data-ttu-id="58253-126">출력</span><span class="sxs-lookup"><span data-stu-id="58253-126">OUTPUTS</span></span>

### <span data-ttu-id="58253-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="58253-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="58253-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="58253-128">NOTES</span></span>

## <span data-ttu-id="58253-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58253-129">RELATED LINKS</span></span>
