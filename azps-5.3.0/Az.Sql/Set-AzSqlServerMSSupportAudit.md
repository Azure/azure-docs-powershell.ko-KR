---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 623f52f1de9370c679f6df09b6cf05c50f38ca6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492125"
---
# <span data-ttu-id="1724f-101">Set-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="1724f-101">Set-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="1724f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1724f-102">SYNOPSIS</span></span>
<span data-ttu-id="1724f-103">Azure SQL 서버의 Microsoft 지원 작업 감사 설정을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-103">Changes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="1724f-104">구문</span><span class="sxs-lookup"><span data-stu-id="1724f-104">SYNTAX</span></span>

### <span data-ttu-id="1724f-105">ServerParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1724f-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerMSSupportAudit
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>]
 [-LogAnalyticsTargetState <String>] [-WorkspaceResourceId <String>]
 [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1724f-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1724f-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerMSSupportAudit [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1724f-107">설명</span><span class="sxs-lookup"><span data-stu-id="1724f-107">DESCRIPTION</span></span>
<span data-ttu-id="1724f-108">**Set-AzSqlServerMSSupportAudit** cmdlet은 Azure SQL 서버의 Microsoft 지원 작업 감사 설정을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-108">The **Set-AzSqlServerMSSupportAudit** cmdlet changes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="1724f-109">cmdlet을 사용 설정하기 위해 *ResourceGroupName* 및 *ServerName* 매개 변수를 사용하여 서버를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="1724f-110">Blob Storage가 감사 로그의 대상인 경우 *StorageAccountResourceId* 매개 변수를 지정하여 감사 로그에 대한 스토리지 계정을 판단합니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs.</span></span>

## <span data-ttu-id="1724f-111">예제</span><span class="sxs-lookup"><span data-stu-id="1724f-111">EXAMPLES</span></span>

### <span data-ttu-id="1724f-112">예제 1: Blob Storage 사용 Microsoft는 Azure SQL 서버의 작업 감사 정책을 지원</span><span class="sxs-lookup"><span data-stu-id="1724f-112">Example 1: Enable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="1724f-113">예제 2: Blob Storage 사용 안 하여 Microsoft는 Azure SQL 서버의 작업 감사 정책을 지원</span><span class="sxs-lookup"><span data-stu-id="1724f-113">Example 2: Disable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="1724f-114">예제 3: Azure SQL 서버의 작업 감사 정책을 지원하는 이벤트 허브 사용</span><span class="sxs-lookup"><span data-stu-id="1724f-114">Example 3: Enable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="1724f-115">예제 4: Azure SQL 서버의 작업 감사 정책을 지원하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="1724f-115">Example 4: Disable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="1724f-116">예제 5: 로그 분석 사용 Microsoft는 Azure SQL 서버의 작업 감사 정책을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-116">Example 5: Enable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="1724f-117">예제 6: 로그 분석 사용 안 하여 Microsoft는 Azure SQL 서버의 작업 감사 정책을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-117">Example 6: Disable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="1724f-118">예제 7: 파이프라인을 통해 비활성화, 로그 분석 Microsoft는 Azure SQL 서버의 작업 감사 정책을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-118">Example 7: Disable, through pipeline, the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerMSSupportAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="1724f-119">예제 8: Azure SQL 서버의 레코드를 Blob Storage에 감사하고 로그 분석에 보낼 수 있도록 Microsoft 지원 작업 보내기 사용 안 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="1724f-119">Example 8: Disable sending Microsoft support operations audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="1724f-120">예제 9: Azure SQL 서버의 레코드를 Blob Storage, 이벤트 허브 및 로그 분석에 Microsoft 지원 서비스로 보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-120">Example 9: Enable sending Microsoft support operations audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="1724f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1724f-121">PARAMETERS</span></span>

### <span data-ttu-id="1724f-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1724f-122">-AsJob</span></span>
<span data-ttu-id="1724f-123">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1724f-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1724f-124">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="1724f-124">-BlobStorageTargetState</span></span>
<span data-ttu-id="1724f-125">Blob Storage가 Microsoft 지원 작업 감사 레코드의 대상인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-125">Indicates whether blob storage is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="1724f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1724f-126">-DefaultProfile</span></span>
<span data-ttu-id="1724f-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1724f-128">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="1724f-128">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="1724f-129">이벤트 허브 권한 부여 규칙에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="1724f-129">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="1724f-130">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="1724f-130">-EventHubName</span></span>
<span data-ttu-id="1724f-131">이벤트 허브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-131">The name of the event hub.</span></span> <span data-ttu-id="1724f-132">EventHubAuthorizationRuleResourceId를 제공하는 경우 지정되지 않은 경우 기본 이벤트 허브가 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-132">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="1724f-133">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="1724f-133">-EventHubTargetState</span></span>
<span data-ttu-id="1724f-134">이벤트 허브가 Microsoft 지원 작업 감사 레코드의 대상인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-134">Indicates whether event hub is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="1724f-135">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="1724f-135">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="1724f-136">로그 분석이 Microsoft 지원 작업 감사 레코드의 대상인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-136">Indicates whether log analytics is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="1724f-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1724f-137">-PassThru</span></span>
<span data-ttu-id="1724f-138">cmdlet 실행 종료 시 Microsoft 지원 작업 감사 정책을 출력할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-138">Specifies whether to output the Microsoft support operations auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="1724f-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1724f-139">-ResourceGroupName</span></span>
<span data-ttu-id="1724f-140">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="1724f-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1724f-141">-ServerName</span></span>
<span data-ttu-id="1724f-142">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-142">SQL server name.</span></span>

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

### <span data-ttu-id="1724f-143">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="1724f-143">-ServerObject</span></span>
<span data-ttu-id="1724f-144">Microsoft 지원 작업 감사 정책을 관리하는 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-144">The server object to manage its Microsoft support operations audit policy.</span></span>

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

### <span data-ttu-id="1724f-145">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="1724f-145">-StorageAccountResourceId</span></span>
<span data-ttu-id="1724f-146">저장소 계정 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="1724f-146">The storage account resource id</span></span>

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

### <span data-ttu-id="1724f-147">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="1724f-147">-WorkspaceResourceId</span></span>
<span data-ttu-id="1724f-148">Microsoft 지원 작업 감사 로그를 보내고자 하는 Log Analytics 작업 영역의 작업 영역 ID(Log Analytics 작업 영역의 리소스 ID)입니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-148">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Microsoft support operations Audit Logs.</span></span> <span data-ttu-id="1724f-149">예: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="1724f-149">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="1724f-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1724f-150">-Confirm</span></span>
<span data-ttu-id="1724f-151">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1724f-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1724f-152">-WhatIf</span></span>
<span data-ttu-id="1724f-153">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1724f-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1724f-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1724f-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1724f-155">CommonParameters</span></span>
<span data-ttu-id="1724f-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1724f-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1724f-157">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1724f-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1724f-158">입력</span><span class="sxs-lookup"><span data-stu-id="1724f-158">INPUTS</span></span>

### <span data-ttu-id="1724f-159">System.String</span><span class="sxs-lookup"><span data-stu-id="1724f-159">System.String</span></span>

### <span data-ttu-id="1724f-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="1724f-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="1724f-161">System.Guid</span><span class="sxs-lookup"><span data-stu-id="1724f-161">System.Guid</span></span>

### <span data-ttu-id="1724f-162">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1724f-162">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1724f-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="1724f-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="1724f-164">출력</span><span class="sxs-lookup"><span data-stu-id="1724f-164">OUTPUTS</span></span>

### <span data-ttu-id="1724f-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1724f-165">System.Boolean</span></span>

## <span data-ttu-id="1724f-166">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1724f-166">NOTES</span></span>

## <span data-ttu-id="1724f-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1724f-167">RELATED LINKS</span></span>
