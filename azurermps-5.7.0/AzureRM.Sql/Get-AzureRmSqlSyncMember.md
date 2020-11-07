---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncMember.md
ms.openlocfilehash: c17daaf714154d24322111497841a1814dfb5773
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702005"
---
# <span data-ttu-id="90409-101">Get-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="90409-101">Get-AzureRmSqlSyncMember</span></span>

## <span data-ttu-id="90409-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90409-102">SYNOPSIS</span></span>
<span data-ttu-id="90409-103">Azure SQL 데이터베이스 동기화 구성원에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="90409-103">Returns information about Azure SQL Database Sync Members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90409-104">구문과</span><span class="sxs-lookup"><span data-stu-id="90409-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncMember [-Name <String>] [-SyncGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90409-105">설명은</span><span class="sxs-lookup"><span data-stu-id="90409-105">DESCRIPTION</span></span>
<span data-ttu-id="90409-106">**AzureRmSqlSyncMember** cmdlet은 하나 이상의 Azure SQL 데이터베이스 동기화 구성원에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="90409-106">The **Get-AzureRmSqlSyncMember** cmdlet returns information about one or more Azure SQL Database Sync Members.</span></span>
<span data-ttu-id="90409-107">해당 동기화 구성원에 대 한 정보만 표시 하도록 동기화 구성원의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90409-107">Specify the name of a sync member to see information for only that sync member.</span></span>

## <span data-ttu-id="90409-108">예제의</span><span class="sxs-lookup"><span data-stu-id="90409-108">EXAMPLES</span></span>

### <span data-ttu-id="90409-109">예제 1: 동기화 그룹에 할당 된 모든 Azure SQL Sync 구성원 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="90409-109">Example 1: Get all instances of Azure SQL Sync Member assigned to a sync group</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" | Format-List
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

<span data-ttu-id="90409-110">이 명령은 동기화 그룹 SyncGroup01에 할당 된 모든 Azure SQL 데이터베이스 동기화 구성원에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90409-110">This command gets information about all the Azure SQL Database Sync Member assigned to the sync group SyncGroup01.</span></span>

### <span data-ttu-id="90409-111">예제 2: Azure SQL 데이터베이스 동기화 구성원에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="90409-111">Example 2: Get information about an Azure SQL Database Sync Member</span></span>
```
PS C:\>Get-AzureRmSqlSyncMember -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SyncGroupName "SyncGroup01" -Name "SyncMember01" | Format-List
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

<span data-ttu-id="90409-112">이 명령은 이름이 "SyncMember01" 인 Azure SQL 데이터베이스 동기화 구성원에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90409-112">This command gets information about the Azure SQL Database Sync Member with name "SyncMember01"</span></span>

## <span data-ttu-id="90409-113">변수</span><span class="sxs-lookup"><span data-stu-id="90409-113">PARAMETERS</span></span>

### <span data-ttu-id="90409-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="90409-114">-DatabaseName</span></span>
<span data-ttu-id="90409-115">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90409-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="90409-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90409-116">-DefaultProfile</span></span>
<span data-ttu-id="90409-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="90409-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90409-118">-이름</span><span class="sxs-lookup"><span data-stu-id="90409-118">-Name</span></span>
<span data-ttu-id="90409-119">동기화 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90409-119">The sync member name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncMemberName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90409-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90409-120">-ResourceGroupName</span></span>
<span data-ttu-id="90409-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90409-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="90409-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="90409-122">-ServerName</span></span>
<span data-ttu-id="90409-123">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90409-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="90409-124">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="90409-124">-SyncGroupName</span></span>
<span data-ttu-id="90409-125">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90409-125">The sync group name.</span></span>

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

### <span data-ttu-id="90409-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90409-126">CommonParameters</span></span>
<span data-ttu-id="90409-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="90409-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90409-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90409-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90409-129">입력</span><span class="sxs-lookup"><span data-stu-id="90409-129">INPUTS</span></span>

### <span data-ttu-id="90409-130">않아야</span><span class="sxs-lookup"><span data-stu-id="90409-130">None</span></span>
<span data-ttu-id="90409-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90409-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="90409-132">출력</span><span class="sxs-lookup"><span data-stu-id="90409-132">OUTPUTS</span></span>

### <span data-ttu-id="90409-133">AzureSqlSyncMemberModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="90409-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncMemberModel</span></span>

## <span data-ttu-id="90409-134">상속자</span><span class="sxs-lookup"><span data-stu-id="90409-134">NOTES</span></span>

## <span data-ttu-id="90409-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90409-135">RELATED LINKS</span></span>

[<span data-ttu-id="90409-136">새로운 AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="90409-136">New-AzureRmSqlSyncMember</span></span>](./New-AzureRmSqlSyncMember.md)

[<span data-ttu-id="90409-137">업데이트-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="90409-137">Update-AzureRmSqlSyncMember</span></span>](./Update-AzureRmSqlSyncMember.md)

[<span data-ttu-id="90409-138">제거-AzureRmSqlSyncMember</span><span class="sxs-lookup"><span data-stu-id="90409-138">Remove-AzureRmSqlSyncMember</span></span>](./Remove-AzureRmSqlSyncMember.md)

