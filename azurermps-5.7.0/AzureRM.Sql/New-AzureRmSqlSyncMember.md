---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncMember.md
ms.openlocfilehash: d2df78cc4cbf7bea7918653e310193bf013d7495
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531594"
---
# <span data-ttu-id="4e1d2-101">New-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4e1d2-101">New-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="4e1d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e1d2-102">SYNOPSIS</span></span>
<span data-ttu-id="4e1d2-103">Azure SQL 데이터베이스 동기화 구성원을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-103">Creates an Azure SQL Database Sync Member.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e1d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4e1d2-104">SYNTAX</span></span>

### <span data-ttu-id="4e1d2-105">AzureSqlDatabase (기본값)</span><span class="sxs-lookup"><span data-stu-id="4e1d2-105">AzureSqlDatabase (Default)</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -MemberServerName <String>
 -MemberDatabaseName <String> -MemberDatabaseCredential <PSCredential> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e1d2-106">OnPremisesDatabaseSyncAgentComponent</span><span class="sxs-lookup"><span data-stu-id="4e1d2-106">OnPremisesDatabaseSyncAgentComponent</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SyncAgentResourceGroupName <String>
 -SyncAgentServerName <String> -SyncAgentName <String> -SqlServerDatabaseId <String> [-SyncDirection <String>]
 [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e1d2-107">OnPremisesDatabaseSyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="4e1d2-107">OnPremisesDatabaseSyncAgentResourceID</span></span>
```
New-AzureRmSqlSyncMember -Name <String> -MemberDatabaseType <String> -SqlServerDatabaseId <String>
 -SyncAgentResourceID <String> [-SyncDirection <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e1d2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4e1d2-108">DESCRIPTION</span></span>
<span data-ttu-id="4e1d2-109">**AzureRmSqlSyncMember** Cmdlet은 Azure SQL 데이터베이스 동기화 구성원을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-109">The **New-AzureRmSqlSyncMember** cmdlet creates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="4e1d2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4e1d2-110">EXAMPLES</span></span>

### <span data-ttu-id="4e1d2-111">예제 1: Azure SQL 데이터베이스에 대 한 동기화 구성원을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-111">Example 1: Create a sync member for an Azure SQL database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="4e1d2-112">이 명령은 Azure SQL 데이터베이스에 대 한 동기화 구성원을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-112">This command creates a sync member for an Azure SQL database.</span></span>

### <span data-ttu-id="4e1d2-113">예제 2: 온-프레미스 SQL Server 데이터베이스에 대 한 동기화 구성원 만들기</span><span class="sxs-lookup"><span data-stu-id="4e1d2-113">Example 2: Create a sync member for an on-premises SQL Server database</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" -SyncDirection "OneWayMemberToHub"
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

<span data-ttu-id="4e1d2-114">이 명령은 온-프레미스 SQL 데이터베이스에 대 한 동기화 구성원을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-114">This command creates a sync member for an on-premises SQL database.</span></span>

## <span data-ttu-id="4e1d2-115">변수</span><span class="sxs-lookup"><span data-stu-id="4e1d2-115">PARAMETERS</span></span>

### <span data-ttu-id="4e1d2-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e1d2-116">-DatabaseName</span></span>
<span data-ttu-id="4e1d2-117">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-117">The name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e1d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e1d2-118">-DefaultProfile</span></span>
<span data-ttu-id="4e1d2-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4e1d2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1d2-120">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="4e1d2-120">-MemberDatabaseCredential</span></span>
<span data-ttu-id="4e1d2-121">Azure SQL 데이터베이스의 자격 증명 (사용자 이름 및 암호)입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-121">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1d2-122">-MemberDatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e1d2-122">-MemberDatabaseName</span></span>
<span data-ttu-id="4e1d2-123">구성원 데이터베이스의 Azure SQL 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-123">The Azure SQL Database name of the member database.</span></span>

```yaml
Type: String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1d2-124">-MemberDatabaseType</span><span class="sxs-lookup"><span data-stu-id="4e1d2-124">-MemberDatabaseType</span></span>
<span data-ttu-id="4e1d2-125">구성원 데이터베이스의 데이터베이스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-125">The database type of the member database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: SqlServerDatabase, AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e1d2-126">-MemberServerName</span><span class="sxs-lookup"><span data-stu-id="4e1d2-126">-MemberServerName</span></span>
<span data-ttu-id="4e1d2-127">구성원 데이터베이스의 Azure SQL Server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-127">The Azure SQL Server Name of the member database.</span></span>

```yaml
Type: String
Parameter Sets: AzureSqlDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1d2-128">-이름</span><span class="sxs-lookup"><span data-stu-id="4e1d2-128">-Name</span></span>
<span data-ttu-id="4e1d2-129">동기화 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-129">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e1d2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e1d2-130">-ResourceGroupName</span></span>
<span data-ttu-id="4e1d2-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-131">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e1d2-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4e1d2-132">-ServerName</span></span>
<span data-ttu-id="4e1d2-133">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-133">The name of the Azure SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e1d2-134">-SqlServerDatabaseId</span><span class="sxs-lookup"><span data-stu-id="4e1d2-134">-SqlServerDatabaseId</span></span>
<span data-ttu-id="4e1d2-135">동기화 에이전트로 연결 된 SQL server 데이터베이스의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-135">The id of the SQL server database which is connected by the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent, OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1d2-136">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="4e1d2-136">-SyncAgentName</span></span>
<span data-ttu-id="4e1d2-137">동기화 에이전트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-137">The name of the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1d2-138">-SyncAgentResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e1d2-138">-SyncAgentResourceGroupName</span></span>
<span data-ttu-id="4e1d2-139">동기화 에이전트가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-139">The name of the resource group where the sync agent is under.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1d2-140">-SyncAgentResourceID</span><span class="sxs-lookup"><span data-stu-id="4e1d2-140">-SyncAgentResourceID</span></span>
<span data-ttu-id="4e1d2-141">동기화 에이전트의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-141">The resource ID of the sync agent.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentResourceID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1d2-142">-SyncAgentServerName</span><span class="sxs-lookup"><span data-stu-id="4e1d2-142">-SyncAgentServerName</span></span>
<span data-ttu-id="4e1d2-143">동기화 에이전트가 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-143">The name of the Azure SQL Server where the sync agent is under.</span></span>

```yaml
Type: String
Parameter Sets: OnPremisesDatabaseSyncAgentComponent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1d2-144">-SyncDirection</span><span class="sxs-lookup"><span data-stu-id="4e1d2-144">-SyncDirection</span></span>
<span data-ttu-id="4e1d2-145">이 동기화 구성원의 동기화 방향입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-145">The sync direction of this sync member.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Bidirectional, OneWayMemberToHub, OneWayHubToMember

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1d2-146">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4e1d2-146">-SyncGroupName</span></span>
<span data-ttu-id="4e1d2-147">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-147">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e1d2-148">-확인</span><span class="sxs-lookup"><span data-stu-id="4e1d2-148">-Confirm</span></span>
<span data-ttu-id="4e1d2-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e1d2-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e1d2-150">-WhatIf</span></span>
<span data-ttu-id="4e1d2-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e1d2-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e1d2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e1d2-153">CommonParameters</span></span>
<span data-ttu-id="4e1d2-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e1d2-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e1d2-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e1d2-156">입력</span><span class="sxs-lookup"><span data-stu-id="4e1d2-156">INPUTS</span></span>

### <span data-ttu-id="4e1d2-157">않아야</span><span class="sxs-lookup"><span data-stu-id="4e1d2-157">None</span></span>
<span data-ttu-id="4e1d2-158">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4e1d2-159">출력</span><span class="sxs-lookup"><span data-stu-id="4e1d2-159">OUTPUTS</span></span>

### <span data-ttu-id="4e1d2-160">AzureSqlSyncMemberModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e1d2-160">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="4e1d2-161">상속자</span><span class="sxs-lookup"><span data-stu-id="4e1d2-161">NOTES</span></span>

## <span data-ttu-id="4e1d2-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4e1d2-162">RELATED LINKS</span></span>

[<span data-ttu-id="4e1d2-163">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4e1d2-163">Get-AzureRmSqlSyncMember</span></span>](./Get-AzureRmSqlSyncMember.md)

[<span data-ttu-id="4e1d2-164">Set-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4e1d2-164">Set-AzureRmSqlSyncMember</span></span>](./Set-AzureRmSqlSyncMember.md)

[<span data-ttu-id="4e1d2-165">제거-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4e1d2-165">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

