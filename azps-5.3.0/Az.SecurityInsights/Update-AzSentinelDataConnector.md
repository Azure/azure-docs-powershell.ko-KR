---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
ms.openlocfilehash: b998d699836cf99f9d6cb9dc53bef36b6fc94ca3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494908"
---
# <span data-ttu-id="689eb-101">Update-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="689eb-101">Update-AzSentinelDataConnector</span></span>

## <span data-ttu-id="689eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="689eb-102">SYNOPSIS</span></span>
<span data-ttu-id="689eb-103">데이터 커넥터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="689eb-103">Update a Data Connector.</span></span>

## <span data-ttu-id="689eb-104">구문</span><span class="sxs-lookup"><span data-stu-id="689eb-104">SYNTAX</span></span>

### <span data-ttu-id="689eb-105">DataConnectorId(기본값)</span><span class="sxs-lookup"><span data-stu-id="689eb-105">DataConnectorId (Default)</span></span>
```
Update-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-Alerts <String>] [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>]
 [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="689eb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="689eb-106">InputObject</span></span>
```
Update-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-Alerts <String>]
 [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>]
 [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="689eb-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="689eb-107">ResourceId</span></span>
```
Update-AzSentinelDataConnector -ResourceId <String> [-Alerts <String>] [-SubscriptionId <String>]
 [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>]
 [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="689eb-108">설명</span><span class="sxs-lookup"><span data-stu-id="689eb-108">DESCRIPTION</span></span>
<span data-ttu-id="689eb-109">**Update-AzSentinelDataConnector** cmdlet은 지정된 작업 영역의 데이터 커넥터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="689eb-109">The **Update-AzSentinelDataConnector** cmdlet updates the Data Connector in the specified workspace.</span></span>
<span data-ttu-id="689eb-110">**DataConnector** 개체를 매개 변수로 전달하거나 파이프라인 연산자를 사용하여 전달하거나 필요한 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="689eb-110">You can pass an **DataConnector** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="689eb-111">*Confirm* 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="689eb-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="689eb-112">예제</span><span class="sxs-lookup"><span data-stu-id="689eb-112">EXAMPLES</span></span>

### <span data-ttu-id="689eb-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="689eb-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId" -Alerts Disabled
```

<span data-ttu-id="689eb-114">이 명령은 *DataConnectorId에 의해 Data Connector를 얻게* 하여 *경고* 상태를 사용 안 으로 *설정합니다.*</span><span class="sxs-lookup"><span data-stu-id="689eb-114">The command gets the Data Connector by *DataConnectorId* and sets the *Alerts* state to *Disabled*.</span></span>  <span data-ttu-id="689eb-115">다른 모든 속성은 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="689eb-115">All other properties remain the same.</span></span>

## <span data-ttu-id="689eb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="689eb-116">PARAMETERS</span></span>

### <span data-ttu-id="689eb-117">-Alerts</span><span class="sxs-lookup"><span data-stu-id="689eb-117">-Alerts</span></span>
<span data-ttu-id="689eb-118">데이터 커넥터 경고</span><span class="sxs-lookup"><span data-stu-id="689eb-118">Data Connector Alerts</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689eb-119">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="689eb-119">-AwsRoleArn</span></span>
<span data-ttu-id="689eb-120">Data Connector AWS 역할 Arn</span><span class="sxs-lookup"><span data-stu-id="689eb-120">Data Connector AWS Role Arn</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689eb-121">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="689eb-121">-DataConnectorId</span></span>
<span data-ttu-id="689eb-122">데이터 커넥터 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="689eb-122">Data Connector Id.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689eb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="689eb-123">-DefaultProfile</span></span>
<span data-ttu-id="689eb-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="689eb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="689eb-125">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="689eb-125">-DiscoveryLogs</span></span>
<span data-ttu-id="689eb-126">데이터 커넥터 검색 로그</span><span class="sxs-lookup"><span data-stu-id="689eb-126">Data Connector Discovery Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689eb-127">-Exchange</span><span class="sxs-lookup"><span data-stu-id="689eb-127">-Exchange</span></span>
<span data-ttu-id="689eb-128">Data Connector Exchange</span><span class="sxs-lookup"><span data-stu-id="689eb-128">Data Connector Exchange</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689eb-129">-Indicators</span><span class="sxs-lookup"><span data-stu-id="689eb-129">-Indicators</span></span>
<span data-ttu-id="689eb-130">데이터 커넥터 표시기</span><span class="sxs-lookup"><span data-stu-id="689eb-130">Data Connector Indicators</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689eb-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="689eb-131">-InputObject</span></span>
<span data-ttu-id="689eb-132">InputObject.</span><span class="sxs-lookup"><span data-stu-id="689eb-132">InputObject.</span></span>

```yaml
Type: PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="689eb-133">-Logs</span><span class="sxs-lookup"><span data-stu-id="689eb-133">-Logs</span></span>
<span data-ttu-id="689eb-134">데이터 커넥터 로그</span><span class="sxs-lookup"><span data-stu-id="689eb-134">Data Connector Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689eb-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="689eb-135">-ResourceGroupName</span></span>
<span data-ttu-id="689eb-136">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="689eb-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689eb-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="689eb-137">-ResourceId</span></span>
<span data-ttu-id="689eb-138">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="689eb-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="689eb-139">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="689eb-139">-SharePoint</span></span>
<span data-ttu-id="689eb-140">데이터 커넥터 SharePoint</span><span class="sxs-lookup"><span data-stu-id="689eb-140">Data Connector SharePoint</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689eb-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="689eb-141">-SubscriptionId</span></span>
<span data-ttu-id="689eb-142">데이터 커넥터 구독 ID</span><span class="sxs-lookup"><span data-stu-id="689eb-142">Data connector Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689eb-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="689eb-143">-WorkspaceName</span></span>
<span data-ttu-id="689eb-144">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="689eb-144">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689eb-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="689eb-145">-Confirm</span></span>
<span data-ttu-id="689eb-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="689eb-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689eb-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="689eb-147">-WhatIf</span></span>
<span data-ttu-id="689eb-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="689eb-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="689eb-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="689eb-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="689eb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="689eb-150">CommonParameters</span></span>
<span data-ttu-id="689eb-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="689eb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="689eb-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="689eb-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="689eb-153">입력</span><span class="sxs-lookup"><span data-stu-id="689eb-153">INPUTS</span></span>

### <span data-ttu-id="689eb-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="689eb-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

### <span data-ttu-id="689eb-155">System.String</span><span class="sxs-lookup"><span data-stu-id="689eb-155">System.String</span></span>

## <span data-ttu-id="689eb-156">출력</span><span class="sxs-lookup"><span data-stu-id="689eb-156">OUTPUTS</span></span>

### <span data-ttu-id="689eb-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="689eb-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

## <span data-ttu-id="689eb-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="689eb-158">NOTES</span></span>

## <span data-ttu-id="689eb-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="689eb-159">RELATED LINKS</span></span>
