---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
ms.openlocfilehash: 3ce7abdb2feb053fe2731484fda0f301225c0b6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005296"
---
# <span data-ttu-id="48873-101">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="48873-101">Get-AzSqlSyncGroup</span></span>

## <span data-ttu-id="48873-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48873-102">SYNOPSIS</span></span>
<span data-ttu-id="48873-103">Azure 데이터베이스 동기화 그룹에 대한 SQL 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="48873-103">Returns information about Azure SQL Database Sync Groups.</span></span>

## <span data-ttu-id="48873-104">구문</span><span class="sxs-lookup"><span data-stu-id="48873-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48873-105">설명</span><span class="sxs-lookup"><span data-stu-id="48873-105">DESCRIPTION</span></span>
<span data-ttu-id="48873-106">**Get-AzSqlSyncGroup** cmdlet은 데이터베이스 동기화 그룹에 대한 하나 SQL 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="48873-106">The **Get-AzSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="48873-107">동기화 그룹의 이름을 지정하여 해당 동기화 그룹에 대한 정보만 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="48873-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="48873-108">예제</span><span class="sxs-lookup"><span data-stu-id="48873-108">EXAMPLES</span></span>

### <span data-ttu-id="48873-109">예제 1: Azure SQL 데이터베이스에 할당된 Azure SQL 동기화 그룹의 모든 인스턴스 SQL</span><span class="sxs-lookup"><span data-stu-id="48873-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
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

<span data-ttu-id="48873-110">이 명령은 Azure SQL 데이터베이스에 할당된 모든 Azure SQL 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48873-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="48873-111">예제 2: Azure 데이터베이스 동기화 그룹에 대한 SQL 정보 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48873-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
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

<span data-ttu-id="48873-112">이 명령은 "SyncGroup01"을 사용하여 Azure SQL 데이터베이스 동기화 그룹에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48873-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

### <span data-ttu-id="48873-113">예제 3: 필터링을 사용하여 Azure SQL 데이터베이스에 할당된 Azure SQL 동기화 그룹의 모든 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48873-113">Example 3: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database using filtering</span></span>
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

<span data-ttu-id="48873-114">이 명령은 "SyncGroup"SQL Azure SQL 데이터베이스 동기화 그룹에 할당된 모든 Azure 데이터베이스 동기화 그룹에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48873-114">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database that start with "SyncGroup".</span></span>

## <span data-ttu-id="48873-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="48873-115">PARAMETERS</span></span>

### <span data-ttu-id="48873-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="48873-116">-DatabaseName</span></span>
<span data-ttu-id="48873-117">Azure 데이터베이스의 SQL 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="48873-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="48873-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48873-118">-DefaultProfile</span></span>
<span data-ttu-id="48873-119">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="48873-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48873-120">-Name</span><span class="sxs-lookup"><span data-stu-id="48873-120">-Name</span></span>
<span data-ttu-id="48873-121">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48873-121">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48873-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48873-122">-ResourceGroupName</span></span>
<span data-ttu-id="48873-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48873-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="48873-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="48873-124">-ServerName</span></span>
<span data-ttu-id="48873-125">The name of the Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="48873-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="48873-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48873-126">CommonParameters</span></span>
<span data-ttu-id="48873-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="48873-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48873-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48873-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48873-129">입력</span><span class="sxs-lookup"><span data-stu-id="48873-129">INPUTS</span></span>

### <span data-ttu-id="48873-130">System.String</span><span class="sxs-lookup"><span data-stu-id="48873-130">System.String</span></span>

## <span data-ttu-id="48873-131">출력</span><span class="sxs-lookup"><span data-stu-id="48873-131">OUTPUTS</span></span>

### <span data-ttu-id="48873-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="48873-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="48873-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="48873-133">NOTES</span></span>

## <span data-ttu-id="48873-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48873-134">RELATED LINKS</span></span>

[<span data-ttu-id="48873-135">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="48873-135">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="48873-136">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="48873-136">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="48873-137">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="48873-137">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

