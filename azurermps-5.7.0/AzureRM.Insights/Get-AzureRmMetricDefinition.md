---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
ms.openlocfilehash: de839f4b56f4aa1111e130bdf6396875f9aeb185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530524"
---
# <span data-ttu-id="a511f-101">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="a511f-101">Get-AzureRmMetricDefinition</span></span>

## <span data-ttu-id="a511f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a511f-102">SYNOPSIS</span></span>
<span data-ttu-id="a511f-103">메트릭 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a511f-103">Gets metric definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a511f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a511f-104">SYNTAX</span></span>

```
Get-AzureRmMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a511f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a511f-105">DESCRIPTION</span></span>
<span data-ttu-id="a511f-106">**Get-AzureRmMetricDefinition** cmdlet은 메트릭 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a511f-106">The **Get-AzureRmMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="a511f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a511f-107">EXAMPLES</span></span>

### <span data-ttu-id="a511f-108">예제 1: 리소스에 대 한 메트릭 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="a511f-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
Name                   : CpuTime
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Seconds
Name                   : Requests
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="a511f-109">이 명령은 지정 된 리소스에 대 한 메트릭 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a511f-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="a511f-110">예제 2: 자세한 출력을 사용 하 여 메트릭 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="a511f-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : Requests
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="a511f-111">이 명령은 website2에 대 한 메트릭 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a511f-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="a511f-112">출력이 자세히 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a511f-112">The output is detailed.</span></span>

### <span data-ttu-id="a511f-113">예제 3: 이름별 메트릭 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="a511f-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricNames "BytesSent,CpuTime"
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : BytesSent
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Bytes
```

<span data-ttu-id="a511f-114">이 명령은 BytesSent 및 CpuTime 메트릭스에 대 한 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a511f-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="a511f-115">출력이 자세히 설명 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a511f-115">The output is detailed.</span></span>

## <span data-ttu-id="a511f-116">변수</span><span class="sxs-lookup"><span data-stu-id="a511f-116">PARAMETERS</span></span>

### <span data-ttu-id="a511f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a511f-117">-DefaultProfile</span></span>
<span data-ttu-id="a511f-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a511f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a511f-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="a511f-119">-DetailedOutput</span></span>
<span data-ttu-id="a511f-120">이 작업에 자세한 출력이 포함 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a511f-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="a511f-121">이 매개 변수를 지정 하지 않으면 출력이 요약 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a511f-121">If you do not specify this parameter, the output is summarized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a511f-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="a511f-122">-MetricName</span></span>
<span data-ttu-id="a511f-123">메트릭의 이름 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a511f-123">Specifies an array of names of metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: MetricNames

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a511f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a511f-124">-ResourceId</span></span>
<span data-ttu-id="a511f-125">리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a511f-125">Specifies the resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a511f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a511f-126">CommonParameters</span></span>
<span data-ttu-id="a511f-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a511f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a511f-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a511f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a511f-129">입력</span><span class="sxs-lookup"><span data-stu-id="a511f-129">INPUTS</span></span>

### <span data-ttu-id="a511f-130">않아야</span><span class="sxs-lookup"><span data-stu-id="a511f-130">None</span></span>
<span data-ttu-id="a511f-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a511f-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a511f-132">출력</span><span class="sxs-lookup"><span data-stu-id="a511f-132">OUTPUTS</span></span>

### <span data-ttu-id="a511f-133">PSMetricDefinition [] (으)로</span><span class="sxs-lookup"><span data-stu-id="a511f-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition[]</span></span>

## <span data-ttu-id="a511f-134">상속자</span><span class="sxs-lookup"><span data-stu-id="a511f-134">NOTES</span></span>

## <span data-ttu-id="a511f-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a511f-135">RELATED LINKS</span></span>

[<span data-ttu-id="a511f-136">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="a511f-136">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


