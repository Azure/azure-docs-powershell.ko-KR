---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: fe6779c64a3cbc5a484dd4a3ee3662bcdaf59059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530049"
---
# <span data-ttu-id="a06af-101">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a06af-101">Get-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="a06af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a06af-102">SYNOPSIS</span></span>
<span data-ttu-id="a06af-103">Azure SQL 관리 인스턴스 데이터베이스에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a06af-103">Returns information about Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a06af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a06af-104">SYNTAX</span></span>

### <span data-ttu-id="a06af-105">Getinstancedatabase찡그린 Minputparameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="a06af-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a06af-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="a06af-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a06af-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="a06af-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a06af-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a06af-108">DESCRIPTION</span></span>
<span data-ttu-id="a06af-109">**AzureRmSqlInstanceDatabase** Cmdlet은 Azure Sql Database 관리 인스턴스에서 하나 이상의 azure sql 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a06af-109">The **Get-AzureRmSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="a06af-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a06af-110">EXAMPLES</span></span>

### <span data-ttu-id="a06af-111">예제 1: 인스턴스의 모든 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="a06af-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
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

<span data-ttu-id="a06af-112">이 명령은 managedInstance1 이라는 인스턴스의 모든 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a06af-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="a06af-113">예제 2: 관리 되는 인스턴스에서 이름으로 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="a06af-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="a06af-114">이 명령은 managedInstance1 라는 인스턴스에서 managedDatabase1 이라는 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a06af-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

## <span data-ttu-id="a06af-115">변수</span><span class="sxs-lookup"><span data-stu-id="a06af-115">PARAMETERS</span></span>

### <span data-ttu-id="a06af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a06af-116">-DefaultProfile</span></span>
<span data-ttu-id="a06af-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a06af-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a06af-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a06af-118">-InstanceName</span></span>
<span data-ttu-id="a06af-119">인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a06af-119">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06af-120">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="a06af-120">-InstanceObject</span></span>
<span data-ttu-id="a06af-121">인스턴스 데이터베이스를 가져오는 데 사용할 인스턴스 개체</span><span class="sxs-lookup"><span data-stu-id="a06af-121">The instance object to use for getting instance database</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a06af-122">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="a06af-122">-InstanceResourceId</span></span>
<span data-ttu-id="a06af-123">가져올 인스턴스 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a06af-123">The resource id of instance object to get</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a06af-124">-이름</span><span class="sxs-lookup"><span data-stu-id="a06af-124">-Name</span></span>
<span data-ttu-id="a06af-125">검색할 Azure SQL 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a06af-125">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06af-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a06af-126">-ResourceGroupName</span></span>
<span data-ttu-id="a06af-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a06af-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a06af-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a06af-128">CommonParameters</span></span>
<span data-ttu-id="a06af-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a06af-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a06af-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a06af-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a06af-131">입력</span><span class="sxs-lookup"><span data-stu-id="a06af-131">INPUTS</span></span>

### <span data-ttu-id="a06af-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a06af-132">System.String</span></span>
<span data-ttu-id="a06af-133">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="a06af-133">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="a06af-134">출력</span><span class="sxs-lookup"><span data-stu-id="a06af-134">OUTPUTS</span></span>

### <span data-ttu-id="a06af-135">AzureSqlManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="a06af-135">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="a06af-136">상속자</span><span class="sxs-lookup"><span data-stu-id="a06af-136">NOTES</span></span>

## <span data-ttu-id="a06af-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a06af-137">RELATED LINKS</span></span>
