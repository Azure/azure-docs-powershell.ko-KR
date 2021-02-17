---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: 57af759caa940686d69118157973eb01c9a6928e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196113"
---
# <span data-ttu-id="e6e7b-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6e7b-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="e6e7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e7b-103">데이터베이스 또는 탄력적 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="e6e7b-104">구문</span><span class="sxs-lookup"><span data-stu-id="e6e7b-104">SYNTAX</span></span>

### <span data-ttu-id="e6e7b-105">DtuBasedDatabase(기본값)</span><span class="sxs-lookup"><span data-stu-id="e6e7b-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-Force] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6e7b-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="e6e7b-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] [-Force] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-HighAvailabilityReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-SecondaryType <String>] [-MaintenanceConfigurationId <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6e7b-107">설명</span><span class="sxs-lookup"><span data-stu-id="e6e7b-107">DESCRIPTION</span></span>
<span data-ttu-id="e6e7b-108">**New-AzSqlDatabase** cmdlet은 Azure SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="e6e7b-109">*ElasticPoolName* 매개 변수를 기존 탄력적 풀로 설정하여 탄력적 데이터베이스를 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="e6e7b-110">예제</span><span class="sxs-lookup"><span data-stu-id="e6e7b-110">EXAMPLES</span></span>

### <span data-ttu-id="e6e7b-111">예제 1: 지정된 서버에 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="e6e7b-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="e6e7b-112">이 명령은 server Server01에 Database01이라는 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="e6e7b-113">예제 2: 지정된 서버에 탄력적 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="e6e7b-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="e6e7b-114">이 명령은 Server01의 ElasticPool01 탄력적 풀에 Database02라는 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="e6e7b-115">예제 3: 지정된 서버에 Vcore 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="e6e7b-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database03
Location                      : Central US
DatabaseId                    : 34d9d561-42a7-484e-bf05-62ddef8000ab
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveName   : GP_Gen4_2
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   : LicenseIncluded
Tags                          :
```

<span data-ttu-id="e6e7b-116">이 명령은 Server Server01에 Database03이라는 Vcore 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="e6e7b-117">예제 4: 지정된 서버에서 서버리스 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="e6e7b-117">Example 4: Create an Serverless database on the specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database04" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen5" -ComputeModel Serverless
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database04
Location                      : Central US
DatabaseId                    : ef5a9698-012c-4def-8d94-7f6bfb7b4f04
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 34359738368
Status                        : Online
CreationDate                  : 4/12/2019 11:20:29 PM
CurrentServiceObjectiveName   : GP_S_Gen5_2
RequestedServiceObjectiveName : GP_S_Gen5_2
ElasticPoolName               :
EarliestRestoreDate           : 4/12/2019 11:50:29 PM
Tags                          :
CreateMode                    :
ReadScale                     : Disabled
ZoneRedundant                 : False
Capacity                      : 2
Family                        : Gen5
SkuName                       : GP_S_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       : 360
MinimumCapacity          : 0.5
```

<span data-ttu-id="e6e7b-118">이 명령은 Server Server01에 Database04라는 서버리스 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="e6e7b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6e7b-119">PARAMETERS</span></span>

