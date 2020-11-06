---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncGroup.md
ms.openlocfilehash: 71a4d20c6296c8a9d725cb9a16960d6c4a06646c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528775"
---
# <span data-ttu-id="30451-101">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="30451-101">Get-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="30451-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30451-102">SYNOPSIS</span></span>
<span data-ttu-id="30451-103">Azure SQL 데이터베이스 동기화 그룹에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="30451-103">Returns information about Azure SQL Database Sync Groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30451-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30451-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncGroup [[-Name] <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30451-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30451-105">DESCRIPTION</span></span>
<span data-ttu-id="30451-106">**AzureRmSqlSyncGroup** cmdlet은 하나 이상의 Azure SQL 데이터베이스 동기화 그룹에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="30451-106">The **Get-AzureRmSqlSyncGroup** cmdlet returns information about one or more Azure SQL Database Sync Groups.</span></span>
<span data-ttu-id="30451-107">동기화 그룹의 이름을 지정 하 여 해당 동기화 그룹에 대 한 정보만 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="30451-107">Specify the name of a sync group to see information for only that sync group.</span></span>

## <span data-ttu-id="30451-108">예제의</span><span class="sxs-lookup"><span data-stu-id="30451-108">EXAMPLES</span></span>

### <span data-ttu-id="30451-109">예제 1: Azure SQL 데이터베이스에 할당 된 모든 Azure SQL 동기화 그룹 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="30451-109">Example 1: Get all instances of Azure SQL Sync Group assigned to an Azure SQL Database</span></span>
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

<span data-ttu-id="30451-110">이 명령은 Azure SQL 데이터베이스에 할당 된 모든 Azure SQL 데이터베이스 동기화 그룹에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30451-110">This command gets information about all the Azure SQL Database Sync Groups assigned to an Azure SQL Database.</span></span>

### <span data-ttu-id="30451-111">예제 2: Azure SQL 데이터베이스 동기화 그룹에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="30451-111">Example 2: Get information about an Azure SQL Database Sync Group</span></span>
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

<span data-ttu-id="30451-112">이 명령은 이름이 "SyncGroup01" 인 Azure SQL 데이터베이스 동기화 그룹에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="30451-112">This command gets information about the Azure SQL Database Sync Group with name "SyncGroup01"</span></span>

## <span data-ttu-id="30451-113">변수</span><span class="sxs-lookup"><span data-stu-id="30451-113">PARAMETERS</span></span>

### <span data-ttu-id="30451-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="30451-114">-DatabaseName</span></span>
<span data-ttu-id="30451-115">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30451-115">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="30451-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30451-116">-DefaultProfile</span></span>
<span data-ttu-id="30451-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="30451-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30451-118">-이름</span><span class="sxs-lookup"><span data-stu-id="30451-118">-Name</span></span>
<span data-ttu-id="30451-119">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30451-119">The sync group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30451-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30451-120">-ResourceGroupName</span></span>
<span data-ttu-id="30451-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30451-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="30451-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="30451-122">-ServerName</span></span>
<span data-ttu-id="30451-123">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="30451-123">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="30451-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30451-124">CommonParameters</span></span>
<span data-ttu-id="30451-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30451-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30451-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30451-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30451-127">입력</span><span class="sxs-lookup"><span data-stu-id="30451-127">INPUTS</span></span>

### <span data-ttu-id="30451-128">않아야</span><span class="sxs-lookup"><span data-stu-id="30451-128">None</span></span>
<span data-ttu-id="30451-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30451-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30451-130">출력</span><span class="sxs-lookup"><span data-stu-id="30451-130">OUTPUTS</span></span>

### <span data-ttu-id="30451-131">AzureSqlSyncGroupModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="30451-131">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="30451-132">상속자</span><span class="sxs-lookup"><span data-stu-id="30451-132">NOTES</span></span>

## <span data-ttu-id="30451-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30451-133">RELATED LINKS</span></span>

[<span data-ttu-id="30451-134">새로운 AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="30451-134">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="30451-135">업데이트-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="30451-135">Update-AzureRmSqlSyncGroup</span></span>](./Update-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="30451-136">제거-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="30451-136">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

