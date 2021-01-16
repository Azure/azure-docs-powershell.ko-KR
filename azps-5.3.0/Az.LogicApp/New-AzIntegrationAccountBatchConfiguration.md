---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: c31768cff6af5f36212dbf32b08b016fa47c8a63
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493417"
---
# <span data-ttu-id="4ec11-101">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ec11-101">New-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="4ec11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ec11-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec11-103">통합 계정 일괄 처리 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-103">Creates an integration account batch configuration.</span></span>

## <span data-ttu-id="4ec11-104">구문</span><span class="sxs-lookup"><span data-stu-id="4ec11-104">SYNTAX</span></span>

### <span data-ttu-id="4ec11-105">ByIntegrationAccountAndParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="4ec11-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ec11-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="4ec11-106">ByIntegrationAccountAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ec11-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="4ec11-107">ByIntegrationAccountAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ec11-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="4ec11-108">ByInputObjectAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ec11-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="4ec11-109">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ec11-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="4ec11-110">ByInputObjectAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ec11-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="4ec11-111">ByResourceIdAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ec11-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="4ec11-112">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ec11-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="4ec11-113">ByResourceIdAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ec11-114">설명</span><span class="sxs-lookup"><span data-stu-id="4ec11-114">DESCRIPTION</span></span>
<span data-ttu-id="4ec11-115">**Get-AzIntegrationAccountBatchConfiguration** cmdlet은 통합 계정에 새 일괄 처리 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-115">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet creates a new batch configuration in an integration account.</span></span>

## <span data-ttu-id="4ec11-116">예제</span><span class="sxs-lookup"><span data-stu-id="4ec11-116">EXAMPLES</span></span>

### <span data-ttu-id="4ec11-117">예제 1: 로컬 파일을 사용하여 새 일괄 처리 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="4ec11-117">Example 1: Create new batch configuration using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="4ec11-118">"$batchConfigurationFilePath"에 포함된 파일 경로에 있는 로컬 파일을 사용하여 새 배치 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-118">Creates a new batch configuration using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="4ec11-119">예제 2: JSON 문자열을 사용하여 새 일괄 처리 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="4ec11-119">Example 2: Create new batch configuration using a JSON string</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="4ec11-120">"$batchConfigurationContent"에 포함된 JSON 문자열을 사용하여 새 일괄 처리 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-120">Creates a new batch configuration using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="4ec11-121">예제 3: 매개 변수를 사용하여 새 일괄 처리 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="4ec11-121">Example 3: Create new batch configuration using parameters</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="4ec11-122">필요한 모든 매개 변수를 수동으로 제공하여 새 일괄 처리 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-122">Creates a new batch configuration by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="4ec11-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ec11-123">PARAMETERS</span></span>

### <span data-ttu-id="4ec11-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="4ec11-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="4ec11-125">통합 계정 일괄 처리 구성 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="4ec11-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="4ec11-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="4ec11-127">통합 계정 일괄 처리 구성 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="4ec11-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="4ec11-128">-BatchGroupName</span></span>
<span data-ttu-id="4ec11-129">통합 계정 일괄 처리 구성 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="4ec11-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="4ec11-130">-BatchSize</span></span>
<span data-ttu-id="4ec11-131">통합 계정 일괄 처리 구성 일괄 처리 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="4ec11-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec11-132">-DefaultProfile</span></span>
<span data-ttu-id="4ec11-133">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ec11-134">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="4ec11-134">-MessageCount</span></span>
<span data-ttu-id="4ec11-135">통합 계정 일괄 처리 구성 메시지 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-135">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="4ec11-136">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4ec11-136">-Metadata</span></span>
<span data-ttu-id="4ec11-137">통합 계정 일괄 처리 구성 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-137">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="4ec11-138">-Name</span><span class="sxs-lookup"><span data-stu-id="4ec11-138">-Name</span></span>
<span data-ttu-id="4ec11-139">통합 계정 일괄 처리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-139">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec11-140">-ParentName</span><span class="sxs-lookup"><span data-stu-id="4ec11-140">-ParentName</span></span>
<span data-ttu-id="4ec11-141">통합 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-141">The integration account name.</span></span>

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

### <span data-ttu-id="4ec11-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4ec11-142">-ParentObject</span></span>
<span data-ttu-id="4ec11-143">통합 계정 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-143">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec11-144">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4ec11-144">-ParentResourceId</span></span>
<span data-ttu-id="4ec11-145">통합 계정 일괄 처리 구성 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-145">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="4ec11-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ec11-146">-ResourceGroupName</span></span>
<span data-ttu-id="4ec11-147">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-147">The resource group name.</span></span>

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

### <span data-ttu-id="4ec11-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="4ec11-148">-ScheduleFrequency</span></span>
<span data-ttu-id="4ec11-149">통합 계정 일괄 처리 구성 일정 빈도입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="4ec11-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="4ec11-150">-ScheduleInterval</span></span>
<span data-ttu-id="4ec11-151">통합 계정 일괄 처리 구성 일정 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="4ec11-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="4ec11-152">-ScheduleStartTime</span></span>
<span data-ttu-id="4ec11-153">통합 계정 일괄 처리 구성 일정 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="4ec11-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="4ec11-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="4ec11-155">통합 계정 일괄 처리 구성 일정 표준 시간대입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="4ec11-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ec11-156">-Confirm</span></span>
<span data-ttu-id="4ec11-157">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ec11-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ec11-158">-WhatIf</span></span>
<span data-ttu-id="4ec11-159">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4ec11-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ec11-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ec11-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec11-161">CommonParameters</span></span>
<span data-ttu-id="4ec11-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ec11-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec11-163">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4ec11-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec11-164">입력</span><span class="sxs-lookup"><span data-stu-id="4ec11-164">INPUTS</span></span>

### <span data-ttu-id="4ec11-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="4ec11-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="4ec11-166">System.String</span><span class="sxs-lookup"><span data-stu-id="4ec11-166">System.String</span></span>

## <span data-ttu-id="4ec11-167">출력</span><span class="sxs-lookup"><span data-stu-id="4ec11-167">OUTPUTS</span></span>

### <span data-ttu-id="4ec11-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ec11-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="4ec11-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4ec11-169">NOTES</span></span>

## <span data-ttu-id="4ec11-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ec11-170">RELATED LINKS</span></span>
