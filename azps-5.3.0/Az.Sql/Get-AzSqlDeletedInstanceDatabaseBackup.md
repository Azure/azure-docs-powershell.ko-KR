---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeletedinstancedatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
ms.openlocfilehash: bee6bd373c6b9c67afa8c70385c397d9334b733e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374837"
---
# <span data-ttu-id="3f189-101">Get-AzSqlDeletedInstanceDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="3f189-101">Get-AzSqlDeletedInstanceDatabaseBackup</span></span>

## <span data-ttu-id="3f189-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f189-102">SYNOPSIS</span></span>
<span data-ttu-id="3f189-103">복원할 수 있는 삭제된 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3f189-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="3f189-104">구문</span><span class="sxs-lookup"><span data-stu-id="3f189-104">SYNTAX</span></span>

### <span data-ttu-id="3f189-105">DeletedDatabaseList(기본값)</span><span class="sxs-lookup"><span data-stu-id="3f189-105">DeletedDatabaseList (Default)</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f189-106">DeletedDatabaseByNameAndDeletedTime</span><span class="sxs-lookup"><span data-stu-id="3f189-106">DeletedDatabaseByNameAndDeletedTime</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 -DatabaseName <String> [-DeletionDate] <DateTime> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f189-107">설명</span><span class="sxs-lookup"><span data-stu-id="3f189-107">DESCRIPTION</span></span>
<span data-ttu-id="3f189-108">**Get-AzSqlDeletedInstanceDatabaseBackup** cmdlet은 복원할 수 있는 지정된 삭제된 SQL Instance 데이터베이스 백업 또는 복원할 수 있는 모든 삭제된 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3f189-108">The **Get-AzSqlDeletedInstanceDatabaseBackup** cmdlet gets a specified deleted SQL Instance database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="3f189-109">이 cmdlet은 Azure의 SQL Instance Stretch Database 서비스에서도 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="3f189-109">This cmdlet is also supported by the SQL Instance Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3f189-110">예제</span><span class="sxs-lookup"><span data-stu-id="3f189-110">EXAMPLES</span></span>

### <span data-ttu-id="3f189-111">예제 1: 서버에서 모든 삭제된 데이터베이스 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3f189-111">Example 1: Get all deleted database backups on a server</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000

DeletionDate         : 2019-03-04 04:00:08 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB3
CreationDate         : 2019-03-04 03:00:31 AM
EarliestRestorePoint : 2019-03-04 03:05:23 AM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB3,13196145
                       6082100000
```

<span data-ttu-id="3f189-112">이 명령은 서버에서 삭제된 모든 데이터베이스 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3f189-112">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="3f189-113">예제 2: 지정된 삭제된 데이터베이스 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3f189-113">Example 2: Get a specified deleted database backup</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000
```

## <span data-ttu-id="3f189-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f189-114">PARAMETERS</span></span>

### <span data-ttu-id="3f189-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3f189-115">-DatabaseName</span></span>
<span data-ttu-id="3f189-116">백업을 검색할 Azure SQL Instance 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f189-116">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f189-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f189-117">-DefaultProfile</span></span>
<span data-ttu-id="3f189-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f189-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f189-119">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="3f189-119">-DeletionDate</span></span>
<span data-ttu-id="3f189-120">밀리초 정밀도(예: 2016-02-23T00:21:22.847Z)를 사용하여 백업을 검색할 Azure SQL Instance Database의 지운 날짜입니다.</span><span class="sxs-lookup"><span data-stu-id="3f189-120">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f189-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3f189-121">-InstanceName</span></span>
<span data-ttu-id="3f189-122">데이터베이스가 있는 Azure SQL Managed Instance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f189-122">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f189-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f189-123">-ResourceGroupName</span></span>
<span data-ttu-id="3f189-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f189-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f189-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f189-125">CommonParameters</span></span>
<span data-ttu-id="3f189-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3f189-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f189-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3f189-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f189-128">입력</span><span class="sxs-lookup"><span data-stu-id="3f189-128">INPUTS</span></span>

### <span data-ttu-id="3f189-129">없음</span><span class="sxs-lookup"><span data-stu-id="3f189-129">None</span></span>

## <span data-ttu-id="3f189-130">출력</span><span class="sxs-lookup"><span data-stu-id="3f189-130">OUTPUTS</span></span>

### <span data-ttu-id="3f189-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="3f189-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span></span>

## <span data-ttu-id="3f189-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3f189-132">NOTES</span></span>

## <span data-ttu-id="3f189-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f189-133">RELATED LINKS</span></span>
