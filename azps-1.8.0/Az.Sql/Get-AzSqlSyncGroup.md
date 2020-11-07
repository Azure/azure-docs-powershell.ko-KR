---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
ms.openlocfilehash: fdee39766c7793b4d326077e5c18e0328a5e4c4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698917"
---
# <span data-ttu-id="91280-101">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="91280-101">Get-AzSqlSyncGroup</span></span>

## <span data-ttu-id="91280-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91280-102">SYNOPSIS</span></span>
<span data-ttu-id="91280-103">Azure SQL 데이터베이스 동기화 그룹에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="91280-103">Returns information about Azure SQL Database Sync Groups.</span></span>

## <span data-ttu-id="91280-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91280-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91280-105">설명은</span><span class="sxs-lookup"><span data-stu-id="91280-105">DESCRIPTION</span></span>
<span data-ttu-id="91280-106">**AzSqlSyncGroup** cmdlet은 하나 이상의 Azure SQL 데이터베이스 동기화 그룹에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="91280-106">The **Get-AzSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="91280-107">동기화 그룹의 이름을 지정 하 여 해당 동기화 그룹에 대 한 정보만 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="91280-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="91280-108">예제의</span><span class="sxs-lookup"><span data-stu-id="91280-108">EXAMPLES</span></span>

### <span data-ttu-id="91280-109">예제 1: Azure SQL 데이터베이스에 할당 된 모든 Azure SQL 동기화 그룹 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="91280-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="91280-110">이 명령은 Azure SQL 데이터베이스에 할당 된 모든 Azure SQL 데이터베이스 동기화 그룹에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91280-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="91280-111">예제 2: Azure SQL 데이터베이스 동기화 그룹에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="91280-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="91280-112">이 명령은 이름이 "SyncGroup01" 인 Azure SQL 데이터베이스 동기화 그룹에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91280-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

### <span data-ttu-id="91280-113">예제 3: 필터링을 사용 하 여 Azure SQL 데이터베이스에 할당 된 모든 Azure SQL 동기화 그룹 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="91280-113">Example 3: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database using filtering</span></span>
```
PS C:\>Get-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup*" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :  

ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="91280-114">이 명령은 "SyncGroup"으로 시작 하는 Azure SQL 데이터베이스에 할당 된 모든 Azure SQL 데이터베이스 동기화 그룹에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="91280-114">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database that start with "SyncGroup".</span></span>

## <span data-ttu-id="91280-115">변수</span><span class="sxs-lookup"><span data-stu-id="91280-115">PARAMETERS</span></span>

### <span data-ttu-id="91280-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="91280-116">-DatabaseName</span></span>
<span data-ttu-id="91280-117">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91280-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="91280-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91280-118">-DefaultProfile</span></span>
<span data-ttu-id="91280-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="91280-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91280-120">-이름</span><span class="sxs-lookup"><span data-stu-id="91280-120">-Name</span></span>
<span data-ttu-id="91280-121">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91280-121">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="91280-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91280-122">-ResourceGroupName</span></span>
<span data-ttu-id="91280-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91280-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="91280-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="91280-124">-ServerName</span></span>
<span data-ttu-id="91280-125">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="91280-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="91280-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91280-126">CommonParameters</span></span>
<span data-ttu-id="91280-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91280-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91280-128">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="91280-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91280-129">입력</span><span class="sxs-lookup"><span data-stu-id="91280-129">INPUTS</span></span>

### <span data-ttu-id="91280-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="91280-130">System.String</span></span>

## <span data-ttu-id="91280-131">출력</span><span class="sxs-lookup"><span data-stu-id="91280-131">OUTPUTS</span></span>

### <span data-ttu-id="91280-132">AzureSqlSyncGroupModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="91280-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="91280-133">상속자</span><span class="sxs-lookup"><span data-stu-id="91280-133">NOTES</span></span>

## <span data-ttu-id="91280-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91280-134">RELATED LINKS</span></span>

[<span data-ttu-id="91280-135">새로운 AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="91280-135">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="91280-136">업데이트-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="91280-136">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="91280-137">제거-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="91280-137">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

