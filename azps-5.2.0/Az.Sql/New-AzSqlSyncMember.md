---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: f7fc860711c5037e6ce6390f9fb7d79ddfa7d6ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344042"
---
# <span data-ttu-id="c9559-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c9559-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="c9559-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9559-102">SYNOPSIS</span></span>
<span data-ttu-id="c9559-103">Azure SQL 데이터베이스 동기화 멤버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="c9559-104">구문</span><span class="sxs-lookup"><span data-stu-id="c9559-104">SYNTAX</span></span>

### <span data-ttu-id="c9559-105">AzureSqlDatabase(기본값)</span><span class="sxs-lookup"><span data-stu-id="c9559-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9559-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="c9559-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-UsePrivateLinkConnection] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9559-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="c9559-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-UsePrivateLinkConnection]
 [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9559-108">설명</span><span class="sxs-lookup"><span data-stu-id="c9559-108">DESCRIPTION</span></span>
<span data-ttu-id="c9559-109">**New-AzSqlSyncMember** cmdlet은 Azure SQL 데이터베이스 동기화 멤버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="c9559-110">예제</span><span class="sxs-lookup"><span data-stu-id="c9559-110">EXAMPLES</span></span>

### <span data-ttu-id="c9559-111">예제 1: Azure SQL 데이터베이스의 동기화 멤버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "AzureSqlDatabase" -MemberServerName "memberServer01.full.dns.name" -MemberDatabaseName "memberDatabase01" -MemberDatabaseCredential $credential | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : UnProvisioned
```

<span data-ttu-id="c9559-112">이 명령은 Azure SQL 데이터베이스에 대한 동기화 멤버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="c9559-113">예제 2: 데이터베이스에 대한 동기화 멤버 만들기 SQL Server</span><span class="sxs-lookup"><span data-stu-id="c9559-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
-MemberDatabaseType "SqlServerDatabase" -SqlServerDatabaseId "dbId" -syncAgentResourceGroupName "syncAgentResourceGroupName" -syncAgentServerName "syncAgentServerName" 
-syncAgentDatabaseName "syncAgentDatabaseName" -syncAgentName "agentName" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember01
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : /subscriptions/{subscriptionId}/resourceGroups/{syncAgentResourceGroupName}/servers/{syncAgentServerName}/syncAgents/{syncAgentId}
SqlServerDatabaseId         : dbId
MemberServerName            : 
MemberDatabaseName          : 
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      : 
SyncState                   : UnProvisioned
```

<span data-ttu-id="c9559-114">이 명령은 데이터베이스에 대한 동기화 멤버를 SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="c9559-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9559-115">PARAMETERS</span></span>

### <span data-ttu-id="c9559-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c9559-116">-DatabaseName</span></span>
<span data-ttu-id="c9559-117">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-117">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9559-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9559-118">-DefaultProfile</span></span>
<span data-ttu-id="c9559-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c9559-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9559-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="c9559-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="c9559-121">Azure SQL Database의 자격 증명(사용자 이름 및 암호)입니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-121">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9559-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c9559-122">-MemberDatabaseName</span></span>
<span data-ttu-id="c9559-123">Azure SQL 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-123">The Azure SQL Database name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9559-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="c9559-124">-MemberDatabaseType</span></span>
<span data-ttu-id="c9559-125">멤버 데이터베이스의 데이터베이스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-125">The database type of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SqlServerDatabase, AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9559-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="c9559-126">-MemberServerName</span></span>
<span data-ttu-id="c9559-127">Azure SQL Server 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-127">The Azure SQL Server Name of the member database.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9559-128">-Name</span><span class="sxs-lookup"><span data-stu-id="c9559-128">-Name</span></span>
<span data-ttu-id="c9559-129">동기화 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-129">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9559-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9559-130">-ResourceGroupName</span></span>
<span data-ttu-id="c9559-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9559-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c9559-132">-ServerName</span></span>
<span data-ttu-id="c9559-133">The name of the Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c9559-133">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9559-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="c9559-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="c9559-135">동기화 에이전트에 SQL 서버 데이터베이스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-135">The id of the SQL server database which is connected by the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent, OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9559-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="c9559-136">-SyncAgentName</span></span>
<span data-ttu-id="c9559-137">동기화 에이전트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-137">The name of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9559-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9559-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="c9559-139">동기화 에이전트가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-139">The name of the resource group where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9559-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="c9559-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="c9559-141">동기화 에이전트의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-141">The resource ID of the sync agent.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9559-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="c9559-142">-SyncAgentServerName</span></span>
<span data-ttu-id="c9559-143">동기화 에이전트가 SQL Server Azure 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

```yaml
Type: System.String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9559-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="c9559-144">-SyncDirection</span></span>
<span data-ttu-id="c9559-145">이 동기화 멤버의 동기화 방향입니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-145">The sync direction of this sync member.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Bidirectional, OneWayMemberToHub, OneWayHubToMember

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9559-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="c9559-146">-SyncGroupName</span></span>
<span data-ttu-id="c9559-147">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-147">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9559-148">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="c9559-148">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="c9559-149">UsePrivateLinkConnection이 true로 설정된 경우 사용되는 동기화 멤버 데이터베이스에 대한 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-149">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="c9559-150">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="c9559-150">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="c9559-151">이 동기화 멤버에 연결할 때 개인 링크 연결을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="c9559-151">Use a private link connection when connecting to this sync member.</span></span>

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

### <span data-ttu-id="c9559-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9559-152">-Confirm</span></span>
<span data-ttu-id="c9559-153">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9559-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9559-154">-WhatIf</span></span>
<span data-ttu-id="c9559-155">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c9559-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9559-156">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9559-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9559-157">CommonParameters</span></span>
<span data-ttu-id="c9559-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9559-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9559-159">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c9559-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9559-160">입력</span><span class="sxs-lookup"><span data-stu-id="c9559-160">INPUTS</span></span>

### <span data-ttu-id="c9559-161">System.String</span><span class="sxs-lookup"><span data-stu-id="c9559-161">System.String</span></span>

## <span data-ttu-id="c9559-162">출력</span><span class="sxs-lookup"><span data-stu-id="c9559-162">OUTPUTS</span></span>

### <span data-ttu-id="c9559-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="c9559-163">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="c9559-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c9559-164">NOTES</span></span>

## <span data-ttu-id="c9559-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9559-165">RELATED LINKS</span></span>

[<span data-ttu-id="c9559-166">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c9559-166">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="c9559-167">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c9559-167">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="c9559-168">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="c9559-168">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

