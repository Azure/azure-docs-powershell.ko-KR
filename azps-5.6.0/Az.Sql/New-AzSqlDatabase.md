---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: c4ccb57292fd4abc2c9b6fd14c5e4492047a2e89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956592"
---
# <span data-ttu-id="aefec-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aefec-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="aefec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aefec-102">SYNOPSIS</span></span>
<span data-ttu-id="aefec-103">데이터베이스 또는 탄력적 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="aefec-104">구문</span><span class="sxs-lookup"><span data-stu-id="aefec-104">SYNTAX</span></span>

### <span data-ttu-id="aefec-105">DtuBasedDatabase(기본값)</span><span class="sxs-lookup"><span data-stu-id="aefec-105">DtuBasedDatabase (Default)</span></span>
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

### <span data-ttu-id="aefec-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="aefec-106">VcoreBasedDatabase</span></span>
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

## <span data-ttu-id="aefec-107">설명</span><span class="sxs-lookup"><span data-stu-id="aefec-107">DESCRIPTION</span></span>
<span data-ttu-id="aefec-108">**New-AzSqlDatabase** cmdlet은 Azure SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="aefec-109">*ElasticPoolName* 매개 변수를 기존 탄력적 풀로 설정하여 탄력적 데이터베이스를 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="aefec-110">예제</span><span class="sxs-lookup"><span data-stu-id="aefec-110">EXAMPLES</span></span>

### <span data-ttu-id="aefec-111">예제 1: 지정된 서버에서 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="aefec-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="aefec-112">이 명령은 server Server01에서 Database01이라는 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="aefec-113">예제 2: 지정된 서버에서 탄력적 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="aefec-113">Example 2: Create an elastic database on a specified server</span></span>
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

<span data-ttu-id="aefec-114">이 명령은 Server01의 ElasticPool01이라는 탄력적 풀에 Database02라는 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="aefec-115">예제 3: 지정된 서버에서 Vcore 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="aefec-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="aefec-116">이 명령은 Server01에서 Database03이라는 Vcore 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="aefec-117">예제 4: 지정된 서버에서 Serverless 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="aefec-117">Example 4: Create an Serverless database on the specified server</span></span>
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

<span data-ttu-id="aefec-118">이 명령은 Server01에서 Database04라는 Serverless 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="aefec-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aefec-119">PARAMETERS</span></span>

### <span data-ttu-id="aefec-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aefec-120">-AsJob</span></span>
<span data-ttu-id="aefec-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="aefec-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aefec-122">-AutoPauseDelayInMinutes</span><span class="sxs-lookup"><span data-stu-id="aefec-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="aefec-123">데이터베이스의 자동 일시 중지 지연(서버리스만 해당), -1에서 옵트아웃</span><span class="sxs-lookup"><span data-stu-id="aefec-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

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

### <span data-ttu-id="aefec-124">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="aefec-124">-BackupStorageRedundancy</span></span>
<span data-ttu-id="aefec-125">백업 데이터베이스에 대한 백업을 저장하는 데 SQL 저장소 중복성입니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-125">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="aefec-126">옵션은 로컬, 영역 및 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-126">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="aefec-127">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="aefec-127">-CatalogCollation</span></span>
<span data-ttu-id="aefec-128">데이터베이스 카탈로그 SQL 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-128">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="aefec-129">-CollationName</span><span class="sxs-lookup"><span data-stu-id="aefec-129">-CollationName</span></span>
<span data-ttu-id="aefec-130">데이터베이스 데이터 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-130">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="aefec-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="aefec-131">-ComputeGeneration</span></span>
<span data-ttu-id="aefec-132">할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-132">The compute generation to assign.</span></span>

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

### <span data-ttu-id="aefec-133">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="aefec-133">-ComputeModel</span></span>
<span data-ttu-id="aefec-134">Azure Sql Database의 계산 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-134">The compute model for Azure Sql database.</span></span> <span data-ttu-id="aefec-135">서버리스 또는 프로비전</span><span class="sxs-lookup"><span data-stu-id="aefec-135">Serverless or Provisioned</span></span>

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

