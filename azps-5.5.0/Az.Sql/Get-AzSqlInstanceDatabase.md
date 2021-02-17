---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 8fb9b14dca32940911f0ef3bdae80a187c64b374
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188092"
---
# <span data-ttu-id="d4041-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="d4041-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="d4041-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4041-102">SYNOPSIS</span></span>
<span data-ttu-id="d4041-103">Azure SQL Managed Instance 데이터베이스에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d4041-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="d4041-104">구문</span><span class="sxs-lookup"><span data-stu-id="d4041-104">SYNTAX</span></span>

### <span data-ttu-id="d4041-105">GetInstanceDatabaseFromInputParameters(기본값)</span><span class="sxs-lookup"><span data-stu-id="d4041-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4041-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="d4041-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4041-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="d4041-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4041-108">설명</span><span class="sxs-lookup"><span data-stu-id="d4041-108">DESCRIPTION</span></span>
<span data-ttu-id="d4041-109">**Get-AzSqlInstanceDatabase** cmdlet은 Azure SQL Database Managed Instance에서 하나 이상의 Azure SQL 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d4041-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="d4041-110">예제</span><span class="sxs-lookup"><span data-stu-id="d4041-110">EXAMPLES</span></span>

### <span data-ttu-id="d4041-111">예제 1: 인스턴스의 모든 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d4041-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="d4041-112">이 명령은 managedInstance1이라는 인스턴스의 모든 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d4041-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="d4041-113">예제 2: Managed Instance에서 이름으로 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d4041-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="d4041-114">이 명령은 managedInstance1이라는 인스턴스에서 managedDatabase1이라는 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d4041-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="d4041-115">예제 3: 필터링을 사용하여 인스턴스의 모든 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d4041-115">Example 3: Get all databases on a instance using filtering</span></span>
```
PS C:\> Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="d4041-116">이 명령은 "managedDatabase"로 시작하는 managedInstance1 인스턴스의 모든 데이터베이스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d4041-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="d4041-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4041-117">PARAMETERS</span></span>

### <span data-ttu-id="d4041-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4041-118">-DefaultProfile</span></span>
<span data-ttu-id="d4041-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4041-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4041-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d4041-120">-InstanceName</span></span>
<span data-ttu-id="d4041-121">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4041-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4041-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="d4041-122">-InstanceObject</span></span>
<span data-ttu-id="d4041-123">인스턴스 데이터베이스를 생성하는 데 사용할 인스턴스 개체</span><span class="sxs-lookup"><span data-stu-id="d4041-123">The instance object to use for getting instance database</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4041-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="d4041-124">-InstanceResourceId</span></span>
<span data-ttu-id="d4041-125">얻을 인스턴스 개체의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d4041-125">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4041-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d4041-126">-Name</span></span>
<span data-ttu-id="d4041-127">검색할 Azure SQL Instance 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4041-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4041-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4041-128">-ResourceGroupName</span></span>
<span data-ttu-id="d4041-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4041-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4041-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4041-130">CommonParameters</span></span>
<span data-ttu-id="d4041-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d4041-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4041-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d4041-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4041-133">입력</span><span class="sxs-lookup"><span data-stu-id="d4041-133">INPUTS</span></span>

### <span data-ttu-id="d4041-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d4041-134">System.String</span></span>

### <span data-ttu-id="d4041-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d4041-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="d4041-136">출력</span><span class="sxs-lookup"><span data-stu-id="d4041-136">OUTPUTS</span></span>

### <span data-ttu-id="d4041-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d4041-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="d4041-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d4041-138">NOTES</span></span>

## <span data-ttu-id="d4041-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4041-139">RELATED LINKS</span></span>
