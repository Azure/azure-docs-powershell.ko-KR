---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: ff474116854838c40a4862cf93f4d017ccdf4527
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698908"
---
# <span data-ttu-id="13fee-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="13fee-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="13fee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13fee-102">SYNOPSIS</span></span>
<span data-ttu-id="13fee-103">데이터베이스 또는 탄력적 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="13fee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="13fee-104">SYNTAX</span></span>

### <span data-ttu-id="13fee-105">DtuBasedDatabase (기본값)</span><span class="sxs-lookup"><span data-stu-id="13fee-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13fee-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="13fee-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13fee-107">설명은</span><span class="sxs-lookup"><span data-stu-id="13fee-107">DESCRIPTION</span></span>
<span data-ttu-id="13fee-108">**AzSqlDatabase** Cmdlet은 Azure SQL 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="13fee-109">*ElasticPoolName* 매개 변수를 기존 탄력적 풀로 설정 하 여 탄력적 데이터베이스를 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="13fee-110">예제의</span><span class="sxs-lookup"><span data-stu-id="13fee-110">EXAMPLES</span></span>

### <span data-ttu-id="13fee-111">예제 1: 지정 된 서버에서 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="13fee-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="13fee-112">이 명령은 서버 Server01에 Database01 이라는 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="13fee-113">예제 2: 지정 된 서버에서 탄력적 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="13fee-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="13fee-114">이 명령은 서버 Server01의 ElasticPool01 이라는 탄력적 풀에 Database02 이라는 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="13fee-115">예제 3: 지정 된 서버에서 Vcore 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="13fee-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="13fee-116">이 명령은 서버 Server01에 Database03 이라는 Vcore 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="13fee-117">변수</span><span class="sxs-lookup"><span data-stu-id="13fee-117">PARAMETERS</span></span>

### <span data-ttu-id="13fee-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13fee-118">-AsJob</span></span>
<span data-ttu-id="13fee-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="13fee-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13fee-120">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="13fee-120">-CatalogCollation</span></span>
<span data-ttu-id="13fee-121">SQL 데이터베이스 카탈로그 데이터 정렬의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-121">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="13fee-122">-CollationName</span><span class="sxs-lookup"><span data-stu-id="13fee-122">-CollationName</span></span>
<span data-ttu-id="13fee-123">SQL 데이터베이스 데이터 정렬의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-123">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="13fee-124">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="13fee-124">-ComputeGeneration</span></span>
<span data-ttu-id="13fee-125">할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="13fee-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="13fee-126">-DatabaseName</span></span>
<span data-ttu-id="13fee-127">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="13fee-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13fee-128">-DefaultProfile</span></span>
<span data-ttu-id="13fee-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="13fee-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13fee-130">-에디션</span><span class="sxs-lookup"><span data-stu-id="13fee-130">-Edition</span></span>
<span data-ttu-id="13fee-131">데이터베이스에 할당할 에디션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="13fee-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="13fee-133">않아야</span><span class="sxs-lookup"><span data-stu-id="13fee-133">None</span></span>
- <span data-ttu-id="13fee-134">기본적</span><span class="sxs-lookup"><span data-stu-id="13fee-134">Basic</span></span>
- <span data-ttu-id="13fee-135">표준이</span><span class="sxs-lookup"><span data-stu-id="13fee-135">Standard</span></span>
- <span data-ttu-id="13fee-136">Premium</span><span class="sxs-lookup"><span data-stu-id="13fee-136">Premium</span></span>
- <span data-ttu-id="13fee-137">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="13fee-137">DataWarehouse</span></span>
- <span data-ttu-id="13fee-138">비우거나</span><span class="sxs-lookup"><span data-stu-id="13fee-138">Free</span></span>
- <span data-ttu-id="13fee-139">늘이고</span><span class="sxs-lookup"><span data-stu-id="13fee-139">Stretch</span></span>
- <span data-ttu-id="13fee-140">일반 목적</span><span class="sxs-lookup"><span data-stu-id="13fee-140">GeneralPurpose</span></span>
- <span data-ttu-id="13fee-141">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="13fee-141">BusinessCritical</span></span>

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

