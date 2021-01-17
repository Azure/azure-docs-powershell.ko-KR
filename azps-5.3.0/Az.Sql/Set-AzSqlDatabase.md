---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 6d737abb6c58ea8c74085f8390d7a6acbdf54dc8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376454"
---
# <span data-ttu-id="a4f9c-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a4f9c-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="a4f9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4f9c-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f9c-103">데이터베이스에 대한 속성을 설정하거나 기존 데이터베이스를 탄력적 풀로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="a4f9c-104">구문</span><span class="sxs-lookup"><span data-stu-id="a4f9c-104">SYNTAX</span></span>

### <span data-ttu-id="a4f9c-105">업데이트(기본값)</span><span class="sxs-lookup"><span data-stu-id="a4f9c-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4f9c-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="a4f9c-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4f9c-107">이름 이름 다시하기</span><span class="sxs-lookup"><span data-stu-id="a4f9c-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4f9c-108">설명</span><span class="sxs-lookup"><span data-stu-id="a4f9c-108">DESCRIPTION</span></span>
<span data-ttu-id="a4f9c-109">**Set-AzSqlDatabase** cmdlet은 Azure SQL Database의 데이터베이스에 대한 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="a4f9c-110">이 cmdlet은 데이터베이스에 대한 서비스 *계층(버전),* 성능 *수준(RequestedServiceObjectiveName)* 및 저장소 최대 *크기(MaxSizeBytes)를* 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-110">This cmdlet can modify the service tier (*Edition*), performance level (*RequestedServiceObjectiveName*), and storage max size (*MaxSizeBytes*) for the database.</span></span>  <span data-ttu-id="a4f9c-111">또한 *ElasticPoolName* 매개 변수를 지정하여 데이터베이스를 탄력적 풀로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="a4f9c-112">데이터베이스가 이미 탄력적 풀에 있는 경우 *RequestedServiceObjectiveName* 매개 변수를 사용하여 데이터베이스를 탄력적 풀에서 단일 데이터베이스의 성능 수준으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="a4f9c-113">예제</span><span class="sxs-lookup"><span data-stu-id="a4f9c-113">EXAMPLES</span></span>

### <span data-ttu-id="a4f9c-114">예제 1: 표준 S0 데이터베이스로 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="a4f9c-114">Example 1: Update a database to a Standard S0 database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S0"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="a4f9c-115">이 명령은 Database01이라는 데이터베이스를 Server01 서버의 표준 S0 데이터베이스로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="a4f9c-116">예제 2: 탄력적 풀에 데이터베이스 추가</span><span class="sxs-lookup"><span data-stu-id="a4f9c-116">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="a4f9c-117">이 명령은 Server01이라는 서버에 호스트되는 ElasticPool01이라는 탄력적 풀에 Database01이라는 데이터베이스를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="a4f9c-118">예제 3: 데이터베이스의 저장소 최대 크기 수정</span><span class="sxs-lookup"><span data-stu-id="a4f9c-118">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 1099511627776
Status                        : Online
CreationDate                  : 8/24/2017 9:00:37 AM
CurrentServiceObjectiveId     : 789681b8-ca10-4eb0-bdf2-e0b050601b40
CurrentServiceObjectiveName   : S3
RequestedServiceObjectiveId   : 789681b8-ca10-4eb0-bdf2-e0b050601b40
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="a4f9c-119">이 명령은 Database01이라는 데이터베이스를 업데이트하여 최대 크기를 1 TB로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

