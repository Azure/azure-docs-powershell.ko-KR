---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Set-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 6e101beb73b68427f806fdae3fa2406082a9b47a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985572"
---
# <span data-ttu-id="84486-101">Set-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="84486-101">Set-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="84486-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84486-102">SYNOPSIS</span></span>
<span data-ttu-id="84486-103">Azure 서버의 Microsoft 지원 작업 감사 설정을 SQL 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="84486-103">Changes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="84486-104">구문</span><span class="sxs-lookup"><span data-stu-id="84486-104">SYNTAX</span></span>

### <span data-ttu-id="84486-105">ServerParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="84486-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerMSSupportAudit
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>]
 [-LogAnalyticsTargetState <String>] [-WorkspaceResourceId <String>]
 [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84486-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84486-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerMSSupportAudit [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84486-107">설명</span><span class="sxs-lookup"><span data-stu-id="84486-107">DESCRIPTION</span></span>
<span data-ttu-id="84486-108">**Set-AzSqlServerMSSupportAudit** cmdlet은 Azure 서버의 Microsoft 지원 작업 감사 설정을 SQL 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="84486-108">The **Set-AzSqlServerMSSupportAudit** cmdlet changes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="84486-109">cmdlet을 사용하 는 *ResourceGroupName* 및 *ServerName* 매개 변수를 사용하여 서버를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="84486-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="84486-110">Blob Storage가 감사 로그의 대상이면 *StorageAccountResourceId* 매개 변수를 지정하여 감사 로그에 대한 저장소 계정을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="84486-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs.</span></span>

## <span data-ttu-id="84486-111">예제</span><span class="sxs-lookup"><span data-stu-id="84486-111">EXAMPLES</span></span>

### <span data-ttu-id="84486-112">예제 1: Blob Storage Microsoft 지원 작업 감사 정책 Azure SQL 사용</span><span class="sxs-lookup"><span data-stu-id="84486-112">Example 1: Enable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="84486-113">예제 2: Blob Storage 사용 안 하세요 Microsoft 지원 작업 감사 정책 Azure SQL 서버</span><span class="sxs-lookup"><span data-stu-id="84486-113">Example 2: Disable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="84486-114">예제 3: 이벤트 허브 Microsoft에서 Azure 서버의 작업 감사 정책을 SQL 사용</span><span class="sxs-lookup"><span data-stu-id="84486-114">Example 3: Enable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="84486-115">예제 4: Azure 서버의 이벤트 허브 Microsoft 지원 작업 감사 정책 사용 안 SQL</span><span class="sxs-lookup"><span data-stu-id="84486-115">Example 4: Disable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="84486-116">예제 5: Azure 서버의 로그 분석 Microsoft 지원 작업 감사 정책 사용 SQL</span><span class="sxs-lookup"><span data-stu-id="84486-116">Example 5: Enable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="84486-117">예제 6: Azure 서버의 로그 분석 Microsoft 지원 작업 감사 정책 사용 안 SQL</span><span class="sxs-lookup"><span data-stu-id="84486-117">Example 6: Disable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="84486-118">예제 7: 파이프라인을 통해 사용 안 하세요, 로그 분석 Microsoft는 Azure 서버의 작업 감사 정책을 SQL 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="84486-118">Example 7: Disable, through pipeline, the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerMSSupportAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="84486-119">예제 8: Azure SQL 서버의 Microsoft 지원 작업 감사 레코드를 Blob Storage에 보내지 않도록 설정하고 로그 분석에 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84486-119">Example 8: Disable sending Microsoft support operations audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="84486-120">예제 9: Azure SQL 서버의 Microsoft 지원 작업 감사 레코드를 Blob Storage, 이벤트 허브 및 로그 분석에 전송하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="84486-120">Example 9: Enable sending Microsoft support operations audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="84486-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="84486-121">PARAMETERS</span></span>

### <span data-ttu-id="84486-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84486-122">-AsJob</span></span>
<span data-ttu-id="84486-123">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="84486-123">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84486-124">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="84486-124">-BlobStorageTargetState</span></span>
<span data-ttu-id="84486-125">Blob Storage가 Microsoft 지원 작업 감사 레코드의 대상인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="84486-125">Indicates whether blob storage is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84486-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84486-126">-DefaultProfile</span></span>
<span data-ttu-id="84486-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84486-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84486-128">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="84486-128">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="84486-129">이벤트 허브 권한 부여 규칙에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="84486-129">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="84486-130">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="84486-130">-EventHubName</span></span>
<span data-ttu-id="84486-131">이벤트 허브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84486-131">The name of the event hub.</span></span> <span data-ttu-id="84486-132">EventHubAuthorizationRuleResourceId를 제공 할 때 지정되지 않은 경우 기본 이벤트 허브가 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="84486-132">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="84486-133">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="84486-133">-EventHubTargetState</span></span>
<span data-ttu-id="84486-134">이벤트 허브가 Microsoft 지원 작업 감사 레코드의 대상인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="84486-134">Indicates whether event hub is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84486-135">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="84486-135">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="84486-136">로그 분석이 Microsoft 지원 작업 감사 레코드의 대상인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="84486-136">Indicates whether log analytics is a destination for Microsoft support operations audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84486-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84486-137">-PassThru</span></span>
<span data-ttu-id="84486-138">cmdlet 실행이 끝날 때 Microsoft 지원 작업 감사 정책을 출력할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="84486-138">Specifies whether to output the Microsoft support operations auditing policy at end of cmdlet execution</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84486-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84486-139">-ResourceGroupName</span></span>
<span data-ttu-id="84486-140">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84486-140">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84486-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="84486-141">-ServerName</span></span>
<span data-ttu-id="84486-142">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84486-142">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84486-143">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="84486-143">-ServerObject</span></span>
<span data-ttu-id="84486-144">Microsoft 지원 작업 감사 정책을 관리하는 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="84486-144">The server object to manage its Microsoft support operations audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84486-145">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="84486-145">-StorageAccountResourceId</span></span>
<span data-ttu-id="84486-146">저장소 계정 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="84486-146">The storage account resource id</span></span>

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

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84486-147">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="84486-147">-WorkspaceResourceId</span></span>
<span data-ttu-id="84486-148">Microsoft 지원 작업 감사 로그를 보내고자 하는 Log Analytics 작업 영역의 작업 영역 ID(Log Analytics 작업 영역의 리소스 ID)입니다.</span><span class="sxs-lookup"><span data-stu-id="84486-148">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Microsoft support operations Audit Logs.</span></span> <span data-ttu-id="84486-149">예제: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="84486-149">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="84486-150">-확인</span><span class="sxs-lookup"><span data-stu-id="84486-150">-Confirm</span></span>
<span data-ttu-id="84486-151">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="84486-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84486-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84486-152">-WhatIf</span></span>
<span data-ttu-id="84486-153">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="84486-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84486-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84486-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84486-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84486-155">CommonParameters</span></span>
<span data-ttu-id="84486-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="84486-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84486-157">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84486-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84486-158">입력</span><span class="sxs-lookup"><span data-stu-id="84486-158">INPUTS</span></span>

### <span data-ttu-id="84486-159">System.String</span><span class="sxs-lookup"><span data-stu-id="84486-159">System.String</span></span>

### <span data-ttu-id="84486-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="84486-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="84486-161">System.Guid</span><span class="sxs-lookup"><span data-stu-id="84486-161">System.Guid</span></span>

### <span data-ttu-id="84486-162">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="84486-162">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="84486-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="84486-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="84486-164">출력</span><span class="sxs-lookup"><span data-stu-id="84486-164">OUTPUTS</span></span>

### <span data-ttu-id="84486-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="84486-165">System.Boolean</span></span>

## <span data-ttu-id="84486-166">참고 사항</span><span class="sxs-lookup"><span data-stu-id="84486-166">NOTES</span></span>

## <span data-ttu-id="84486-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84486-167">RELATED LINKS</span></span>
