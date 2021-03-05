---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
ms.openlocfilehash: 7eb4675e44a252feec913b531a30f9062f6b791b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976347"
---
# <span data-ttu-id="5b0e6-101">New-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="5b0e6-101">New-AzSentinelDataConnector</span></span>

## <span data-ttu-id="5b0e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b0e6-102">SYNOPSIS</span></span>
<span data-ttu-id="5b0e6-103">데이터 커넥터를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5b0e6-103">Create a Data Connector.</span></span>

## <span data-ttu-id="5b0e6-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b0e6-104">SYNTAX</span></span>

### <span data-ttu-id="5b0e6-105">AzureActiveDirectory(기본값)</span><span class="sxs-lookup"><span data-stu-id="5b0e6-105">AzureActiveDirectory (Default)</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureActiveDirectory] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b0e6-106">AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="5b0e6-106">AzureAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0e6-107">AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="5b0e6-107">AzureSecurityCenter</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureSecurityCenter] -Alerts <String> -SubscriptionId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0e6-108">AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="5b0e6-108">AmazonWebServicesCloudTrail</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AmazonWebServicesCloudTrail] -AwsRoleArn <String> -Logs <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0e6-109">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="5b0e6-109">MicrosoftCloudAppSecurity</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftCloudAppSecurity] -Alerts <String> -DiscoveryLogs <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0e6-110">MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="5b0e6-110">MicrosoftDefenderAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftDefenderAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0e6-111">Office365</span><span class="sxs-lookup"><span data-stu-id="5b0e6-111">Office365</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-Office365] -Exchange <String> -SharePoint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b0e6-112">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="5b0e6-112">ThreatIntelligence</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-ThreatIntelligence] -Indicators <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b0e6-113">설명</span><span class="sxs-lookup"><span data-stu-id="5b0e6-113">DESCRIPTION</span></span>
<span data-ttu-id="5b0e6-114">**New-AzSentinelAlertRule** cmdlet은 지정된 작업 영역의 분석(경고 규칙)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b0e6-114">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="5b0e6-115">만들 경고 규칙의 종류를 지정하려면 매개 변수(예: -AzureActiveDirectory)를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b0e6-115">You must specify one of the parameters, for example -AzureActiveDirectory, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="5b0e6-116">각 종류에는 서로 다른 필수 파라마터가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b0e6-116">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="5b0e6-117">확인 매개  변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b0e6-117">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="5b0e6-118">참고: 포털에서 사용할 수 있는 모든 데이터 커넥터가 API를 통해 Avaialble이 아바얼블은 아바얼블이 아바탈블은 아바탈블이 아는 것은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5b0e6-118">Note:  Not all data connectors available in the portal are avaialble via API.</span></span>

## <span data-ttu-id="5b0e6-119">예제</span><span class="sxs-lookup"><span data-stu-id="5b0e6-119">EXAMPLES</span></span>

### <span data-ttu-id="5b0e6-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="5b0e6-120">Example 1</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AzureSecurityCenter -Alerts Enabled -SubscriptionId ((Get-AzContext).Subscription.Id)
```

<span data-ttu-id="5b0e6-121">이 예제에서는 지정된 작업 영역의 Azure Security Center용 **DataConnector를** 만든 다음, 해당 $DataConnector 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5b0e6-121">This example creates a **DataConnector** for Azure Security Center in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

### <span data-ttu-id="5b0e6-122">예제 2</span><span class="sxs-lookup"><span data-stu-id="5b0e6-122">Example 2</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftCloudAppSecurity -Alerts Enabled -DiscoveryLogs Disabled
```

<span data-ttu-id="5b0e6-123">이 예제에서는 지정된 작업 영역의 Microsoft Cloud App Security용 **DataConnector를** 만든 다음, 해당 $DataConnector 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5b0e6-123">This example creates a **DataConnector** for Microsoft Cloud App Security in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="5b0e6-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5b0e6-124">PARAMETERS</span></span>

### <span data-ttu-id="5b0e6-125">-Alerts</span><span class="sxs-lookup"><span data-stu-id="5b0e6-125">-Alerts</span></span>
<span data-ttu-id="5b0e6-126">데이터 커넥터 경고</span><span class="sxs-lookup"><span data-stu-id="5b0e6-126">Data Connector Alerts</span></span>

