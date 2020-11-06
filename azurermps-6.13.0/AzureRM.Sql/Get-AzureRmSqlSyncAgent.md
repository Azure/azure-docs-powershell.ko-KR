---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgent.md
ms.openlocfilehash: 8b590e6ba8329ba6e0c45d30f7163c637d90f79e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530038"
---
# <span data-ttu-id="c6b4f-101">Get-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c6b4f-101">Get-AzureRmSqlSyncAgent</span></span>

## <span data-ttu-id="c6b4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6b4f-102">SYNOPSIS</span></span>
<span data-ttu-id="c6b4f-103">Azure SQL 동기화 에이전트에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6b4f-103">Returns information about Azure SQL Sync Agents.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6b4f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6b4f-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgent [[-Name] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6b4f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c6b4f-105">DESCRIPTION</span></span>
<span data-ttu-id="c6b4f-106">**AzureRmSqlSyncAgent** cmdlet은 하나 이상의 Azure SQL 동기화 에이전트에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6b4f-106">The **Get-AzureRmSqlSyncAgent** cmdlet returns information about one or more Azure SQL Sync Agents.</span></span>
<span data-ttu-id="c6b4f-107">동기화 에이전트의 이름을 지정 하 여 해당 동기화 에이전트에 대 한 정보만 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6b4f-107">Specify the name of a sync agent to see information for only that sync agent.</span></span>

## <span data-ttu-id="c6b4f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c6b4f-108">EXAMPLES</span></span>

### <span data-ttu-id="c6b4f-109">예제 1: Azure SQL Server에 할당 된 모든 Azure SQL 동기화 에이전트 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="c6b4f-109">Example 1: Get all instances of Azure SQL Sync Agent assigned to an Azure SQL Server</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
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

<span data-ttu-id="c6b4f-110">이 명령은 Azure SQL Server에 할당 된 모든 Azure SQL 동기화 에이전트에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6b4f-110">This command gets information about all the Azure SQL Sync Agents assigned to an Azure SQL Server.</span></span>

### <span data-ttu-id="c6b4f-111">예제 2: Azure SQL 동기화 에이전트에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="c6b4f-111">Example 2: Get information about an Azure SQL Sync Agent</span></span>
```
PS C:\>Get-AzureRmSqlSyncAgent -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -Name "SyncAgent01" | Format-List
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

<span data-ttu-id="c6b4f-112">이 명령은 이름이 "SyncAgent01" 인 Azure SQL 데이터베이스 동기화 에이전트에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6b4f-112">This command gets information about the Azure SQL Database Sync Agent with name "SyncAgent01"</span></span>

## <span data-ttu-id="c6b4f-113">변수</span><span class="sxs-lookup"><span data-stu-id="c6b4f-113">PARAMETERS</span></span>

### <span data-ttu-id="c6b4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6b4f-114">-DefaultProfile</span></span>
<span data-ttu-id="c6b4f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c6b4f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6b4f-116">-이름</span><span class="sxs-lookup"><span data-stu-id="c6b4f-116">-Name</span></span>
<span data-ttu-id="c6b4f-117">동기화 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6b4f-117">The sync agent name.</span></span>

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

### <span data-ttu-id="c6b4f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6b4f-118">-ResourceGroupName</span></span>
<span data-ttu-id="c6b4f-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6b4f-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="c6b4f-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c6b4f-120">-ServerName</span></span>
<span data-ttu-id="c6b4f-121">동기화 에이전트가 있는 Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6b4f-121">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="c6b4f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6b4f-122">CommonParameters</span></span>
<span data-ttu-id="c6b4f-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6b4f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6b4f-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6b4f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6b4f-125">입력</span><span class="sxs-lookup"><span data-stu-id="c6b4f-125">INPUTS</span></span>

### <span data-ttu-id="c6b4f-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c6b4f-126">System.String</span></span>

## <span data-ttu-id="c6b4f-127">출력</span><span class="sxs-lookup"><span data-stu-id="c6b4f-127">OUTPUTS</span></span>

### <span data-ttu-id="c6b4f-128">AzureSqlSyncAgentModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6b4f-128">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentModel</span></span>

## <span data-ttu-id="c6b4f-129">상속자</span><span class="sxs-lookup"><span data-stu-id="c6b4f-129">NOTES</span></span>

## <span data-ttu-id="c6b4f-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6b4f-130">RELATED LINKS</span></span>

[<span data-ttu-id="c6b4f-131">제거-AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c6b4f-131">Remove-AzureRmSqlSyncAgent</span></span>](./Remove-AzureRmSqlSyncAgent.md)

[<span data-ttu-id="c6b4f-132">새로운 AzureRmSqlSyncAgent</span><span class="sxs-lookup"><span data-stu-id="c6b4f-132">New-AzureRmSqlSyncAgent</span></span>](./New-AzureRmSqlSyncAgent.md)

