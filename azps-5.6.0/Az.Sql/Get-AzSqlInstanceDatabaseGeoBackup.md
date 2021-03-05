---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseGeoBackup.md
ms.openlocfilehash: dd66238627c96d2b3b1a8aaa2ebc7e2505515d66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999467"
---
# <span data-ttu-id="ccf1b-101">Get-AzSqlInstanceDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="ccf1b-101">Get-AzSqlInstanceDatabaseGeoBackup</span></span>

## <span data-ttu-id="ccf1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccf1b-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf1b-103">Managed Instance 데이터베이스 중복 SQL Azure에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1b-103">Returns information about Azure SQL Managed Instance database redundant backup.</span></span>

## <span data-ttu-id="ccf1b-104">구문</span><span class="sxs-lookup"><span data-stu-id="ccf1b-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseGeoBackup [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccf1b-105">설명</span><span class="sxs-lookup"><span data-stu-id="ccf1b-105">DESCRIPTION</span></span>
<span data-ttu-id="ccf1b-106">**Get-AzSqlInstanceDatabaseGeoBackup** cmdlet은 Azure SQL 데이터베이스 관리 인스턴스에서 하나 이상의 Azure SQL 백업을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1b-106">The **Get-AzSqlInstanceDatabaseGeoBackup** cmdlet gets one or more Azure SQL databases redundant backups from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="ccf1b-107">예제</span><span class="sxs-lookup"><span data-stu-id="ccf1b-107">EXAMPLES</span></span>

### <span data-ttu-id="ccf1b-108">예제 1: 인스턴스에서 모든 데이터베이스 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1b-108">Example 1: Get all database redundant backups on a instance</span></span>
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

<span data-ttu-id="ccf1b-109">이 명령은 managedInstance1이라는 인스턴스의 모든 데이터베이스 중복 백업을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1b-109">This command gets all database redundant backups on the instance named managedInstance1.</span></span>

### <span data-ttu-id="ccf1b-110">예제 2: 관리되는 인스턴스의 이름으로 데이터베이스 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1b-110">Example 2: Get a database redundant backup by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabaseGeoBackup -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
Name                     : managedDatabase1
LastAvailableBackupDate  : 01/31/2019 20:44:57
RecoverableDatabaseId   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/recoverableDatabases/managedDatabase1
```

<span data-ttu-id="ccf1b-111">이 명령은 managedInstance1이라는 인스턴스에서 managedDatabase1이라는 데이터베이스 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1b-111">This command gets a database redundant backup named managedDatabase1 from an instance named managedInstance1.</span></span>

### <span data-ttu-id="ccf1b-112">예제 3: 필터링을 사용하여 인스턴스의 모든 데이터베이스 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1b-112">Example 3: Get all database redundant backups on a instance using filtering</span></span>
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

<span data-ttu-id="ccf1b-113">이 명령은 "managedDatabase"로 시작하는 managedInstance1이라는 인스턴스의 모든 데이터베이스 중복 백업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1b-113">This command gets all database redundant backups on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="ccf1b-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ccf1b-114">PARAMETERS</span></span>

### <span data-ttu-id="ccf1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf1b-115">-DefaultProfile</span></span>
<span data-ttu-id="ccf1b-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccf1b-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ccf1b-117">-InstanceName</span></span>
<span data-ttu-id="ccf1b-118">인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1b-118">The name of the instance.</span></span>

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

### <span data-ttu-id="ccf1b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ccf1b-119">-Name</span></span>
<span data-ttu-id="ccf1b-120">검색할 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1b-120">The name of the instance database to retrieve.</span></span>

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

### <span data-ttu-id="ccf1b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccf1b-121">-ResourceGroupName</span></span>
<span data-ttu-id="ccf1b-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1b-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="ccf1b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf1b-123">CommonParameters</span></span>
<span data-ttu-id="ccf1b-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf1b-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ccf1b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf1b-126">입력</span><span class="sxs-lookup"><span data-stu-id="ccf1b-126">INPUTS</span></span>

### <span data-ttu-id="ccf1b-127">없음</span><span class="sxs-lookup"><span data-stu-id="ccf1b-127">None</span></span>

## <span data-ttu-id="ccf1b-128">출력</span><span class="sxs-lookup"><span data-stu-id="ccf1b-128">OUTPUTS</span></span>

### <span data-ttu-id="ccf1b-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ccf1b-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

## <span data-ttu-id="ccf1b-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ccf1b-130">NOTES</span></span>

## <span data-ttu-id="ccf1b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccf1b-131">RELATED LINKS</span></span>