### <span data-ttu-id="13fee-142">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="13fee-142">-ElasticPoolName</span></span>
<span data-ttu-id="13fee-143">데이터베이스를 저장할 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-143">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="13fee-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="13fee-144">-LicenseType</span></span>
<span data-ttu-id="13fee-145">Azure Sql 데이터베이스에 대 한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-145">The license type for the Azure Sql database.</span></span> <span data-ttu-id="13fee-146">사용할 수 있는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-146">Possible values are:</span></span>
- <span data-ttu-id="13fee-147">BasePrice-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-147">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="13fee-148">기존 SQL Server 라이선스 소유자에 게 데이터베이스 가격이 할인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-148">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="13fee-149">LicenseIncluded-Azure 하이브리드 혜택 (AHB) 기존 SQL Server 라이선스 소유자에 대 한 할인 가격이 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-149">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="13fee-150">데이터베이스 가격에는 새로운 SQL Server 라이선스 비용이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-150">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="13fee-151">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="13fee-151">-MaxSizeBytes</span></span>
<span data-ttu-id="13fee-152">데이터베이스의 최대 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-152">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="13fee-153">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="13fee-153">-ReadScale</span></span>
<span data-ttu-id="13fee-154">Azure SQL 데이터베이스에 할당할 읽기 배율 옵션입니다. (사용/사용 안 함)</span><span class="sxs-lookup"><span data-stu-id="13fee-154">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="13fee-155">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="13fee-155">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="13fee-156">데이터베이스에 할당할 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-156">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="13fee-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13fee-157">-ResourceGroupName</span></span>
<span data-ttu-id="13fee-158">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-158">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="13fee-159">-SampleName</span><span class="sxs-lookup"><span data-stu-id="13fee-159">-SampleName</span></span>
<span data-ttu-id="13fee-160">이 데이터베이스를 만들 때 적용할 샘플 스키마의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-160">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="13fee-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="13fee-161">-ServerName</span></span>
<span data-ttu-id="13fee-162">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-162">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="13fee-163">태그</span><span class="sxs-lookup"><span data-stu-id="13fee-163">-Tags</span></span>
<span data-ttu-id="13fee-164">이 cmdlet가 새 데이터베이스와 연결 하는 해시 테이블 형식으로 키-값 쌍의 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-164">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="13fee-165">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="13fee-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="13fee-166">-VCore</span><span class="sxs-lookup"><span data-stu-id="13fee-166">-VCore</span></span>
<span data-ttu-id="13fee-167">Azure Sql 데이터베이스의 Vcore 번호</span><span class="sxs-lookup"><span data-stu-id="13fee-167">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13fee-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="13fee-168">-ZoneRedundant</span></span>
<span data-ttu-id="13fee-169">Azure Sql Database와 연결 되는 영역 중복성</span><span class="sxs-lookup"><span data-stu-id="13fee-169">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="13fee-170">-확인</span><span class="sxs-lookup"><span data-stu-id="13fee-170">-Confirm</span></span>
<span data-ttu-id="13fee-171">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13fee-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13fee-172">-WhatIf</span></span>
<span data-ttu-id="13fee-173">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13fee-174">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13fee-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13fee-175">CommonParameters</span></span>
<span data-ttu-id="13fee-176">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="13fee-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13fee-177">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="13fee-177">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13fee-178">입력</span><span class="sxs-lookup"><span data-stu-id="13fee-178">INPUTS</span></span>

### <span data-ttu-id="13fee-179">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="13fee-179">System.String</span></span>

## <span data-ttu-id="13fee-180">출력</span><span class="sxs-lookup"><span data-stu-id="13fee-180">OUTPUTS</span></span>

### <span data-ttu-id="13fee-181">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="13fee-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="13fee-182">상속자</span><span class="sxs-lookup"><span data-stu-id="13fee-182">NOTES</span></span>

## <span data-ttu-id="13fee-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13fee-183">RELATED LINKS</span></span>

[<span data-ttu-id="13fee-184">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="13fee-184">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="13fee-185">새로운 AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="13fee-185">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="13fee-186">새로운 AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="13fee-186">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="13fee-187">제거-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="13fee-187">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="13fee-188">이력서-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="13fee-188">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="13fee-189">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="13fee-189">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="13fee-190">일시 중단-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="13fee-190">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="13fee-191">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="13fee-191">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

