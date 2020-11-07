---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: 3d36c94ebcc1b733559f9fb4075fb20e4ec67144
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702677"
---
# <span data-ttu-id="260eb-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="260eb-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="260eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="260eb-102">SYNOPSIS</span></span>
<span data-ttu-id="260eb-103">데이터베이스의 속성을 설정 하거나 기존 데이터베이스를 탄력적인 풀로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="260eb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="260eb-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="260eb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="260eb-105">DESCRIPTION</span></span>
<span data-ttu-id="260eb-106">**Set-AzureRmSqlDatabase** Cmdlet은 Azure SQL 데이터베이스의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-106">The **Set-AzureRmSqlDatabase** cmdlet sets properties for an Azure SQL database.</span></span>
<span data-ttu-id="260eb-107">또한 *ElasticPoolName* 매개 변수를 지정 하 여 데이터베이스를 탄력적인 풀로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-107">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span>
<span data-ttu-id="260eb-108">탄력적 풀에 데이터베이스가 이미 있는 경우 *RequestedServiceObjectiveName* 매개 변수를 사용 하 여 성능 수준을 할당할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-108">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to assign a performance level.</span></span>

## <span data-ttu-id="260eb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="260eb-109">EXAMPLES</span></span>

### <span data-ttu-id="260eb-110">예제 1: 데이터베이스를 표준 S2 데이터베이스로 업데이트</span><span class="sxs-lookup"><span data-stu-id="260eb-110">Example 1: Update a database to a Standard S2 database</span></span>
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

<span data-ttu-id="260eb-111">이 명령은 Database01 이라는 데이터베이스를 Server01 라는 서버의 표준 S2 데이터베이스로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-111">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="260eb-112">예제 2: 탄력적 풀에 데이터베이스 추가</span><span class="sxs-lookup"><span data-stu-id="260eb-112">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="260eb-113">이 명령은 Database01 이라는 데이터베이스를 Server01 이라는 서버에서 호스팅된 ElasticPool01 이라는 탄력적 풀에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-113">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

## <span data-ttu-id="260eb-114">변수</span><span class="sxs-lookup"><span data-stu-id="260eb-114">PARAMETERS</span></span>

### <span data-ttu-id="260eb-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="260eb-115">-DatabaseName</span></span>
<span data-ttu-id="260eb-116">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-116">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="260eb-117">-에디션</span><span class="sxs-lookup"><span data-stu-id="260eb-117">-Edition</span></span>
<span data-ttu-id="260eb-118">데이터베이스의 에디션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-118">Specifies the edition for the database.</span></span>
<span data-ttu-id="260eb-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="260eb-120">않아야</span><span class="sxs-lookup"><span data-stu-id="260eb-120">None</span></span>
- <span data-ttu-id="260eb-121">Premium</span><span class="sxs-lookup"><span data-stu-id="260eb-121">Premium</span></span>
- <span data-ttu-id="260eb-122">기본적</span><span class="sxs-lookup"><span data-stu-id="260eb-122">Basic</span></span>
- <span data-ttu-id="260eb-123">표준이</span><span class="sxs-lookup"><span data-stu-id="260eb-123">Standard</span></span>
- <span data-ttu-id="260eb-124">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="260eb-124">DataWarehouse</span></span>
- <span data-ttu-id="260eb-125">비우거나</span><span class="sxs-lookup"><span data-stu-id="260eb-125">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="260eb-126">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="260eb-126">-ElasticPoolName</span></span>
<span data-ttu-id="260eb-127">데이터베이스를 이동할 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-127">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="260eb-128">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="260eb-128">-MaxSizeBytes</span></span>
<span data-ttu-id="260eb-129">데이터베이스의 새로운 최대 크기 (바이트)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-129">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="260eb-130">이 매개 변수 또는 *Maxsizegb* 중 하나를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-130">You can specify either this parameter or *MaxSizeGB*.</span></span>
<span data-ttu-id="260eb-131">*Maxsizegb* 매개 변수는 에디션에 허용 되는 값을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="260eb-131">See the *MaxSizeGB* parameter for acceptable values per edition.</span></span>

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

### <span data-ttu-id="260eb-132">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="260eb-132">-ReadScale</span></span>
<span data-ttu-id="260eb-133">Azure SQL 데이터베이스에 할당할 읽기 배율 옵션입니다. (사용/사용 안 함)</span><span class="sxs-lookup"><span data-stu-id="260eb-133">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="260eb-134">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="260eb-134">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="260eb-135">데이터베이스에 할당할 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-135">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="260eb-136">서비스 목표에 대 한 자세한 내용은 Microsoft 개발자 네트워크 라이브러리의 [AZURE SQL 데이터베이스 서비스 계층 및 성능 수준을](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="260eb-136">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="260eb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="260eb-137">-ResourceGroupName</span></span>
<span data-ttu-id="260eb-138">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-138">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="260eb-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="260eb-139">-ServerName</span></span>
<span data-ttu-id="260eb-140">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-140">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="260eb-141">태그</span><span class="sxs-lookup"><span data-stu-id="260eb-141">-Tags</span></span>
<span data-ttu-id="260eb-142">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-142">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="260eb-143">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="260eb-143">For example:</span></span>

<span data-ttu-id="260eb-144">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="260eb-144">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="260eb-145">-확인</span><span class="sxs-lookup"><span data-stu-id="260eb-145">-Confirm</span></span>
<span data-ttu-id="260eb-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="260eb-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="260eb-147">-WhatIf</span></span>
<span data-ttu-id="260eb-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="260eb-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="260eb-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="260eb-150">-DefaultProfile</span></span>
<span data-ttu-id="260eb-151">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="260eb-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="260eb-152">CommonParameters</span></span>
<span data-ttu-id="260eb-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="260eb-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="260eb-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="260eb-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="260eb-155">입력</span><span class="sxs-lookup"><span data-stu-id="260eb-155">INPUTS</span></span>

## <span data-ttu-id="260eb-156">출력</span><span class="sxs-lookup"><span data-stu-id="260eb-156">OUTPUTS</span></span>

### <span data-ttu-id="260eb-157">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="260eb-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="260eb-158">상속자</span><span class="sxs-lookup"><span data-stu-id="260eb-158">NOTES</span></span>

## <span data-ttu-id="260eb-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="260eb-159">RELATED LINKS</span></span>

[<span data-ttu-id="260eb-160">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="260eb-160">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="260eb-161">새로운 AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="260eb-161">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="260eb-162">제거-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="260eb-162">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="260eb-163">이력서-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="260eb-163">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="260eb-164">일시 중단-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="260eb-164">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="260eb-165">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="260eb-165">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
