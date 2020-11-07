---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncMember.md
ms.openlocfilehash: 503f7be9d4d7f595ac8d337568038d7e7e724d1f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698865"
---
# <span data-ttu-id="23f60-101">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="23f60-101">New-AzSqlSyncMember</span></span>

## <span data-ttu-id="23f60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23f60-102">SYNOPSIS</span></span>
<span data-ttu-id="23f60-103">Azure SQL 데이터베이스 동기화 구성원을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-103">Creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="23f60-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23f60-104">SYNTAX</span></span>

### <span data-ttu-id="23f60-105">AzureSqlDatabase (기본값)</span><span class="sxs-lookup"><span data-stu-id="23f60-105">AzureSqlDatabase (Default)</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23f60-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="23f60-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23f60-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="23f60-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23f60-108">설명은</span><span class="sxs-lookup"><span data-stu-id="23f60-108">DESCRIPTION</span></span>
<span data-ttu-id="23f60-109">**AzSqlSyncMember** Cmdlet은 Azure SQL 데이터베이스 동기화 구성원을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-109">The **New-AzSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="23f60-110">예제의</span><span class="sxs-lookup"><span data-stu-id="23f60-110">EXAMPLES</span></span>

### <span data-ttu-id="23f60-111">예제 1: Azure SQL 데이터베이스에 대 한 동기화 구성원을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
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

<span data-ttu-id="23f60-112">이 명령은 Azure SQL 데이터베이스에 대 한 동기화 구성원을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="23f60-113">예제 2: 온-프레미스 SQL Server 데이터베이스에 대 한 동기화 구성원 만들기</span><span class="sxs-lookup"><span data-stu-id="23f60-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
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

<span data-ttu-id="23f60-114">이 명령은 온-프레미스 SQL 데이터베이스에 대 한 동기화 구성원을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="23f60-115">변수</span><span class="sxs-lookup"><span data-stu-id="23f60-115">PARAMETERS</span></span>

### <span data-ttu-id="23f60-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="23f60-116">-DatabaseName</span></span>
<span data-ttu-id="23f60-117">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="23f60-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f60-118">-DefaultProfile</span></span>
<span data-ttu-id="23f60-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="23f60-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23f60-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="23f60-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="23f60-121">Azure SQL 데이터베이스의 자격 증명 (사용자 이름 및 암호)입니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-121">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="23f60-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="23f60-122">-MemberDatabaseName</span></span>
<span data-ttu-id="23f60-123">구성원 데이터베이스의 Azure SQL 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-123">The Azure SQL Database name of the member database.</span></span>

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

### <span data-ttu-id="23f60-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="23f60-124">-MemberDatabaseType</span></span>
<span data-ttu-id="23f60-125">구성원 데이터베이스의 데이터베이스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-125">The database type of the member database.</span></span>

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

### <span data-ttu-id="23f60-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="23f60-126">-MemberServerName</span></span>
<span data-ttu-id="23f60-127">구성원 데이터베이스의 Azure SQL Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-127">The Azure SQL Server Name of the member database.</span></span>

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

### <span data-ttu-id="23f60-128">-이름</span><span class="sxs-lookup"><span data-stu-id="23f60-128">-Name</span></span>
<span data-ttu-id="23f60-129">동기화 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-129">The sync member name.</span></span>

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

### <span data-ttu-id="23f60-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23f60-130">-ResourceGroupName</span></span>
<span data-ttu-id="23f60-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="23f60-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="23f60-132">-ServerName</span></span>
<span data-ttu-id="23f60-133">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-133">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="23f60-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="23f60-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="23f60-135">동기화 에이전트로 연결 된 SQL server 데이터베이스의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-135">The id of the SQL server database which is connected by the sync agent.</span></span>

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

### <span data-ttu-id="23f60-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="23f60-136">-SyncAgentName</span></span>
<span data-ttu-id="23f60-137">동기화 에이전트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-137">The name of the sync agent.</span></span>

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

### <span data-ttu-id="23f60-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23f60-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="23f60-139">동기화 에이전트가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-139">The name of the resource group where the sync agent is under.</span></span>

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

### <span data-ttu-id="23f60-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="23f60-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="23f60-141">동기화 에이전트의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-141">The resource ID of the sync agent.</span></span>

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

### <span data-ttu-id="23f60-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="23f60-142">-SyncAgentServerName</span></span>
<span data-ttu-id="23f60-143">동기화 에이전트가 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

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

### <span data-ttu-id="23f60-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="23f60-144">-SyncDirection</span></span>
<span data-ttu-id="23f60-145">이 동기화 구성원의 동기화 방향입니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-145">The sync direction of this sync member.</span></span>

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

### <span data-ttu-id="23f60-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="23f60-146">-SyncGroupName</span></span>
<span data-ttu-id="23f60-147">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-147">The sync group name.</span></span>

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

### <span data-ttu-id="23f60-148">-확인</span><span class="sxs-lookup"><span data-stu-id="23f60-148">-Confirm</span></span>
<span data-ttu-id="23f60-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23f60-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23f60-150">-WhatIf</span></span>
<span data-ttu-id="23f60-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23f60-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23f60-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f60-153">CommonParameters</span></span>
<span data-ttu-id="23f60-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f60-155">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="23f60-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f60-156">입력</span><span class="sxs-lookup"><span data-stu-id="23f60-156">INPUTS</span></span>

### <span data-ttu-id="23f60-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="23f60-157">System.String</span></span>

## <span data-ttu-id="23f60-158">출력</span><span class="sxs-lookup"><span data-stu-id="23f60-158">OUTPUTS</span></span>

### <span data-ttu-id="23f60-159">AzureSqlSyncMemberModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="23f60-159">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="23f60-160">상속자</span><span class="sxs-lookup"><span data-stu-id="23f60-160">NOTES</span></span>

## <span data-ttu-id="23f60-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23f60-161">RELATED LINKS</span></span>

[<span data-ttu-id="23f60-162">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="23f60-162">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="23f60-163">Set-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="23f60-163">Set-AzSqlSyncMember</span></span>](./Set-AzSqlSyncMember.md)

[<span data-ttu-id="23f60-164">제거-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="23f60-164">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

