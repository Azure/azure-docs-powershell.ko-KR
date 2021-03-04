---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgent.md
ms.openlocfilehash: 08248056ec98d79e00f2c606870e21af495310f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959355"
---
# <span data-ttu-id="21dc1-101">Get-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="21dc1-101">Get-AzSqlSyncAgent</span></span>

## <span data-ttu-id="21dc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21dc1-102">SYNOPSIS</span></span>
<span data-ttu-id="21dc1-103">Azure SQL 동기화 에이전트에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="21dc1-103">Returns information about Azure SQL Sync Agents.</span></span>

## <span data-ttu-id="21dc1-104">구문</span><span class="sxs-lookup"><span data-stu-id="21dc1-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21dc1-105">설명</span><span class="sxs-lookup"><span data-stu-id="21dc1-105">DESCRIPTION</span></span>
<span data-ttu-id="21dc1-106">**Get-AzSqlSyncAgent** cmdlet은 하나 이상의 Azure SQL 동기화 에이전트에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="21dc1-106">The **Get-AzSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="21dc1-107">동기화 에이전트의 이름을 지정하여 해당 동기화 에이전트에 대한 정보를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="21dc1-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="21dc1-108">예제</span><span class="sxs-lookup"><span data-stu-id="21dc1-108">EXAMPLES</span></span>

### <span data-ttu-id="21dc1-109">예제 1: Azure SQL 할당된 Azure SQL 동기화 에이전트의 모든 인스턴스를 SQL Server</span><span class="sxs-lookup"><span data-stu-id="21dc1-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
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

<span data-ttu-id="21dc1-110">이 명령은 Azure SQL 할당된 모든 Azure SQL Server 정보를 SQL Server.</span><span class="sxs-lookup"><span data-stu-id="21dc1-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="21dc1-111">예제 2: Azure SQL 동기화 에이전트에 대한 정보 얻음</span><span class="sxs-lookup"><span data-stu-id="21dc1-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
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

<span data-ttu-id="21dc1-112">이 명령은 "SyncAgent01"을 SQL Azure 데이터베이스 동기화 에이전트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="21dc1-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

### <span data-ttu-id="21dc1-113">예제 3: 필터링을 사용하여 Azure SQL Azure SQL Server 동기화 에이전트의 모든 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="21dc1-113">Example 3: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server using filtering</span></span>
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

<span data-ttu-id="21dc1-114">이 명령은 "SyncAgent"로 시작하는 Azure SQL 할당된 모든 Azure SQL Server 동기화 에이전트에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="21dc1-114">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server that start with "SyncAgent".</span></span>

## <span data-ttu-id="21dc1-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="21dc1-115">PARAMETERS</span></span>

### <span data-ttu-id="21dc1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21dc1-116">-DefaultProfile</span></span>
<span data-ttu-id="21dc1-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="21dc1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21dc1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="21dc1-118">-Name</span></span>
<span data-ttu-id="21dc1-119">동기화 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21dc1-119">The sync agent name.</span></span>

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

### <span data-ttu-id="21dc1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21dc1-120">-ResourceGroupName</span></span>
<span data-ttu-id="21dc1-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21dc1-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="21dc1-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="21dc1-122">-ServerName</span></span>
<span data-ttu-id="21dc1-123">동기화 에이전트가 SQL Server Azure 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21dc1-123">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="21dc1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21dc1-124">CommonParameters</span></span>
<span data-ttu-id="21dc1-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="21dc1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21dc1-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21dc1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21dc1-127">입력</span><span class="sxs-lookup"><span data-stu-id="21dc1-127">INPUTS</span></span>

### <span data-ttu-id="21dc1-128">System.String</span><span class="sxs-lookup"><span data-stu-id="21dc1-128">System.String</span></span>

## <span data-ttu-id="21dc1-129">출력</span><span class="sxs-lookup"><span data-stu-id="21dc1-129">OUTPUTS</span></span>

### <span data-ttu-id="21dc1-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span><span class="sxs-lookup"><span data-stu-id="21dc1-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="21dc1-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="21dc1-131">NOTES</span></span>

## <span data-ttu-id="21dc1-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21dc1-132">RELATED LINKS</span></span>

[<span data-ttu-id="21dc1-133">Remove-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="21dc1-133">Remove-AzSqlSyncAgent</span></span>](./Remove-AzSqlSyncAgent.md)

[<span data-ttu-id="21dc1-134">New-AzSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="21dc1-134">New-AzSqlSyncAgent</span></span>](./New-AzSqlSyncAgent.md)