### <span data-ttu-id="aefec-136">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aefec-136">-DatabaseName</span></span>
<span data-ttu-id="aefec-137">데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-137">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="aefec-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aefec-138">-DefaultProfile</span></span>
<span data-ttu-id="aefec-139">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="aefec-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aefec-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="aefec-140">-Edition</span></span>
<span data-ttu-id="aefec-141">데이터베이스에 할당할 에디션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-141">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="aefec-142">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aefec-143">없음</span><span class="sxs-lookup"><span data-stu-id="aefec-143">None</span></span>
- <span data-ttu-id="aefec-144">기본</span><span class="sxs-lookup"><span data-stu-id="aefec-144">Basic</span></span>
- <span data-ttu-id="aefec-145">표준</span><span class="sxs-lookup"><span data-stu-id="aefec-145">Standard</span></span>
- <span data-ttu-id="aefec-146">프리미엄</span><span class="sxs-lookup"><span data-stu-id="aefec-146">Premium</span></span>
- <span data-ttu-id="aefec-147">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="aefec-147">DataWarehouse</span></span>
- <span data-ttu-id="aefec-148">무료</span><span class="sxs-lookup"><span data-stu-id="aefec-148">Free</span></span>
- <span data-ttu-id="aefec-149">스트레치</span><span class="sxs-lookup"><span data-stu-id="aefec-149">Stretch</span></span>
- <span data-ttu-id="aefec-150">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="aefec-150">GeneralPurpose</span></span>
- <span data-ttu-id="aefec-151">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="aefec-151">BusinessCritical</span></span>

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

### <span data-ttu-id="aefec-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="aefec-152">-ElasticPoolName</span></span>
<span data-ttu-id="aefec-153">데이터베이스를 넣을 탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-153">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="aefec-154">-Force</span><span class="sxs-lookup"><span data-stu-id="aefec-154">-Force</span></span>
<span data-ttu-id="aefec-155">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="aefec-155">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="aefec-156">-HighAvailabilityReplicaCount</span><span class="sxs-lookup"><span data-stu-id="aefec-156">-HighAvailabilityReplicaCount</span></span>
<span data-ttu-id="aefec-157">애플리케이션 의도 연결을 가독성으로 라우팅할 수 있는 데이터베이스와 연결된 읽기 보조 복제본의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-157">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="aefec-158">이 속성은 Hyperscale 버전 데이터베이스에만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-158">This property is only settable for Hyperscale edition databases.</span></span>

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

### <span data-ttu-id="aefec-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="aefec-159">-LicenseType</span></span>
<span data-ttu-id="aefec-160">Azure Sql 데이터베이스에 대한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-160">The license type for the Azure Sql database.</span></span> <span data-ttu-id="aefec-161">가능한 값은:</span><span class="sxs-lookup"><span data-stu-id="aefec-161">Possible values are:</span></span>
- <span data-ttu-id="aefec-162">BasePrice - 기존 라이선스 소유자에 대한 AHB(Azure Hybrid Benefit) 할인된 가격 SQL Server 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-162">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="aefec-163">기존 라이선스 소유자에 대해 데이터베이스 SQL Server 할인됩니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-163">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="aefec-164">LicenseIncluded - 기존 라이선스 소유자에 대한 AHB(Azure Hybrid Benefit) SQL Server 가격 책정은 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-164">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="aefec-165">데이터베이스 가격에는 새 라이선스 SQL Server 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-165">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="aefec-166">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="aefec-166">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="aefec-167">데이터베이스의 유지 관리 SQL ID입니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-167">The Maintenance configuration id for the SQL Database.</span></span>

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

### <span data-ttu-id="aefec-168">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="aefec-168">-MaxSizeBytes</span></span>
<span data-ttu-id="aefec-169">데이터베이스의 최대 크기를 bytes로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-169">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="aefec-170">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="aefec-170">-MinimumCapacity</span></span>
<span data-ttu-id="aefec-171">일시 중지되지 않은 경우 데이터베이스가 항상 할당하는 최소 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-171">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="aefec-172">서버리스 Azure Sql 데이터베이스의 경우만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-172">For serverless Azure Sql databases only.</span></span>

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

