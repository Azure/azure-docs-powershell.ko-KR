---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 180cd3c8d9301ab287bc4a37c13f7b07276f7794
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034333"
---
# <span data-ttu-id="2bd5e-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2bd5e-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="2bd5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bd5e-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd5e-103">데이터베이스의 속성을 설정 하거나 기존 데이터베이스를 탄력적인 풀로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="2bd5e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2bd5e-104">SYNTAX</span></span>

### <span data-ttu-id="2bd5e-105">업데이트 (기본값)</span><span class="sxs-lookup"><span data-stu-id="2bd5e-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bd5e-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="2bd5e-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bd5e-107">바꿉니다</span><span class="sxs-lookup"><span data-stu-id="2bd5e-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2bd5e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2bd5e-108">DESCRIPTION</span></span>
<span data-ttu-id="2bd5e-109">**AzSqlDatabase** Cmdlet은 Azure SQL 데이터베이스의 데이터베이스에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="2bd5e-110">이 cmdlet은 데이터베이스에 대 한 *버전* (서비스 계층), *RequestedServiceObjectiveName* (성능 수준) 및 저장소 최대 크기 ( *maxsizebytes* )를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="2bd5e-111">또한 *ElasticPoolName* 매개 변수를 지정 하 여 데이터베이스를 탄력적인 풀로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="2bd5e-112">탄력적 풀에 데이터베이스가 이미 있는 경우 *RequestedServiceObjectiveName* 매개 변수를 사용 하 여 데이터베이스를 탄력적 풀에서 이동 하 고 단일 데이터베이스의 성능 수준으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="2bd5e-113">예제의</span><span class="sxs-lookup"><span data-stu-id="2bd5e-113">EXAMPLES</span></span>

### <span data-ttu-id="2bd5e-114">예제 1: 표준 S0 데이터베이스로 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="2bd5e-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="2bd5e-115">이 명령은 Database01 이라는 데이터베이스를 Server01 라는 서버의 표준 S0 데이터베이스로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="2bd5e-116">예제 2: 탄력적 풀에 데이터베이스 추가</span><span class="sxs-lookup"><span data-stu-id="2bd5e-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="2bd5e-117">이 명령은 Database01 이라는 데이터베이스를 Server01 이라는 서버에서 호스팅된 ElasticPool01 이라는 탄력적 풀에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="2bd5e-118">예제 3: 데이터베이스의 저장소 최대 크기 수정</span><span class="sxs-lookup"><span data-stu-id="2bd5e-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="2bd5e-119">이 명령은 Database01 이라는 데이터베이스를 업데이트 하 여 최대 크기를 1TB로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="2bd5e-120">변수</span><span class="sxs-lookup"><span data-stu-id="2bd5e-120">PARAMETERS</span></span>

### <span data-ttu-id="2bd5e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bd5e-121">-AsJob</span></span>
<span data-ttu-id="2bd5e-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2bd5e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2bd5e-123">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="2bd5e-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="2bd5e-124">데이터베이스에 대 한 자동 일시 정지 지연 시간 (서버를 사용할 수 없음),-1에서 옵트아웃</span><span class="sxs-lookup"><span data-stu-id="2bd5e-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="2bd5e-125">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="2bd5e-125">-ComputeGeneration</span></span>
<span data-ttu-id="2bd5e-126">할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-126">The compute generation to assign.</span></span>

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

### <span data-ttu-id="2bd5e-127">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="2bd5e-127">-ComputeModel</span></span>
<span data-ttu-id="2bd5e-128">Azure Sql 데이터베이스의 계산 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-128">Computed model of Azure Sql database.</span></span> <span data-ttu-id="2bd5e-129">서버에서 또는 프로 비전 됨</span><span class="sxs-lookup"><span data-stu-id="2bd5e-129">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="2bd5e-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2bd5e-130">-DatabaseName</span></span>
<span data-ttu-id="2bd5e-131">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-131">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="2bd5e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd5e-132">-DefaultProfile</span></span>
<span data-ttu-id="2bd5e-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2bd5e-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2bd5e-134">-에디션</span><span class="sxs-lookup"><span data-stu-id="2bd5e-134">-Edition</span></span>
<span data-ttu-id="2bd5e-135">데이터베이스의 에디션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-135">Specifies the edition for the database.</span></span>
<span data-ttu-id="2bd5e-136">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2bd5e-137">않아야</span><span class="sxs-lookup"><span data-stu-id="2bd5e-137">None</span></span>
- <span data-ttu-id="2bd5e-138">기본적</span><span class="sxs-lookup"><span data-stu-id="2bd5e-138">Basic</span></span>
- <span data-ttu-id="2bd5e-139">표준이</span><span class="sxs-lookup"><span data-stu-id="2bd5e-139">Standard</span></span>
- <span data-ttu-id="2bd5e-140">Premium</span><span class="sxs-lookup"><span data-stu-id="2bd5e-140">Premium</span></span>
- <span data-ttu-id="2bd5e-141">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="2bd5e-141">DataWarehouse</span></span>
- <span data-ttu-id="2bd5e-142">비우거나</span><span class="sxs-lookup"><span data-stu-id="2bd5e-142">Free</span></span>
- <span data-ttu-id="2bd5e-143">늘이고</span><span class="sxs-lookup"><span data-stu-id="2bd5e-143">Stretch</span></span>
- <span data-ttu-id="2bd5e-144">일반 목적</span><span class="sxs-lookup"><span data-stu-id="2bd5e-144">GeneralPurpose</span></span>
- <span data-ttu-id="2bd5e-145">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="2bd5e-145">BusinessCritical</span></span>

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

