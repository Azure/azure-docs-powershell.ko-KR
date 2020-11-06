---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: CA67985F-C5D5-4CF4-81A4-C35FD769AF0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmUsage.md
ms.openlocfilehash: 9f02a1c9dfe0c4c41fa1e873201dbeb1d849dd77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534079"
---
# <span data-ttu-id="47e93-101">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="47e93-101">Get-AzureRmUsage</span></span>

## <span data-ttu-id="47e93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47e93-102">SYNOPSIS</span></span>
<span data-ttu-id="47e93-103">리소스에 대 한 사용 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47e93-103">Gets the usage metrics for a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47e93-104">구문과</span><span class="sxs-lookup"><span data-stu-id="47e93-104">SYNTAX</span></span>

```
Get-AzureRmUsage [-ResourceId] <String> [-ApiVersion <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-MetricNames <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47e93-105">설명은</span><span class="sxs-lookup"><span data-stu-id="47e93-105">DESCRIPTION</span></span>
<span data-ttu-id="47e93-106">**AzureRmUsage** cmdlet은 지정 된 리소스에 대 한 사용 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47e93-106">The **Get-AzureRmUsage** cmdlet gets the usage metrics for a specified resource.</span></span>

## <span data-ttu-id="47e93-107">예제의</span><span class="sxs-lookup"><span data-stu-id="47e93-107">EXAMPLES</span></span>

### <span data-ttu-id="47e93-108">예제 1: 리소스 ID 별 사용 현황 메트릭 가져오기</span><span class="sxs-lookup"><span data-stu-id="47e93-108">Example 1: Get usage metrics by resource ID</span></span>
```
PS C:\>Get-AzureRmUsage -ResourceId "/subscriptions/bcdeb07f-1c43-20be-1f3b-4f0febc10f5b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/pattifuller"
```

<span data-ttu-id="47e93-109">이 명령은 지정 된 웹 사이트에 대 한 사용 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47e93-109">This command gets the usage metrics for the specified website.</span></span>

## <span data-ttu-id="47e93-110">변수</span><span class="sxs-lookup"><span data-stu-id="47e93-110">PARAMETERS</span></span>

### <span data-ttu-id="47e93-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="47e93-111">-ApiVersion</span></span>
<span data-ttu-id="47e93-112">리소스 공급자가 허용 하는 API 버전 문자열 (예: 2014-04-01)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47e93-112">Specifies an API version string, for example, 2014-04-01, which is accepted by the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47e93-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="47e93-113">-EndTime</span></span>
<span data-ttu-id="47e93-114">검색할 최신 날짜와 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47e93-114">Specifies the latest time and date to search.</span></span>

<span data-ttu-id="47e93-115">Get-Date cmdlet을 사용 하 여 **DateTime** 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47e93-115">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47e93-116">-MetricNames</span><span class="sxs-lookup"><span data-stu-id="47e93-116">-MetricNames</span></span>
<span data-ttu-id="47e93-117">메트릭의 이름 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47e93-117">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47e93-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47e93-118">-ResourceId</span></span>
<span data-ttu-id="47e93-119">메트릭의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47e93-119">Specifies the ID of the resource for the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47e93-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="47e93-120">-StartTime</span></span>
<span data-ttu-id="47e93-121">검색할 가장 빠른 시간 및 날짜를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="47e93-121">Specifies the earliest time and date to search.</span></span>

<span data-ttu-id="47e93-122">Get-Date cmdlet을 사용 하 여 **DateTime** 개체를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47e93-122">You can use the Get-Date cmdlet to get a **DateTime** object.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47e93-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e93-123">-DefaultProfile</span></span>
<span data-ttu-id="47e93-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47e93-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47e93-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e93-125">CommonParameters</span></span>
<span data-ttu-id="47e93-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="47e93-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e93-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47e93-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e93-128">입력</span><span class="sxs-lookup"><span data-stu-id="47e93-128">INPUTS</span></span>

## <span data-ttu-id="47e93-129">출력</span><span class="sxs-lookup"><span data-stu-id="47e93-129">OUTPUTS</span></span>

### <span data-ttu-id="47e93-130">PSUsageMetric [] (으)로</span><span class="sxs-lookup"><span data-stu-id="47e93-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSUsageMetric[]</span></span>

## <span data-ttu-id="47e93-131">상속자</span><span class="sxs-lookup"><span data-stu-id="47e93-131">NOTES</span></span>

## <span data-ttu-id="47e93-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47e93-132">RELATED LINKS</span></span>

[<span data-ttu-id="47e93-133">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="47e93-133">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


