---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azmetricfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzMetricFilter.md
ms.openlocfilehash: e7d499dd14182a9eaa804ccdcbacac4f65ae1497
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331562"
---
# <span data-ttu-id="987fd-101">New-AzMetricFilter</span><span class="sxs-lookup"><span data-stu-id="987fd-101">New-AzMetricFilter</span></span>

## <span data-ttu-id="987fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="987fd-102">SYNOPSIS</span></span>
<span data-ttu-id="987fd-103">메트릭을 쿼리하는 데 사용할 수 있는 메트릭 차원 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="987fd-103">Creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="987fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="987fd-104">SYNTAX</span></span>

```
New-AzMetricFilter [-Dimension] <String> [-Operator] <String> [-Value] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="987fd-105">설명</span><span class="sxs-lookup"><span data-stu-id="987fd-105">DESCRIPTION</span></span>
<span data-ttu-id="987fd-106">**New-AzMetricFilter** cmdlet은 메트릭을 쿼리하는 데 사용할 수 있는 메트릭 차원 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="987fd-106">The **New-AzMetricFilter** cmdlet creates a metric dimension filter that can be used to query metrics.</span></span>

## <span data-ttu-id="987fd-107">예제</span><span class="sxs-lookup"><span data-stu-id="987fd-107">EXAMPLES</span></span>

### <span data-ttu-id="987fd-108">예제 1: 메트릭 차원 필터 만들기</span><span class="sxs-lookup"><span data-stu-id="987fd-108">Example 1: Create a metric dimension filter</span></span>
```
PS C:\>New-AzMetricFilter -Dimension City -Operator eq -Value "Seattle","New York"
```

<span data-ttu-id="987fd-109">이 명령은 "City eq 'Seattle' 또는 City eq 'New York' 형식의 메트릭 차원 필터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="987fd-109">This command creates metric dimension filter of the format "City eq 'Seattle' or City eq 'New York'".</span></span>

## <span data-ttu-id="987fd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="987fd-110">PARAMETERS</span></span>

### <span data-ttu-id="987fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="987fd-111">-DefaultProfile</span></span>
<span data-ttu-id="987fd-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="987fd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="987fd-113">-Dimension</span><span class="sxs-lookup"><span data-stu-id="987fd-113">-Dimension</span></span>
<span data-ttu-id="987fd-114">메트릭 차원의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="987fd-114">The name of the metric dimension.</span></span> 

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

### <span data-ttu-id="987fd-115">-Operator</span><span class="sxs-lookup"><span data-stu-id="987fd-115">-Operator</span></span>
<span data-ttu-id="987fd-116">메트릭 차원을 선택하는 데 사용되는 연산자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="987fd-116">Specifies the operator used to select the metric dimension.</span></span>

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

### <span data-ttu-id="987fd-117">-Value</span><span class="sxs-lookup"><span data-stu-id="987fd-117">-Value</span></span>
<span data-ttu-id="987fd-118">메트릭 차원 값의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="987fd-118">Specifies the array of metric dimension values.</span></span>

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

### <span data-ttu-id="987fd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="987fd-119">CommonParameters</span></span>
<span data-ttu-id="987fd-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="987fd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="987fd-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="987fd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="987fd-122">입력</span><span class="sxs-lookup"><span data-stu-id="987fd-122">INPUTS</span></span>

### <span data-ttu-id="987fd-123">System.String</span><span class="sxs-lookup"><span data-stu-id="987fd-123">System.String</span></span>

### <span data-ttu-id="987fd-124">System.String[]</span><span class="sxs-lookup"><span data-stu-id="987fd-124">System.String[]</span></span>

## <span data-ttu-id="987fd-125">출력</span><span class="sxs-lookup"><span data-stu-id="987fd-125">OUTPUTS</span></span>

### <span data-ttu-id="987fd-126">System.String</span><span class="sxs-lookup"><span data-stu-id="987fd-126">System.String</span></span>

## <span data-ttu-id="987fd-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="987fd-127">NOTES</span></span>

## <span data-ttu-id="987fd-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="987fd-128">RELATED LINKS</span></span>

<span data-ttu-id="987fd-129">[Get-AzMetric](./Get-AzMetric.md) 
 [Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span><span class="sxs-lookup"><span data-stu-id="987fd-129">[Get-AzMetric](./Get-AzMetric.md)
[Get-AzMetricDefinition](./Get-AzMetricDefinition.md)</span></span>

