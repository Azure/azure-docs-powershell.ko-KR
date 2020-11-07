---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryrulesource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSource.md
ms.openlocfilehash: 23c32ae1520ac750aa91db3a5924b2a4d292417a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871021"
---
# <span data-ttu-id="b5b50-101">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="b5b50-101">New-AzScheduledQueryRuleSource</span></span>

## <span data-ttu-id="b5b50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5b50-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b50-103">원본 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5b50-103">Creates an object of type Source</span></span>

## <span data-ttu-id="b5b50-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5b50-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSource -Query <String> [-AuthorizedResource <String[]>] -DataSourceId <String>
 [-QueryType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5b50-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b5b50-105">DESCRIPTION</span></span>
<span data-ttu-id="b5b50-106">Source 형식의 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5b50-106">Creates an object of type Source.</span></span>
<span data-ttu-id="b5b50-107">이 개체는 로그 알림 규칙을 만드는 명령에 전달 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5b50-107">This object is to be passed to the command that creates Log Alert Rule</span></span>

## <span data-ttu-id="b5b50-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b5b50-108">EXAMPLES</span></span>

### <span data-ttu-id="b5b50-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="b5b50-109">Example 1</span></span>
```powershell
PS C:\> $source = New-AzScheduledQueryRuleSource -Query "Heartbeat | summarize AggregatedValue = count() by bin(TimeGenerated, 5m)"
                  -DataSourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace" 
                  -QueryType "ResultCount"
```

## <span data-ttu-id="b5b50-110">변수</span><span class="sxs-lookup"><span data-stu-id="b5b50-110">PARAMETERS</span></span>

### <span data-ttu-id="b5b50-111">-AuthorizedResource</span><span class="sxs-lookup"><span data-stu-id="b5b50-111">-AuthorizedResource</span></span>
<span data-ttu-id="b5b50-112">이 경고에 대 한 승인 된 리소스 목록</span><span class="sxs-lookup"><span data-stu-id="b5b50-112">The list of authorized resources for this alert</span></span>

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

### <span data-ttu-id="b5b50-113">-DataSourceId</span><span class="sxs-lookup"><span data-stu-id="b5b50-113">-DataSourceId</span></span>
<span data-ttu-id="b5b50-114">이 경고가 생성 되는 데이터 원본</span><span class="sxs-lookup"><span data-stu-id="b5b50-114">The data source on which this alert is created</span></span>

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

### <span data-ttu-id="b5b50-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b50-115">-DefaultProfile</span></span>
<span data-ttu-id="b5b50-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5b50-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5b50-117">-쿼리</span><span class="sxs-lookup"><span data-stu-id="b5b50-117">-Query</span></span>
<span data-ttu-id="b5b50-118">알림 쿼리</span><span class="sxs-lookup"><span data-stu-id="b5b50-118">The alert query</span></span>

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

### <span data-ttu-id="b5b50-119">-QueryType</span><span class="sxs-lookup"><span data-stu-id="b5b50-119">-QueryType</span></span>
<span data-ttu-id="b5b50-120">쿼리 형식-현재 지원 되는 값: ResultCount</span><span class="sxs-lookup"><span data-stu-id="b5b50-120">Type of Query - currently supported values : ResultCount</span></span>

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

### <span data-ttu-id="b5b50-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b50-121">CommonParameters</span></span>
<span data-ttu-id="b5b50-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5b50-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b50-123">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b5b50-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b50-124">입력</span><span class="sxs-lookup"><span data-stu-id="b5b50-124">INPUTS</span></span>

### <span data-ttu-id="b5b50-125">않아야</span><span class="sxs-lookup"><span data-stu-id="b5b50-125">None</span></span>

## <span data-ttu-id="b5b50-126">출력</span><span class="sxs-lookup"><span data-stu-id="b5b50-126">OUTPUTS</span></span>

### <span data-ttu-id="b5b50-127">PSScheduledQueryRuleSource를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5b50-127">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSource</span></span>

## <span data-ttu-id="b5b50-128">상속자</span><span class="sxs-lookup"><span data-stu-id="b5b50-128">NOTES</span></span>

## <span data-ttu-id="b5b50-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5b50-129">RELATED LINKS</span></span>
