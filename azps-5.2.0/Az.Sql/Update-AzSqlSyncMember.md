---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: eff96559dce38bd1a78fa4e8c789c514ea7b93ec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364778"
---
# <span data-ttu-id="24ebb-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="24ebb-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="24ebb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="24ebb-103">Azure SQL 데이터베이스 동기화 멤버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="24ebb-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="24ebb-104">구문</span><span class="sxs-lookup"><span data-stu-id="24ebb-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> [-MemberDatabaseCredential <PSCredential>]
 [-UsePrivateLinkConnection <Boolean>] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24ebb-105">설명</span><span class="sxs-lookup"><span data-stu-id="24ebb-105">DESCRIPTION</span></span>
<span data-ttu-id="24ebb-106">**Update-AzSqlSyncGroup** cmdlet은 Azure SQL 데이터베이스 동기화 멤버의 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="24ebb-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="24ebb-107">예제</span><span class="sxs-lookup"><span data-stu-id="24ebb-107">EXAMPLES</span></span>

### <span data-ttu-id="24ebb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="24ebb-108">Example 1</span></span>
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

<span data-ttu-id="24ebb-109">이 명령은 멤버 데이터베이스에 대한 관리자 암호를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="24ebb-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="24ebb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24ebb-110">PARAMETERS</span></span>

### <span data-ttu-id="24ebb-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="24ebb-111">-DatabaseName</span></span>
<span data-ttu-id="24ebb-112">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24ebb-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="24ebb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ebb-113">-DefaultProfile</span></span>
<span data-ttu-id="24ebb-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="24ebb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24ebb-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="24ebb-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="24ebb-116">Azure SQL Database의 자격 증명(사용자 이름 및 암호)입니다.</span><span class="sxs-lookup"><span data-stu-id="24ebb-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="24ebb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="24ebb-117">-Name</span></span>
<span data-ttu-id="24ebb-118">동기화 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24ebb-118">The sync member name.</span></span>

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

### <span data-ttu-id="24ebb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24ebb-119">-ResourceGroupName</span></span>
<span data-ttu-id="24ebb-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24ebb-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="24ebb-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="24ebb-121">-ServerName</span></span>
<span data-ttu-id="24ebb-122">The name of the Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="24ebb-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="24ebb-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="24ebb-123">-SyncGroupName</span></span>
<span data-ttu-id="24ebb-124">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24ebb-124">The sync group name.</span></span>

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

### <span data-ttu-id="24ebb-125">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="24ebb-125">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="24ebb-126">UsePrivateLinkConnection이 true로 설정된 경우 사용되는 동기화 멤버 데이터베이스에 대한 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="24ebb-126">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="24ebb-127">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="24ebb-127">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="24ebb-128">이 동기화 멤버에 연결할 때 개인 링크를 사용할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="24ebb-128">Whether to use private link when connecting to this sync member.</span></span>

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

### <span data-ttu-id="24ebb-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24ebb-129">-Confirm</span></span>
<span data-ttu-id="24ebb-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="24ebb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24ebb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24ebb-131">-WhatIf</span></span>
<span data-ttu-id="24ebb-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="24ebb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24ebb-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24ebb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24ebb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ebb-134">CommonParameters</span></span>
<span data-ttu-id="24ebb-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="24ebb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ebb-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="24ebb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ebb-137">입력</span><span class="sxs-lookup"><span data-stu-id="24ebb-137">INPUTS</span></span>

### <span data-ttu-id="24ebb-138">System.String</span><span class="sxs-lookup"><span data-stu-id="24ebb-138">System.String</span></span>

## <span data-ttu-id="24ebb-139">출력</span><span class="sxs-lookup"><span data-stu-id="24ebb-139">OUTPUTS</span></span>

### <span data-ttu-id="24ebb-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span><span class="sxs-lookup"><span data-stu-id="24ebb-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="24ebb-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="24ebb-141">NOTES</span></span>

## <span data-ttu-id="24ebb-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24ebb-142">RELATED LINKS</span></span>

[<span data-ttu-id="24ebb-143">New-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="24ebb-143">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="24ebb-144">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="24ebb-144">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="24ebb-145">Remove-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="24ebb-145">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