### <span data-ttu-id="e6e7b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6e7b-120">-AsJob</span></span>
<span data-ttu-id="e6e7b-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e6e7b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6e7b-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="e6e7b-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="e6e7b-123">데이터베이스의 자동 일시 중지 지연(서버리스만 해당), -1에서 옵트아웃하는 시간(분)</span><span class="sxs-lookup"><span data-stu-id="e6e7b-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-124">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="e6e7b-124">-BackupStorageRedundancy</span></span>
<span data-ttu-id="e6e7b-125">SQL 데이터베이스에 대한 백업을 저장하는 데 사용되는 Backup 저장소 중복성입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-125">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="e6e7b-126">옵션은 로컬, 영역 및 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-126">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="e6e7b-127">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="e6e7b-127">-CatalogCollation</span></span>
<span data-ttu-id="e6e7b-128">데이터베이스 카탈로그 데이터 SQL 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-128">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="e6e7b-129">-CollationName</span><span class="sxs-lookup"><span data-stu-id="e6e7b-129">-CollationName</span></span>
<span data-ttu-id="e6e7b-130">데이터베이스 데이터 데이터 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-130">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="e6e7b-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="e6e7b-131">-ComputeGeneration</span></span>
<span data-ttu-id="e6e7b-132">할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-132">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-133">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="e6e7b-133">-ComputeModel</span></span>
<span data-ttu-id="e6e7b-134">Azure Sql 데이터베이스에 대한 계산 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-134">The compute model for Azure Sql database.</span></span> <span data-ttu-id="e6e7b-135">서버리스 또는 프로비전</span><span class="sxs-lookup"><span data-stu-id="e6e7b-135">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-136">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e6e7b-136">-DatabaseName</span></span>
<span data-ttu-id="e6e7b-137">데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-137">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e7b-138">-DefaultProfile</span></span>
<span data-ttu-id="e6e7b-139">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e6e7b-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6e7b-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="e6e7b-140">-Edition</span></span>
<span data-ttu-id="e6e7b-141">데이터베이스에 할당할 에디션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-141">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="e6e7b-142">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="e6e7b-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e6e7b-143">없음</span><span class="sxs-lookup"><span data-stu-id="e6e7b-143">None</span></span>
- <span data-ttu-id="e6e7b-144">기본</span><span class="sxs-lookup"><span data-stu-id="e6e7b-144">Basic</span></span>
- <span data-ttu-id="e6e7b-145">표준</span><span class="sxs-lookup"><span data-stu-id="e6e7b-145">Standard</span></span>
- <span data-ttu-id="e6e7b-146">프리미엄</span><span class="sxs-lookup"><span data-stu-id="e6e7b-146">Premium</span></span>
- <span data-ttu-id="e6e7b-147">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="e6e7b-147">DataWarehouse</span></span>
- <span data-ttu-id="e6e7b-148">무료</span><span class="sxs-lookup"><span data-stu-id="e6e7b-148">Free</span></span>
- <span data-ttu-id="e6e7b-149">Stretch</span><span class="sxs-lookup"><span data-stu-id="e6e7b-149">Stretch</span></span>
- <span data-ttu-id="e6e7b-150">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="e6e7b-150">GeneralPurpose</span></span>
- <span data-ttu-id="e6e7b-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="e6e7b-151">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e6e7b-152">-ElasticPoolName</span></span>
<span data-ttu-id="e6e7b-153">데이터베이스를 넣을 탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-153">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-154">-Force</span><span class="sxs-lookup"><span data-stu-id="e6e7b-154">-Force</span></span>
<span data-ttu-id="e6e7b-155">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="e6e7b-155">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="e6e7b-156">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="e6e7b-156">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="e6e7b-157">읽기 전용 애플리케이션 의도 연결이 라우팅될 수 있는 데이터베이스와 연결된 읽기 전용 보조 복제본의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-157">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="e6e7b-158">이 속성은 하이퍼스케일 버전 데이터베이스에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-158">This property is only settable for Hyperscale edition databases.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ReadReplicaCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e6e7b-159">-LicenseType</span></span>
<span data-ttu-id="e6e7b-160">Azure Sql 데이터베이스에 대한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-160">The license type for the Azure Sql database.</span></span> <span data-ttu-id="e6e7b-161">가능한 값은</span><span class="sxs-lookup"><span data-stu-id="e6e7b-161">Possible values are:</span></span>
- <span data-ttu-id="e6e7b-162">BasePrice - 기존 라이선스 소유자에 대한 AHB(Azure 하이브리드 혜택) SQL Server 가격이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-162">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="e6e7b-163">기존 라이선스 소유자에 대해 데이터베이스 SQL Server 할인됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-163">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="e6e7b-164">LicenseIncluded - 기존 라이선스 소유자에 대한 AHB(Azure 하이브리드 혜택) SQL Server 가격은 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-164">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="e6e7b-165">데이터베이스 가격에는 새 라이선스 SQL Server 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-165">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="e6e7b-166">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e6e7b-166">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="e6e7b-167">SQL 데이터베이스의 유지 관리 구성 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-167">The Maintenance configuration id for the SQL Database.</span></span>

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

