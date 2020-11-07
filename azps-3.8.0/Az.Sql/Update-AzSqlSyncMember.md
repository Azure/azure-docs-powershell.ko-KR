---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncMember.md
ms.openlocfilehash: 634ce84e355dbd106865b0f1072b693bd03a623b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878665"
---
# <span data-ttu-id="0e8ab-101">Update-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="0e8ab-101">Update-AzSqlSyncMember</span></span>

## <span data-ttu-id="0e8ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e8ab-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8ab-103">Azure SQL 데이터베이스 동기화 구성원을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ab-103">Updates an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="0e8ab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e8ab-104">SYNTAX</span></span>

```
Update-AzSqlSyncMember -Name <String> -MemberDatabaseCredential <PSCredential> [-SyncGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e8ab-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0e8ab-105">DESCRIPTION</span></span>
<span data-ttu-id="0e8ab-106">**업데이트 AzSqlSyncGroup** Cmdlet은 Azure SQL 데이터베이스 동기화 구성원의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ab-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Member.</span></span>

## <span data-ttu-id="0e8ab-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0e8ab-107">EXAMPLES</span></span>

### <span data-ttu-id="0e8ab-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0e8ab-108">Example 1</span></span>
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

<span data-ttu-id="0e8ab-109">이 명령은 구성원 데이터베이스에 대 한 관리자 암호를 재설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ab-109">This command resets the administrator password for the member database.</span></span>

## <span data-ttu-id="0e8ab-110">변수</span><span class="sxs-lookup"><span data-stu-id="0e8ab-110">PARAMETERS</span></span>

### <span data-ttu-id="0e8ab-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0e8ab-111">-DatabaseName</span></span>
<span data-ttu-id="0e8ab-112">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ab-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="0e8ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e8ab-113">-DefaultProfile</span></span>
<span data-ttu-id="0e8ab-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0e8ab-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e8ab-115">-MemberDatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="0e8ab-115">-MemberDatabaseCredential</span></span>
<span data-ttu-id="0e8ab-116">Azure SQL 데이터베이스의 자격 증명 (사용자 이름 및 암호)입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ab-116">The credential (username and password) of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="0e8ab-117">-이름</span><span class="sxs-lookup"><span data-stu-id="0e8ab-117">-Name</span></span>
<span data-ttu-id="0e8ab-118">동기화 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ab-118">The sync member name.</span></span>

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

### <span data-ttu-id="0e8ab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e8ab-119">-ResourceGroupName</span></span>
<span data-ttu-id="0e8ab-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ab-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="0e8ab-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0e8ab-121">-ServerName</span></span>
<span data-ttu-id="0e8ab-122">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ab-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="0e8ab-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="0e8ab-123">-SyncGroupName</span></span>
<span data-ttu-id="0e8ab-124">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ab-124">The sync group name.</span></span>

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

### <span data-ttu-id="0e8ab-125">-확인</span><span class="sxs-lookup"><span data-stu-id="0e8ab-125">-Confirm</span></span>
<span data-ttu-id="0e8ab-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ab-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e8ab-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e8ab-127">-WhatIf</span></span>
<span data-ttu-id="0e8ab-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ab-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e8ab-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ab-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e8ab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e8ab-130">CommonParameters</span></span>
<span data-ttu-id="0e8ab-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e8ab-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e8ab-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e8ab-133">입력</span><span class="sxs-lookup"><span data-stu-id="0e8ab-133">INPUTS</span></span>

### <span data-ttu-id="0e8ab-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0e8ab-134">System.String</span></span>

## <span data-ttu-id="0e8ab-135">출력</span><span class="sxs-lookup"><span data-stu-id="0e8ab-135">OUTPUTS</span></span>

### <span data-ttu-id="0e8ab-136">AzureSqlSyncMemberModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ab-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="0e8ab-137">상속자</span><span class="sxs-lookup"><span data-stu-id="0e8ab-137">NOTES</span></span>

## <span data-ttu-id="0e8ab-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e8ab-138">RELATED LINKS</span></span>

[<span data-ttu-id="0e8ab-139">새로운 AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="0e8ab-139">New-AzSqlSyncMember</span></span>](./New-AzSqlSyncMember.md)

[<span data-ttu-id="0e8ab-140">Get-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="0e8ab-140">Get-AzSqlSyncMember</span></span>](./Get-AzSqlSyncMember.md)

[<span data-ttu-id="0e8ab-141">제거-AzSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="0e8ab-141">Remove-AzSqlSyncMember</span></span>](./Remove-AzSqlSyncMember.md)

