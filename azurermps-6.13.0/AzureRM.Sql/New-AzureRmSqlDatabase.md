---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 7eaa753b973b887cbbddc132b998d05f3e374e3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704105"
---
# <span data-ttu-id="1d667-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1d667-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="1d667-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d667-102">SYNOPSIS</span></span>
<span data-ttu-id="1d667-103">데이터베이스 또는 탄력적 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d667-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1d667-104">SYNTAX</span></span>

### <span data-ttu-id="1d667-105">DtuBasedDatabase (기본값)</span><span class="sxs-lookup"><span data-stu-id="1d667-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d667-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="1d667-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d667-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1d667-107">DESCRIPTION</span></span>
<span data-ttu-id="1d667-108">**AzureRmSqlDatabase** Cmdlet은 Azure SQL 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-108">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="1d667-109">*ElasticPoolName* 매개 변수를 기존 탄력적 풀로 설정 하 여 탄력적 데이터베이스를 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="1d667-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1d667-110">EXAMPLES</span></span>

### <span data-ttu-id="1d667-111">예제 1: 지정 된 서버에서 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="1d667-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="1d667-112">이 명령은 서버 Server01에 Database01 이라는 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="1d667-113">예제 2: 지정 된 서버에서 탄력적 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="1d667-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="1d667-114">이 명령은 서버 Server01의 ElasticPool01 이라는 탄력적 풀에 Database02 이라는 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="1d667-115">예제 3: 지정 된 서버에서 Vcore 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="1d667-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
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

<span data-ttu-id="1d667-116">이 명령은 서버 Server01에 Database03 이라는 Vcore 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="1d667-117">변수</span><span class="sxs-lookup"><span data-stu-id="1d667-117">PARAMETERS</span></span>

### <span data-ttu-id="1d667-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d667-118">-AsJob</span></span>
<span data-ttu-id="1d667-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1d667-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d667-120">-CatalogCollation</span><span class="sxs-lookup"><span data-stu-id="1d667-120">-CatalogCollation</span></span>
<span data-ttu-id="1d667-121">SQL 데이터베이스 카탈로그 데이터 정렬의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-121">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="1d667-122">-CollationName</span><span class="sxs-lookup"><span data-stu-id="1d667-122">-CollationName</span></span>
<span data-ttu-id="1d667-123">SQL 데이터베이스 데이터 정렬의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-123">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="1d667-124">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="1d667-124">-ComputeGeneration</span></span>
<span data-ttu-id="1d667-125">할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="1d667-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1d667-126">-DatabaseName</span></span>
<span data-ttu-id="1d667-127">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="1d667-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d667-128">-DefaultProfile</span></span>
<span data-ttu-id="1d667-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1d667-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d667-130">-에디션</span><span class="sxs-lookup"><span data-stu-id="1d667-130">-Edition</span></span>
<span data-ttu-id="1d667-131">데이터베이스에 할당할 에디션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="1d667-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1d667-133">않아야</span><span class="sxs-lookup"><span data-stu-id="1d667-133">None</span></span>
- <span data-ttu-id="1d667-134">기본적</span><span class="sxs-lookup"><span data-stu-id="1d667-134">Basic</span></span>
- <span data-ttu-id="1d667-135">표준이</span><span class="sxs-lookup"><span data-stu-id="1d667-135">Standard</span></span>
- <span data-ttu-id="1d667-136">Premium</span><span class="sxs-lookup"><span data-stu-id="1d667-136">Premium</span></span>
- <span data-ttu-id="1d667-137">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="1d667-137">DataWarehouse</span></span>
- <span data-ttu-id="1d667-138">비우거나</span><span class="sxs-lookup"><span data-stu-id="1d667-138">Free</span></span>
- <span data-ttu-id="1d667-139">늘이고</span><span class="sxs-lookup"><span data-stu-id="1d667-139">Stretch</span></span>
- <span data-ttu-id="1d667-140">일반 목적</span><span class="sxs-lookup"><span data-stu-id="1d667-140">GeneralPurpose</span></span>
- <span data-ttu-id="1d667-141">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="1d667-141">BusinessCritical</span></span>

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

