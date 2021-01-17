---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: 8bb031ffa2924ce0cace8d2c7daf94be97713eec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374788"
---
# <span data-ttu-id="88ec7-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="88ec7-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="88ec7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88ec7-102">SYNOPSIS</span></span>
<span data-ttu-id="88ec7-103">Azure SQL 동기화 에이전트에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec7-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="88ec7-104">구문</span><span class="sxs-lookup"><span data-stu-id="88ec7-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88ec7-105">설명</span><span class="sxs-lookup"><span data-stu-id="88ec7-105">DESCRIPTION</span></span>
<span data-ttu-id="88ec7-106">**Get-AzSqlSyncAgent** cmdlet은 하나 이상의 Azure SQL 동기화 에이전트에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec7-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="88ec7-107">동기화 에이전트의 이름을 지정하여 해당 동기화 에이전트에 대한 정보만 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec7-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="88ec7-108">예제</span><span class="sxs-lookup"><span data-stu-id="88ec7-108">EXAMPLES</span></span>

### <span data-ttu-id="88ec7-109">예제 1: Azure SQL 동기화 에이전트의 모든 인스턴스를 Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="88ec7-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="88ec7-110">이 명령은 Azure SQL 할당된 모든 Azure SQL 동기화 에이전트에 대한 정보를 SQL Server.</span><span class="sxs-lookup"><span data-stu-id="88ec7-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="88ec7-111">예제 2: Azure SQL 동기화 에이전트에 대한 정보 얻음</span><span class="sxs-lookup"><span data-stu-id="88ec7-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="88ec7-112">이 명령은 이름이 "SyncAgent01"인 Azure SQL 데이터베이스 동기화 에이전트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88ec7-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="88ec7-113">예제 3: 필터링을 사용하여 Azure SQL 할당된 Azure SQL Server 동기화 에이전트의 모든 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88ec7-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
```
PS C:\>Get-AzSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name SyncAgent* | Format-List
ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online

ResourceId                  : subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/syncAgents/{SyncAgent02}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncAgentName               : SyncAgent02
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
LastAliveTime:              : 6/1/2017 5:08:48 AM
Version                     : 4.3.6348.1
IsUpToDate                  : False
ExpiryTime                  : 
State                       : Online
```

<span data-ttu-id="88ec7-114">이 명령은 "SyncAgent"로 시작하는 Azure SQL 할당된 모든 Azure SQL Server 동기화 에이전트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88ec7-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="88ec7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88ec7-115">PARAMETERS</span></span>

### <span data-ttu-id="88ec7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ec7-116">-DefaultProfile</span></span>
<span data-ttu-id="88ec7-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="88ec7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88ec7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="88ec7-118">-Name</span></span>
<span data-ttu-id="88ec7-119">동기화 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88ec7-119">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncAgentName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ec7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88ec7-120">-ResourceGroupName</span></span>
<span data-ttu-id="88ec7-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88ec7-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="88ec7-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="88ec7-122">-ServerName</span></span>
<span data-ttu-id="88ec7-123">동기화 에이전트가 SQL Server Azure 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88ec7-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="88ec7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ec7-124">CommonParameters</span></span>
<span data-ttu-id="88ec7-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88ec7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ec7-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="88ec7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ec7-127">입력</span><span class="sxs-lookup"><span data-stu-id="88ec7-127">INPUTS</span></span>

### <span data-ttu-id="88ec7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="88ec7-128">System.String</span></span>

## <span data-ttu-id="88ec7-129">출력</span><span class="sxs-lookup"><span data-stu-id="88ec7-129">OUTPUTS</span></span>

### <span data-ttu-id="88ec7-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="88ec7-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="88ec7-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="88ec7-131">NOTES</span></span>

## <span data-ttu-id="88ec7-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88ec7-132">RELATED LINKS</span></span>

[<span data-ttu-id="88ec7-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="88ec7-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="88ec7-134">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="88ec7-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

