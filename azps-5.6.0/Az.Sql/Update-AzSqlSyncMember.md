---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: 3c4b50a4d4f4c01365d853e64cb3a53ea9c05d44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992259"
---
# <span data-ttu-id="5464a-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="5464a-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="5464a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5464a-102">SYNOPSIS</span></span>
<span data-ttu-id="5464a-103">Azure 데이터베이스 동기화 SQL 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5464a-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="5464a-104">구문</span><span class="sxs-lookup"><span data-stu-id="5464a-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> [-MemberDatabaseCredential <PSCredential>]
 [-UsePrivateLinkConnection <Boolean>] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5464a-105">설명</span><span class="sxs-lookup"><span data-stu-id="5464a-105">DESCRIPTION</span></span>
<span data-ttu-id="5464a-106">**Update-AzSqlSyncGroup** cmdlet은 Azure 데이터베이스 동기화 멤버의 속성을 SQL 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="5464a-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="5464a-107">예제</span><span class="sxs-lookup"><span data-stu-id="5464a-107">EXAMPLES</span></span>

### <span data-ttu-id="5464a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5464a-108">Example 1</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01"
-MemberDatabaseCredential $credential | Format-List
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
MemberDatabaseUserName      : myAccount-new
MemberDatabasePassword      : 
SyncState                   : Good
```

<span data-ttu-id="5464a-109">이 명령은 멤버 데이터베이스에 대한 관리자 암호를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5464a-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="5464a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5464a-110">PARAMETERS</span></span>

### <span data-ttu-id="5464a-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5464a-111">-DatabaseName</span></span>
<span data-ttu-id="5464a-112">Azure 데이터베이스의 SQL 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="5464a-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="5464a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5464a-113">-DefaultProfile</span></span>
<span data-ttu-id="5464a-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5464a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5464a-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="5464a-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="5464a-116">Azure SQL 데이터베이스의 자격 증명(사용자 이름 및 암호)입니다.</span><span class="sxs-lookup"><span data-stu-id="5464a-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5464a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5464a-117">-Name</span></span>
<span data-ttu-id="5464a-118">동기화 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5464a-118">The sync member name.</span></span>

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

### <span data-ttu-id="5464a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5464a-119">-ResourceGroupName</span></span>
<span data-ttu-id="5464a-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5464a-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="5464a-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5464a-121">-ServerName</span></span>
<span data-ttu-id="5464a-122">The name of the Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5464a-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="5464a-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="5464a-123">-SyncGroupName</span></span>
<span data-ttu-id="5464a-124">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5464a-124">The sync group name.</span></span>

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

### <span data-ttu-id="5464a-125">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="5464a-125">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="5464a-126">UsePrivateLinkConnection이 true로 설정된 경우 사용되는 동기화 멤버 데이터베이스에 대한 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5464a-126">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="5464a-127">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="5464a-127">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="5464a-128">이 동기화 멤버에 연결할 때 개인 링크를 사용할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="5464a-128">Whether to use private link when connecting to this sync member.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5464a-129">-확인</span><span class="sxs-lookup"><span data-stu-id="5464a-129">-Confirm</span></span>
<span data-ttu-id="5464a-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5464a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5464a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5464a-131">-WhatIf</span></span>
<span data-ttu-id="5464a-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5464a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5464a-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5464a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5464a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5464a-134">CommonParameters</span></span>
<span data-ttu-id="5464a-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5464a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5464a-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5464a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5464a-137">입력</span><span class="sxs-lookup"><span data-stu-id="5464a-137">INPUTS</span></span>

### <span data-ttu-id="5464a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5464a-138">System.String</span></span>

## <span data-ttu-id="5464a-139">출력</span><span class="sxs-lookup"><span data-stu-id="5464a-139">OUTPUTS</span></span>

### <span data-ttu-id="5464a-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="5464a-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="5464a-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5464a-141">NOTES</span></span>

## <span data-ttu-id="5464a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5464a-142">RELATED LINKS</span></span>

[<span data-ttu-id="5464a-143">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="5464a-143">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="5464a-144">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="5464a-144">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="5464a-145">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="5464a-145">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

