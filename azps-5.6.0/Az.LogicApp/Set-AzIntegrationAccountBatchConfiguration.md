---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: b1495f4b7473225697567ca3e9d87e98107ce001
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972752"
---
# <span data-ttu-id="8f6de-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f6de-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="8f6de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f6de-102">SYNOPSIS</span></span>
<span data-ttu-id="8f6de-103">통합 계정 일괄 처리 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="8f6de-104">구문</span><span class="sxs-lookup"><span data-stu-id="8f6de-104">SYNTAX</span></span>

### <span data-ttu-id="8f6de-105">ByIntegrationAccountAndParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="8f6de-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6de-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="8f6de-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6de-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="8f6de-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6de-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="8f6de-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6de-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="8f6de-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6de-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="8f6de-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6de-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="8f6de-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6de-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="8f6de-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f6de-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="8f6de-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f6de-114">설명</span><span class="sxs-lookup"><span data-stu-id="8f6de-114">DESCRIPTION</span></span>
<span data-ttu-id="8f6de-115">**Set-AzIntegrationAccountBatchConfiguration** cmdlet은 통합 계정 일괄 처리 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="8f6de-116">예제</span><span class="sxs-lookup"><span data-stu-id="8f6de-116">EXAMPLES</span></span>

### <span data-ttu-id="8f6de-117">예제 1: 로컬 파일을 사용하여 일괄 처리 구성 수정</span><span class="sxs-lookup"><span data-stu-id="8f6de-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="8f6de-118">"$batchConfigurationFilePath"에 포함된 파일 경로에 있는 로컬 파일을 사용하여 "sampleBatchConfig"라는 일괄 처리 구성을 $batchConfigurationFilePath.</span><span class="sxs-lookup"><span data-stu-id="8f6de-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="8f6de-119">예제 2: JSON 문자열을 사용하여 일괄 처리 구성 수정</span><span class="sxs-lookup"><span data-stu-id="8f6de-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="8f6de-120">"$batchConfigurationContent"에 포함된 JSON 문자열을 사용하여 "sampleBatchConfig"라는 일괄 처리 구성을 $batchConfigurationContent.</span><span class="sxs-lookup"><span data-stu-id="8f6de-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="8f6de-121">예제 3: 매개 변수를 사용하여 일괄 처리 구성 수정</span><span class="sxs-lookup"><span data-stu-id="8f6de-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="8f6de-122">필요한 모든 매개 변수를 수동으로 제공하여 "sampleBatchConfig"라는 일괄 처리 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="8f6de-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8f6de-123">PARAMETERS</span></span>

### <span data-ttu-id="8f6de-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="8f6de-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="8f6de-125">통합 계정 일괄 처리 구성 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="8f6de-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="8f6de-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="8f6de-127">통합 계정 일괄 처리 구성 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="8f6de-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="8f6de-128">-BatchGroupName</span></span>
<span data-ttu-id="8f6de-129">통합 계정 일괄 처리 구성 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="8f6de-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="8f6de-130">-BatchSize</span></span>
<span data-ttu-id="8f6de-131">통합 계정 일괄 처리 구성 일괄 처리 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="8f6de-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f6de-132">-DefaultProfile</span></span>
<span data-ttu-id="8f6de-133">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f6de-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f6de-134">-InputObject</span></span>
<span data-ttu-id="8f6de-135">통합 계정 일괄 처리 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-135">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="8f6de-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="8f6de-136">-MessageCount</span></span>
<span data-ttu-id="8f6de-137">통합 계정 일괄 처리 구성 메시지 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-137">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="8f6de-138">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="8f6de-138">-Metadata</span></span>
<span data-ttu-id="8f6de-139">통합 계정 일괄 처리 구성 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-139">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="8f6de-140">-Name</span><span class="sxs-lookup"><span data-stu-id="8f6de-140">-Name</span></span>
<span data-ttu-id="8f6de-141">통합 계정 일괄 처리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-141">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="8f6de-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="8f6de-142">-ParentName</span></span>
<span data-ttu-id="8f6de-143">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-143">The integration account name.</span></span>

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

### <span data-ttu-id="8f6de-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f6de-144">-ResourceGroupName</span></span>
<span data-ttu-id="8f6de-145">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-145">The resource group name.</span></span>

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

### <span data-ttu-id="8f6de-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f6de-146">-ResourceId</span></span>
<span data-ttu-id="8f6de-147">통합 계정 일괄 처리 구성 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-147">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="8f6de-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="8f6de-148">-ScheduleFrequency</span></span>
<span data-ttu-id="8f6de-149">통합 계정 일괄 처리 구성 일정 빈도입니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="8f6de-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="8f6de-150">-ScheduleInterval</span></span>
<span data-ttu-id="8f6de-151">통합 계정 일괄 처리 구성 일정 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="8f6de-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="8f6de-152">-ScheduleStartTime</span></span>
<span data-ttu-id="8f6de-153">통합 계정 일괄 처리 구성 일정 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="8f6de-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="8f6de-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="8f6de-155">통합 계정 일괄 처리 구성 일정 표준 시간대입니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="8f6de-156">-확인</span><span class="sxs-lookup"><span data-stu-id="8f6de-156">-Confirm</span></span>
<span data-ttu-id="8f6de-157">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f6de-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f6de-158">-WhatIf</span></span>
<span data-ttu-id="8f6de-159">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f6de-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f6de-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f6de-161">CommonParameters</span></span>
<span data-ttu-id="8f6de-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8f6de-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f6de-163">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8f6de-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f6de-164">입력</span><span class="sxs-lookup"><span data-stu-id="8f6de-164">INPUTS</span></span>

### <span data-ttu-id="8f6de-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f6de-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="8f6de-166">System.String</span><span class="sxs-lookup"><span data-stu-id="8f6de-166">System.String</span></span>

## <span data-ttu-id="8f6de-167">출력</span><span class="sxs-lookup"><span data-stu-id="8f6de-167">OUTPUTS</span></span>

### <span data-ttu-id="8f6de-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f6de-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="8f6de-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8f6de-169">NOTES</span></span>

## <span data-ttu-id="8f6de-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f6de-170">RELATED LINKS</span></span>
