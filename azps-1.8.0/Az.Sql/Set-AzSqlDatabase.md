---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 62823ec87758142b34490f24d3e1b24e0c434f85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698807"
---
# <span data-ttu-id="5d958-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d958-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="5d958-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d958-102">SYNOPSIS</span></span>
<span data-ttu-id="5d958-103">데이터베이스의 속성을 설정 하거나 기존 데이터베이스를 탄력적인 풀로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="5d958-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5d958-104">SYNTAX</span></span>

### <span data-ttu-id="5d958-105">업데이트 (기본값)</span><span class="sxs-lookup"><span data-stu-id="5d958-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d958-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="5d958-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d958-107">바꿉니다</span><span class="sxs-lookup"><span data-stu-id="5d958-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d958-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5d958-108">DESCRIPTION</span></span>
<span data-ttu-id="5d958-109">**AzSqlDatabase** Cmdlet은 Azure SQL 데이터베이스의 데이터베이스에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="5d958-110">이 cmdlet은 데이터베이스에 대 한 *버전* (서비스 계층), *RequestedServiceObjectiveName* (성능 수준) 및 저장소 최대 크기 ( *maxsizebytes* )를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="5d958-111">또한 *ElasticPoolName* 매개 변수를 지정 하 여 데이터베이스를 탄력적인 풀로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="5d958-112">탄력적 풀에 데이터베이스가 이미 있는 경우 *RequestedServiceObjectiveName* 매개 변수를 사용 하 여 데이터베이스를 탄력적 풀에서 이동 하 고 단일 데이터베이스의 성능 수준으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="5d958-113">예제의</span><span class="sxs-lookup"><span data-stu-id="5d958-113">EXAMPLES</span></span>

### <span data-ttu-id="5d958-114">예제 1: 표준 S0 데이터베이스로 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d958-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="5d958-115">이 명령은 Database01 이라는 데이터베이스를 Server01 라는 서버의 표준 S0 데이터베이스로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="5d958-116">예제 2: 탄력적 풀에 데이터베이스 추가</span><span class="sxs-lookup"><span data-stu-id="5d958-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="5d958-117">이 명령은 Database01 이라는 데이터베이스를 Server01 이라는 서버에서 호스팅된 ElasticPool01 이라는 탄력적 풀에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="5d958-118">예제 3: 데이터베이스의 저장소 최대 크기 수정</span><span class="sxs-lookup"><span data-stu-id="5d958-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="5d958-119">이 명령은 Database01 이라는 데이터베이스를 업데이트 하 여 최대 크기를 1TB로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="5d958-120">변수</span><span class="sxs-lookup"><span data-stu-id="5d958-120">PARAMETERS</span></span>

### <span data-ttu-id="5d958-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d958-121">-AsJob</span></span>
<span data-ttu-id="5d958-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5d958-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d958-123">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="5d958-123">-ComputeGeneration</span></span>
<span data-ttu-id="5d958-124">할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-124">The compute generation to assign.</span></span>

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

### <span data-ttu-id="5d958-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5d958-125">-DatabaseName</span></span>
<span data-ttu-id="5d958-126">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-126">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="5d958-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d958-127">-DefaultProfile</span></span>
<span data-ttu-id="5d958-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5d958-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d958-129">-에디션</span><span class="sxs-lookup"><span data-stu-id="5d958-129">-Edition</span></span>
<span data-ttu-id="5d958-130">데이터베이스의 에디션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-130">Specifies the edition for the database.</span></span>
<span data-ttu-id="5d958-131">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5d958-132">않아야</span><span class="sxs-lookup"><span data-stu-id="5d958-132">None</span></span>
- <span data-ttu-id="5d958-133">기본적</span><span class="sxs-lookup"><span data-stu-id="5d958-133">Basic</span></span>
- <span data-ttu-id="5d958-134">표준이</span><span class="sxs-lookup"><span data-stu-id="5d958-134">Standard</span></span>
- <span data-ttu-id="5d958-135">Premium</span><span class="sxs-lookup"><span data-stu-id="5d958-135">Premium</span></span>
- <span data-ttu-id="5d958-136">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="5d958-136">DataWarehouse</span></span>
- <span data-ttu-id="5d958-137">비우거나</span><span class="sxs-lookup"><span data-stu-id="5d958-137">Free</span></span>
- <span data-ttu-id="5d958-138">늘이고</span><span class="sxs-lookup"><span data-stu-id="5d958-138">Stretch</span></span>
- <span data-ttu-id="5d958-139">일반 목적</span><span class="sxs-lookup"><span data-stu-id="5d958-139">GeneralPurpose</span></span>
- <span data-ttu-id="5d958-140">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="5d958-140">BusinessCritical</span></span>

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

