---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: f57d3b3eb254a547059cb2e7c37a0720ee5f6310
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969931"
---
# <span data-ttu-id="eec22-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="eec22-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="eec22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eec22-102">SYNOPSIS</span></span>
<span data-ttu-id="eec22-103">IoT 보안 집계 권장 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="eec22-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="eec22-104">구문</span><span class="sxs-lookup"><span data-stu-id="eec22-104">SYNTAX</span></span>

### <span data-ttu-id="eec22-105">SolutionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="eec22-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eec22-106">SolutionLevelResource</span><span class="sxs-lookup"><span data-stu-id="eec22-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eec22-107">설명</span><span class="sxs-lookup"><span data-stu-id="eec22-107">DESCRIPTION</span></span>
<span data-ttu-id="eec22-108">Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet은 iot Hub의 디바이스에 대해 하나 이상의 집계된 권장 사항을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="eec22-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="eec22-109">집계된 권장의 이름은 해당 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="eec22-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="eec22-110">예제</span><span class="sxs-lookup"><span data-stu-id="eec22-110">EXAMPLES</span></span>

### <span data-ttu-id="eec22-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="eec22-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Name IoT_OpenPorts

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default/aggregatedRecommendations/IoT_OpenPorts"
Name: "IoT_OpenPorts"
Type: "Microsoft.Security/IoTSecurityAggregatedRecommendation"
RecommendationName: "IoT_OpenPorts"
RecommendationDisplayName: "Device has open ports"
RecommendationTypeId: ""
DetectedBy: "IoTSecurity"
HealthyDevices: -1
UnhealthyDeviceCount: 5
RemediationSteps: "Review open ports on the device and make sure they belong to legitimate and necessary processes for the device to function correctly."
ReportedSeverity: "Medium"
Description: "Found a listening endpoint on the device."
LogAnalyticsQuery: "SecurityRecommendation | where tolower(AssessedResourceId) == tolower('/subscriptions/075423e9-7d33-4166-8bdf-3920b04e3735/resourcegroups/iot-hub-demo/providers/microsoft.devices/iothubs/ascforiot-demo') and tolower(RecommendationName) == tolower('IoT_OpenPorts') and TimeGenerated  < now()"
```

<span data-ttu-id="eec22-112">보안 솔루션 "mySolution" 및 리소스 그룹 "MyResourceGroup"에서 집계된 권장 "IoT_OpenPorts"를 얻음</span><span class="sxs-lookup"><span data-stu-id="eec22-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="eec22-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="eec22-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="eec22-114">보안 솔루션 "MySolution" 및 리소스 그룹 "MyResourceGroup"에서 집계된 권장 사항 목록 얻기</span><span class="sxs-lookup"><span data-stu-id="eec22-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="eec22-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="eec22-115">PARAMETERS</span></span>

### <span data-ttu-id="eec22-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec22-116">-DefaultProfile</span></span>
<span data-ttu-id="eec22-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eec22-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eec22-118">-Name</span><span class="sxs-lookup"><span data-stu-id="eec22-118">-Name</span></span>
<span data-ttu-id="eec22-119">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eec22-119">Resource name.</span></span>

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

### <span data-ttu-id="eec22-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eec22-120">-ResourceGroupName</span></span>
<span data-ttu-id="eec22-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eec22-121">Resource group name.</span></span>

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

### <span data-ttu-id="eec22-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="eec22-122">-SolutionName</span></span>
<span data-ttu-id="eec22-123">솔루션 이름</span><span class="sxs-lookup"><span data-stu-id="eec22-123">Solution name</span></span>

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

### <span data-ttu-id="eec22-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec22-124">CommonParameters</span></span>
<span data-ttu-id="eec22-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eec22-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec22-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eec22-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec22-127">입력</span><span class="sxs-lookup"><span data-stu-id="eec22-127">INPUTS</span></span>

### <span data-ttu-id="eec22-128">없음</span><span class="sxs-lookup"><span data-stu-id="eec22-128">None</span></span>

## <span data-ttu-id="eec22-129">출력</span><span class="sxs-lookup"><span data-stu-id="eec22-129">OUTPUTS</span></span>

### <span data-ttu-id="eec22-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="eec22-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="eec22-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eec22-131">NOTES</span></span>

## <span data-ttu-id="eec22-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eec22-132">RELATED LINKS</span></span>
