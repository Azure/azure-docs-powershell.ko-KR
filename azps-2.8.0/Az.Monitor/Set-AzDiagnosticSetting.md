---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: d41d99993961906f88dc500603f74fc1a0d4fdf0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404924"
---
# <span data-ttu-id="4d3b0-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="4d3b0-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="4d3b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d3b0-102">SYNOPSIS</span></span>
<span data-ttu-id="4d3b0-103">리소스에 대한 로그 및 메트릭 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="4d3b0-104">구문</span><span class="sxs-lookup"><span data-stu-id="4d3b0-104">SYNTAX</span></span>

### <span data-ttu-id="4d3b0-105">OldSetDiagnosticSetting(기본값)</span><span class="sxs-lookup"><span data-stu-id="4d3b0-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d3b0-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="4d3b0-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d3b0-107">설명</span><span class="sxs-lookup"><span data-stu-id="4d3b0-107">DESCRIPTION</span></span>
<span data-ttu-id="4d3b0-108">**Set-AzDiagnosticSetting** cmdlet은 특정 리소스에 대한 각 시간 조직 및 로그 범주를 활성화하거나 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="4d3b0-109">로그 및 메트릭은 지정된 저장소 계정에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="4d3b0-110">이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 리소스를 실제로 만들거나 수정하거나 제거하기 전에 사용자로부터 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="4d3b0-111">예제</span><span class="sxs-lookup"><span data-stu-id="4d3b0-111">EXAMPLES</span></span>

