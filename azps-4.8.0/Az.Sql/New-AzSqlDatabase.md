---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: 264fecd37738a0da484c28f1ec8ce84f14efe159
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204282"
---
# <span data-ttu-id="eb955-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eb955-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="eb955-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb955-102">SYNOPSIS</span></span>
<span data-ttu-id="eb955-103">데이터베이스 또는 탄력적 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="eb955-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eb955-104">SYNTAX</span></span>

### <span data-ttu-id="eb955-105">DtuBasedDatabase (기본값)</span><span class="sxs-lookup"><span data-stu-id="eb955-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-Force] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb955-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="eb955-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] [-Force] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb955-107">설명은</span><span class="sxs-lookup"><span data-stu-id="eb955-107">DESCRIPTION</span></span>
<span data-ttu-id="eb955-108">**AzSqlDatabase** Cmdlet은 Azure SQL 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="eb955-109">*ElasticPoolName* 매개 변수를 기존 탄력적 풀로 설정 하 여 탄력적 데이터베이스를 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="eb955-110">예제의</span><span class="sxs-lookup"><span data-stu-id="eb955-110">EXAMPLES</span></span>

### <span data-ttu-id="eb955-111">예제 1: 지정 된 서버에서 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="eb955-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="eb955-112">이 명령은 서버 Server01에 Database01 이라는 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="eb955-113">예제 2: 지정 된 서버에서 탄력적 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="eb955-113">Example 2: Create an elastic database on a specified server</span></span>
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

<span data-ttu-id="eb955-114">이 명령은 서버 Server01의 ElasticPool01 이라는 탄력적 풀에 Database02 이라는 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="eb955-115">예제 3: 지정 된 서버에서 Vcore 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="eb955-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="eb955-116">이 명령은 서버 Server01에 Database03 이라는 Vcore 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="eb955-117">예제 4: 지정 된 서버에서 서버를 실행 하지 않은 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="eb955-117">Example 4: Create an Serverless database on the specified server</span></span>
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

<span data-ttu-id="eb955-118">이 명령은 서버 Server01에서 Database04 이라는 데이터베이스를 만들 때 생성 되지 않은 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="eb955-119">변수</span><span class="sxs-lookup"><span data-stu-id="eb955-119">PARAMETERS</span></span>

### <span data-ttu-id="eb955-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb955-120">-AsJob</span></span>
<span data-ttu-id="eb955-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="eb955-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb955-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="eb955-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="eb955-123">데이터베이스에 대 한 자동 일시 정지 지연 시간 (서버를 사용할 수 없음),-1에서 옵트아웃</span><span class="sxs-lookup"><span data-stu-id="eb955-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="eb955-124">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="eb955-124">-BackupStorageRedundancy</span></span>
<span data-ttu-id="eb955-125">SQL 데이터베이스에 대 한 백업을 저장 하는 데 사용 되는 백업 저장소 중복성입니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-125">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="eb955-126">지역, Zone, Geo 등의 옵션을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-126">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="eb955-127">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="eb955-127">-CatalogCollation</span></span>
<span data-ttu-id="eb955-128">SQL 데이터베이스 카탈로그 데이터 정렬의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-128">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="eb955-129">-CollationName</span><span class="sxs-lookup"><span data-stu-id="eb955-129">-CollationName</span></span>
<span data-ttu-id="eb955-130">SQL 데이터베이스 데이터 정렬의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-130">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="eb955-131">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="eb955-131">-ComputeGeneration</span></span>
<span data-ttu-id="eb955-132">할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-132">The compute generation to assign.</span></span>

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

### <span data-ttu-id="eb955-133">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="eb955-133">-ComputeModel</span></span>
<span data-ttu-id="eb955-134">Azure Sql 데이터베이스의 계산 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-134">The compute model for Azure Sql database.</span></span> <span data-ttu-id="eb955-135">서버에서 또는 프로 비전 됨</span><span class="sxs-lookup"><span data-stu-id="eb955-135">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="eb955-136">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb955-136">-DatabaseName</span></span>
<span data-ttu-id="eb955-137">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-137">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="eb955-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb955-138">-DefaultProfile</span></span>
<span data-ttu-id="eb955-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="eb955-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb955-140">-에디션</span><span class="sxs-lookup"><span data-stu-id="eb955-140">-Edition</span></span>
<span data-ttu-id="eb955-141">데이터베이스에 할당할 에디션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-141">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="eb955-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb955-143">않아야</span><span class="sxs-lookup"><span data-stu-id="eb955-143">None</span></span>
- <span data-ttu-id="eb955-144">기본적</span><span class="sxs-lookup"><span data-stu-id="eb955-144">Basic</span></span>
- <span data-ttu-id="eb955-145">표준이</span><span class="sxs-lookup"><span data-stu-id="eb955-145">Standard</span></span>
- <span data-ttu-id="eb955-146">Premium</span><span class="sxs-lookup"><span data-stu-id="eb955-146">Premium</span></span>
- <span data-ttu-id="eb955-147">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="eb955-147">DataWarehouse</span></span>
- <span data-ttu-id="eb955-148">비우거나</span><span class="sxs-lookup"><span data-stu-id="eb955-148">Free</span></span>
- <span data-ttu-id="eb955-149">늘이고</span><span class="sxs-lookup"><span data-stu-id="eb955-149">Stretch</span></span>
- <span data-ttu-id="eb955-150">일반 목적</span><span class="sxs-lookup"><span data-stu-id="eb955-150">GeneralPurpose</span></span>
- <span data-ttu-id="eb955-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="eb955-151">BusinessCritical</span></span>

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