### <span data-ttu-id="2bd5e-146">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2bd5e-146">-ElasticPoolName</span></span>
<span data-ttu-id="2bd5e-147">데이터베이스를 이동할 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-147">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="2bd5e-148">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2bd5e-148">-LicenseType</span></span>
<span data-ttu-id="2bd5e-149">Azure Sql 데이터베이스에 대 한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-149">The license type for the Azure Sql database.</span></span> <span data-ttu-id="2bd5e-150">사용할 수 있는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-150">Possible values are:</span></span>
- <span data-ttu-id="2bd5e-151">BasePrice-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-151">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="2bd5e-152">기존 SQL Server 라이선스 소유자에 게 데이터베이스 가격이 할인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-152">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="2bd5e-153">LicenseIncluded-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-153">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="2bd5e-154">데이터베이스 가격에는 새로운 SQL Server 라이선스 비용이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-154">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="2bd5e-155">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="2bd5e-155">-MaxSizeBytes</span></span>
<span data-ttu-id="2bd5e-156">Azure SQL 데이터베이스의 최대 크기 (바이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-156">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="2bd5e-157">-가을 용량</span><span class="sxs-lookup"><span data-stu-id="2bd5e-157">-MinimumCapacity</span></span>
<span data-ttu-id="2bd5e-158">데이터베이스가 일시 중지 되지 않은 경우 항상 할당 되는 최소 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-158">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="2bd5e-159">서버를 사용할 경우 Azure Sql 데이터베이스에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-159">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="2bd5e-160">-NewName</span><span class="sxs-lookup"><span data-stu-id="2bd5e-160">-NewName</span></span>
<span data-ttu-id="2bd5e-161">데이터베이스 이름을 바꿀 새 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-161">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="2bd5e-162">-ReadReplicaCount</span><span class="sxs-lookup"><span data-stu-id="2bd5e-162">-ReadReplicaCount</span></span>
<span data-ttu-id="2bd5e-163">데이터베이스와 연결 된 읽기 전용 보조 복제본의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-163">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="2bd5e-164">Hyperscale edition에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-164">For Hyperscale edition only.</span></span>

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

### <span data-ttu-id="2bd5e-165">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="2bd5e-165">-ReadScale</span></span>
<span data-ttu-id="2bd5e-166">이 기능을 사용 하도록 설정 하면 응용 프로그램 의도가 연결 문자열의 readonly로 설정 된 연결이 읽기 전용 보조 복제본으로 라우팅될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-166">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="2bd5e-167">이 속성은 Premium 및 비즈니스 중요 데이터베이스에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-167">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="2bd5e-168">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="2bd5e-168">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="2bd5e-169">데이터베이스에 할당할 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-169">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="2bd5e-170">서비스 목표에 대 한 자세한 내용은 Microsoft 개발자 네트워크 라이브러리의 [AZURE SQL 데이터베이스 서비스 계층 및 성능 수준을](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-170">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="2bd5e-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bd5e-171">-ResourceGroupName</span></span>
<span data-ttu-id="2bd5e-172">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-172">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="2bd5e-173">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2bd5e-173">-ServerName</span></span>
<span data-ttu-id="2bd5e-174">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-174">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="2bd5e-175">태그</span><span class="sxs-lookup"><span data-stu-id="2bd5e-175">-Tags</span></span>
<span data-ttu-id="2bd5e-176">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-176">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2bd5e-177">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2bd5e-177">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2bd5e-178">-VCore</span><span class="sxs-lookup"><span data-stu-id="2bd5e-178">-VCore</span></span>
<span data-ttu-id="2bd5e-179">Azure Sql 데이터베이스의 Vcore 번호</span><span class="sxs-lookup"><span data-stu-id="2bd5e-179">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="2bd5e-180">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="2bd5e-180">-ZoneRedundant</span></span>
<span data-ttu-id="2bd5e-181">Azure Sql Database와 연결 되는 영역 중복성</span><span class="sxs-lookup"><span data-stu-id="2bd5e-181">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="2bd5e-182">-확인</span><span class="sxs-lookup"><span data-stu-id="2bd5e-182">-Confirm</span></span>
<span data-ttu-id="2bd5e-183">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bd5e-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bd5e-184">-WhatIf</span></span>
<span data-ttu-id="2bd5e-185">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bd5e-186">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bd5e-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd5e-187">CommonParameters</span></span>
<span data-ttu-id="2bd5e-188">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd5e-189">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd5e-190">입력</span><span class="sxs-lookup"><span data-stu-id="2bd5e-190">INPUTS</span></span>

### <span data-ttu-id="2bd5e-191">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2bd5e-191">System.String</span></span>

## <span data-ttu-id="2bd5e-192">출력</span><span class="sxs-lookup"><span data-stu-id="2bd5e-192">OUTPUTS</span></span>

### <span data-ttu-id="2bd5e-193">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-193">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="2bd5e-194">상속자</span><span class="sxs-lookup"><span data-stu-id="2bd5e-194">NOTES</span></span>

## <span data-ttu-id="2bd5e-195">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2bd5e-195">RELATED LINKS</span></span>

[<span data-ttu-id="2bd5e-196">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2bd5e-196">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="2bd5e-197">새로운 AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2bd5e-197">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="2bd5e-198">제거-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2bd5e-198">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="2bd5e-199">이력서-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2bd5e-199">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="2bd5e-200">일시 중단-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2bd5e-200">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="2bd5e-201">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="2bd5e-201">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
