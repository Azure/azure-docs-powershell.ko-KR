---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: 7c33c351b7daea7b39fd614a8d842a4ed8be7f2b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700786"
---
# <span data-ttu-id="a19fc-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="a19fc-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="a19fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a19fc-102">SYNOPSIS</span></span>
<span data-ttu-id="a19fc-103">리소스에 대 한 로그 및 메트릭 설정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="a19fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a19fc-104">SYNTAX</span></span>

### <span data-ttu-id="a19fc-105">OldSetDiagnosticSetting (기본값)</span><span class="sxs-lookup"><span data-stu-id="a19fc-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a19fc-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="a19fc-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a19fc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a19fc-107">DESCRIPTION</span></span>
<span data-ttu-id="a19fc-108">**AzDiagnosticSetting** cmdlet은 특정 리소스에 대해 각 시간 세분화 및 로그 범주를 사용 하거나 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="a19fc-109">로그 및 메트릭은 지정 된 저장소 계정에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="a19fc-110">이 cmdlet은 ShouldProcess 패턴을 구현 합니다. 즉, 리소스를 실제로 생성, 수정 또는 제거 하기 전에 사용자에 게 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="a19fc-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a19fc-111">EXAMPLES</span></span>

### <span data-ttu-id="a19fc-112">예제 1: 리소스에 대 한 모든 메트릭 및 로그 사용</span><span class="sxs-lookup"><span data-stu-id="a19fc-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="a19fc-113">이 명령은 Resource01에 대해 사용 가능한 모든 메트릭과 로그를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="a19fc-114">예제 2: 모든 메트릭 및 로그 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="a19fc-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="a19fc-115">이 명령은 리소스 Resource01 사용할 수 있는 모든 메트릭 및 로그를 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="a19fc-116">예제 3: 여러 메트릭 범주 사용/사용 안 함</span><span class="sxs-lookup"><span data-stu-id="a19fc-116">Example 3: Enable/disable multiple metrics categories</span></span>
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

<span data-ttu-id="a19fc-117">이 명령은 Category1 및 Category2 이라는 메트릭 cateories를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-117">This command disables the metrics cateories called Category1 and Category2.</span></span>
<span data-ttu-id="a19fc-118">다른 모든 범주는 동일 하 게 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="a19fc-119">예제 4: 여러 로그 범주 사용/사용 안 함</span><span class="sxs-lookup"><span data-stu-id="a19fc-119">Example 4: Enable/disable multiple log categories</span></span>
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

