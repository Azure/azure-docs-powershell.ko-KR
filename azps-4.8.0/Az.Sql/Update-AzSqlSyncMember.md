---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: eff96559dce38bd1a78fa4e8c789c514ea7b93ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047540"
---
# <span data-ttu-id="0e3fe-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="0e3fe-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="0e3fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e3fe-102">SYNOPSIS</span></span>
<span data-ttu-id="0e3fe-103">Azure SQL 데이터베이스 동기화 구성원을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3fe-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="0e3fe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e3fe-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> [-MemberDatabaseCredential <PSCredential>]
 [-UsePrivateLinkConnection <Boolean>] [-SyncMemberAzureDatabaseResourceId <String>] [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e3fe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0e3fe-105">DESCRIPTION</span></span>
<span data-ttu-id="0e3fe-106">**업데이트 AzSqlSyncGroup** Cmdlet은 Azure SQL 데이터베이스 동기화 구성원의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3fe-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="0e3fe-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0e3fe-107">EXAMPLES</span></span>

### <span data-ttu-id="0e3fe-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0e3fe-108">Example 1</span></span>
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

<span data-ttu-id="0e3fe-109">이 명령은 구성원 데이터베이스에 대 한 관리자 암호를 재설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3fe-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="0e3fe-110">변수</span><span class="sxs-lookup"><span data-stu-id="0e3fe-110">PARAMETERS</span></span>

### <span data-ttu-id="0e3fe-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0e3fe-111">-DatabaseName</span></span>
<span data-ttu-id="0e3fe-112">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e3fe-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="0e3fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e3fe-113">-DefaultProfile</span></span>
<span data-ttu-id="0e3fe-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0e3fe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e3fe-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="0e3fe-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="0e3fe-116">Azure SQL 데이터베이스의 자격 증명 (사용자 이름 및 암호)입니다.</span><span class="sxs-lookup"><span data-stu-id="0e3fe-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="0e3fe-117">-이름</span><span class="sxs-lookup"><span data-stu-id="0e3fe-117">-Name</span></span>
<span data-ttu-id="0e3fe-118">동기화 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e3fe-118">The sync member name.</span></span>

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

### <span data-ttu-id="0e3fe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e3fe-119">-ResourceGroupName</span></span>
<span data-ttu-id="0e3fe-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e3fe-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="0e3fe-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0e3fe-121">-ServerName</span></span>
<span data-ttu-id="0e3fe-122">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e3fe-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="0e3fe-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="0e3fe-123">-SyncGroupName</span></span>
<span data-ttu-id="0e3fe-124">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e3fe-124">The sync group name.</span></span>

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

### <span data-ttu-id="0e3fe-125">-SyncMemberAzureDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="0e3fe-125">-SyncMemberAzureDatabaseResourceId</span></span>
<span data-ttu-id="0e3fe-126">UsePrivateLinkConnection가 true로 설정 된 경우 사용 되는 동기화 구성원 데이터베이스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0e3fe-126">The resource ID for the sync member database, used if UsePrivateLinkConnection is set to true.</span></span>

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

### <span data-ttu-id="0e3fe-127">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="0e3fe-127">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="0e3fe-128">이 동기화 구성원에 연결할 때 비공개 링크를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3fe-128">Whether to use private link when connecting to this sync member.</span></span>

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

### <span data-ttu-id="0e3fe-129">-확인</span><span class="sxs-lookup"><span data-stu-id="0e3fe-129">-Confirm</span></span>
<span data-ttu-id="0e3fe-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3fe-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e3fe-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e3fe-131">-WhatIf</span></span>
<span data-ttu-id="0e3fe-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0e3fe-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e3fe-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e3fe-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e3fe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e3fe-134">CommonParameters</span></span>
<span data-ttu-id="0e3fe-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3fe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e3fe-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e3fe-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e3fe-137">입력</span><span class="sxs-lookup"><span data-stu-id="0e3fe-137">INPUTS</span></span>

### <span data-ttu-id="0e3fe-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0e3fe-138">System.String</span></span>

## <span data-ttu-id="0e3fe-139">출력</span><span class="sxs-lookup"><span data-stu-id="0e3fe-139">OUTPUTS</span></span>

### <span data-ttu-id="0e3fe-140">AzureSqlSyncMemberModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e3fe-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="0e3fe-141">상속자</span><span class="sxs-lookup"><span data-stu-id="0e3fe-141">NOTES</span></span>

## <span data-ttu-id="0e3fe-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e3fe-142">RELATED LINKS</span></span>

[<span data-ttu-id="0e3fe-143">새로운 AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="0e3fe-143">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="0e3fe-144">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="0e3fe-144">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="0e3fe-145">제거-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="0e3fe-145">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

