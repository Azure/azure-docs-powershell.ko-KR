---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeletedinstancedatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
ms.openlocfilehash: ce68b8c8a03fbfe99adbb6070df072dd8ebb0cd2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873676"
---
# <span data-ttu-id="9a031-101">Get-AzSqlDeletedInstanceDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="9a031-101">Get-AzSqlDeletedInstanceDatabaseBackup</span></span>

## <span data-ttu-id="9a031-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a031-102">SYNOPSIS</span></span>
<span data-ttu-id="9a031-103">복원할 수 있는 삭제 된 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a031-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="9a031-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a031-104">SYNTAX</span></span>

### <span data-ttu-id="9a031-105">DeletedDatabaseList (기본값)</span><span class="sxs-lookup"><span data-stu-id="9a031-105">DeletedDatabaseList (Default)</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a031-106">DeletedDatabaseByNameAndDeletedTime</span><span class="sxs-lookup"><span data-stu-id="9a031-106">DeletedDatabaseByNameAndDeletedTime</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 -DatabaseName <String> [-DeletionDate] <DateTime> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a031-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9a031-107">DESCRIPTION</span></span>
<span data-ttu-id="9a031-108">**AzSqlDeletedInstanceDatabaseBackup** cmdlet은 복원할 수 있는 지정한 삭제 된 SQL 인스턴스 데이터베이스 백업을 만들거나, 모든 삭제 된 백업을 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a031-108">The **Get-AzSqlDeletedInstanceDatabaseBackup** cmdlet gets a specified deleted SQL Instance database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="9a031-109">이 cmdlet은 Azure의 SQL 인스턴스 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a031-109">This cmdlet is also supported by the SQL Instance Stretch Database service on Azure.</span></span>

## <span data-ttu-id="9a031-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9a031-110">EXAMPLES</span></span>

### <span data-ttu-id="9a031-111">예제 1: 서버에서 삭제 된 모든 데이터베이스 백업 가져오기</span><span class="sxs-lookup"><span data-stu-id="9a031-111">Example 1: Get all deleted database backups on a server</span></span>
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

<span data-ttu-id="9a031-112">이 명령은 서버에서 삭제 된 모든 데이터베이스 백업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a031-112">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="9a031-113">예제 2: 지정한 삭제 된 데이터베이스 백업 가져오기</span><span class="sxs-lookup"><span data-stu-id="9a031-113">Example 2: Get a specified deleted database backup</span></span>
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

## <span data-ttu-id="9a031-114">변수</span><span class="sxs-lookup"><span data-stu-id="9a031-114">PARAMETERS</span></span>

### <span data-ttu-id="9a031-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9a031-115">-DatabaseName</span></span>
<span data-ttu-id="9a031-116">백업을 검색할 Azure SQL 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a031-116">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="9a031-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a031-117">-DefaultProfile</span></span>
<span data-ttu-id="9a031-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a031-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a031-119">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="9a031-119">-DeletionDate</span></span>
<span data-ttu-id="9a031-120">백업을 검색할 Azure SQL 인스턴스 데이터베이스의 삭제 날짜입니다 (예: 2016-02-23T00:21:22.847 Z).</span><span class="sxs-lookup"><span data-stu-id="9a031-120">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="9a031-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9a031-121">-InstanceName</span></span>
<span data-ttu-id="9a031-122">데이터베이스가 있는 Azure SQL 관리 되는 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a031-122">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="9a031-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a031-123">-ResourceGroupName</span></span>
<span data-ttu-id="9a031-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a031-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="9a031-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a031-125">CommonParameters</span></span>
<span data-ttu-id="9a031-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a031-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a031-127">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9a031-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a031-128">입력</span><span class="sxs-lookup"><span data-stu-id="9a031-128">INPUTS</span></span>

### <span data-ttu-id="9a031-129">않아야</span><span class="sxs-lookup"><span data-stu-id="9a031-129">None</span></span>

## <span data-ttu-id="9a031-130">출력</span><span class="sxs-lookup"><span data-stu-id="9a031-130">OUTPUTS</span></span>

### <span data-ttu-id="9a031-131">AzureSqlDeletedManagedDatabaseBackupModel (\*). m. ManagedDatabaseBackup.</span><span class="sxs-lookup"><span data-stu-id="9a031-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span></span>

## <span data-ttu-id="9a031-132">상속자</span><span class="sxs-lookup"><span data-stu-id="9a031-132">NOTES</span></span>

## <span data-ttu-id="9a031-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a031-133">RELATED LINKS</span></span>
