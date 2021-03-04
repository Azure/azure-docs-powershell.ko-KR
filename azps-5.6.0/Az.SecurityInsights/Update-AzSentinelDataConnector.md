---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
ms.openlocfilehash: 6ccb7b5a38a85d114e3bb93b594d838c61dcff4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974331"
---
# <span data-ttu-id="0a8b9-101">Update-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="0a8b9-101">Update-AzSentinelDataConnector</span></span>

## <span data-ttu-id="0a8b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="0a8b9-103">데이터 커넥터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-103">Update a Data Connector.</span></span>

## <span data-ttu-id="0a8b9-104">구문</span><span class="sxs-lookup"><span data-stu-id="0a8b9-104">SYNTAX</span></span>

### <span data-ttu-id="0a8b9-105">DataConnectorId(기본값)</span><span class="sxs-lookup"><span data-stu-id="0a8b9-105">DataConnectorId (Default)</span></span>
```
Update-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-Alerts <String>] [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>]
 [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8b9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0a8b9-106">InputObject</span></span>
```
Update-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-Alerts <String>]
 [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>]
 [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a8b9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a8b9-107">ResourceId</span></span>
```
Update-AzSentinelDataConnector -ResourceId <String> [-Alerts <String>] [-SubscriptionId <String>]
 [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>]
 [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a8b9-108">설명</span><span class="sxs-lookup"><span data-stu-id="0a8b9-108">DESCRIPTION</span></span>
<span data-ttu-id="0a8b9-109">**Update-AzSentinelDataConnector** cmdlet은 지정된 작업 영역의 데이터 커넥터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-109">The **Update-AzSentinelDataConnector** cmdlet updates the Data Connector in the specified workspace.</span></span>
<span data-ttu-id="0a8b9-110">**DataConnector** 개체를 매개 변수로 전달하거나 파이프라인 연산자를 사용하여 전달하거나 필요한 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-110">You can pass an **DataConnector** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="0a8b9-111">확인 매개  변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="0a8b9-112">예제</span><span class="sxs-lookup"><span data-stu-id="0a8b9-112">EXAMPLES</span></span>

### <span data-ttu-id="0a8b9-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="0a8b9-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId" -Alerts Disabled
```

<span data-ttu-id="0a8b9-114">명령은 *DataConnectorId에* 의해 Data Connector를  얻게 하여 경고 상태를 사용 안 으로 *설정합니다.*</span><span class="sxs-lookup"><span data-stu-id="0a8b9-114">The command gets the Data Connector by *DataConnectorId* and sets the *Alerts* state to *Disabled*.</span></span>  <span data-ttu-id="0a8b9-115">다른 모든 속성은 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-115">All other properties remain the same.</span></span>

## <span data-ttu-id="0a8b9-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0a8b9-116">PARAMETERS</span></span>

### <span data-ttu-id="0a8b9-117">-Alerts</span><span class="sxs-lookup"><span data-stu-id="0a8b9-117">-Alerts</span></span>
<span data-ttu-id="0a8b9-118">데이터 커넥터 경고</span><span class="sxs-lookup"><span data-stu-id="0a8b9-118">Data Connector Alerts</span></span>

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

### <span data-ttu-id="0a8b9-119">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="0a8b9-119">-AwsRoleArn</span></span>
<span data-ttu-id="0a8b9-120">Data Connector AWS 역할 Arn</span><span class="sxs-lookup"><span data-stu-id="0a8b9-120">Data Connector AWS Role Arn</span></span>

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

### <span data-ttu-id="0a8b9-121">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="0a8b9-121">-DataConnectorId</span></span>
<span data-ttu-id="0a8b9-122">데이터 커넥터 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-122">Data Connector Id.</span></span>

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

### <span data-ttu-id="0a8b9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a8b9-123">-DefaultProfile</span></span>
<span data-ttu-id="0a8b9-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a8b9-125">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="0a8b9-125">-DiscoveryLogs</span></span>
<span data-ttu-id="0a8b9-126">데이터 커넥터 검색 로그</span><span class="sxs-lookup"><span data-stu-id="0a8b9-126">Data Connector Discovery Logs</span></span>

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

### <span data-ttu-id="0a8b9-127">-Exchange</span><span class="sxs-lookup"><span data-stu-id="0a8b9-127">-Exchange</span></span>
<span data-ttu-id="0a8b9-128">데이터 커넥터 교환</span><span class="sxs-lookup"><span data-stu-id="0a8b9-128">Data Connector Exchange</span></span>

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

### <span data-ttu-id="0a8b9-129">-Indicators</span><span class="sxs-lookup"><span data-stu-id="0a8b9-129">-Indicators</span></span>
<span data-ttu-id="0a8b9-130">데이터 커넥터 표시기</span><span class="sxs-lookup"><span data-stu-id="0a8b9-130">Data Connector Indicators</span></span>

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

### <span data-ttu-id="0a8b9-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a8b9-131">-InputObject</span></span>
<span data-ttu-id="0a8b9-132">InputObject.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-132">InputObject.</span></span>

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

### <span data-ttu-id="0a8b9-133">-Logs</span><span class="sxs-lookup"><span data-stu-id="0a8b9-133">-Logs</span></span>
<span data-ttu-id="0a8b9-134">데이터 커넥터 로그</span><span class="sxs-lookup"><span data-stu-id="0a8b9-134">Data Connector Logs</span></span>

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

### <span data-ttu-id="0a8b9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a8b9-135">-ResourceGroupName</span></span>
<span data-ttu-id="0a8b9-136">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-136">Resource group name.</span></span>

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

### <span data-ttu-id="0a8b9-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a8b9-137">-ResourceId</span></span>
<span data-ttu-id="0a8b9-138">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-138">Resource Id.</span></span>

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

### <span data-ttu-id="0a8b9-139">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="0a8b9-139">-SharePoint</span></span>
<span data-ttu-id="0a8b9-140">데이터 커넥터 SharePoint</span><span class="sxs-lookup"><span data-stu-id="0a8b9-140">Data Connector SharePoint</span></span>

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

### <span data-ttu-id="0a8b9-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a8b9-141">-SubscriptionId</span></span>
<span data-ttu-id="0a8b9-142">데이터 커넥터 구독 ID</span><span class="sxs-lookup"><span data-stu-id="0a8b9-142">Data connector Subscription Id</span></span>

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

### <span data-ttu-id="0a8b9-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0a8b9-143">-WorkspaceName</span></span>
<span data-ttu-id="0a8b9-144">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-144">Workspace Name.</span></span>

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

### <span data-ttu-id="0a8b9-145">-확인</span><span class="sxs-lookup"><span data-stu-id="0a8b9-145">-Confirm</span></span>
<span data-ttu-id="0a8b9-146">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a8b9-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a8b9-147">-WhatIf</span></span>
<span data-ttu-id="0a8b9-148">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a8b9-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a8b9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a8b9-150">CommonParameters</span></span>
<span data-ttu-id="0a8b9-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0a8b9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a8b9-152">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a8b9-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a8b9-153">입력</span><span class="sxs-lookup"><span data-stu-id="0a8b9-153">INPUTS</span></span>

### <span data-ttu-id="0a8b9-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="0a8b9-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

### <span data-ttu-id="0a8b9-155">System.String</span><span class="sxs-lookup"><span data-stu-id="0a8b9-155">System.String</span></span>

## <span data-ttu-id="0a8b9-156">출력</span><span class="sxs-lookup"><span data-stu-id="0a8b9-156">OUTPUTS</span></span>

### <span data-ttu-id="0a8b9-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="0a8b9-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

## <span data-ttu-id="0a8b9-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0a8b9-158">NOTES</span></span>

## <span data-ttu-id="0a8b9-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a8b9-159">RELATED LINKS</span></span>