### <span data-ttu-id="a4f9c-120">예제 4: 기존 일반 용도 데이터베이스를 하이퍼스케일 서비스 계층으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="a4f9c-120">Example 4: Update a existing General Purpose database to Hyperscale service tier</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Hyperscale" -RequestedServiceObjectiveName "HS_Gen5_2"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : 56246136-839f-4171-80af-4c28142463b1
Edition                       : Hyperscale
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : -1
Status                        : Online
CreationDate                  : 12/6/2020 5:34:16 PM
CurrentServiceObjectiveId     : 00000000-0000-0000-0000-000000000000
CurrentServiceObjectiveName   : HS_Gen5_2
RequestedServiceObjectiveName : HS_Gen5_2
RequestedServiceObjectiveId   :
ElasticPoolName               :
EarliestRestoreDate           : 12/6/2020 5:34:16 PM
Tags                          : {}
ResourceId                    : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/Server01/databases/Database01
CreateMode                    :
ReadScale                     : Enabled
ZoneRedundant                 :
Capacity                      : 2
Family                        : Gen5
SkuName                       : HS_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       :
MinimumCapacity               :
ReadReplicaCount              : 1
BackupStorageRedundancy       : Geo
```

<span data-ttu-id="a4f9c-121">이 명령은 Database01이라는 데이터베이스를 일반 용도에서 하이퍼스케일 서비스 계층으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-121">This command updates a database named Database01 from General Purpose to Hyperscale service tier.</span></span>

## <span data-ttu-id="a4f9c-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4f9c-122">PARAMETERS</span></span>

### <span data-ttu-id="a4f9c-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4f9c-123">-AsJob</span></span>
<span data-ttu-id="a4f9c-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a4f9c-124">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-125">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="a4f9c-125">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="a4f9c-126">데이터베이스의 자동 일시 중지 지연(서버리스만 해당), -1을 사용하여 옵트아웃</span><span class="sxs-lookup"><span data-stu-id="a4f9c-126">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-127">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="a4f9c-127">-BackupStorageRedundancy</span></span>
<span data-ttu-id="a4f9c-128">SQL 데이터베이스에 대한 백업을 저장하는 데 사용되는 Backup 저장소 중복성입니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-128">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="a4f9c-129">옵션은 로컬, 영역 및 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-129">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-130">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="a4f9c-130">-ComputeGeneration</span></span>
<span data-ttu-id="a4f9c-131">할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-131">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-132">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="a4f9c-132">-ComputeModel</span></span>
<span data-ttu-id="a4f9c-133">Azure Sql 데이터베이스의 계산된 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-133">Computed model of Azure Sql database.</span></span> <span data-ttu-id="a4f9c-134">서버리스 또는 프로비전</span><span class="sxs-lookup"><span data-stu-id="a4f9c-134">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a4f9c-135">-DatabaseName</span></span>
<span data-ttu-id="a4f9c-136">데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-136">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f9c-137">-DefaultProfile</span></span>
<span data-ttu-id="a4f9c-138">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a4f9c-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4f9c-139">-Edition</span><span class="sxs-lookup"><span data-stu-id="a4f9c-139">-Edition</span></span>
<span data-ttu-id="a4f9c-140">데이터베이스에 대한 에디션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-140">Specifies the edition for the database.</span></span>
<span data-ttu-id="a4f9c-141">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="a4f9c-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a4f9c-142">없음</span><span class="sxs-lookup"><span data-stu-id="a4f9c-142">None</span></span>
- <span data-ttu-id="a4f9c-143">기본</span><span class="sxs-lookup"><span data-stu-id="a4f9c-143">Basic</span></span>
- <span data-ttu-id="a4f9c-144">표준</span><span class="sxs-lookup"><span data-stu-id="a4f9c-144">Standard</span></span>
- <span data-ttu-id="a4f9c-145">프리미엄</span><span class="sxs-lookup"><span data-stu-id="a4f9c-145">Premium</span></span>
- <span data-ttu-id="a4f9c-146">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="a4f9c-146">DataWarehouse</span></span>
- <span data-ttu-id="a4f9c-147">무료</span><span class="sxs-lookup"><span data-stu-id="a4f9c-147">Free</span></span>
- <span data-ttu-id="a4f9c-148">Stretch</span><span class="sxs-lookup"><span data-stu-id="a4f9c-148">Stretch</span></span>
- <span data-ttu-id="a4f9c-149">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="a4f9c-149">GeneralPurpose</span></span>
- <span data-ttu-id="a4f9c-150">하이퍼스케일</span><span class="sxs-lookup"><span data-stu-id="a4f9c-150">Hyperscale</span></span>
- <span data-ttu-id="a4f9c-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="a4f9c-151">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a4f9c-152">-ElasticPoolName</span></span>
<span data-ttu-id="a4f9c-153">데이터베이스를 이동할 탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-153">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-154">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="a4f9c-154">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="a4f9c-155">데이터베이스와 연결된 읽기 전용 보조 복제본의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-155">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="a4f9c-156">하이퍼스케일 버전에만 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-156">For Hyperscale edition only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases: ReadReplicaCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-157">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a4f9c-157">-LicenseType</span></span>
<span data-ttu-id="a4f9c-158">Azure Sql 데이터베이스에 대한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-158">The license type for the Azure Sql database.</span></span> <span data-ttu-id="a4f9c-159">가능한 값은</span><span class="sxs-lookup"><span data-stu-id="a4f9c-159">Possible values are:</span></span>
- <span data-ttu-id="a4f9c-160">BasePrice - 기존 라이선스 소유자에 대한 AHB(Azure 하이브리드 혜택) SQL Server 가격이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-160">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="a4f9c-161">기존 라이선스 소유자에 대해 데이터베이스 SQL Server 할인됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-161">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="a4f9c-162">LicenseIncluded - 기존 라이선스 소유자에 대한 AHB(Azure 하이브리드 혜택) SQL Server 가격은 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-162">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="a4f9c-163">데이터베이스 가격에는 새 라이선스 SQL Server 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-163">Database price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-164">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="a4f9c-164">-MaxSizeBytes</span></span>
<span data-ttu-id="a4f9c-165">Azure SQL 데이터베이스의 최대 크기(byte)입니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-165">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-166">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="a4f9c-166">-MinimumCapacity</span></span>
<span data-ttu-id="a4f9c-167">일시 중지되지 않은 경우 데이터베이스가 항상 할당할 최소 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-167">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="a4f9c-168">서버리스 Azure Sql 데이터베이스에만 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-168">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: Update, VcoreBasedDatabase
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-169">-NewName</span><span class="sxs-lookup"><span data-stu-id="a4f9c-169">-NewName</span></span>
<span data-ttu-id="a4f9c-170">데이터베이스 이름을 변경하는 새 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-170">The new name to rename the database to.</span></span>

```yaml
Type: System.String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-171">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="a4f9c-171">-ReadScale</span></span>
<span data-ttu-id="a4f9c-172">사용하도록 설정하면 애플리케이션 의도가 해당 연결 문자열에서 읽기 전용으로 설정된 연결은 읽기 전용 보조 복제본으로 라우팅될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-172">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="a4f9c-173">이 속성은 프리미엄 및 중요 비즈니스용 데이터베이스에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-173">This property is only settable for Premium and Business Critical databases.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: Update, VcoreBasedDatabase
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-174">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="a4f9c-174">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="a4f9c-175">데이터베이스에 할당할 서비스 목표의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-175">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="a4f9c-176">서비스 목표에 대한 자세한 내용은 Microsoft Developer Network [라이브러리의 Azure](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) SQL Database 서비스 계층 및 성능 수준을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-176">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4f9c-177">-ResourceGroupName</span></span>
<span data-ttu-id="a4f9c-178">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-178">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a4f9c-179">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="a4f9c-179">-SecondaryType</span></span>
<span data-ttu-id="a4f9c-180">보조 데이터베이스인 경우 데이터베이스의 보조 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-180">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="a4f9c-181">유효한 값은 Geo 및 Named입니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-181">Valid values are Geo and Named.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Named, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-182">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a4f9c-182">-ServerName</span></span>
<span data-ttu-id="a4f9c-183">데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-183">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="a4f9c-184">-Tags</span><span class="sxs-lookup"><span data-stu-id="a4f9c-184">-Tags</span></span>
<span data-ttu-id="a4f9c-185">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-185">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a4f9c-186">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="a4f9c-186">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update, VcoreBasedDatabase
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-187">-VCore</span><span class="sxs-lookup"><span data-stu-id="a4f9c-187">-VCore</span></span>
<span data-ttu-id="a4f9c-188">Azure Sql 데이터베이스에 대한 Vcore 번호</span><span class="sxs-lookup"><span data-stu-id="a4f9c-188">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-189">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="a4f9c-189">-ZoneRedundant</span></span>
<span data-ttu-id="a4f9c-190">Azure Sql Database와 연결하기 위해 영역 중복</span><span class="sxs-lookup"><span data-stu-id="a4f9c-190">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4f9c-191">-Confirm</span></span>
<span data-ttu-id="a4f9c-192">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-192">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4f9c-193">-WhatIf</span></span>
<span data-ttu-id="a4f9c-194">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a4f9c-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4f9c-195">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-195">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f9c-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f9c-196">CommonParameters</span></span>
<span data-ttu-id="a4f9c-197">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f9c-198">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a4f9c-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f9c-199">입력</span><span class="sxs-lookup"><span data-stu-id="a4f9c-199">INPUTS</span></span>

### <span data-ttu-id="a4f9c-200">System.String</span><span class="sxs-lookup"><span data-stu-id="a4f9c-200">System.String</span></span>

## <span data-ttu-id="a4f9c-201">출력</span><span class="sxs-lookup"><span data-stu-id="a4f9c-201">OUTPUTS</span></span>

### <span data-ttu-id="a4f9c-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a4f9c-202">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a4f9c-203">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a4f9c-203">NOTES</span></span>

## <span data-ttu-id="a4f9c-204">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4f9c-204">RELATED LINKS</span></span>

[<span data-ttu-id="a4f9c-205">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a4f9c-205">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="a4f9c-206">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a4f9c-206">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="a4f9c-207">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a4f9c-207">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="a4f9c-208">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a4f9c-208">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="a4f9c-209">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a4f9c-209">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="a4f9c-210">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="a4f9c-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
