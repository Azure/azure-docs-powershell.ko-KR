---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmMetricFilter.md
ms.openlocfilehash: 783f5c780b0202ddb78666c2c7446ba07b5434e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711680"
---
# <span data-ttu-id="c02ef-101">New-AzureRmMetricFilter</span><span class="sxs-lookup"><span data-stu-id="c02ef-101">New-AzureRmMetricFilter</span></span>

## <span data-ttu-id="c02ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c02ef-102">SYNOPSIS</span></span>
<span data-ttu-id="c02ef-103">메트릭을 쿼리 하는 데 사용할 수 있는 메트릭 차원 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c02ef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c02ef-104">SYNTAX</span></span>

```
New-AzureRmMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c02ef-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c02ef-105">DESCRIPTION</span></span>
<span data-ttu-id="c02ef-106">**AzureRmMetricFilter** cmdlet은 메트릭을 쿼리 하는 데 사용할 수 있는 메트릭 차원 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-106">The **New-AzureRmMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="c02ef-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c02ef-107">EXAMPLES</span></span>

### <span data-ttu-id="c02ef-108">예제 1: 메트릭 차원 필터 만들기</span><span class="sxs-lookup"><span data-stu-id="c02ef-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzureRmMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="c02ef-109">이 명령은 "도시 eq ' 시애틀 ' 또는 도시 eq ' 뉴욕 '" 형식의 미터법 차원 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="c02ef-110">변수</span><span class="sxs-lookup"><span data-stu-id="c02ef-110">PARAMETERS</span></span>

### <span data-ttu-id="c02ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c02ef-111">-DefaultProfile</span></span>
<span data-ttu-id="c02ef-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c02ef-113">-차원</span><span class="sxs-lookup"><span data-stu-id="c02ef-113">-Dimension</span></span>
<span data-ttu-id="c02ef-114">메트릭 차원의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="c02ef-115">-연산자</span><span class="sxs-lookup"><span data-stu-id="c02ef-115">-Operator</span></span>
<span data-ttu-id="c02ef-116">메트릭 차원을 선택 하는 데 사용 되는 연산자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-116">Specifies the operator used to select the metric dimension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02ef-117">-값</span><span class="sxs-lookup"><span data-stu-id="c02ef-117">-Value</span></span>
<span data-ttu-id="c02ef-118">메트릭 차원 값의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-118">Specifies the array of metric dimension values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02ef-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c02ef-119">CommonParameters</span></span>
<span data-ttu-id="c02ef-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c02ef-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c02ef-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c02ef-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c02ef-122">입력</span><span class="sxs-lookup"><span data-stu-id="c02ef-122">INPUTS</span></span>

### <span data-ttu-id="c02ef-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c02ef-123">System.String</span></span>

### <span data-ttu-id="c02ef-124">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="c02ef-124">System.String[]</span></span>

## <span data-ttu-id="c02ef-125">출력</span><span class="sxs-lookup"><span data-stu-id="c02ef-125">OUTPUTS</span></span>

### <span data-ttu-id="c02ef-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c02ef-126">System.String</span></span>

## <span data-ttu-id="c02ef-127">상속자</span><span class="sxs-lookup"><span data-stu-id="c02ef-127">NOTES</span></span>

## <span data-ttu-id="c02ef-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c02ef-128">RELATED LINKS</span></span>

<span data-ttu-id="c02ef-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md) 
 [Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="c02ef-129">[Get-AzureRmMetric](./Get-AzureRmMetric.md)
[Get-AzureRmMetricDefinition](./Get-AzureRmMetricDefinition.md)</span></span>