### <span data-ttu-id="e6e7b-168">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="e6e7b-168">-MaxSizeBytes</span></span>
<span data-ttu-id="e6e7b-169">데이터베이스의 최대 크기를 지정합니다(Bytes).</span><span class="sxs-lookup"><span data-stu-id="e6e7b-169">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-170">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="e6e7b-170">-MinimumCapacity</span></span>
<span data-ttu-id="e6e7b-171">일시 중지되지 않은 경우 데이터베이스가 항상 할당하는 최소 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-171">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="e6e7b-172">서버리스 Azure Sql 데이터베이스의 경우만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-172">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-173">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="e6e7b-173">-ReadScale</span></span>
<span data-ttu-id="e6e7b-174">사용하도록 설정하면 해당 연결 문자열에서 애플리케이션 의도가 읽기 전용으로 설정된 연결은 읽기 전용 보조 복제본으로 라우팅될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-174">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="e6e7b-175">이 속성은 프리미엄 및 중요 비즈니스용 데이터베이스에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-175">This property is only settable for Premium and Business Critical databases.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-176">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="e6e7b-176">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="e6e7b-177">데이터베이스에 할당할 서비스 목표의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-177">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6e7b-178">-ResourceGroupName</span></span>
<span data-ttu-id="e6e7b-179">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-179">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e6e7b-180">-SampleName</span><span class="sxs-lookup"><span data-stu-id="e6e7b-180">-SampleName</span></span>
<span data-ttu-id="e6e7b-181">이 데이터베이스를 만들 때 적용할 샘플의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-181">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-182">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="e6e7b-182">-SecondaryType</span></span>
<span data-ttu-id="e6e7b-183">보조 데이터베이스인 경우 데이터베이스의 보조 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-183">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="e6e7b-184">유효한 값은 Geo 및 Named입니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-184">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="e6e7b-185">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e6e7b-185">-ServerName</span></span>
<span data-ttu-id="e6e7b-186">데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-186">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="e6e7b-187">-Tags</span><span class="sxs-lookup"><span data-stu-id="e6e7b-187">-Tags</span></span>
<span data-ttu-id="e6e7b-188">이 cmdlet이 새 데이터베이스와 연결되는 해시 테이블 형태로 키-값 쌍의 사전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-188">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="e6e7b-189">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="e6e7b-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-190">-VCore</span><span class="sxs-lookup"><span data-stu-id="e6e7b-190">-VCore</span></span>
<span data-ttu-id="e6e7b-191">Azure Sql 데이터베이스에 대한 Vcore 번호</span><span class="sxs-lookup"><span data-stu-id="e6e7b-191">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6e7b-192">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="e6e7b-192">-ZoneRedundant</span></span>
<span data-ttu-id="e6e7b-193">Azure Sql Database와 연결하기 위해 영역 중복</span><span class="sxs-lookup"><span data-stu-id="e6e7b-193">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="e6e7b-194">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6e7b-194">-Confirm</span></span>
<span data-ttu-id="e6e7b-195">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6e7b-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6e7b-196">-WhatIf</span></span>
<span data-ttu-id="e6e7b-197">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e6e7b-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6e7b-198">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6e7b-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e7b-199">CommonParameters</span></span>
<span data-ttu-id="e6e7b-200">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e7b-201">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e7b-202">입력</span><span class="sxs-lookup"><span data-stu-id="e6e7b-202">INPUTS</span></span>

### <span data-ttu-id="e6e7b-203">System.String</span><span class="sxs-lookup"><span data-stu-id="e6e7b-203">System.String</span></span>

## <span data-ttu-id="e6e7b-204">출력</span><span class="sxs-lookup"><span data-stu-id="e6e7b-204">OUTPUTS</span></span>

### <span data-ttu-id="e6e7b-205">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e6e7b-205">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="e6e7b-206">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e6e7b-206">NOTES</span></span>

## <span data-ttu-id="e6e7b-207">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6e7b-207">RELATED LINKS</span></span>

[<span data-ttu-id="e6e7b-208">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6e7b-208">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="e6e7b-209">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e6e7b-209">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="e6e7b-210">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="e6e7b-210">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="e6e7b-211">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6e7b-211">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="e6e7b-212">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6e7b-212">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="e6e7b-213">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6e7b-213">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="e6e7b-214">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e6e7b-214">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="e6e7b-215">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="e6e7b-215">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

