---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 8fb9b14dca32940911f0ef3bdae80a187c64b374
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304388"
---
# <span data-ttu-id="0750f-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0750f-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="0750f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0750f-102">SYNOPSIS</span></span>
<span data-ttu-id="0750f-103">Azure SQL 관리 인스턴스 데이터베이스에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0750f-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="0750f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0750f-104">SYNTAX</span></span>

### <span data-ttu-id="0750f-105">Getinstancedatabase찡그린 Minputparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="0750f-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0750f-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="0750f-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0750f-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="0750f-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0750f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0750f-108">DESCRIPTION</span></span>
<span data-ttu-id="0750f-109">**AzSqlInstanceDatabase** Cmdlet은 Azure Sql Database 관리 인스턴스에서 하나 이상의 azure sql 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0750f-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="0750f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0750f-110">EXAMPLES</span></span>

### <span data-ttu-id="0750f-111">예제 1: 인스턴스의 모든 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="0750f-111">Example 1: Get all databases on a instance</span></span>
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

<span data-ttu-id="0750f-112">이 명령은 managedInstance1 이라는 인스턴스의 모든 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0750f-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="0750f-113">예제 2: 관리 되는 인스턴스에서 이름으로 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="0750f-113">Example 2: Get a database by name on a Managed instance</span></span>
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

<span data-ttu-id="0750f-114">이 명령은 managedInstance1 라는 인스턴스에서 managedDatabase1 이라는 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0750f-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="0750f-115">예제 3: 필터링을 사용 하 여 인스턴스의 모든 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="0750f-115">Example 3: Get all databases on a instance using filtering</span></span>
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

<span data-ttu-id="0750f-116">이 명령은 "managedDatabase"로 시작 하는 managedInstance1 이라는 인스턴스의 모든 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0750f-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="0750f-117">변수</span><span class="sxs-lookup"><span data-stu-id="0750f-117">PARAMETERS</span></span>

### <span data-ttu-id="0750f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0750f-118">-DefaultProfile</span></span>
<span data-ttu-id="0750f-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0750f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0750f-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="0750f-120">-InstanceName</span></span>
<span data-ttu-id="0750f-121">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0750f-121">The instance name.</span></span>

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

### <span data-ttu-id="0750f-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="0750f-122">-InstanceObject</span></span>
<span data-ttu-id="0750f-123">인스턴스 데이터베이스를 가져오는 데 사용할 인스턴스 개체</span><span class="sxs-lookup"><span data-stu-id="0750f-123">The instance object to use for getting instance database</span></span>

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

### <span data-ttu-id="0750f-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="0750f-124">-InstanceResourceId</span></span>
<span data-ttu-id="0750f-125">가져올 인스턴스 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0750f-125">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="0750f-126">-이름</span><span class="sxs-lookup"><span data-stu-id="0750f-126">-Name</span></span>
<span data-ttu-id="0750f-127">검색할 Azure SQL 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0750f-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

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

### <span data-ttu-id="0750f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0750f-128">-ResourceGroupName</span></span>
<span data-ttu-id="0750f-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0750f-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="0750f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0750f-130">CommonParameters</span></span>
<span data-ttu-id="0750f-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0750f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0750f-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0750f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0750f-133">입력</span><span class="sxs-lookup"><span data-stu-id="0750f-133">INPUTS</span></span>

### <span data-ttu-id="0750f-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0750f-134">System.String</span></span>

### <span data-ttu-id="0750f-135">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="0750f-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="0750f-136">출력</span><span class="sxs-lookup"><span data-stu-id="0750f-136">OUTPUTS</span></span>

### <span data-ttu-id="0750f-137">AzureSqlManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="0750f-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="0750f-138">상속자</span><span class="sxs-lookup"><span data-stu-id="0750f-138">NOTES</span></span>

## <span data-ttu-id="0750f-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0750f-139">RELATED LINKS</span></span>
