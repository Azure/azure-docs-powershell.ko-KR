---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 17e6c492828f877ebf53c634a7670e8d60c9ccba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995031"
---
# <span data-ttu-id="5d1c4-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d1c4-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="5d1c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d1c4-102">SYNOPSIS</span></span>
<span data-ttu-id="5d1c4-103">데이터베이스에 대한 속성을 설정하거나 기존 데이터베이스를 탄력적 풀로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="5d1c4-104">구문</span><span class="sxs-lookup"><span data-stu-id="5d1c4-104">SYNTAX</span></span>

### <span data-ttu-id="5d1c4-105">업데이트(기본값)</span><span class="sxs-lookup"><span data-stu-id="5d1c4-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-MaintenanceConfigurationId <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d1c4-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="5d1c4-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-MaintenanceConfigurationId <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d1c4-107">이름 개명</span><span class="sxs-lookup"><span data-stu-id="5d1c4-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d1c4-108">설명</span><span class="sxs-lookup"><span data-stu-id="5d1c4-108">DESCRIPTION</span></span>
<span data-ttu-id="5d1c4-109">**Set-AzSqlDatabase** cmdlet은 Azure SQL 데이터베이스의 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="5d1c4-110">이 cmdlet은 데이터베이스에 대한 서비스 *계층(버전),* 성능 *수준(RequestedServiceObjectiveName)* 및 저장소 최대 *크기(MaxSizeBytes)를* 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-110">This cmdlet can modify the service tier (*Edition*), performance level (*RequestedServiceObjectiveName*), and storage max size (*MaxSizeBytes*) for the database.</span></span>  <span data-ttu-id="5d1c4-111">또한 *ElasticPoolName* 매개 변수를 지정하여 데이터베이스를 탄력적 풀로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="5d1c4-112">데이터베이스가 탄력적 풀에 이미 있는 경우 *RequestedServiceObjectiveName* 매개 변수를 사용하여 탄력적 풀에서 단일 데이터베이스의 성능 수준으로 데이터베이스를 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="5d1c4-113">예제</span><span class="sxs-lookup"><span data-stu-id="5d1c4-113">EXAMPLES</span></span>

### <span data-ttu-id="5d1c4-114">예제 1: 표준 S0 데이터베이스로 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d1c4-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="5d1c4-115">이 명령은 Server01이라는 서버에서 Database01이라는 데이터베이스를 표준 S0 데이터베이스로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="5d1c4-116">예제 2: 탄력적 풀에 데이터베이스 추가</span><span class="sxs-lookup"><span data-stu-id="5d1c4-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="5d1c4-117">이 명령은 Server01이라는 서버에서 호스팅되는 ElasticPool01이라는 탄력적 풀에 Database01이라는 데이터베이스를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="5d1c4-118">예제 3: 데이터베이스의 저장소 최대 크기 수정</span><span class="sxs-lookup"><span data-stu-id="5d1c4-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="5d1c4-119">이 명령은 Database01이라는 데이터베이스를 업데이트하여 최대 크기를 1 TB로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

### <span data-ttu-id="5d1c4-120">예제 4: 기존 일반 목적 데이터베이스를 Hyperscale 서비스 계층으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d1c4-120">Example 4: Update a existing General Purpose database to Hyperscale service tier</span></span>
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

<span data-ttu-id="5d1c4-121">이 명령은 데이터베이스01이라는 데이터베이스를 일반 용도에서 Hyperscale 서비스 계층으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-121">This command updates a database named Database01 from General Purpose to Hyperscale service tier.</span></span>

## <span data-ttu-id="5d1c4-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5d1c4-122">PARAMETERS</span></span>

### <span data-ttu-id="5d1c4-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d1c4-123">-AsJob</span></span>
<span data-ttu-id="5d1c4-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5d1c4-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d1c4-125">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="5d1c4-125">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="5d1c4-126">데이터베이스의 자동 일시 중지 지연(서버리스만 해당), -1에서 옵트아웃</span><span class="sxs-lookup"><span data-stu-id="5d1c4-126">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="5d1c4-127">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="5d1c4-127">-BackupStorageRedundancy</span></span>
<span data-ttu-id="5d1c4-128">백업 데이터베이스에 대한 백업을 저장하는 데 SQL 저장소 중복성입니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-128">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="5d1c4-129">옵션은 로컬, 영역 및 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-129">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="5d1c4-130">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="5d1c4-130">-ComputeGeneration</span></span>
<span data-ttu-id="5d1c4-131">할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-131">The compute generation to assign.</span></span>

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

