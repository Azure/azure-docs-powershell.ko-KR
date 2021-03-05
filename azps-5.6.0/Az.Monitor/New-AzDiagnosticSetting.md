---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDiagnosticSetting.md
ms.openlocfilehash: e38eef2213785ccb2840db933b74833289ec3c53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984522"
---
# <span data-ttu-id="d4347-101">New-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="d4347-101">New-AzDiagnosticSetting</span></span>

## <span data-ttu-id="d4347-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4347-102">SYNOPSIS</span></span>
<span data-ttu-id="d4347-103">PSServiceDiagnosticSettings 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d4347-103">Create PSServiceDiagnosticSettings object.</span></span>

## <span data-ttu-id="d4347-104">구문</span><span class="sxs-lookup"><span data-stu-id="d4347-104">SYNTAX</span></span>

```
New-AzDiagnosticSetting -TargetResourceId <String> -Name <String> [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-WorkspaceId <String>] [-DedicatedLogAnalyticsDestinationType] [-Setting <PSDiagnosticDetailSettings[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4347-105">설명</span><span class="sxs-lookup"><span data-stu-id="d4347-105">DESCRIPTION</span></span>
<span data-ttu-id="d4347-106">PSServiceDiagnosticSettings 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d4347-106">Create PSServiceDiagnosticSettings object.</span></span>
<span data-ttu-id="d4347-107">이 매개 변수로 사용할 `-InputObject` 수 있습니다. `Set-AzDiagnosticSetting`</span><span class="sxs-lookup"><span data-stu-id="d4347-107">This can be used as parameter `-InputObject` for `Set-AzDiagnosticSetting`</span></span>

## <span data-ttu-id="d4347-108">예제</span><span class="sxs-lookup"><span data-stu-id="d4347-108">EXAMPLES</span></span>

### <span data-ttu-id="d4347-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="d4347-109">Example 1</span></span>
```powershell
$TimeGrain=New-TimeSpan -Days 90
$metric = New-AzDiagnosticDetailSetting -Metric -RetentionInDays 1 -RetentionEnabled -Category AllMetrics
$log = New-AzDiagnosticDetailSetting -Log -RetentionInDays 1 -RetentionEnabled -Category Audit -Enabled
$setting = New-AzDiagnosticSetting -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX -Name diagnostic-test -WorkspaceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX -DedicatedLogAnalyticsDestinationType -Setting $log,$metric
Location                    :
Tags                        :
Id                          : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/diagnosticSettings/diagnostic-test
Name                        : diagnostic-test
StorageAccountId            :
ServiceBusRuleId            :
EventHubAuthorizationRuleId :
EventHubName                :
Metrics
    TimeGrain       :
    Category        : AllMetrics
    Enabled         : False
    RetentionPolicy
    Enabled : True
    Days    : 1


Logs
    Category        : Audit
    Enabled         : True
    RetentionPolicy
    Enabled : True
    Days    : 1


WorkspaceId                 : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.OperationalInsights/workspaces/XXXXXXXXX
LogAnalyticsDestinationType : Dedicated
Type                        :

Set-AzDiagnosticSetting -InputObject $setting
```

<span data-ttu-id="d4347-110">PSServiceDiagnosticSettings 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d4347-110">Create PSServiceDiagnosticSettings object.</span></span> <span data-ttu-id="d4347-111">대상 리소스에 대한 진단 설정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4347-111">And create diagnostic setting for target resource.</span></span>

## <span data-ttu-id="d4347-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d4347-112">PARAMETERS</span></span>

### <span data-ttu-id="d4347-113">-DedicatedLogAnalyticsDestinationType</span><span class="sxs-lookup"><span data-stu-id="d4347-113">-DedicatedLogAnalyticsDestinationType</span></span>
<span data-ttu-id="d4347-114">리소스별(있는 경우) 또는 AzureDiagnostics(기본값, 존재하지 않는 경우)로 내보낼지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d4347-114">The value indicating whether to export (to ODS) to resource-specific (if present) or to AzureDiagnostics (default, not present)</span></span>

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

### <span data-ttu-id="d4347-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4347-115">-DefaultProfile</span></span>
<span data-ttu-id="d4347-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4347-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4347-117">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="d4347-117">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="d4347-118">이벤트 허브 규칙 ID</span><span class="sxs-lookup"><span data-stu-id="d4347-118">The event hub rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4347-119">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="d4347-119">-EventHubName</span></span>
<span data-ttu-id="d4347-120">Service Bus 규칙 ID</span><span class="sxs-lookup"><span data-stu-id="d4347-120">The service bus rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4347-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d4347-121">-Name</span></span>
<span data-ttu-id="d4347-122">진단 설정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4347-122">The name of the diagnostic setting.</span></span>
<span data-ttu-id="d4347-123">기본값은 'service'입니다.</span><span class="sxs-lookup"><span data-stu-id="d4347-123">Defaults to 'service'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4347-124">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="d4347-124">-ServiceBusRuleId</span></span>
<span data-ttu-id="d4347-125">Service Bus 규칙 ID</span><span class="sxs-lookup"><span data-stu-id="d4347-125">The service bus rule id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4347-126">-설정</span><span class="sxs-lookup"><span data-stu-id="d4347-126">-Setting</span></span>
<span data-ttu-id="d4347-127">메트릭 설정 또는 로그 설정</span><span class="sxs-lookup"><span data-stu-id="d4347-127">Metric settings or Log settings</span></span>

```yaml
Type: PSDiagnosticDetailSettings[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4347-128">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d4347-128">-StorageAccountId</span></span>
<span data-ttu-id="d4347-129">저장소 계정 ID</span><span class="sxs-lookup"><span data-stu-id="d4347-129">The storage account id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4347-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d4347-130">-TargetResourceId</span></span>
<span data-ttu-id="d4347-131">리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d4347-131">The resource id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4347-132">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="d4347-132">-WorkspaceId</span></span>
<span data-ttu-id="d4347-133">로그/메트릭을 보내기 위해 Log Analytics 작업 영역의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d4347-133">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4347-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4347-134">CommonParameters</span></span>
<span data-ttu-id="d4347-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d4347-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4347-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4347-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4347-137">입력</span><span class="sxs-lookup"><span data-stu-id="d4347-137">INPUTS</span></span>

### <span data-ttu-id="d4347-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d4347-138">System.String</span></span>

### <span data-ttu-id="d4347-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d4347-139">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d4347-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings[]</span><span class="sxs-lookup"><span data-stu-id="d4347-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticDetailSettings[]</span></span>

## <span data-ttu-id="d4347-141">출력</span><span class="sxs-lookup"><span data-stu-id="d4347-141">OUTPUTS</span></span>

### <span data-ttu-id="d4347-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="d4347-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="d4347-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d4347-143">NOTES</span></span>

## <span data-ttu-id="d4347-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4347-144">RELATED LINKS</span></span>
