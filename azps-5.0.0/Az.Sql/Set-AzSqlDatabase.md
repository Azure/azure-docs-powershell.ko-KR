---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: f236c00f50d9ec74a98def114d08ab851e5a89f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216965"
---
# <span data-ttu-id="3d780-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d780-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="3d780-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d780-102">SYNOPSIS</span></span>
<span data-ttu-id="3d780-103">데이터베이스의 속성을 설정 하거나 기존 데이터베이스를 탄력적인 풀로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="3d780-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d780-104">SYNTAX</span></span>

### <span data-ttu-id="3d780-105">업데이트 (기본값)</span><span class="sxs-lookup"><span data-stu-id="3d780-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d780-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="3d780-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d780-107">바꿉니다</span><span class="sxs-lookup"><span data-stu-id="3d780-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d780-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3d780-108">DESCRIPTION</span></span>
<span data-ttu-id="3d780-109">**AzSqlDatabase** Cmdlet은 Azure SQL 데이터베이스의 데이터베이스에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="3d780-110">이 cmdlet은 데이터베이스에 대 한 *버전* (서비스 계층), *RequestedServiceObjectiveName* (성능 수준) 및 저장소 최대 크기 ( *maxsizebytes* )를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="3d780-111">또한 *ElasticPoolName* 매개 변수를 지정 하 여 데이터베이스를 탄력적인 풀로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="3d780-112">탄력적 풀에 데이터베이스가 이미 있는 경우 *RequestedServiceObjectiveName* 매개 변수를 사용 하 여 데이터베이스를 탄력적 풀에서 이동 하 고 단일 데이터베이스의 성능 수준으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="3d780-113">예제의</span><span class="sxs-lookup"><span data-stu-id="3d780-113">EXAMPLES</span></span>

### <span data-ttu-id="3d780-114">예제 1: 표준 S0 데이터베이스로 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="3d780-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="3d780-115">이 명령은 Database01 이라는 데이터베이스를 Server01 라는 서버의 표준 S0 데이터베이스로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="3d780-116">예제 2: 탄력적 풀에 데이터베이스 추가</span><span class="sxs-lookup"><span data-stu-id="3d780-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="3d780-117">이 명령은 Database01 이라는 데이터베이스를 Server01 이라는 서버에서 호스팅된 ElasticPool01 이라는 탄력적 풀에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="3d780-118">예제 3: 데이터베이스의 저장소 최대 크기 수정</span><span class="sxs-lookup"><span data-stu-id="3d780-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="3d780-119">이 명령은 Database01 이라는 데이터베이스를 업데이트 하 여 최대 크기를 1TB로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="3d780-120">변수</span><span class="sxs-lookup"><span data-stu-id="3d780-120">PARAMETERS</span></span>

### <span data-ttu-id="3d780-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d780-121">-AsJob</span></span>
<span data-ttu-id="3d780-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3d780-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d780-123">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="3d780-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="3d780-124">데이터베이스에 대 한 자동 일시 정지 지연 시간 (서버를 사용할 수 없음),-1에서 옵트아웃</span><span class="sxs-lookup"><span data-stu-id="3d780-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="3d780-125">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="3d780-125">-BackupStorageRedundancy</span></span>
<span data-ttu-id="3d780-126">SQL 데이터베이스에 대 한 백업을 저장 하는 데 사용 되는 백업 저장소 중복성입니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-126">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="3d780-127">지역, Zone, Geo 등의 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-127">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="3d780-128">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="3d780-128">-ComputeGeneration</span></span>
<span data-ttu-id="3d780-129">할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-129">The compute generation to assign.</span></span>

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

### <span data-ttu-id="3d780-130">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="3d780-130">-ComputeModel</span></span>
<span data-ttu-id="3d780-131">Azure Sql 데이터베이스의 계산 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-131">Computed model of Azure Sql database.</span></span> <span data-ttu-id="3d780-132">서버에서 또는 프로 비전 됨</span><span class="sxs-lookup"><span data-stu-id="3d780-132">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="3d780-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3d780-133">-DatabaseName</span></span>
<span data-ttu-id="3d780-134">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-134">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="3d780-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d780-135">-DefaultProfile</span></span>
<span data-ttu-id="3d780-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3d780-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d780-137">-에디션</span><span class="sxs-lookup"><span data-stu-id="3d780-137">-Edition</span></span>
<span data-ttu-id="3d780-138">데이터베이스의 에디션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-138">Specifies the edition for the database.</span></span>
<span data-ttu-id="3d780-139">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3d780-140">않아야</span><span class="sxs-lookup"><span data-stu-id="3d780-140">None</span></span>
- <span data-ttu-id="3d780-141">기본적</span><span class="sxs-lookup"><span data-stu-id="3d780-141">Basic</span></span>
- <span data-ttu-id="3d780-142">표준이</span><span class="sxs-lookup"><span data-stu-id="3d780-142">Standard</span></span>
- <span data-ttu-id="3d780-143">Premium</span><span class="sxs-lookup"><span data-stu-id="3d780-143">Premium</span></span>
- <span data-ttu-id="3d780-144">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="3d780-144">DataWarehouse</span></span>
- <span data-ttu-id="3d780-145">비우거나</span><span class="sxs-lookup"><span data-stu-id="3d780-145">Free</span></span>
- <span data-ttu-id="3d780-146">늘이고</span><span class="sxs-lookup"><span data-stu-id="3d780-146">Stretch</span></span>
- <span data-ttu-id="3d780-147">일반 목적</span><span class="sxs-lookup"><span data-stu-id="3d780-147">GeneralPurpose</span></span>
- <span data-ttu-id="3d780-148">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="3d780-148">BusinessCritical</span></span>

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

