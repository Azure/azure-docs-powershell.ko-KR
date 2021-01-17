---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncMember.md
ms.openlocfilehash: e5bb853d9dd818801298254eac1f120efcc829a4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374704"
---
# <span data-ttu-id="4f69a-101">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4f69a-101">Get-AzSqlSyncMember</span></span>

## <span data-ttu-id="4f69a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f69a-102">SYNOPSIS</span></span>
<span data-ttu-id="4f69a-103">Azure SQL 데이터베이스 동기화 멤버에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4f69a-103">Returns information about Azure SQL Database Sync Members.</span></span>

## <span data-ttu-id="4f69a-104">구문</span><span class="sxs-lookup"><span data-stu-id="4f69a-104">SYNTAX</span></span>

```
Get-AzSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f69a-105">설명</span><span class="sxs-lookup"><span data-stu-id="4f69a-105">DESCRIPTION</span></span>
<span data-ttu-id="4f69a-106">**Get-AzSqlSyncMember** cmdlet은 하나 이상의 Azure SQL 데이터베이스 동기화 멤버에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4f69a-106">The **Get-AzSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="4f69a-107">동기화 멤버의 이름을 지정하여 해당 동기화 멤버에 대한 정보만 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="4f69a-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="4f69a-108">예제</span><span class="sxs-lookup"><span data-stu-id="4f69a-108">EXAMPLES</span></span>

### <span data-ttu-id="4f69a-109">예제 1: 동기화 그룹에 할당된 Azure SQL 동기화 멤버의 모든 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f69a-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
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
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="4f69a-110">이 명령은 SyncGroup01에 할당된 모든 Azure SQL 데이터베이스 동기화 멤버에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f69a-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="4f69a-111">예제 2: Azure SQL 데이터베이스 동기화 멤버에 대한 정보 얻음</span><span class="sxs-lookup"><span data-stu-id="4f69a-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
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
SyncState                   : Good
```

<span data-ttu-id="4f69a-112">이 명령은 이름이 "SyncMember01"인 Azure SQL 데이터베이스 동기화 멤버에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f69a-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

### <span data-ttu-id="4f69a-113">예제 3: 필터링을 사용하여 동기화 그룹에 할당된 Azure SQL 동기화 멤버의 모든 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f69a-113">Example 3: Get all instances of Azure SQL Sync Member assigned to a sync group using filtering</span></span>
```
PS C:\> Get-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember*" | Format-List
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
SyncState                   : Good 

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}/syncMembers/{SyncMember02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncMemberName              : SyncMember02
SyncDirection               : OneWayMemberToHub
MemberDatabaseType:         : AzureSqlDatabase
SyncAgentId                 : 
SqlServerDatabaseId         : 
MemberServerName            : memberServer01.full.dns.name
MemberDatabaseName          : memberDatabase01
MemberDatabaseUserName      : myAccount
MemberDatabasePassword      :  
SyncState                   : Good
```

<span data-ttu-id="4f69a-114">이 명령은 "SyncMember"로 시작하는 SyncGroup01에 할당된 모든 Azure SQL 데이터베이스 동기화 멤버에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f69a-114">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01 that start with "SyncMember".</span></span>

## <span data-ttu-id="4f69a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f69a-115">PARAMETERS</span></span>

### <span data-ttu-id="4f69a-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4f69a-116">-DatabaseName</span></span>
<span data-ttu-id="4f69a-117">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f69a-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="4f69a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f69a-118">-DefaultProfile</span></span>
<span data-ttu-id="4f69a-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4f69a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f69a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4f69a-120">-Name</span></span>
<span data-ttu-id="4f69a-121">동기화 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f69a-121">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f69a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f69a-122">-ResourceGroupName</span></span>
<span data-ttu-id="4f69a-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f69a-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="4f69a-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4f69a-124">-ServerName</span></span>
<span data-ttu-id="4f69a-125">The name of the Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="4f69a-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="4f69a-126">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="4f69a-126">-SyncGroupName</span></span>
<span data-ttu-id="4f69a-127">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f69a-127">The sync group name.</span></span>

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

### <span data-ttu-id="4f69a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f69a-128">CommonParameters</span></span>
<span data-ttu-id="4f69a-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4f69a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f69a-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4f69a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f69a-131">입력</span><span class="sxs-lookup"><span data-stu-id="4f69a-131">INPUTS</span></span>

### <span data-ttu-id="4f69a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4f69a-132">System.String</span></span>

## <span data-ttu-id="4f69a-133">출력</span><span class="sxs-lookup"><span data-stu-id="4f69a-133">OUTPUTS</span></span>

### <span data-ttu-id="4f69a-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="4f69a-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="4f69a-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4f69a-135">NOTES</span></span>

## <span data-ttu-id="4f69a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f69a-136">RELATED LINKS</span></span>

[<span data-ttu-id="4f69a-137">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4f69a-137">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="4f69a-138">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4f69a-138">Update-AzSqlSyncMember</span></span>](./Update-AzSqlSyncMember.md)

[<span data-ttu-id="4f69a-139">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="4f69a-139">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