### <span data-ttu-id="4d3b0-112">예제 1: 리소스에 대한 모든 메트릭 및 로그 사용</span><span class="sxs-lookup"><span data-stu-id="4d3b0-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="4d3b0-113">이 명령은 Resource01에 사용 가능한 모든 메트릭 및 로그를 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="4d3b0-114">예제 2: 모든 메트릭 및 로그 비활성화</span><span class="sxs-lookup"><span data-stu-id="4d3b0-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="4d3b0-115">이 명령은 리소스 Resource01에 사용 가능한 모든 메트릭 및 로그를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="4d3b0-116">예제 3: 여러 메트릭 범주 사용/사용 안 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="4d3b0-116">Example 3: Enable/disable multiple metrics categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False -MetricCategory MetricCategory1,MetricCategory2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="4d3b0-117">이 명령은 Category1 및 Category2라는 메트릭 범주를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-117">This command disables the metrics categories called Category1 and Category2.</span></span>
<span data-ttu-id="4d3b0-118">다른 모든 범주는 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="4d3b0-119">예제 4: 여러 로그 범주 사용/사용 안 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="4d3b0-119">Example 4: Enable/disable multiple log categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="4d3b0-120">이 명령은 Category1 및 Category2를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="4d3b0-121">다른 모든 메트릭 및 로그 범주는 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="4d3b0-122">예제 4: 시간 세분화 및 여러 범주 사용</span><span class="sxs-lookup"><span data-stu-id="4d3b0-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="4d3b0-123">이 명령은 Category1, Category2 및 time grain PT1M만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="4d3b0-124">다른 모든 시간 세분화 및 범주는 모두 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="4d3b0-125">예제 5: 파이프라인 사용</span><span class="sxs-lookup"><span data-stu-id="4d3b0-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting
```

<span data-ttu-id="4d3b0-126">이 명령은 PowerShell 파이프라인을 사용하여 진단 설정을 설정(변경하지 않습니다)합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-126">This command uses the PowerShell pipeline to set (not change made) a diagnostic setting.</span></span>

## <span data-ttu-id="4d3b0-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d3b0-127">PARAMETERS</span></span>

### <span data-ttu-id="4d3b0-128">-Category</span><span class="sxs-lookup"><span data-stu-id="4d3b0-128">-Category</span></span>
<span data-ttu-id="4d3b0-129">사용 값에 따라 활성화 또는 비활성화할 로그 범주 목록을 *지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="4d3b0-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="4d3b0-130">범주를 지정하지 않으면 이 명령은 지원되는 모든 범주에서 작동됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-130">If no category is specified, this command operates on all supported categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3b0-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d3b0-131">-DefaultProfile</span></span>
<span data-ttu-id="4d3b0-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4d3b0-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d3b0-133">-Enabled</span><span class="sxs-lookup"><span data-stu-id="4d3b0-133">-Enabled</span></span>
<span data-ttu-id="4d3b0-134">진단을 사용하도록 설정할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="4d3b0-135">진단을 $True 또는 진단을 사용하지 않도록 설정하는 $False 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3b0-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="4d3b0-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="4d3b0-137">이벤트 허브 권한 부여 규칙 ID</span><span class="sxs-lookup"><span data-stu-id="4d3b0-137">The event hub authorization rule id</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3b0-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="4d3b0-138">-EventHubName</span></span>
<span data-ttu-id="4d3b0-139">이벤트 허브 이름</span><span class="sxs-lookup"><span data-stu-id="4d3b0-139">The event hub name</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3b0-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d3b0-140">-InputObject</span></span>
<span data-ttu-id="4d3b0-141">입력 개체(파이프라인에서 가능) 이름 및 resourceId는 이 개체에서 추출됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-141">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings
Parameter Sets: NewSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3b0-142">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="4d3b0-142">-MetricCategory</span></span>
<span data-ttu-id="4d3b0-143">메트릭 범주 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-143">The list of metric categories.</span></span>
<span data-ttu-id="4d3b0-144">범주를 지정하지 않으면 이 명령은 지원되는 모든 범주에서 작동됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-144">If no category is specified, this command operates on all supported categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3b0-145">-Name</span><span class="sxs-lookup"><span data-stu-id="4d3b0-145">-Name</span></span>
<span data-ttu-id="4d3b0-146">진단 설정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-146">The name of the diagnostic setting.</span></span> <span data-ttu-id="4d3b0-147">기본값은 **서비스입니다.**</span><span class="sxs-lookup"><span data-stu-id="4d3b0-147">The default value is **service**.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3b0-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d3b0-148">-ResourceId</span></span>
<span data-ttu-id="4d3b0-149">리소스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-149">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3b0-150">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="4d3b0-150">-RetentionEnabled</span></span>
<span data-ttu-id="4d3b0-151">진단 정보의 보존을 사용하도록 설정되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-151">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3b0-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="4d3b0-152">-RetentionInDays</span></span>
<span data-ttu-id="4d3b0-153">보존 정책(일)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-153">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3b0-154">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="4d3b0-154">-ServiceBusRuleId</span></span>
<span data-ttu-id="4d3b0-155">Service Bus 규칙 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-155">The Service Bus Rule id.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3b0-156">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4d3b0-156">-StorageAccountId</span></span>
<span data-ttu-id="4d3b0-157">데이터를 저장할 Storage 계정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-157">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3b0-158">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="4d3b0-158">-Timegrain</span></span>
<span data-ttu-id="4d3b0-159">Enabled 값에 따라 메트릭에 대해 사용 또는 사용하지 않도록 설정할 시간 단위를 *지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="4d3b0-159">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="4d3b0-160">시간 알을 지정하지 않으면 이 명령은 사용 가능한 모든 시간 세분화에서 작동됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-160">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3b0-161">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="4d3b0-161">-WorkspaceId</span></span>
<span data-ttu-id="4d3b0-162">로그/메트릭을 보낼 Log Analytics 작업 영역의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="4d3b0-162">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3b0-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d3b0-163">-Confirm</span></span>
<span data-ttu-id="4d3b0-164">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d3b0-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d3b0-165">-WhatIf</span></span>
<span data-ttu-id="4d3b0-166">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4d3b0-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d3b0-167">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-167">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d3b0-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d3b0-168">CommonParameters</span></span>
<span data-ttu-id="4d3b0-169">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d3b0-170">자세한 내용은 [다음](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4d3b0-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d3b0-171">입력</span><span class="sxs-lookup"><span data-stu-id="4d3b0-171">INPUTS</span></span>

### <span data-ttu-id="4d3b0-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="4d3b0-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="4d3b0-173">System.String</span><span class="sxs-lookup"><span data-stu-id="4d3b0-173">System.String</span></span>

### <span data-ttu-id="4d3b0-174">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d3b0-174">System.Boolean</span></span>

### <span data-ttu-id="4d3b0-175">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4d3b0-175">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4d3b0-176">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4d3b0-176">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4d3b0-177">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4d3b0-177">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4d3b0-178">출력</span><span class="sxs-lookup"><span data-stu-id="4d3b0-178">OUTPUTS</span></span>

### <span data-ttu-id="4d3b0-179">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="4d3b0-179">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="4d3b0-180">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4d3b0-180">NOTES</span></span>

## <span data-ttu-id="4d3b0-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d3b0-181">RELATED LINKS</span></span>

<span data-ttu-id="4d3b0-182">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="4d3b0-182">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
