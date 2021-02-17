---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: dd57b5d6e4301b1ab22b041367388d37986a946e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188089"
---
# <span data-ttu-id="f45db-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="f45db-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="f45db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f45db-102">SYNOPSIS</span></span>
<span data-ttu-id="f45db-103">Azure SQL Managed Instance 데이터베이스 중복 백업에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f45db-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="f45db-104">구문</span><span class="sxs-lookup"><span data-stu-id="f45db-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f45db-105">설명</span><span class="sxs-lookup"><span data-stu-id="f45db-105">DESCRIPTION</span></span>
<span data-ttu-id="f45db-106">**Get-AzSqlInstanceDatabaseGeoBackup** cmdlet은 Azure SQL Database Managed Instance에서 하나 이상의 Azure SQL 데이터베이스 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f45db-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="f45db-107">예제</span><span class="sxs-lookup"><span data-stu-id="f45db-107">EXAMPLES</span></span>

### <span data-ttu-id="f45db-108">예제 1: 인스턴스에서 모든 데이터베이스 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f45db-108">Example 1: Get all database redundant backups on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="f45db-109">이 명령은 managedInstance1이라는 인스턴스에서 모든 데이터베이스 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f45db-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="f45db-110">예제 2: Managed Instance에서 이름으로 데이터베이스 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f45db-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="f45db-111">이 명령은 managedInstance1이라는 인스턴스에서 managedDatabase1이라는 데이터베이스 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f45db-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="f45db-112">예제 3: 필터링을 사용하여 인스턴스의 모든 데이터베이스 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f45db-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
Name                     : managedDatabase2
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase2
```

<span data-ttu-id="f45db-113">이 명령은 "managedDatabase"로 시작하는 managedInstance1 인스턴스의 모든 데이터베이스 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f45db-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="f45db-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f45db-114">PARAMETERS</span></span>

### <span data-ttu-id="f45db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f45db-115">-DefaultProfile</span></span>
<span data-ttu-id="f45db-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f45db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f45db-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f45db-117">-InstanceName</span></span>
<span data-ttu-id="f45db-118">인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f45db-118">The name of the instance.</span></span>

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

### <span data-ttu-id="f45db-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f45db-119">-Name</span></span>
<span data-ttu-id="f45db-120">검색할 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f45db-120">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RecoverableInstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f45db-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f45db-121">-ResourceGroupName</span></span>
<span data-ttu-id="f45db-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f45db-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f45db-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f45db-123">CommonParameters</span></span>
<span data-ttu-id="f45db-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f45db-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f45db-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f45db-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f45db-126">입력</span><span class="sxs-lookup"><span data-stu-id="f45db-126">INPUTS</span></span>

### <span data-ttu-id="f45db-127">없음</span><span class="sxs-lookup"><span data-stu-id="f45db-127">None</span></span>

## <span data-ttu-id="f45db-128">출력</span><span class="sxs-lookup"><span data-stu-id="f45db-128">OUTPUTS</span></span>

### <span data-ttu-id="f45db-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f45db-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="f45db-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f45db-130">NOTES</span></span>

## <span data-ttu-id="f45db-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f45db-131">RELATED LINKS</span></span>