### <span data-ttu-id="5d1c4-132">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="5d1c4-132">-ComputeModel</span></span>
<span data-ttu-id="5d1c4-133">Azure Sql Database의 계산된 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-133">Computed model of Azure Sql database.</span></span> <span data-ttu-id="5d1c4-134">서버리스 또는 프로비전</span><span class="sxs-lookup"><span data-stu-id="5d1c4-134">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="5d1c4-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5d1c4-135">-DatabaseName</span></span>
<span data-ttu-id="5d1c4-136">데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="5d1c4-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d1c4-137">-DefaultProfile</span></span>
<span data-ttu-id="5d1c4-138">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5d1c4-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d1c4-139">-Edition</span><span class="sxs-lookup"><span data-stu-id="5d1c4-139">-Edition</span></span>
<span data-ttu-id="5d1c4-140">데이터베이스에 대한 에디션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-140">Specifies the edition for the database.</span></span>
<span data-ttu-id="5d1c4-141">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5d1c4-142">없음</span><span class="sxs-lookup"><span data-stu-id="5d1c4-142">None</span></span>
- <span data-ttu-id="5d1c4-143">기본</span><span class="sxs-lookup"><span data-stu-id="5d1c4-143">Basic</span></span>
- <span data-ttu-id="5d1c4-144">표준</span><span class="sxs-lookup"><span data-stu-id="5d1c4-144">Standard</span></span>
- <span data-ttu-id="5d1c4-145">프리미엄</span><span class="sxs-lookup"><span data-stu-id="5d1c4-145">Premium</span></span>
- <span data-ttu-id="5d1c4-146">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="5d1c4-146">DataWarehouse</span></span>
- <span data-ttu-id="5d1c4-147">무료</span><span class="sxs-lookup"><span data-stu-id="5d1c4-147">Free</span></span>
- <span data-ttu-id="5d1c4-148">스트레치</span><span class="sxs-lookup"><span data-stu-id="5d1c4-148">Stretch</span></span>
- <span data-ttu-id="5d1c4-149">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="5d1c4-149">GeneralPurpose</span></span>
- <span data-ttu-id="5d1c4-150">하이퍼스케일</span><span class="sxs-lookup"><span data-stu-id="5d1c4-150">Hyperscale</span></span>
- <span data-ttu-id="5d1c4-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="5d1c4-151">BusinessCritical</span></span>

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

### <span data-ttu-id="5d1c4-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5d1c4-152">-ElasticPoolName</span></span>
<span data-ttu-id="5d1c4-153">데이터베이스를 이동할 탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-153">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="5d1c4-154">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="5d1c4-154">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="5d1c4-155">데이터베이스에 연결된 보조 복제본의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-155">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="5d1c4-156">Hyperscale 버전에만 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-156">For Hyperscale edition only.</span></span>

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