<span data-ttu-id="a19fc-120">이 명령은 Category1 및 Category2를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="a19fc-121">다른 모든 메트릭과 로그 범주는 동일 하 게 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="a19fc-122">예제 4: 시간 세분화 및 여러 범주 사용</span><span class="sxs-lookup"><span data-stu-id="a19fc-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="a19fc-123">이 명령은 Category1, Category2 및 시간 세분화 PT1M만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="a19fc-124">다른 모든 시간 grains 및 범주는 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="a19fc-125">예제 5: 파이프라인 사용</span><span class="sxs-lookup"><span data-stu-id="a19fc-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting
```

<span data-ttu-id="a19fc-126">이 명령은 PowerShell 파이프라인을 사용 하 여 진단 설정을 설정 (변경 하지 않음) 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-126">This command uses the PowerShell pipeline to set (not change made) a diagnostic setting.</span></span>

## <span data-ttu-id="a19fc-127">변수</span><span class="sxs-lookup"><span data-stu-id="a19fc-127">PARAMETERS</span></span>

### <span data-ttu-id="a19fc-128">-범주</span><span class="sxs-lookup"><span data-stu-id="a19fc-128">-Category</span></span>
<span data-ttu-id="a19fc-129">사용 *가능* 값에 따라 사용 하거나 사용 하지 않도록 설정할 로그 범주 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="a19fc-130">범주를 지정 하지 않으면이 명령은 지원 되는 모든 범주에 대해 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-130">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="a19fc-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a19fc-131">-DefaultProfile</span></span>
<span data-ttu-id="a19fc-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a19fc-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a19fc-133">-사용</span><span class="sxs-lookup"><span data-stu-id="a19fc-133">-Enabled</span></span>
<span data-ttu-id="a19fc-134">진단을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="a19fc-135">진단 기능을 사용 하도록 $True를 지정 하거나 진단을 사용 하지 않도록 $False 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="a19fc-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="a19fc-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="a19fc-137">이벤트 허브 인증 규칙 id</span><span class="sxs-lookup"><span data-stu-id="a19fc-137">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="a19fc-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="a19fc-138">-EventHubName</span></span>
<span data-ttu-id="a19fc-139">이벤트 허브 이름</span><span class="sxs-lookup"><span data-stu-id="a19fc-139">The event hub name</span></span>

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

### <span data-ttu-id="a19fc-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a19fc-140">-InputObject</span></span>
<span data-ttu-id="a19fc-141">입력 개체 (파이프라인에서 가능) 이름 및 resourceId가이 개체에서 추출 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-141">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="a19fc-142">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="a19fc-142">-MetricCategory</span></span>
<span data-ttu-id="a19fc-143">메트릭 범주 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-143">The list of metric categories.</span></span> <span data-ttu-id="a19fc-144">범주를 지정 하지 않으면이 명령은 지원 되는 모든 범주에 대해 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-144">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="a19fc-145">-이름</span><span class="sxs-lookup"><span data-stu-id="a19fc-145">-Name</span></span>
<span data-ttu-id="a19fc-146">진단 설정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-146">The name of the diagnostic setting.</span></span> <span data-ttu-id="a19fc-147">기본 값은 **서비스** 입니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-147">The default value is **service**.</span></span>

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

### <span data-ttu-id="a19fc-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a19fc-148">-ResourceId</span></span>
<span data-ttu-id="a19fc-149">리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-149">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="a19fc-150">-보존 설정</span><span class="sxs-lookup"><span data-stu-id="a19fc-150">-RetentionEnabled</span></span>
<span data-ttu-id="a19fc-151">진단 정보의 보존을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-151">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="a19fc-152">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="a19fc-152">-RetentionInDays</span></span>
<span data-ttu-id="a19fc-153">보존 정책을 일 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-153">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="a19fc-154">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="a19fc-154">-ServiceBusRuleId</span></span>
<span data-ttu-id="a19fc-155">서비스 버스 규칙 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-155">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="a19fc-156">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a19fc-156">-StorageAccountId</span></span>
<span data-ttu-id="a19fc-157">데이터를 저장할 저장소 계정의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-157">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="a19fc-158">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="a19fc-158">-Timegrain</span></span>
<span data-ttu-id="a19fc-159">*사용* 값에 따라 메트릭을 사용 하거나 사용 하지 않도록 설정 하는 시간 grains 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-159">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="a19fc-160">시간 세분화를 지정 하지 않으면이 명령은 사용 가능한 모든 시간 grains에 대해 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-160">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="a19fc-161">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="a19fc-161">-WorkspaceId</span></span>
<span data-ttu-id="a19fc-162">작업 영역의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-162">The Id of the workspace</span></span>

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

### <span data-ttu-id="a19fc-163">-확인</span><span class="sxs-lookup"><span data-stu-id="a19fc-163">-Confirm</span></span>
<span data-ttu-id="a19fc-164">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a19fc-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a19fc-165">-WhatIf</span></span>
<span data-ttu-id="a19fc-166">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a19fc-167">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a19fc-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a19fc-168">CommonParameters</span></span>
<span data-ttu-id="a19fc-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a19fc-170">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a19fc-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a19fc-171">입력</span><span class="sxs-lookup"><span data-stu-id="a19fc-171">INPUTS</span></span>

### <span data-ttu-id="a19fc-172">PSServiceDiagnosticSettings를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="a19fc-173">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a19fc-173">System.String</span></span>

### <span data-ttu-id="a19fc-174">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a19fc-174">System.Boolean</span></span>

### <span data-ttu-id="a19fc-175">System.webserver. List ' 1 [[System.webserver], CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a19fc-175">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a19fc-176">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a19fc-176">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a19fc-177">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="a19fc-177">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a19fc-178">출력</span><span class="sxs-lookup"><span data-stu-id="a19fc-178">OUTPUTS</span></span>

### <span data-ttu-id="a19fc-179">PSServiceDiagnosticSettings를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="a19fc-179">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="a19fc-180">상속자</span><span class="sxs-lookup"><span data-stu-id="a19fc-180">NOTES</span></span>

## <span data-ttu-id="a19fc-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a19fc-181">RELATED LINKS</span></span>

<span data-ttu-id="a19fc-182">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [제거-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="a19fc-182">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
