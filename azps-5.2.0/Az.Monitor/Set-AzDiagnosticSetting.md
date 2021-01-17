---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: eeadf64c83f62a8d245a7ace8f750b34ddc230ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361978"
---
# <span data-ttu-id="74060-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="74060-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="74060-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74060-102">SYNOPSIS</span></span>
<span data-ttu-id="74060-103">리소스에 대한 로그 및 메트릭 설정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="74060-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="74060-104">구문</span><span class="sxs-lookup"><span data-stu-id="74060-104">SYNTAX</span></span>

### <span data-ttu-id="74060-105">OldSetDiagnosticSetting(기본값)</span><span class="sxs-lookup"><span data-stu-id="74060-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-ExportToResourceSpecific] [-EnableLog <Boolean>]
 [-EnableMetrics <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74060-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="74060-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74060-107">설명</span><span class="sxs-lookup"><span data-stu-id="74060-107">DESCRIPTION</span></span>
<span data-ttu-id="74060-108">**Set-AzDiagnosticSetting** cmdlet은 특정 리소스에 대한 각 시간 조직 및 로그 범주를 활성화하거나 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="74060-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="74060-109">로그 및 메트릭은 지정된 저장소 계정에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="74060-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="74060-110">이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 리소스를 실제로 만들거나 수정하거나 제거하기 전에 사용자로부터 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74060-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="74060-111">예제</span><span class="sxs-lookup"><span data-stu-id="74060-111">EXAMPLES</span></span>

### <span data-ttu-id="74060-112">예제 1: 리소스에 대한 모든 메트릭 및 로그 사용</span><span class="sxs-lookup"><span data-stu-id="74060-112">Example 1: Enable all metrics and logs for a resource</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="74060-113">이 명령은 Resource01에 사용 가능한 모든 메트릭 및 로그를 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="74060-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="74060-114">예제 2: 모든 메트릭 및 로그 비활성화</span><span class="sxs-lookup"><span data-stu-id="74060-114">Example 2: Disable all metrics and logs</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="74060-115">이 명령은 리소스 Resource01에 사용 가능한 모든 메트릭 및 로그를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="74060-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="74060-116">예제 3: 여러 메트릭 범주 사용/사용 안 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="74060-116">Example 3: Enable/disable multiple metrics categories</span></span>
```powershell
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

<span data-ttu-id="74060-117">이 명령은 Category1 및 Category2라는 메트릭 범주를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="74060-117">This command disables the metrics categories called Category1 and Category2.</span></span>
<span data-ttu-id="74060-118">다른 모든 범주는 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="74060-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="74060-119">예제 4: 여러 로그 범주 사용/사용 안 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="74060-119">Example 4: Enable/disable multiple log categories</span></span>
```powershell
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

<span data-ttu-id="74060-120">이 명령은 Category1 및 Category2를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74060-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="74060-121">다른 모든 메트릭 및 로그 범주는 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="74060-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="74060-122">예제 5: 시간 세분화 및 여러 범주 사용</span><span class="sxs-lookup"><span data-stu-id="74060-122">Example 5: Enable a time grain and multiple categories</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="74060-123">이 명령은 Category1, Category2 및 time grain PT1M만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="74060-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="74060-124">다른 모든 시간 세분화 및 범주는 서로 다른 것이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="74060-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="74060-125">예제 6: 파이프라인 사용</span><span class="sxs-lookup"><span data-stu-id="74060-125">Example 6: Using pipeline</span></span>
```powershell
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting -Enabled $True -Category Category1,Category2
```

<span data-ttu-id="74060-126">이 명령은 PowerShell 파이프라인을 사용하여 진단 설정을 설정(변경하지 않습니다)합니다.</span><span class="sxs-lookup"><span data-stu-id="74060-126">This command uses the PowerShell pipeline to set (no change made) a diagnostic setting.</span></span>

## <span data-ttu-id="74060-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74060-127">PARAMETERS</span></span>

### <span data-ttu-id="74060-128">-Category</span><span class="sxs-lookup"><span data-stu-id="74060-128">-Category</span></span>
<span data-ttu-id="74060-129">사용 값에 따라 활성화 또는 비활성화할 로그 범주 목록을 *지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="74060-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="74060-130">범주를 지정하지 않으면 이 명령은 지원되는 모든 범주에서 작동됩니다.</span><span class="sxs-lookup"><span data-stu-id="74060-130">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="74060-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74060-131">-DefaultProfile</span></span>
<span data-ttu-id="74060-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="74060-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74060-133">-Enabled</span><span class="sxs-lookup"><span data-stu-id="74060-133">-Enabled</span></span>
<span data-ttu-id="74060-134">진단을 사용하도록 설정할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="74060-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="74060-135">진단을 $True 또는 진단을 사용하지 않도록 설정하려면 $False 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="74060-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="74060-136">-EnableLog</span><span class="sxs-lookup"><span data-stu-id="74060-136">-EnableLog</span></span>
<span data-ttu-id="74060-137">진단 로그를 사용할지 또는 사용하지 않도록 설정해야 하는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="74060-137">The value indicating whether the diagnostic logs should be enabled or disabled</span></span>

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

### <span data-ttu-id="74060-138">-EnableMetrics</span><span class="sxs-lookup"><span data-stu-id="74060-138">-EnableMetrics</span></span>
<span data-ttu-id="74060-139">진단 메트릭을 사용할지 또는 사용하지 않도록 설정해야 하는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="74060-139">The value indicating whether the diagnostic metrics should be enabled or disabled</span></span>

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

### <span data-ttu-id="74060-140">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="74060-140">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="74060-141">이벤트 허브 권한 부여 규칙 ID</span><span class="sxs-lookup"><span data-stu-id="74060-141">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="74060-142">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="74060-142">-EventHubName</span></span>
<span data-ttu-id="74060-143">이벤트 허브 이름</span><span class="sxs-lookup"><span data-stu-id="74060-143">The event hub name</span></span>

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

### <span data-ttu-id="74060-144">-ExportToResourceSpecific</span><span class="sxs-lookup"><span data-stu-id="74060-144">-ExportToResourceSpecific</span></span>
<span data-ttu-id="74060-145">LA로 내보내기를 리소스 특정 테이블(즉,</span><span class="sxs-lookup"><span data-stu-id="74060-145">Flag indicating that the export to LA must be done to a resource specific table, a.k.a.</span></span> <span data-ttu-id="74060-146">**AzureDiagnostics라는** 기본 동적  SCHEMA 테이블과는 반대로 전용 또는 고정된 스마마 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="74060-146">dedicated or fixed schema table, as opposed to the **default** dynamic schema table called **AzureDiagnostics**.</span></span>

<span data-ttu-id="74060-147">이 인수는 **-workspaceId** 인수도 제공된 경우 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="74060-147">This argument is effective only when the argument **-workspaceId** is also given.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74060-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74060-148">-InputObject</span></span>
<span data-ttu-id="74060-149">입력 개체(파이프라인에서 가능) 이름 및 resourceId는 이 개체에서 추출됩니다.</span><span class="sxs-lookup"><span data-stu-id="74060-149">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="74060-150">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="74060-150">-MetricCategory</span></span>
<span data-ttu-id="74060-151">메트릭 범주 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="74060-151">The list of metric categories.</span></span> <span data-ttu-id="74060-152">범주를 지정하지 않으면 이 명령은 지원되는 모든 범주에서 작동됩니다.</span><span class="sxs-lookup"><span data-stu-id="74060-152">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="74060-153">-Name</span><span class="sxs-lookup"><span data-stu-id="74060-153">-Name</span></span>
<span data-ttu-id="74060-154">진단 설정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74060-154">The name of the diagnostic setting.</span></span> <span data-ttu-id="74060-155">기본값은 **서비스입니다.**</span><span class="sxs-lookup"><span data-stu-id="74060-155">The default value is **service**.</span></span>

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

### <span data-ttu-id="74060-156">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74060-156">-ResourceId</span></span>
<span data-ttu-id="74060-157">리소스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="74060-157">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="74060-158">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="74060-158">-RetentionEnabled</span></span>
<span data-ttu-id="74060-159">진단 정보의 보존을 사용하도록 설정되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="74060-159">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="74060-160">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="74060-160">-RetentionInDays</span></span>
<span data-ttu-id="74060-161">보존 정책(일)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="74060-161">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="74060-162">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="74060-162">-ServiceBusRuleId</span></span>
<span data-ttu-id="74060-163">Service Bus 규칙 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="74060-163">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="74060-164">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="74060-164">-StorageAccountId</span></span>
<span data-ttu-id="74060-165">데이터를 저장할 Storage 계정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="74060-165">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="74060-166">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="74060-166">-Timegrain</span></span>
<span data-ttu-id="74060-167">Enabled 값에 따라 메트릭에 대해 사용 또는 사용하지 않도록 설정할 시간 단위를 *지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="74060-167">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="74060-168">시간 알을 지정하지 않으면 이 명령은 사용 가능한 모든 시간 세분화에서 작동됩니다.</span><span class="sxs-lookup"><span data-stu-id="74060-168">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="74060-169">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="74060-169">-WorkspaceId</span></span>
<span data-ttu-id="74060-170">로그/메트릭을 보낼 Log Analytics 작업 영역의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="74060-170">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

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

### <span data-ttu-id="74060-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74060-171">-Confirm</span></span>
<span data-ttu-id="74060-172">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="74060-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74060-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74060-173">-WhatIf</span></span>
<span data-ttu-id="74060-174">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="74060-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74060-175">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74060-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74060-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74060-176">CommonParameters</span></span>
<span data-ttu-id="74060-177">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74060-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74060-178">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="74060-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74060-179">입력</span><span class="sxs-lookup"><span data-stu-id="74060-179">INPUTS</span></span>

### <span data-ttu-id="74060-180">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="74060-180">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="74060-181">System.String</span><span class="sxs-lookup"><span data-stu-id="74060-181">System.String</span></span>

### <span data-ttu-id="74060-182">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="74060-182">System.Boolean</span></span>

### <span data-ttu-id="74060-183">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="74060-183">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="74060-184">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="74060-184">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="74060-185">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="74060-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="74060-186">출력</span><span class="sxs-lookup"><span data-stu-id="74060-186">OUTPUTS</span></span>

### <span data-ttu-id="74060-187">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="74060-187">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="74060-188">참고 사항</span><span class="sxs-lookup"><span data-stu-id="74060-188">NOTES</span></span>

## <span data-ttu-id="74060-189">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74060-189">RELATED LINKS</span></span>

<span data-ttu-id="74060-190">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="74060-190">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