### <span data-ttu-id="1d667-142">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="1d667-142">-ElasticPoolName</span></span>
<span data-ttu-id="1d667-143">데이터베이스를 저장할 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-143">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="1d667-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1d667-144">-LicenseType</span></span>
<span data-ttu-id="1d667-145">Azure Sql 데이터베이스에 대 한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-145">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="1d667-146">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="1d667-146">-MaxSizeBytes</span></span>
<span data-ttu-id="1d667-147">데이터베이스의 최대 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-147">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="1d667-148">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="1d667-148">-ReadScale</span></span>
<span data-ttu-id="1d667-149">Azure SQL 데이터베이스에 할당할 읽기 배율 옵션입니다. (사용/사용 안 함)</span><span class="sxs-lookup"><span data-stu-id="1d667-149">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="1d667-150">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="1d667-150">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="1d667-151">데이터베이스에 할당할 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-151">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="1d667-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d667-152">-ResourceGroupName</span></span>
<span data-ttu-id="1d667-153">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-153">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="1d667-154">-SampleName</span><span class="sxs-lookup"><span data-stu-id="1d667-154">-SampleName</span></span>
<span data-ttu-id="1d667-155">이 데이터베이스를 만들 때 적용할 샘플 스키마의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-155">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="1d667-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1d667-156">-ServerName</span></span>
<span data-ttu-id="1d667-157">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-157">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="1d667-158">태그</span><span class="sxs-lookup"><span data-stu-id="1d667-158">-Tags</span></span>
<span data-ttu-id="1d667-159">이 cmdlet가 새 데이터베이스와 연결 하는 해시 테이블 형식으로 키-값 쌍의 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-159">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="1d667-160">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1d667-160">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1d667-161">-VCore</span><span class="sxs-lookup"><span data-stu-id="1d667-161">-VCore</span></span>
<span data-ttu-id="1d667-162">Azure Sql 데이터베이스의 Vcore 번호</span><span class="sxs-lookup"><span data-stu-id="1d667-162">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="1d667-163">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="1d667-163">-ZoneRedundant</span></span>
<span data-ttu-id="1d667-164">Azure Sql Database와 연결 되는 영역 중복성</span><span class="sxs-lookup"><span data-stu-id="1d667-164">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="1d667-165">-확인</span><span class="sxs-lookup"><span data-stu-id="1d667-165">-Confirm</span></span>
<span data-ttu-id="1d667-166">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d667-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d667-167">-WhatIf</span></span>
<span data-ttu-id="1d667-168">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d667-169">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d667-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d667-170">CommonParameters</span></span>
<span data-ttu-id="1d667-171">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d667-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d667-172">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d667-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d667-173">입력</span><span class="sxs-lookup"><span data-stu-id="1d667-173">INPUTS</span></span>

### <span data-ttu-id="1d667-174">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1d667-174">System.String</span></span>

## <span data-ttu-id="1d667-175">출력</span><span class="sxs-lookup"><span data-stu-id="1d667-175">OUTPUTS</span></span>

### <span data-ttu-id="1d667-176">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="1d667-176">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="1d667-177">상속자</span><span class="sxs-lookup"><span data-stu-id="1d667-177">NOTES</span></span>

## <span data-ttu-id="1d667-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d667-178">RELATED LINKS</span></span>

[<span data-ttu-id="1d667-179">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1d667-179">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="1d667-180">새로운 AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="1d667-180">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="1d667-181">새로운 AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="1d667-181">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="1d667-182">제거-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1d667-182">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="1d667-183">이력서-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1d667-183">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="1d667-184">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1d667-184">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="1d667-185">일시 중단-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1d667-185">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="1d667-186">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="1d667-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

