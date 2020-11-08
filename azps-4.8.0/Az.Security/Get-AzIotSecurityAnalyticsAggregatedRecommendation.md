---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalyticsAggregatedRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalyticsAggregatedRecommendation.md
ms.openlocfilehash: 944c029b4085316225887b821c4f6c8f52e7f92b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213986"
---
# <span data-ttu-id="923be-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="923be-101">Get-AzIotSecurityAnalyticsAggregatedRecommendation</span></span>

## <span data-ttu-id="923be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="923be-102">SYNOPSIS</span></span>
<span data-ttu-id="923be-103">IoT security 집계 권장 사항 가져오기</span><span class="sxs-lookup"><span data-stu-id="923be-103">Get IoT security aggregated recommendation</span></span>

## <span data-ttu-id="923be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="923be-104">SYNTAX</span></span>

### <span data-ttu-id="923be-105">솔루션 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="923be-105">SolutionScope (Default)</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="923be-106">솔루션 Levelresource</span><span class="sxs-lookup"><span data-stu-id="923be-106">SolutionLevelResource</span></span>
```
Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName <String> -SolutionName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="923be-107">설명은</span><span class="sxs-lookup"><span data-stu-id="923be-107">DESCRIPTION</span></span>
<span data-ttu-id="923be-108">Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet은 iot hub 장치에서 하나 이상의 집계 된 권장 사항을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="923be-108">The Get-AzIotSecurityAnalyticsAggregatedAlert cmdlet returns one or more aggregated recommendations on devices of iot hub.</span></span> <span data-ttu-id="923be-109">집계 된 추천의 이름은 해당 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="923be-109">The name of an aggregated recommendation is its type</span></span>

## <span data-ttu-id="923be-110">예제의</span><span class="sxs-lookup"><span data-stu-id="923be-110">EXAMPLES</span></span>

### <span data-ttu-id="923be-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="923be-111">Example 1</span></span>
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

<span data-ttu-id="923be-112">보안 솔루션 "MySolution" 및 리소스 그룹 "Mysolution"에서 집계 된 권장 구성 "IoT_OpenPorts"를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="923be-112">Get the aggregated recommendation "IoT_OpenPorts" in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="923be-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="923be-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalyticsAggregatedRecommendation -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution"

Array of aggregated recommendation items as shown in example 1
```

<span data-ttu-id="923be-114">보안 솔루션 "MySolution" 및 리소스 그룹 "Mysolution"에서 집계 권장 사항 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="923be-114">Get a list of aggregated recommendations in security solution "MySolution" and resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="923be-115">변수</span><span class="sxs-lookup"><span data-stu-id="923be-115">PARAMETERS</span></span>

### <span data-ttu-id="923be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="923be-116">-DefaultProfile</span></span>
<span data-ttu-id="923be-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="923be-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="923be-118">-이름</span><span class="sxs-lookup"><span data-stu-id="923be-118">-Name</span></span>
<span data-ttu-id="923be-119">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="923be-119">Resource name.</span></span>

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

### <span data-ttu-id="923be-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="923be-120">-ResourceGroupName</span></span>
<span data-ttu-id="923be-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="923be-121">Resource group name.</span></span>

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

### <span data-ttu-id="923be-122">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="923be-122">-SolutionName</span></span>
<span data-ttu-id="923be-123">솔루션 이름</span><span class="sxs-lookup"><span data-stu-id="923be-123">Solution name</span></span>

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

### <span data-ttu-id="923be-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="923be-124">CommonParameters</span></span>
<span data-ttu-id="923be-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="923be-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="923be-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="923be-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="923be-127">입력</span><span class="sxs-lookup"><span data-stu-id="923be-127">INPUTS</span></span>

### <span data-ttu-id="923be-128">않아야</span><span class="sxs-lookup"><span data-stu-id="923be-128">None</span></span>

## <span data-ttu-id="923be-129">출력</span><span class="sxs-lookup"><span data-stu-id="923be-129">OUTPUTS</span></span>

### <span data-ttu-id="923be-130">Microsoft. Azure. Irootsecurity솔루션 PSIoTSecurityAggregatedRecommendation</span><span class="sxs-lookup"><span data-stu-id="923be-130">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedRecommendation</span></span>

## <span data-ttu-id="923be-131">상속자</span><span class="sxs-lookup"><span data-stu-id="923be-131">NOTES</span></span>

## <span data-ttu-id="923be-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="923be-132">RELATED LINKS</span></span>
