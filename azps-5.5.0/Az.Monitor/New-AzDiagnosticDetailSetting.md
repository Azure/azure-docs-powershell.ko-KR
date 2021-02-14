---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdiagnosticdetailsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticDetailSetting.md
ms.openlocfilehash: b990a386feebe8e04ba612c45550ecbd07524c7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203416"
---
# <span data-ttu-id="c5d69-101">New-AzDiagnosticDetailSetting</span><span class="sxs-lookup"><span data-stu-id="c5d69-101">New-AzDiagnosticDetailSetting</span></span>

## <span data-ttu-id="c5d69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5d69-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d69-103">PSDiagnosticDetailSetting 개체 만들기, 형식은 메트릭 또는 로그일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5d69-103">Create PSDiagnosticDetailSetting Object, type could be metric or log</span></span>

## <span data-ttu-id="c5d69-104">구문</span><span class="sxs-lookup"><span data-stu-id="c5d69-104">SYNTAX</span></span>

### <span data-ttu-id="c5d69-105">LogSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5d69-105">LogSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Log [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5d69-106">MetricSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5d69-106">MetricSettingParameterSet</span></span>
```
New-AzDiagnosticDetailSetting -Metric [-RetentionInDays <Int32>] [-RetentionEnabled] -Category <String>
 [-Enabled] [-TimeGrain <TimeSpan>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5d69-107">설명</span><span class="sxs-lookup"><span data-stu-id="c5d69-107">DESCRIPTION</span></span>
<span data-ttu-id="c5d69-108">PSMetricSettings 또는 PSLogSettings 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c5d69-108">Create PSMetricSettings or PSLogSettings object.</span></span> <span data-ttu-id="c5d69-109">.를 사용하여 범주를 얻을 수 `Get-AzDiagnosticSettingCategory` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5d69-109">You can get categories by using `Get-AzDiagnosticSettingCategory`.</span></span>

## <span data-ttu-id="c5d69-110">예제</span><span class="sxs-lookup"><span data-stu-id="c5d69-110">EXAMPLES</span></span>

### <span data-ttu-id="c5d69-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c5d69-111">Example 1</span></span>
```powershell
PS C:\> $TimeGrain=New-TimeSpan -Days 90
PS C:\> New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics -Enabled -TimeGrain $TimeGrain
TimeGrain       : 90.00:00:00
Category        : AllMetrics
Enabled         : True
RetentionPolicy :
                  Enabled : True
                  Days    : 1
CategoryType    : Metrics
```

<span data-ttu-id="c5d69-112">PSMetricSettings 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c5d69-112">Create PSMetricSettings object.</span></span>

### <span data-ttu-id="c5d69-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c5d69-113">Example 2</span></span>
```powershell
PS C:\> New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
Category Enabled RetentionPolicy               CategoryType
-------- ------- ---------------               ------------
Audit       True …                                     Logs
```

<span data-ttu-id="c5d69-114">PSLogSettings 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c5d69-114">Create PSLogSettings object.</span></span>

## <span data-ttu-id="c5d69-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5d69-115">PARAMETERS</span></span>

### <span data-ttu-id="c5d69-116">-Category</span><span class="sxs-lookup"><span data-stu-id="c5d69-116">-Category</span></span>
<span data-ttu-id="c5d69-117">설정 범주</span><span class="sxs-lookup"><span data-stu-id="c5d69-117">Category of setting</span></span>

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

### <span data-ttu-id="c5d69-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5d69-118">-DefaultProfile</span></span>
<span data-ttu-id="c5d69-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5d69-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5d69-120">-Enabled</span><span class="sxs-lookup"><span data-stu-id="c5d69-120">-Enabled</span></span>
<span data-ttu-id="c5d69-121">설정 사용</span><span class="sxs-lookup"><span data-stu-id="c5d69-121">Enable the setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d69-122">-Log</span><span class="sxs-lookup"><span data-stu-id="c5d69-122">-Log</span></span>
<span data-ttu-id="c5d69-123">로그 설정을 만들면</span><span class="sxs-lookup"><span data-stu-id="c5d69-123">To create log setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d69-124">-Metric</span><span class="sxs-lookup"><span data-stu-id="c5d69-124">-Metric</span></span>
<span data-ttu-id="c5d69-125">메트릭 설정을 만들면</span><span class="sxs-lookup"><span data-stu-id="c5d69-125">To create metric setting</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d69-126">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="c5d69-126">-RetentionEnabled</span></span>
<span data-ttu-id="c5d69-127">보존 정책 사용</span><span class="sxs-lookup"><span data-stu-id="c5d69-127">Enable Retention policy</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d69-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c5d69-128">-RetentionInDays</span></span>
<span data-ttu-id="c5d69-129">보존 정책의 보존 기간(일)</span><span class="sxs-lookup"><span data-stu-id="c5d69-129">Retention days for retention policy</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d69-130">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="c5d69-130">-TimeGrain</span></span>
<span data-ttu-id="c5d69-131">메트릭 설정에 대한 TimeGrain</span><span class="sxs-lookup"><span data-stu-id="c5d69-131">TimeGrain for metric setting</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: MetricSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5d69-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d69-132">CommonParameters</span></span>
<span data-ttu-id="c5d69-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c5d69-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d69-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c5d69-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d69-135">입력</span><span class="sxs-lookup"><span data-stu-id="c5d69-135">INPUTS</span></span>

### <span data-ttu-id="c5d69-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c5d69-136">System.String</span></span>

## <span data-ttu-id="c5d69-137">출력</span><span class="sxs-lookup"><span data-stu-id="c5d69-137">OUTPUTS</span></span>

### <span data-ttu-id="c5d69-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span><span class="sxs-lookup"><span data-stu-id="c5d69-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings</span></span>

## <span data-ttu-id="c5d69-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c5d69-139">NOTES</span></span>

## <span data-ttu-id="c5d69-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5d69-140">RELATED LINKS</span></span>