### <span data-ttu-id="aefec-173">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="aefec-173">-ReadScale</span></span>
<span data-ttu-id="aefec-174">사용이 설정된 경우 애플리케이션 의도가 해당 연결 문자열에서 읽기로 설정되어 있는 연결은 읽기 보조 복제본으로 라우팅될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-174">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="aefec-175">이 속성은 Premium 및 Business Critical 데이터베이스에만 설정 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-175">This property is only settable for Premium and Business Critical databases.</span></span>

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

### <span data-ttu-id="aefec-176">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="aefec-176">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="aefec-177">데이터베이스에 할당할 서비스 목표의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-177">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="aefec-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aefec-178">-ResourceGroupName</span></span>
<span data-ttu-id="aefec-179">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-179">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="aefec-180">-SampleName</span><span class="sxs-lookup"><span data-stu-id="aefec-180">-SampleName</span></span>
<span data-ttu-id="aefec-181">이 데이터베이스를 만들 때 적용할 샘플 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-181">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="aefec-182">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="aefec-182">-SecondaryType</span></span>
<span data-ttu-id="aefec-183">보조 데이터베이스의 보조 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-183">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="aefec-184">유효한 값은 지역 및 명명입니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-184">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="aefec-185">-ServerName</span><span class="sxs-lookup"><span data-stu-id="aefec-185">-ServerName</span></span>
<span data-ttu-id="aefec-186">데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-186">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="aefec-187">-Tags</span><span class="sxs-lookup"><span data-stu-id="aefec-187">-Tags</span></span>
<span data-ttu-id="aefec-188">이 cmdlet이 새 데이터베이스와 연결되는 해시 테이블의 형태로 Key-value 쌍의 사전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-188">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="aefec-189">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="aefec-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="aefec-190">-VCore</span><span class="sxs-lookup"><span data-stu-id="aefec-190">-VCore</span></span>
<span data-ttu-id="aefec-191">Azure Sql 데이터베이스에 대한 Vcore 번호</span><span class="sxs-lookup"><span data-stu-id="aefec-191">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="aefec-192">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="aefec-192">-ZoneRedundant</span></span>
<span data-ttu-id="aefec-193">Azure Sql Database와 연결되는 영역 중복성</span><span class="sxs-lookup"><span data-stu-id="aefec-193">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="aefec-194">-확인</span><span class="sxs-lookup"><span data-stu-id="aefec-194">-Confirm</span></span>
<span data-ttu-id="aefec-195">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aefec-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aefec-196">-WhatIf</span></span>
<span data-ttu-id="aefec-197">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aefec-198">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aefec-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aefec-199">CommonParameters</span></span>
<span data-ttu-id="aefec-200">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aefec-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aefec-201">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aefec-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aefec-202">입력</span><span class="sxs-lookup"><span data-stu-id="aefec-202">INPUTS</span></span>

### <span data-ttu-id="aefec-203">System.String</span><span class="sxs-lookup"><span data-stu-id="aefec-203">System.String</span></span>

## <span data-ttu-id="aefec-204">출력</span><span class="sxs-lookup"><span data-stu-id="aefec-204">OUTPUTS</span></span>

### <span data-ttu-id="aefec-205">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="aefec-205">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="aefec-206">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aefec-206">NOTES</span></span>

## <span data-ttu-id="aefec-207">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aefec-207">RELATED LINKS</span></span>

[<span data-ttu-id="aefec-208">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aefec-208">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="aefec-209">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="aefec-209">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="aefec-210">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="aefec-210">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="aefec-211">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aefec-211">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="aefec-212">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aefec-212">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="aefec-213">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aefec-213">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="aefec-214">suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="aefec-214">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="aefec-215">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="aefec-215">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

