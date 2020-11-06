---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: b0493433f7419039acacd696748b3c5f9518aef5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528755"
---
# <span data-ttu-id="eb8b9-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eb8b9-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="eb8b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="eb8b9-103">데이터베이스의 속성을 설정 하거나 기존 데이터베이스를 탄력적인 풀로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb8b9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eb8b9-104">SYNTAX</span></span>

### <span data-ttu-id="eb8b9-105">Update</span><span class="sxs-lookup"><span data-stu-id="eb8b9-105">Update</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb8b9-106">바꿉니다</span><span class="sxs-lookup"><span data-stu-id="eb8b9-106">Rename</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb8b9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="eb8b9-107">DESCRIPTION</span></span>
<span data-ttu-id="eb8b9-108">**AzureRmSqlDatabase** Cmdlet은 Azure SQL 데이터베이스의 데이터베이스에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-108">The **Set-AzureRmSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="eb8b9-109">이 cmdlet은 데이터베이스에 대 한 *버전* (서비스 계층), *RequestedServiceObjectiveName* (성능 수준) 및 저장소 최대 크기 ( *maxsizebytes* )를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-109">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="eb8b9-110">또한 *ElasticPoolName* 매개 변수를 지정 하 여 데이터베이스를 탄력적인 풀로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-110">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="eb8b9-111">탄력적 풀에 데이터베이스가 이미 있는 경우 *RequestedServiceObjectiveName* 매개 변수를 사용 하 여 데이터베이스를 탄력적 풀에서 이동 하 고 단일 데이터베이스의 성능 수준으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-111">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="eb8b9-112">예제의</span><span class="sxs-lookup"><span data-stu-id="eb8b9-112">EXAMPLES</span></span>

### <span data-ttu-id="eb8b9-113">예제 1: 데이터베이스를 표준 S2 데이터베이스로 업데이트</span><span class="sxs-lookup"><span data-stu-id="eb8b9-113">Example 1: Update a database to a Standard S2 database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S2"
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
CurrentServiceObjectiveName   : S2
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="eb8b9-114">이 명령은 Database01 이라는 데이터베이스를 Server01 라는 서버의 표준 S2 데이터베이스로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-114">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="eb8b9-115">예제 2: 탄력적 풀에 데이터베이스 추가</span><span class="sxs-lookup"><span data-stu-id="eb8b9-115">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="eb8b9-116">이 명령은 Database01 이라는 데이터베이스를 Server01 이라는 서버에서 호스팅된 ElasticPool01 이라는 탄력적 풀에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-116">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="eb8b9-117">예제 3: 데이터베이스의 저장소 최대 크기 수정</span><span class="sxs-lookup"><span data-stu-id="eb8b9-117">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
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

<span data-ttu-id="eb8b9-118">이 명령은 Database01 이라는 데이터베이스를 업데이트 하 여 최대 크기를 1TB로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-118">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="eb8b9-119">변수</span><span class="sxs-lookup"><span data-stu-id="eb8b9-119">PARAMETERS</span></span>