### <span data-ttu-id="5d1c4-157">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5d1c4-157">-LicenseType</span></span>
<span data-ttu-id="5d1c4-158">Azure Sql 데이터베이스에 대한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-158">The license type for the Azure Sql database.</span></span> <span data-ttu-id="5d1c4-159">가능한 값은:</span><span class="sxs-lookup"><span data-stu-id="5d1c4-159">Possible values are:</span></span>
- <span data-ttu-id="5d1c4-160">BasePrice - 기존 라이선스 소유자에 대한 AHB(Azure Hybrid Benefit) 할인된 가격 SQL Server 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-160">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="5d1c4-161">기존 라이선스 소유자에 대해 데이터베이스 SQL Server 할인됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-161">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="5d1c4-162">LicenseIncluded - 기존 라이선스 소유자에 대한 AHB(Azure Hybrid Benefit) SQL Server 가격 책정은 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-162">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="5d1c4-163">데이터베이스 가격에는 새 라이선스 SQL Server 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-163">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="5d1c4-164">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5d1c4-164">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="5d1c4-165">데이터베이스의 유지 관리 SQL ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-165">The Maintenance configuration id for the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d1c4-166">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="5d1c4-166">-MaxSizeBytes</span></span>
<span data-ttu-id="5d1c4-167">Azure 데이터베이스의 최대 크기는 SQL 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-167">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="5d1c4-168">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="5d1c4-168">-MinimumCapacity</span></span>
<span data-ttu-id="5d1c4-169">일시 중지되지 않은 경우 데이터베이스가 항상 할당하는 최소 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-169">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="5d1c4-170">서버리스 Azure Sql 데이터베이스의 경우만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-170">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="5d1c4-171">-NewName</span><span class="sxs-lookup"><span data-stu-id="5d1c4-171">-NewName</span></span>
<span data-ttu-id="5d1c4-172">데이터베이스의 이름을 변경하는 새 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-172">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="5d1c4-173">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="5d1c4-173">-ReadScale</span></span>
<span data-ttu-id="5d1c4-174">사용이 설정된 경우 애플리케이션 의도가 해당 연결 문자열에서 읽기로 설정되어 있는 연결은 읽기 보조 복제본으로 라우팅될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-174">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="5d1c4-175">이 속성은 Premium 및 Business Critical 데이터베이스에만 설정 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-175">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="5d1c4-176">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="5d1c4-176">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="5d1c4-177">데이터베이스에 할당할 서비스 목표의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-177">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="5d1c4-178">서비스 목표에 대한 자세한 내용은 azure SQL [라이브러리의 데이터베이스](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits-single-databases) 서비스 계층 및 성능 수준을 Microsoft Developer Network 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-178">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="5d1c4-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d1c4-179">-ResourceGroupName</span></span>
<span data-ttu-id="5d1c4-180">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-180">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5d1c4-181">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="5d1c4-181">-SecondaryType</span></span>
<span data-ttu-id="5d1c4-182">보조 데이터베이스의 보조 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-182">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="5d1c4-183">유효한 값은 지역 및 명명입니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-183">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="5d1c4-184">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5d1c4-184">-ServerName</span></span>
<span data-ttu-id="5d1c4-185">데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-185">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="5d1c4-186">-Tags</span><span class="sxs-lookup"><span data-stu-id="5d1c4-186">-Tags</span></span>
<span data-ttu-id="5d1c4-187">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-187">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5d1c4-188">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="5d1c4-188">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5d1c4-189">-VCore</span><span class="sxs-lookup"><span data-stu-id="5d1c4-189">-VCore</span></span>
<span data-ttu-id="5d1c4-190">Azure Sql 데이터베이스에 대한 Vcore 번호</span><span class="sxs-lookup"><span data-stu-id="5d1c4-190">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="5d1c4-191">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="5d1c4-191">-ZoneRedundant</span></span>
<span data-ttu-id="5d1c4-192">Azure Sql Database와 연결되는 영역 중복성</span><span class="sxs-lookup"><span data-stu-id="5d1c4-192">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="5d1c4-193">-확인</span><span class="sxs-lookup"><span data-stu-id="5d1c4-193">-Confirm</span></span>
<span data-ttu-id="5d1c4-194">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-194">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d1c4-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d1c4-195">-WhatIf</span></span>
<span data-ttu-id="5d1c4-196">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d1c4-197">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-197">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d1c4-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d1c4-198">CommonParameters</span></span>
<span data-ttu-id="5d1c4-199">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d1c4-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d1c4-200">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d1c4-200">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d1c4-201">입력</span><span class="sxs-lookup"><span data-stu-id="5d1c4-201">INPUTS</span></span>

### <span data-ttu-id="5d1c4-202">System.String</span><span class="sxs-lookup"><span data-stu-id="5d1c4-202">System.String</span></span>

## <span data-ttu-id="5d1c4-203">출력</span><span class="sxs-lookup"><span data-stu-id="5d1c4-203">OUTPUTS</span></span>

### <span data-ttu-id="5d1c4-204">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5d1c4-204">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5d1c4-205">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5d1c4-205">NOTES</span></span>

## <span data-ttu-id="5d1c4-206">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d1c4-206">RELATED LINKS</span></span>

[<span data-ttu-id="5d1c4-207">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d1c4-207">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="5d1c4-208">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d1c4-208">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="5d1c4-209">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d1c4-209">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="5d1c4-210">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d1c4-210">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="5d1c4-211">suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d1c4-211">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="5d1c4-212">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="5d1c4-212">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
