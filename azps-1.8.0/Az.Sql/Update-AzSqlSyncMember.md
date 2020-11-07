---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: 76b7366dabc648dc7f5812aedcc7fef18437b68e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698713"
---
# <span data-ttu-id="461da-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="461da-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="461da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="461da-102">SYNOPSIS</span></span>
<span data-ttu-id="461da-103">Azure SQL 데이터베이스 동기화 구성원을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="461da-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="461da-104">구문과</span><span class="sxs-lookup"><span data-stu-id="461da-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="461da-105">설명은</span><span class="sxs-lookup"><span data-stu-id="461da-105">DESCRIPTION</span></span>
<span data-ttu-id="461da-106">**업데이트 AzSqlSyncGroup** Cmdlet은 Azure SQL 데이터베이스 동기화 구성원의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="461da-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="461da-107">예제의</span><span class="sxs-lookup"><span data-stu-id="461da-107">EXAMPLES</span></span>

### <span data-ttu-id="461da-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="461da-108">Example 1</span></span>
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

<span data-ttu-id="461da-109">이 명령은 구성원 데이터베이스에 대 한 관리자 암호를 재설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="461da-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="461da-110">변수</span><span class="sxs-lookup"><span data-stu-id="461da-110">PARAMETERS</span></span>

### <span data-ttu-id="461da-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="461da-111">-DatabaseName</span></span>
<span data-ttu-id="461da-112">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="461da-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="461da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="461da-113">-DefaultProfile</span></span>
<span data-ttu-id="461da-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="461da-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="461da-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="461da-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="461da-116">Azure SQL 데이터베이스의 자격 증명 (사용자 이름 및 암호)입니다.</span><span class="sxs-lookup"><span data-stu-id="461da-116">The credential (username and password) of the Azure SQL Database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="461da-117">-이름</span><span class="sxs-lookup"><span data-stu-id="461da-117">-Name</span></span>
<span data-ttu-id="461da-118">동기화 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="461da-118">The sync member name.</span></span>

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

### <span data-ttu-id="461da-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="461da-119">-ResourceGroupName</span></span>
<span data-ttu-id="461da-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="461da-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="461da-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="461da-121">-ServerName</span></span>
<span data-ttu-id="461da-122">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="461da-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="461da-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="461da-123">-SyncGroupName</span></span>
<span data-ttu-id="461da-124">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="461da-124">The sync group name.</span></span>

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

### <span data-ttu-id="461da-125">-확인</span><span class="sxs-lookup"><span data-stu-id="461da-125">-Confirm</span></span>
<span data-ttu-id="461da-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="461da-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="461da-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="461da-127">-WhatIf</span></span>
<span data-ttu-id="461da-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="461da-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="461da-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="461da-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="461da-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="461da-130">CommonParameters</span></span>
<span data-ttu-id="461da-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="461da-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="461da-132">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="461da-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="461da-133">입력</span><span class="sxs-lookup"><span data-stu-id="461da-133">INPUTS</span></span>

### <span data-ttu-id="461da-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="461da-134">System.String</span></span>

## <span data-ttu-id="461da-135">출력</span><span class="sxs-lookup"><span data-stu-id="461da-135">OUTPUTS</span></span>

### <span data-ttu-id="461da-136">AzureSqlSyncMemberModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="461da-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="461da-137">상속자</span><span class="sxs-lookup"><span data-stu-id="461da-137">NOTES</span></span>

## <span data-ttu-id="461da-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="461da-138">RELATED LINKS</span></span>

[<span data-ttu-id="461da-139">새로운 AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="461da-139">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="461da-140">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="461da-140">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="461da-141">제거-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="461da-141">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

