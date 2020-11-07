---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 0679f4281d9528a7124f4a9a5235d47dd8af107c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875737"
---
# <span data-ttu-id="15048-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="15048-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="15048-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15048-102">SYNOPSIS</span></span>
<span data-ttu-id="15048-103">원본 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15048-103">Creates an object of type Source</span></span>

## <span data-ttu-id="15048-104">구문과</span><span class="sxs-lookup"><span data-stu-id="15048-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15048-105">설명은</span><span class="sxs-lookup"><span data-stu-id="15048-105">DESCRIPTION</span></span>
<span data-ttu-id="15048-106">Source 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15048-106">Creates an object of type Source.</span></span>
<span data-ttu-id="15048-107">이 개체는 로그 알림 규칙을 만드는 명령에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="15048-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="15048-108">예제의</span><span class="sxs-lookup"><span data-stu-id="15048-108">EXAMPLES</span></span>

### <span data-ttu-id="15048-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="15048-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

## <span data-ttu-id="15048-110">변수</span><span class="sxs-lookup"><span data-stu-id="15048-110">PARAMETERS</span></span>

### <span data-ttu-id="15048-111">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="15048-111">-AuthorizedResource</span></span>
<span data-ttu-id="15048-112">이 경고에 대 한 승인 된 리소스 목록</span><span class="sxs-lookup"><span data-stu-id="15048-112">The list of authorized resources for this alert</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15048-113">-DataSourceId</span><span class="sxs-lookup"><span data-stu-id="15048-113">-DataSourceId</span></span>
<span data-ttu-id="15048-114">이 경고가 생성 되는 데이터 원본</span><span class="sxs-lookup"><span data-stu-id="15048-114">The data source on which this alert is created</span></span>

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

### <span data-ttu-id="15048-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15048-115">-DefaultProfile</span></span>
<span data-ttu-id="15048-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15048-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15048-117">-쿼리</span><span class="sxs-lookup"><span data-stu-id="15048-117">-Query</span></span>
<span data-ttu-id="15048-118">알림 쿼리</span><span class="sxs-lookup"><span data-stu-id="15048-118">The alert query</span></span>

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

### <span data-ttu-id="15048-119">-QueryType</span><span class="sxs-lookup"><span data-stu-id="15048-119">-QueryType</span></span>
<span data-ttu-id="15048-120">쿼리 형식-현재 지원 되는 값: ResultCount</span><span class="sxs-lookup"><span data-stu-id="15048-120">Type of Query - currently supported values : ResultCount</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15048-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15048-121">CommonParameters</span></span>
<span data-ttu-id="15048-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15048-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15048-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="15048-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15048-124">입력</span><span class="sxs-lookup"><span data-stu-id="15048-124">INPUTS</span></span>

### <span data-ttu-id="15048-125">않아야</span><span class="sxs-lookup"><span data-stu-id="15048-125">None</span></span>

## <span data-ttu-id="15048-126">출력</span><span class="sxs-lookup"><span data-stu-id="15048-126">OUTPUTS</span></span>

### <span data-ttu-id="15048-127">PSScheduledQueryRuleSource를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="15048-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="15048-128">상속자</span><span class="sxs-lookup"><span data-stu-id="15048-128">NOTES</span></span>

## <span data-ttu-id="15048-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15048-129">RELATED LINKS</span></span>
