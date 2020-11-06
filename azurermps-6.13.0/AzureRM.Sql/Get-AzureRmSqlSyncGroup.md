---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
ms.openlocfilehash: bc4a547ec216cc4c88837f48eadc1c1e80c9087a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535111"
---
# <span data-ttu-id="4eb56-101">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4eb56-101">Get-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="4eb56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eb56-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb56-103">Azure SQL 데이터베이스 동기화 그룹에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eb56-103">Returns information about Azure SQL Database Sync Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4eb56-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4eb56-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4eb56-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4eb56-105">DESCRIPTION</span></span>
<span data-ttu-id="4eb56-106">**AzureRmSqlSyncGroup** cmdlet은 하나 이상의 Azure SQL 데이터베이스 동기화 그룹에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eb56-106">The **Get-AzureRmSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="4eb56-107">동기화 그룹의 이름을 지정 하 여 해당 동기화 그룹에 대 한 정보만 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eb56-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="4eb56-108">예제의</span><span class="sxs-lookup"><span data-stu-id="4eb56-108">EXAMPLES</span></span>

### <span data-ttu-id="4eb56-109">예제 1: Azure SQL 데이터베이스에 할당 된 모든 Azure SQL 동기화 그룹 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="4eb56-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Format-List
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

<span data-ttu-id="4eb56-110">이 명령은 Azure SQL 데이터베이스에 할당 된 모든 Azure SQL 데이터베이스 동기화 그룹에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4eb56-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="4eb56-111">예제 2: Azure SQL 데이터베이스 동기화 그룹에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="4eb56-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
```
PS C:\>Get-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" | Format-List
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

<span data-ttu-id="4eb56-112">이 명령은 이름이 "SyncGroup01" 인 Azure SQL 데이터베이스 동기화 그룹에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4eb56-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

## <span data-ttu-id="4eb56-113">변수</span><span class="sxs-lookup"><span data-stu-id="4eb56-113">PARAMETERS</span></span>

### <span data-ttu-id="4eb56-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4eb56-114">-DatabaseName</span></span>
<span data-ttu-id="4eb56-115">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4eb56-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="4eb56-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb56-116">-DefaultProfile</span></span>
<span data-ttu-id="4eb56-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4eb56-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4eb56-118">-이름</span><span class="sxs-lookup"><span data-stu-id="4eb56-118">-Name</span></span>
<span data-ttu-id="4eb56-119">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4eb56-119">The sync group name.</span></span>

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

### <span data-ttu-id="4eb56-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb56-120">-ResourceGroupName</span></span>
<span data-ttu-id="4eb56-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4eb56-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="4eb56-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4eb56-122">-ServerName</span></span>
<span data-ttu-id="4eb56-123">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4eb56-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="4eb56-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb56-124">CommonParameters</span></span>
<span data-ttu-id="4eb56-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eb56-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb56-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eb56-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb56-127">입력</span><span class="sxs-lookup"><span data-stu-id="4eb56-127">INPUTS</span></span>

### <span data-ttu-id="4eb56-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4eb56-128">System.String</span></span>

## <span data-ttu-id="4eb56-129">출력</span><span class="sxs-lookup"><span data-stu-id="4eb56-129">OUTPUTS</span></span>

### <span data-ttu-id="4eb56-130">AzureSqlSyncGroupModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="4eb56-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="4eb56-131">상속자</span><span class="sxs-lookup"><span data-stu-id="4eb56-131">NOTES</span></span>

## <span data-ttu-id="4eb56-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4eb56-132">RELATED LINKS</span></span>

[<span data-ttu-id="4eb56-133">새로운 AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4eb56-133">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="4eb56-134">업데이트-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4eb56-134">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="4eb56-135">제거-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="4eb56-135">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