### <span data-ttu-id="eb8b9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb8b9-120">-AsJob</span></span>
<span data-ttu-id="eb8b9-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="eb8b9-121">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eb8b9-122">-DatabaseName</span></span>
<span data-ttu-id="eb8b9-123">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-123">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb8b9-124">-DefaultProfile</span></span>
<span data-ttu-id="eb8b9-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="eb8b9-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-126">-에디션</span><span class="sxs-lookup"><span data-stu-id="eb8b9-126">-Edition</span></span>
<span data-ttu-id="eb8b9-127">데이터베이스의 에디션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-127">Specifies the edition for the database.</span></span>
<span data-ttu-id="eb8b9-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eb8b9-129">않아야</span><span class="sxs-lookup"><span data-stu-id="eb8b9-129">None</span></span>
- <span data-ttu-id="eb8b9-130">Premium</span><span class="sxs-lookup"><span data-stu-id="eb8b9-130">Premium</span></span>
- <span data-ttu-id="eb8b9-131">기본적</span><span class="sxs-lookup"><span data-stu-id="eb8b9-131">Basic</span></span>
- <span data-ttu-id="eb8b9-132">표준이</span><span class="sxs-lookup"><span data-stu-id="eb8b9-132">Standard</span></span>
- <span data-ttu-id="eb8b9-133">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="eb8b9-133">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: Update
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-134">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="eb8b9-134">-ElasticPoolName</span></span>
<span data-ttu-id="eb8b9-135">데이터베이스를 이동할 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-135">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-136">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="eb8b9-136">-MaxSizeBytes</span></span>
<span data-ttu-id="eb8b9-137">Azure SQL 데이터베이스의 최대 크기 (바이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-137">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-138">-NewName</span><span class="sxs-lookup"><span data-stu-id="eb8b9-138">-NewName</span></span>
<span data-ttu-id="eb8b9-139">데이터베이스 이름을 바꿀 새 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-139">The new name to rename the database to.</span></span>

```yaml
Type: String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-140">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="eb8b9-140">-ReadScale</span></span>
<span data-ttu-id="eb8b9-141">Azure SQL 데이터베이스에 할당할 읽기 배율 옵션입니다. (사용/사용 안 함)</span><span class="sxs-lookup"><span data-stu-id="eb8b9-141">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: DatabaseReadScale
Parameter Sets: Update
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-142">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="eb8b9-142">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="eb8b9-143">데이터베이스에 할당할 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-143">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="eb8b9-144">서비스 목표에 대 한 자세한 내용은 Microsoft 개발자 네트워크 라이브러리의 [AZURE SQL 데이터베이스 서비스 계층 및 성능 수준을](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-144">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb8b9-145">-ResourceGroupName</span></span>
<span data-ttu-id="eb8b9-146">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-146">Specifies the name of resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eb8b9-147">-ServerName</span></span>
<span data-ttu-id="eb8b9-148">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-148">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-149">태그</span><span class="sxs-lookup"><span data-stu-id="eb8b9-149">-Tags</span></span>
<span data-ttu-id="eb8b9-150">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-150">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="eb8b9-151">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="eb8b9-151">For example:</span></span>

<span data-ttu-id="eb8b9-152">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="eb8b9-152">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: Update
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-153">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="eb8b9-153">-ZoneRedundant</span></span>
<span data-ttu-id="eb8b9-154">Azure Sql Database와 연결 되는 영역 중복성</span><span class="sxs-lookup"><span data-stu-id="eb8b9-154">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-155">-확인</span><span class="sxs-lookup"><span data-stu-id="eb8b9-155">-Confirm</span></span>
<span data-ttu-id="eb8b9-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb8b9-157">-WhatIf</span></span>
<span data-ttu-id="eb8b9-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb8b9-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb8b9-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb8b9-160">CommonParameters</span></span>
<span data-ttu-id="eb8b9-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb8b9-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb8b9-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb8b9-163">입력</span><span class="sxs-lookup"><span data-stu-id="eb8b9-163">INPUTS</span></span>

### <span data-ttu-id="eb8b9-164">않아야</span><span class="sxs-lookup"><span data-stu-id="eb8b9-164">None</span></span>
<span data-ttu-id="eb8b9-165">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb8b9-166">출력</span><span class="sxs-lookup"><span data-stu-id="eb8b9-166">OUTPUTS</span></span>

### <span data-ttu-id="eb8b9-167">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="eb8b9-167">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="eb8b9-168">상속자</span><span class="sxs-lookup"><span data-stu-id="eb8b9-168">NOTES</span></span>

## <span data-ttu-id="eb8b9-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb8b9-169">RELATED LINKS</span></span>

[<span data-ttu-id="eb8b9-170">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eb8b9-170">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="eb8b9-171">새로운 AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eb8b9-171">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="eb8b9-172">제거-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eb8b9-172">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="eb8b9-173">이력서-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eb8b9-173">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="eb8b9-174">일시 중단-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eb8b9-174">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="eb8b9-175">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="eb8b9-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
