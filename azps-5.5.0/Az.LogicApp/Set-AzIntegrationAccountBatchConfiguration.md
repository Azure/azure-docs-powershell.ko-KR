---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 443f93d6e9099986c9412730ba24eae3655a2b48
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194201"
---
# <span data-ttu-id="c4ecd-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4ecd-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="c4ecd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4ecd-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ecd-103">통합 계정 일괄 처리 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="c4ecd-104">구문</span><span class="sxs-lookup"><span data-stu-id="c4ecd-104">SYNTAX</span></span>

### <span data-ttu-id="c4ecd-105">ByIntegrationAccountAndParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="c4ecd-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4ecd-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="c4ecd-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4ecd-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="c4ecd-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4ecd-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="c4ecd-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4ecd-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="c4ecd-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4ecd-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="c4ecd-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4ecd-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="c4ecd-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4ecd-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="c4ecd-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4ecd-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="c4ecd-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4ecd-114">설명</span><span class="sxs-lookup"><span data-stu-id="c4ecd-114">DESCRIPTION</span></span>
<span data-ttu-id="c4ecd-115">**Set-AzIntegrationAccountBatchConfiguration** cmdlet은 통합 계정 일괄 처리 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="c4ecd-116">예제</span><span class="sxs-lookup"><span data-stu-id="c4ecd-116">EXAMPLES</span></span>

### <span data-ttu-id="c4ecd-117">예제 1: 로컬 파일을 사용하여 일괄 처리 구성 수정</span><span class="sxs-lookup"><span data-stu-id="c4ecd-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="c4ecd-118">"$batchConfigurationFilePath"에 포함된 파일 경로에 있는 로컬 파일을 사용하여 "sampleBatchConfig"라는 배치 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="c4ecd-119">예제 2: JSON 문자열을 사용하여 일괄 처리 구성 수정</span><span class="sxs-lookup"><span data-stu-id="c4ecd-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="c4ecd-120">"$batchConfigurationContent"에 포함된 JSON 문자열을 사용하여 "sampleBatchConfig"라는 배치 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="c4ecd-121">예제 3: 매개 변수를 사용하여 일괄 처리 구성 수정</span><span class="sxs-lookup"><span data-stu-id="c4ecd-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="c4ecd-122">필요한 모든 매개 변수를 수동으로 제공하여 "sampleBatchConfig"라는 일괄 처리 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="c4ecd-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4ecd-123">PARAMETERS</span></span>

### <span data-ttu-id="c4ecd-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="c4ecd-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="c4ecd-125">통합 계정 일괄 처리 구성 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-125">The integration account batch configuration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndJson, ByInputObjectAndJson, ByResourceIdAndJson
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecd-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="c4ecd-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="c4ecd-127">통합 계정 일괄 처리 구성 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-127">The integration account batch configuration file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecd-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="c4ecd-128">-BatchGroupName</span></span>
<span data-ttu-id="c4ecd-129">통합 계정 일괄 처리 구성 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-129">The integration account batch configuration group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecd-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="c4ecd-130">-BatchSize</span></span>
<span data-ttu-id="c4ecd-131">통합 계정 일괄 처리 구성 일괄 처리 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-131">The integration account batch configuration batch size.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecd-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4ecd-132">-DefaultProfile</span></span>
<span data-ttu-id="c4ecd-133">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4ecd-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4ecd-134">-InputObject</span></span>
<span data-ttu-id="c4ecd-135">통합 계정 일괄 처리 구성</span><span class="sxs-lookup"><span data-stu-id="c4ecd-135">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecd-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="c4ecd-136">-MessageCount</span></span>
<span data-ttu-id="c4ecd-137">통합 계정 일괄 처리 구성 메시지 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-137">The integration account batch configuration message count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecd-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c4ecd-138">-Metadata</span></span>
<span data-ttu-id="c4ecd-139">통합 계정 일괄 처리 구성 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-139">The integration account batch configuration metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecd-140">-Name</span><span class="sxs-lookup"><span data-stu-id="c4ecd-140">-Name</span></span>
<span data-ttu-id="c4ecd-141">통합 계정 일괄 처리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-141">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecd-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="c4ecd-142">-ParentName</span></span>
<span data-ttu-id="c4ecd-143">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-143">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecd-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4ecd-144">-ResourceGroupName</span></span>
<span data-ttu-id="c4ecd-145">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecd-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4ecd-146">-ResourceId</span></span>
<span data-ttu-id="c4ecd-147">통합 계정 일괄 처리 구성 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-147">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndJson, ByResourceIdAndFilePath, ByResourceIdAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecd-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="c4ecd-148">-ScheduleFrequency</span></span>
<span data-ttu-id="c4ecd-149">통합 계정 일괄 처리 구성 일정 빈도입니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-149">The integration account batch configuration schedule frequency.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:
Accepted values: Month, Week, Day, Hour, Minute, Second

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecd-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="c4ecd-150">-ScheduleInterval</span></span>
<span data-ttu-id="c4ecd-151">통합 계정 일괄 처리 구성 일정 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-151">The integration account batch configuration schedule interval.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecd-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="c4ecd-152">-ScheduleStartTime</span></span>
<span data-ttu-id="c4ecd-153">통합 계정 일괄 처리 구성 일정 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-153">The integration account batch configuration schedule start time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecd-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="c4ecd-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="c4ecd-155">통합 계정 일괄 처리 구성 일정 표준 시간대입니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-155">The integration account batch configuration schedule time zone.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4ecd-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4ecd-156">-Confirm</span></span>
<span data-ttu-id="c4ecd-157">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4ecd-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4ecd-158">-WhatIf</span></span>
<span data-ttu-id="c4ecd-159">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c4ecd-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4ecd-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4ecd-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ecd-161">CommonParameters</span></span>
<span data-ttu-id="c4ecd-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ecd-163">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c4ecd-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ecd-164">입력</span><span class="sxs-lookup"><span data-stu-id="c4ecd-164">INPUTS</span></span>

### <span data-ttu-id="c4ecd-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4ecd-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="c4ecd-166">System.String</span><span class="sxs-lookup"><span data-stu-id="c4ecd-166">System.String</span></span>

## <span data-ttu-id="c4ecd-167">출력</span><span class="sxs-lookup"><span data-stu-id="c4ecd-167">OUTPUTS</span></span>

### <span data-ttu-id="c4ecd-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4ecd-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="c4ecd-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c4ecd-169">NOTES</span></span>

## <span data-ttu-id="c4ecd-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4ecd-170">RELATED LINKS</span></span>
