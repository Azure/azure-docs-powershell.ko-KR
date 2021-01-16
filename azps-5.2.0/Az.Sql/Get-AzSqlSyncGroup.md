---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncGroup.md
ms.openlocfilehash: d117ef9685a235528cb91c82a148ff0dddb2d96c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364351"
---
# <span data-ttu-id="1d57d-101">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1d57d-101">Get-AzSqlSyncGroup</span></span>

## <span data-ttu-id="1d57d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d57d-102">SYNOPSIS</span></span>
<span data-ttu-id="1d57d-103">Azure SQL 데이터베이스 동기화 그룹에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1d57d-103">Returns information about Azure SQL Database Sync Groups.</span></span>

## <span data-ttu-id="1d57d-104">구문</span><span class="sxs-lookup"><span data-stu-id="1d57d-104">SYNTAX</span></span>

```
Get-AzSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d57d-105">설명</span><span class="sxs-lookup"><span data-stu-id="1d57d-105">DESCRIPTION</span></span>
<span data-ttu-id="1d57d-106">**Get-AzSqlSyncGroup** cmdlet은 하나 이상의 Azure SQL 데이터베이스 동기화 그룹에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1d57d-106">The **Get-AzSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="1d57d-107">동기화 그룹의 이름을 지정하여 해당 동기화 그룹에 대한 정보만 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="1d57d-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="1d57d-108">예제</span><span class="sxs-lookup"><span data-stu-id="1d57d-108">EXAMPLES</span></span>

### <span data-ttu-id="1d57d-109">예제 1: Azure SQL Database에 할당된 Azure SQL 동기화 그룹의 모든 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d57d-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
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

<span data-ttu-id="1d57d-110">이 명령은 Azure SQL 데이터베이스에 할당된 모든 Azure SQL 데이터베이스 동기화 그룹에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d57d-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="1d57d-111">예제 2: Azure SQL 데이터베이스 동기화 그룹에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="1d57d-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
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

<span data-ttu-id="1d57d-112">이 명령은 이름이 "SyncGroup01"인 Azure SQL 데이터베이스 동기화 그룹에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d57d-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

### <span data-ttu-id="1d57d-113">예제 3: 필터링을 사용하여 Azure SQL 데이터베이스에 할당된 Azure SQL 동기화 그룹의 모든 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d57d-113">Example 3: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database using filtering</span></span>
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

<span data-ttu-id="1d57d-114">이 명령은 "SyncGroup"으로 시작하는 Azure SQL 데이터베이스에 할당된 모든 Azure SQL 데이터베이스 동기화 그룹에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1d57d-114">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database that start with "SyncGroup".</span></span>

## <span data-ttu-id="1d57d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d57d-115">PARAMETERS</span></span>

### <span data-ttu-id="1d57d-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1d57d-116">-DatabaseName</span></span>
<span data-ttu-id="1d57d-117">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d57d-117">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="1d57d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d57d-118">-DefaultProfile</span></span>
<span data-ttu-id="1d57d-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1d57d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d57d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1d57d-120">-Name</span></span>
<span data-ttu-id="1d57d-121">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d57d-121">The sync group name.</span></span>

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

### <span data-ttu-id="1d57d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d57d-122">-ResourceGroupName</span></span>
<span data-ttu-id="1d57d-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d57d-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="1d57d-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1d57d-124">-ServerName</span></span>
<span data-ttu-id="1d57d-125">The name of the Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1d57d-125">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="1d57d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d57d-126">CommonParameters</span></span>
<span data-ttu-id="1d57d-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d57d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d57d-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1d57d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d57d-129">입력</span><span class="sxs-lookup"><span data-stu-id="1d57d-129">INPUTS</span></span>

### <span data-ttu-id="1d57d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1d57d-130">System.String</span></span>

## <span data-ttu-id="1d57d-131">출력</span><span class="sxs-lookup"><span data-stu-id="1d57d-131">OUTPUTS</span></span>

### <span data-ttu-id="1d57d-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="1d57d-132">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="1d57d-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1d57d-133">NOTES</span></span>

## <span data-ttu-id="1d57d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d57d-134">RELATED LINKS</span></span>

[<span data-ttu-id="1d57d-135">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1d57d-135">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="1d57d-136">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1d57d-136">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="1d57d-137">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1d57d-137">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