### <span data-ttu-id="3d780-149">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3d780-149">-ElasticPoolName</span></span>
<span data-ttu-id="3d780-150">데이터베이스를 이동할 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-150">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="3d780-151">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3d780-151">-LicenseType</span></span>
<span data-ttu-id="3d780-152">Azure Sql 데이터베이스에 대 한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-152">The license type for the Azure Sql database.</span></span> <span data-ttu-id="3d780-153">사용할 수 있는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-153">Possible values are:</span></span>
- <span data-ttu-id="3d780-154">BasePrice-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-154">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="3d780-155">기존 SQL Server 라이선스 소유자에 게 데이터베이스 가격이 할인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-155">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="3d780-156">LicenseIncluded-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-156">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="3d780-157">데이터베이스 가격에는 새로운 SQL Server 라이선스 비용이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-157">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="3d780-158">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="3d780-158">-MaxSizeBytes</span></span>
<span data-ttu-id="3d780-159">Azure SQL 데이터베이스의 최대 크기 (바이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-159">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="3d780-160">-가을 용량</span><span class="sxs-lookup"><span data-stu-id="3d780-160">-MinimumCapacity</span></span>
<span data-ttu-id="3d780-161">데이터베이스가 일시 중지 되지 않은 경우 항상 할당 되는 최소 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-161">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="3d780-162">서버를 사용할 경우 Azure Sql 데이터베이스에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-162">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="3d780-163">-NewName</span><span class="sxs-lookup"><span data-stu-id="3d780-163">-NewName</span></span>
<span data-ttu-id="3d780-164">데이터베이스 이름을 바꿀 새 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-164">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="3d780-165">-ReadReplicaCount</span><span class="sxs-lookup"><span data-stu-id="3d780-165">-ReadReplicaCount</span></span>
<span data-ttu-id="3d780-166">데이터베이스와 연결 된 읽기 전용 보조 복제본의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-166">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="3d780-167">Hyperscale edition에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-167">For Hyperscale edition only.</span></span>

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

### <span data-ttu-id="3d780-168">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="3d780-168">-ReadScale</span></span>
<span data-ttu-id="3d780-169">이 기능을 사용 하도록 설정 하면 응용 프로그램 의도가 연결 문자열의 readonly로 설정 된 연결이 읽기 전용 보조 복제본으로 라우팅될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-169">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="3d780-170">이 속성은 Premium 및 비즈니스 중요 데이터베이스에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-170">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="3d780-171">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="3d780-171">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="3d780-172">데이터베이스에 할당할 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-172">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="3d780-173">서비스 목표에 대 한 자세한 내용은 Microsoft 개발자 네트워크 라이브러리의 [AZURE SQL 데이터베이스 서비스 계층 및 성능 수준을](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d780-173">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="3d780-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d780-174">-ResourceGroupName</span></span>
<span data-ttu-id="3d780-175">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-175">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="3d780-176">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3d780-176">-ServerName</span></span>
<span data-ttu-id="3d780-177">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-177">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="3d780-178">태그</span><span class="sxs-lookup"><span data-stu-id="3d780-178">-Tags</span></span>
<span data-ttu-id="3d780-179">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3d780-180">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3d780-180">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3d780-181">-VCore</span><span class="sxs-lookup"><span data-stu-id="3d780-181">-VCore</span></span>
<span data-ttu-id="3d780-182">Azure Sql 데이터베이스의 Vcore 번호</span><span class="sxs-lookup"><span data-stu-id="3d780-182">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="3d780-183">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="3d780-183">-ZoneRedundant</span></span>
<span data-ttu-id="3d780-184">Azure Sql Database와 연결 되는 영역 중복성</span><span class="sxs-lookup"><span data-stu-id="3d780-184">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="3d780-185">-확인</span><span class="sxs-lookup"><span data-stu-id="3d780-185">-Confirm</span></span>
<span data-ttu-id="3d780-186">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d780-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d780-187">-WhatIf</span></span>
<span data-ttu-id="3d780-188">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d780-189">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d780-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d780-190">CommonParameters</span></span>
<span data-ttu-id="3d780-191">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d780-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d780-192">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3d780-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d780-193">입력</span><span class="sxs-lookup"><span data-stu-id="3d780-193">INPUTS</span></span>

### <span data-ttu-id="3d780-194">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3d780-194">System.String</span></span>

## <span data-ttu-id="3d780-195">출력</span><span class="sxs-lookup"><span data-stu-id="3d780-195">OUTPUTS</span></span>

### <span data-ttu-id="3d780-196">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="3d780-196">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="3d780-197">상속자</span><span class="sxs-lookup"><span data-stu-id="3d780-197">NOTES</span></span>

## <span data-ttu-id="3d780-198">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d780-198">RELATED LINKS</span></span>

[<span data-ttu-id="3d780-199">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d780-199">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="3d780-200">새로운 AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d780-200">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="3d780-201">제거-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d780-201">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="3d780-202">이력서-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d780-202">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="3d780-203">일시 중단-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3d780-203">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="3d780-204">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="3d780-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