```yaml
Type: System.String
Parameter Sets: AzureActiveDirectory, AzureAdvancedThreatProtection, AzureSecurityCenter, MicrosoftCloudAppSecurity, MicrosoftDefenderAdvancedThreatProtection
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e6-127">-AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="5b0e6-127">-AmazonWebServicesCloudTrail</span></span>
<span data-ttu-id="5b0e6-128">Data Connector Amazon Web Services 클라우드 트레일</span><span class="sxs-lookup"><span data-stu-id="5b0e6-128">Data Connector Amazon Web Services Cloud Trail</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e6-129">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="5b0e6-129">-AwsRoleArn</span></span>
<span data-ttu-id="5b0e6-130">Data Connector AWS 역할 Arn</span><span class="sxs-lookup"><span data-stu-id="5b0e6-130">Data Connector AWS Role Arn</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e6-131">-AzureActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="5b0e6-131">-AzureActiveDirectory</span></span>
<span data-ttu-id="5b0e6-132">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="5b0e6-132">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureActiveDirectory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e6-133">-AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="5b0e6-133">-AzureAdvancedThreatProtection</span></span>
<span data-ttu-id="5b0e6-134">Data Connector Azure Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="5b0e6-134">Data Connector Azure Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e6-135">-AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="5b0e6-135">-AzureSecurityCenter</span></span>
<span data-ttu-id="5b0e6-136">Data Connector Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="5b0e6-136">Data Connector Azure Security Center</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e6-137">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="5b0e6-137">-DataConnectorId</span></span>
<span data-ttu-id="5b0e6-138">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="5b0e6-138">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e6-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b0e6-139">-DefaultProfile</span></span>
<span data-ttu-id="5b0e6-140">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b0e6-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b0e6-141">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="5b0e6-141">-DiscoveryLogs</span></span>
<span data-ttu-id="5b0e6-142">데이터 커넥터 검색 로그</span><span class="sxs-lookup"><span data-stu-id="5b0e6-142">Data Connector Discovery Logs</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e6-143">-Exchange</span><span class="sxs-lookup"><span data-stu-id="5b0e6-143">-Exchange</span></span>
<span data-ttu-id="5b0e6-144">데이터 커넥터 교환</span><span class="sxs-lookup"><span data-stu-id="5b0e6-144">Data Connector Exchange</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e6-145">-Indicators</span><span class="sxs-lookup"><span data-stu-id="5b0e6-145">-Indicators</span></span>
<span data-ttu-id="5b0e6-146">데이터 커넥터 표시기</span><span class="sxs-lookup"><span data-stu-id="5b0e6-146">Data Connector Indicators</span></span>

```yaml
Type: System.String
Parameter Sets: ThreatIntelligence
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e6-147">-Logs</span><span class="sxs-lookup"><span data-stu-id="5b0e6-147">-Logs</span></span>
<span data-ttu-id="5b0e6-148">데이터 커넥터 로그</span><span class="sxs-lookup"><span data-stu-id="5b0e6-148">Data Connector Logs</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e6-149">-MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="5b0e6-149">-MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="5b0e6-150">Data Connector Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="5b0e6-150">Data Connector Microsoft Cloud App Security</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e6-151">-MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="5b0e6-151">-MicrosoftDefenderAdvancedThreatProtection</span></span>
<span data-ttu-id="5b0e6-152">Data Connector Microsoft Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="5b0e6-152">Data Connector Microsoft Defender Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftDefenderAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e6-153">-Office365</span><span class="sxs-lookup"><span data-stu-id="5b0e6-153">-Office365</span></span>
<span data-ttu-id="5b0e6-154">Data Connector Office 365</span><span class="sxs-lookup"><span data-stu-id="5b0e6-154">Data Connector Office 365</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Office365
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e6-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b0e6-155">-ResourceGroupName</span></span>
<span data-ttu-id="5b0e6-156">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="5b0e6-156">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="5b0e6-157">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="5b0e6-157">-SharePoint</span></span>
<span data-ttu-id="5b0e6-158">데이터 커넥터 SharePoint</span><span class="sxs-lookup"><span data-stu-id="5b0e6-158">Data Connector SharePoint</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e6-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b0e6-159">-SubscriptionId</span></span>
<span data-ttu-id="5b0e6-160">데이터 커넥터 구독 ID</span><span class="sxs-lookup"><span data-stu-id="5b0e6-160">Data connector Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e6-161">-ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="5b0e6-161">-ThreatIntelligence</span></span>
<span data-ttu-id="5b0e6-162">데이터 커넥터 위협 인텔리전스</span><span class="sxs-lookup"><span data-stu-id="5b0e6-162">Data Connector Threat Intelligence</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ThreatIntelligence
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b0e6-163">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5b0e6-163">-WorkspaceName</span></span>
<span data-ttu-id="5b0e6-164">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="5b0e6-164">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="5b0e6-165">-확인</span><span class="sxs-lookup"><span data-stu-id="5b0e6-165">-Confirm</span></span>
<span data-ttu-id="5b0e6-166">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b0e6-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b0e6-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b0e6-167">-WhatIf</span></span>
<span data-ttu-id="5b0e6-168">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5b0e6-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b0e6-169">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b0e6-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b0e6-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b0e6-170">CommonParameters</span></span>
<span data-ttu-id="5b0e6-171">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b0e6-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b0e6-172">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b0e6-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b0e6-173">입력</span><span class="sxs-lookup"><span data-stu-id="5b0e6-173">INPUTS</span></span>

### <span data-ttu-id="5b0e6-174">없음</span><span class="sxs-lookup"><span data-stu-id="5b0e6-174">None</span></span>
## <span data-ttu-id="5b0e6-175">출력</span><span class="sxs-lookup"><span data-stu-id="5b0e6-175">OUTPUTS</span></span>

### <span data-ttu-id="5b0e6-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="5b0e6-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="5b0e6-177">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b0e6-177">NOTES</span></span>

## <span data-ttu-id="5b0e6-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b0e6-178">RELATED LINKS</span></span>
