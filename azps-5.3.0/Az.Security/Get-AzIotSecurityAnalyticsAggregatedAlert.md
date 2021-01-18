---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 5687497c55c6da914b28022320df1d7241f2eba1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495036"
---
# <span data-ttu-id="e9a9c-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="e9a9c-101">Get-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="e9a9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a9c-103">IoT 보안 집계 경고를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9a9c-103">Get IoT security aggregated alert</span></span>

## <span data-ttu-id="e9a9c-104">구문</span><span class="sxs-lookup"><span data-stu-id="e9a9c-104">SYNTAX</span></span>

### <span data-ttu-id="e9a9c-105">SolutionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="e9a9c-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9a9c-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="e9a9c-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9a9c-107">설명</span><span class="sxs-lookup"><span data-stu-id="e9a9c-107">DESCRIPTION</span></span>
<span data-ttu-id="e9a9c-108">이 Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet은 iot Hub의 디바이스에서 하나 이상의 집계된 경고를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a9c-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated alerts on devices of iot hub.</span></span>
<span data-ttu-id="e9a9c-109">집계된 경고의 이름은 경고 유형과 경고가 집계된 날짜를 '/'로 구분한 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a9c-109">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="e9a9c-110">예제</span><span class="sxs-lookup"><span data-stu-id="e9a9c-110">EXAMPLES</span></span>

### <span data-ttu-id="e9a9c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9a9c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name "IoT_Bruteforce_Fail/2019-02-02"

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedAlerts/IoT_Bruteforce_Fail/2019-02-02"
Name: "IoT_Bruteforce_Fail/2019-02-02"
Type: "Microsoft.Security/IoTSecurityAggregatedAlert"
AlertType: "IoT_Bruteforce_Fail"
AlertDisplayName: "Failed Bruteforce"
AggregatedDateUtc: "2019-02-02"
VendorName: "Microsoft"
ReportedSeverity: "Low"
RemediationSteps: ""
Description: "Multiple unsuccsseful login attempts identified. A Bruteforce attack on the device failed."
Count: 50
EffectedResourceType: "IoT Device"
SystemSource: "Devices"
ActionTaken: "Detected"
LogAnalyticsQuery: "SecurityAlert | where tolower(ResourceId) == tolower('/subscriptions/b77ec8a9-04ed-48d2-a87a-e5887b978ba6/resourceGroups/IoT-Solution-DemoEnv/providers/Microsoft.Devices/IotHubs/rtogm-hub') and tolower(AlertName) == tolower('Custom Alert - number of device to cloud messages in MQTT protocol is not in the allowed range') | extend DeviceId=parse_json(ExtendedProperties)['DeviceId'] | project DeviceId, TimeGenerated, DisplayName, AlertSeverity, Description, RemediationSteps, ExtendedProperties"
TopDevicesList: [
                {
                  DeviceId: "testDevice1"
                  AlertsCount: 45
                  LastOccurrence: "10:42"
                }
                {
                  DeviceId: "testDevice2"
                  AlertsCount: 30
                  LastOccurrence: "15:42"
                }
              ]
```

<span data-ttu-id="e9a9c-112">솔루션 "mySolution" 및 리소스 그룹 "myResourceGroup"에서 집계된 경고 "IoT_Bruteforce_Fail/2019-02-02"(경고 유형 및 집계 날짜에서 결합된 이름)를 얻음</span><span class="sxs-lookup"><span data-stu-id="e9a9c-112">Get the aggregated alert "IoT_Bruteforce_Fail/2019-02-02" (the name combined from the alert type and its aggregated date) in solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="e9a9c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e9a9c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated alert items as shown in example 1
```

<span data-ttu-id="e9a9c-114">솔루션 "MySolution" 및 리소스 그룹 "MyResourceGroup"에서 집계된 모든 경고 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e9a9c-114">Get a list of all aggregated alerts in solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="e9a9c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9a9c-115">PARAMETERS</span></span>

### <span data-ttu-id="e9a9c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9a9c-116">-DefaultProfile</span></span>
<span data-ttu-id="e9a9c-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a9c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9a9c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e9a9c-118">-Name</span></span>
<span data-ttu-id="e9a9c-119">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a9c-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9a9c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9a9c-120">-ResourceGroupName</span></span>
<span data-ttu-id="e9a9c-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9a9c-121">Resource group name.</span></span>

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

### <span data-ttu-id="e9a9c-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="e9a9c-122">-SolutionName</span></span>
<span data-ttu-id="e9a9c-123">솔루션 이름</span><span class="sxs-lookup"><span data-stu-id="e9a9c-123">Solution name</span></span>

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

### <span data-ttu-id="e9a9c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9a9c-124">CommonParameters</span></span>
<span data-ttu-id="e9a9c-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e9a9c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9a9c-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e9a9c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9a9c-127">입력</span><span class="sxs-lookup"><span data-stu-id="e9a9c-127">INPUTS</span></span>

### <span data-ttu-id="e9a9c-128">없음</span><span class="sxs-lookup"><span data-stu-id="e9a9c-128">None</span></span>

## <span data-ttu-id="e9a9c-129">출력</span><span class="sxs-lookup"><span data-stu-id="e9a9c-129">OUTPUTS</span></span>

### <span data-ttu-id="e9a9c-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="e9a9c-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

## <span data-ttu-id="e9a9c-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e9a9c-131">NOTES</span></span>

## <span data-ttu-id="e9a9c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9a9c-132">RELATED LINKS</span></span>