### <span data-ttu-id="eb955-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="eb955-152">-ElasticPoolName</span></span>
<span data-ttu-id="eb955-153">데이터베이스를 저장할 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-153">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="eb955-154">-Force</span><span class="sxs-lookup"><span data-stu-id="eb955-154">-Force</span></span>
<span data-ttu-id="eb955-155">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="eb955-155">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="eb955-156">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="eb955-156">-LicenseType</span></span>
<span data-ttu-id="eb955-157">Azure Sql 데이터베이스에 대 한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-157">The license type for the Azure Sql database.</span></span> <span data-ttu-id="eb955-158">사용할 수 있는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-158">Possible values are:</span></span>
- <span data-ttu-id="eb955-159">BasePrice-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-159">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="eb955-160">기존 SQL Server 라이선스 소유자에 게 데이터베이스 가격이 할인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-160">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="eb955-161">LicenseIncluded-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-161">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="eb955-162">데이터베이스 가격에는 새로운 SQL Server 라이선스 비용이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-162">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="eb955-163">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="eb955-163">-MaxSizeBytes</span></span>
<span data-ttu-id="eb955-164">데이터베이스의 최대 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-164">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="eb955-165">-가을 용량</span><span class="sxs-lookup"><span data-stu-id="eb955-165">-MinimumCapacity</span></span>
<span data-ttu-id="eb955-166">데이터베이스가 일시 중지 되지 않은 경우 항상 할당 되는 최소 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-166">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="eb955-167">서버를 사용할 경우 Azure Sql 데이터베이스에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-167">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="eb955-168">-ReadReplicaCount</span><span class="sxs-lookup"><span data-stu-id="eb955-168">-ReadReplicaCount</span></span>
<span data-ttu-id="eb955-169">읽기 전용 응용 프로그램 의도 연결을 라우팅할 수 있는 데이터베이스와 연결 된 읽기 전용 보조 복제본의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-169">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="eb955-170">이 속성은 Hyperscale edition 데이터베이스에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-170">This property is only settable for Hyperscale edition databases.</span></span>

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

### <span data-ttu-id="eb955-171">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="eb955-171">-ReadScale</span></span>
<span data-ttu-id="eb955-172">이 기능을 사용 하도록 설정 하면 응용 프로그램 의도가 연결 문자열의 readonly로 설정 된 연결이 읽기 전용 보조 복제본으로 라우팅될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-172">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="eb955-173">이 속성은 Premium 및 비즈니스 중요 데이터베이스에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-173">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="eb955-174">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="eb955-174">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="eb955-175">데이터베이스에 할당할 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-175">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="eb955-176">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb955-176">-ResourceGroupName</span></span>
<span data-ttu-id="eb955-177">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-177">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="eb955-178">-SampleName</span><span class="sxs-lookup"><span data-stu-id="eb955-178">-SampleName</span></span>
<span data-ttu-id="eb955-179">이 데이터베이스를 만들 때 적용할 샘플 스키마의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-179">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="eb955-180">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eb955-180">-ServerName</span></span>
<span data-ttu-id="eb955-181">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-181">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="eb955-182">태그</span><span class="sxs-lookup"><span data-stu-id="eb955-182">-Tags</span></span>
<span data-ttu-id="eb955-183">이 cmdlet가 새 데이터베이스와 연결 하는 해시 테이블 형식으로 키-값 쌍의 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-183">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="eb955-184">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="eb955-184">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="eb955-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="eb955-185">-VCore</span></span>
<span data-ttu-id="eb955-186">Azure Sql 데이터베이스의 Vcore 번호</span><span class="sxs-lookup"><span data-stu-id="eb955-186">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="eb955-187">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="eb955-187">-ZoneRedundant</span></span>
<span data-ttu-id="eb955-188">Azure Sql Database와 연결 되는 영역 중복성</span><span class="sxs-lookup"><span data-stu-id="eb955-188">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="eb955-189">-확인</span><span class="sxs-lookup"><span data-stu-id="eb955-189">-Confirm</span></span>
<span data-ttu-id="eb955-190">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb955-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb955-191">-WhatIf</span></span>
<span data-ttu-id="eb955-192">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb955-193">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb955-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb955-194">CommonParameters</span></span>
<span data-ttu-id="eb955-195">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb955-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb955-196">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eb955-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb955-197">입력</span><span class="sxs-lookup"><span data-stu-id="eb955-197">INPUTS</span></span>

### <span data-ttu-id="eb955-198">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eb955-198">System.String</span></span>

## <span data-ttu-id="eb955-199">출력</span><span class="sxs-lookup"><span data-stu-id="eb955-199">OUTPUTS</span></span>

### <span data-ttu-id="eb955-200">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="eb955-200">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="eb955-201">상속자</span><span class="sxs-lookup"><span data-stu-id="eb955-201">NOTES</span></span>

## <span data-ttu-id="eb955-202">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb955-202">RELATED LINKS</span></span>

[<span data-ttu-id="eb955-203">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eb955-203">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="eb955-204">새로운 AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="eb955-204">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="eb955-205">새로운 AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="eb955-205">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="eb955-206">제거-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eb955-206">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="eb955-207">이력서-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eb955-207">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="eb955-208">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eb955-208">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="eb955-209">일시 중단-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eb955-209">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="eb955-210">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="eb955-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