### <span data-ttu-id="5d958-141">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5d958-141">-ElasticPoolName</span></span>
<span data-ttu-id="5d958-142">데이터베이스를 이동할 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-142">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="5d958-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5d958-143">-LicenseType</span></span>
<span data-ttu-id="5d958-144">Azure Sql 데이터베이스에 대 한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-144">The license type for the Azure Sql database.</span></span> <span data-ttu-id="5d958-145">사용할 수 있는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-145">Possible values are:</span></span>
- <span data-ttu-id="5d958-146">BasePrice-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-146">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="5d958-147">기존 SQL Server 라이선스 소유자에 게 데이터베이스 가격이 할인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-147">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="5d958-148">LicenseIncluded-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-148">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="5d958-149">데이터베이스 가격에는 새로운 SQL Server 라이선스 비용이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-149">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="5d958-150">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="5d958-150">-MaxSizeBytes</span></span>
<span data-ttu-id="5d958-151">Azure SQL 데이터베이스의 최대 크기 (바이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-151">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="5d958-152">-NewName</span><span class="sxs-lookup"><span data-stu-id="5d958-152">-NewName</span></span>
<span data-ttu-id="5d958-153">데이터베이스 이름을 바꿀 새 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-153">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="5d958-154">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="5d958-154">-ReadScale</span></span>
<span data-ttu-id="5d958-155">Azure SQL 데이터베이스에 할당할 읽기 배율 옵션입니다. (사용/사용 안 함)</span><span class="sxs-lookup"><span data-stu-id="5d958-155">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="5d958-156">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="5d958-156">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="5d958-157">데이터베이스에 할당할 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-157">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="5d958-158">서비스 목표에 대 한 자세한 내용은 Microsoft 개발자 네트워크 라이브러리의 [AZURE SQL 데이터베이스 서비스 계층 및 성능 수준을](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5d958-158">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="5d958-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d958-159">-ResourceGroupName</span></span>
<span data-ttu-id="5d958-160">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-160">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5d958-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5d958-161">-ServerName</span></span>
<span data-ttu-id="5d958-162">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-162">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="5d958-163">태그</span><span class="sxs-lookup"><span data-stu-id="5d958-163">-Tags</span></span>
<span data-ttu-id="5d958-164">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5d958-165">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5d958-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5d958-166">-VCore</span><span class="sxs-lookup"><span data-stu-id="5d958-166">-VCore</span></span>
<span data-ttu-id="5d958-167">Azure Sql 데이터베이스의 Vcore 번호</span><span class="sxs-lookup"><span data-stu-id="5d958-167">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d958-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="5d958-168">-ZoneRedundant</span></span>
<span data-ttu-id="5d958-169">Azure Sql Database와 연결 되는 영역 중복성</span><span class="sxs-lookup"><span data-stu-id="5d958-169">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="5d958-170">-확인</span><span class="sxs-lookup"><span data-stu-id="5d958-170">-Confirm</span></span>
<span data-ttu-id="5d958-171">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d958-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d958-172">-WhatIf</span></span>
<span data-ttu-id="5d958-173">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d958-174">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d958-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d958-175">CommonParameters</span></span>
<span data-ttu-id="5d958-176">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d958-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d958-177">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5d958-177">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d958-178">입력</span><span class="sxs-lookup"><span data-stu-id="5d958-178">INPUTS</span></span>

### <span data-ttu-id="5d958-179">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5d958-179">System.String</span></span>

## <span data-ttu-id="5d958-180">출력</span><span class="sxs-lookup"><span data-stu-id="5d958-180">OUTPUTS</span></span>

### <span data-ttu-id="5d958-181">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="5d958-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5d958-182">상속자</span><span class="sxs-lookup"><span data-stu-id="5d958-182">NOTES</span></span>

## <span data-ttu-id="5d958-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d958-183">RELATED LINKS</span></span>

[<span data-ttu-id="5d958-184">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d958-184">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="5d958-185">새로운 AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d958-185">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="5d958-186">제거-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d958-186">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="5d958-187">이력서-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d958-187">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="5d958-188">일시 중단-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5d958-188">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="5d958-189">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="5d958-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
