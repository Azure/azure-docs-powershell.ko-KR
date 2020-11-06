---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: b23128d2ef55e971f20569e251601b410b218ec2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524815"
---
# <span data-ttu-id="b5ef0-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b5ef0-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="b5ef0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ef0-103">기존 데이터베이스에 대 한 보조 데이터베이스를 만들고 데이터 복제를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5ef0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5ef0-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5ef0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b5ef0-105">DESCRIPTION</span></span>
<span data-ttu-id="b5ef0-106">데이터베이스에 대 한 지리적 복제를 설정 하는 데 사용 되는 **AzureRMSqlDatabaseSecondary** cmdlet은 Start-AzureSqlDatabaseCopy cmdlet을 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-106">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="b5ef0-107">기본 데이터베이스에서 보조 데이터베이스로 지역 복제 링크 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-107">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="b5ef0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b5ef0-108">EXAMPLES</span></span>

### <span data-ttu-id="b5ef0-109">1: 활성 Geo-Replication 설정</span><span class="sxs-lookup"><span data-stu-id="b5ef0-109">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="b5ef0-110">변수</span><span class="sxs-lookup"><span data-stu-id="b5ef0-110">PARAMETERS</span></span>

### <span data-ttu-id="b5ef0-111">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="b5ef0-111">-AllowConnections</span></span>
<span data-ttu-id="b5ef0-112">보조 Azure SQL 데이터베이스의 읽기 의도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-112">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="b5ef0-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5ef0-114">아니요</span><span class="sxs-lookup"><span data-stu-id="b5ef0-114">No</span></span>
- <span data-ttu-id="b5ef0-115">모든</span><span class="sxs-lookup"><span data-stu-id="b5ef0-115">All</span></span>

```yaml
Type: AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ef0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5ef0-116">-AsJob</span></span>
<span data-ttu-id="b5ef0-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b5ef0-117">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="b5ef0-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b5ef0-118">-DatabaseName</span></span>
<span data-ttu-id="b5ef0-119">기본 역할을 할 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-119">Specifies the name of the database to act as primary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ef0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ef0-120">-DefaultProfile</span></span>
<span data-ttu-id="b5ef0-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b5ef0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5ef0-122">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5ef0-122">-PartnerResourceGroupName</span></span>
<span data-ttu-id="b5ef0-123">이 cmdlet이 보조 데이터베이스를 할당 하는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-123">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ef0-124">-(-)-(서버 이름)</span><span class="sxs-lookup"><span data-stu-id="b5ef0-124">-PartnerServerName</span></span>
<span data-ttu-id="b5ef0-125">보조 역할을 할 Azure SQL 데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-125">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ef0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5ef0-126">-ResourceGroupName</span></span>
<span data-ttu-id="b5ef0-127">이 cmdlet이 기본 데이터베이스를 할당 하는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="b5ef0-128">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b5ef0-128">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="b5ef0-129">보조 데이터베이스를 추가할 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-129">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ef0-130">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="b5ef0-130">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="b5ef0-131">보조 데이터베이스에 할당할 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-131">Specifies the name of the service objective to assign to the secondary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ef0-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b5ef0-132">-ServerName</span></span>
<span data-ttu-id="b5ef0-133">기본 SQL 데이터베이스의 SQL Server 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-133">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="b5ef0-134">태그</span><span class="sxs-lookup"><span data-stu-id="b5ef0-134">-Tags</span></span>
<span data-ttu-id="b5ef0-135">SQL 데이터베이스 복제 링크와 연결할 해시 테이블 형태의 키-값 쌍을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-135">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="b5ef0-136">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="b5ef0-136">For example:</span></span>

<span data-ttu-id="b5ef0-137">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b5ef0-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ef0-138">-확인</span><span class="sxs-lookup"><span data-stu-id="b5ef0-138">-Confirm</span></span>
<span data-ttu-id="b5ef0-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5ef0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5ef0-140">-WhatIf</span></span>
<span data-ttu-id="b5ef0-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5ef0-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5ef0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ef0-143">CommonParameters</span></span>
<span data-ttu-id="b5ef0-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ef0-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5ef0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ef0-146">입력</span><span class="sxs-lookup"><span data-stu-id="b5ef0-146">INPUTS</span></span>

### <span data-ttu-id="b5ef0-147">않아야</span><span class="sxs-lookup"><span data-stu-id="b5ef0-147">None</span></span>
<span data-ttu-id="b5ef0-148">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b5ef0-149">출력</span><span class="sxs-lookup"><span data-stu-id="b5ef0-149">OUTPUTS</span></span>

### <span data-ttu-id="b5ef0-150">AzureReplicationLinkModel를 통해 서의.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-150">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>
<span data-ttu-id="b5ef0-151">이 cmdlet은 **ReplicationLink** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5ef0-151">This cmdlet returns **ReplicationLink** objects.</span></span>

## <span data-ttu-id="b5ef0-152">상속자</span><span class="sxs-lookup"><span data-stu-id="b5ef0-152">NOTES</span></span>

## <span data-ttu-id="b5ef0-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5ef0-153">RELATED LINKS</span></span>

[<span data-ttu-id="b5ef0-154">제거-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b5ef0-154">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="b5ef0-155">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b5ef0-155">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="b5ef0-156">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="b5ef0-156">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
