---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
ms.openlocfilehash: 3d43407c9f7e58d7a5d29ef56412f6d38c5c957b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213328"
---
# <span data-ttu-id="5d51a-101">Get-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5d51a-101">Get-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="5d51a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d51a-102">SYNOPSIS</span></span>
<span data-ttu-id="5d51a-103">장치 보안 그룹 가져오기 (IoT Hub 보안)</span><span class="sxs-lookup"><span data-stu-id="5d51a-103">Get device security group (IoT Hub security)</span></span>

## <span data-ttu-id="5d51a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5d51a-104">SYNTAX</span></span>

### <span data-ttu-id="5d51a-105">ResourceIdScope (기본값)</span><span class="sxs-lookup"><span data-stu-id="5d51a-105">ResourceIdScope (Default)</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d51a-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="5d51a-106">ResourceIdLevelResource</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d51a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5d51a-107">DESCRIPTION</span></span>
<span data-ttu-id="5d51a-108">Get-AzDeviceSecurityGroup cmdlet은 iot security 솔루션에 정의 된 장치 보안 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d51a-108">The Get-AzDeviceSecurityGroup cmdlet returns a device security group defined in iot security solution</span></span>

## <span data-ttu-id="5d51a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5d51a-109">EXAMPLES</span></span>

### <span data-ttu-id="5d51a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5d51a-110">Example 1</span></span>
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

<span data-ttu-id="5d51a-111">Reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 인 IoT Hub에서 장치 보안 그룹 "MySecurityGroup" 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d51a-111">Get device security group "MySecurityGroup" in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

### <span data-ttu-id="5d51a-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="5d51a-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 

Array of security group items like the item returned in example 1
```

<span data-ttu-id="5d51a-113">Reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 인 IoT Hub의 디바이스 보안 그룹 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d51a-113">Get list of device security group in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="5d51a-114">변수</span><span class="sxs-lookup"><span data-stu-id="5d51a-114">PARAMETERS</span></span>

### <span data-ttu-id="5d51a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d51a-115">-DefaultProfile</span></span>
<span data-ttu-id="5d51a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d51a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d51a-117">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="5d51a-117">-HubResourceId</span></span>
<span data-ttu-id="5d51a-118">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5d51a-118">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="5d51a-119">-이름</span><span class="sxs-lookup"><span data-stu-id="5d51a-119">-Name</span></span>
<span data-ttu-id="5d51a-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d51a-120">Resource name.</span></span>

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

### <span data-ttu-id="5d51a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d51a-121">CommonParameters</span></span>
<span data-ttu-id="5d51a-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d51a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d51a-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5d51a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d51a-124">입력</span><span class="sxs-lookup"><span data-stu-id="5d51a-124">INPUTS</span></span>

### <span data-ttu-id="5d51a-125">않아야</span><span class="sxs-lookup"><span data-stu-id="5d51a-125">None</span></span>

## <span data-ttu-id="5d51a-126">출력</span><span class="sxs-lookup"><span data-stu-id="5d51a-126">OUTPUTS</span></span>

### <span data-ttu-id="5d51a-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5d51a-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="5d51a-128">상속자</span><span class="sxs-lookup"><span data-stu-id="5d51a-128">NOTES</span></span>

## <span data-ttu-id="5d51a-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d51a-129">RELATED LINKS</span></span>
