---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
ms.openlocfilehash: c1be1a730c9e93778f9632477234d375813708dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528788"
---
# <span data-ttu-id="606ff-101">Get-AzureRmSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="606ff-101">Get-AzureRmSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="606ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="606ff-102">SYNOPSIS</span></span>
<span data-ttu-id="606ff-103">데이터베이스에 대 한 가격 계층 힌트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="606ff-103">Gets pricing tier hints for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="606ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="606ff-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="606ff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="606ff-105">DESCRIPTION</span></span>
<span data-ttu-id="606ff-106">**AzureRmSqlDatabaseUpgradeHint** Cmdlet은 Azure SQL 데이터베이스 업그레이드에 대 한 가격 계층 힌트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="606ff-106">The **Get-AzureRmSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="606ff-107">웹 및 비즈니스 가격 책정 계층에 남아 있는 데이터베이스는 새로운 기본, 표준 또는 프리미엄 가격 책정 계층으로 업그레이드 하는 힌트를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="606ff-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>

<span data-ttu-id="606ff-108">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="606ff-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="606ff-109">예제의</span><span class="sxs-lookup"><span data-stu-id="606ff-109">EXAMPLES</span></span>

### <span data-ttu-id="606ff-110">예제 1: 서버의 모든 데이터베이스에 대 한 권장 사항 보기</span><span class="sxs-lookup"><span data-stu-id="606ff-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="606ff-111">이 명령은 Server01 이라는 서버의 모든 데이터베이스에 대 한 업그레이드 힌트를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="606ff-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="606ff-112">예제 2: 특정 데이터베이스에 대 한 권장 사항 보기</span><span class="sxs-lookup"><span data-stu-id="606ff-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="606ff-113">이 명령은 특정 데이터베이스에 대 한 업그레이드 힌트를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="606ff-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="606ff-114">예제 3: 탄력적 데이터베이스 풀에 없는 모든 데이터베이스에 대 한 권장 사항 가져오기</span><span class="sxs-lookup"><span data-stu-id="606ff-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="606ff-115">이 명령은 탄력적 데이터베이스 풀에 없는 모든 데이터베이스에 대 한 업그레이드 힌트를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="606ff-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

## <span data-ttu-id="606ff-116">변수</span><span class="sxs-lookup"><span data-stu-id="606ff-116">PARAMETERS</span></span>

### <span data-ttu-id="606ff-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="606ff-117">-DatabaseName</span></span>
<span data-ttu-id="606ff-118">이 cmdlet이 업그레이드 힌트를 가져오는 SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="606ff-118">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="606ff-119">데이터베이스를 지정 하지 않으면이 cmdlet은 논리 서버의 모든 데이터베이스에 대 한 힌트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="606ff-119">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="606ff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="606ff-120">-DefaultProfile</span></span>
<span data-ttu-id="606ff-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="606ff-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="606ff-122">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="606ff-122">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="606ff-123">탄력적 데이터베이스 풀의 데이터베이스가 반환 된 권장 사항에서 제외 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="606ff-123">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="606ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="606ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="606ff-125">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="606ff-125">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="606ff-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="606ff-126">-ServerName</span></span>
<span data-ttu-id="606ff-127">이 cmdlet이 업그레이드 힌트를 가져오는 데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="606ff-127">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="606ff-128">-확인</span><span class="sxs-lookup"><span data-stu-id="606ff-128">-Confirm</span></span>
<span data-ttu-id="606ff-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="606ff-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="606ff-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="606ff-130">-WhatIf</span></span>
<span data-ttu-id="606ff-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="606ff-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="606ff-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="606ff-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="606ff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="606ff-133">CommonParameters</span></span>
<span data-ttu-id="606ff-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="606ff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="606ff-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="606ff-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="606ff-136">입력</span><span class="sxs-lookup"><span data-stu-id="606ff-136">INPUTS</span></span>

### <span data-ttu-id="606ff-137">않아야</span><span class="sxs-lookup"><span data-stu-id="606ff-137">None</span></span>
<span data-ttu-id="606ff-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="606ff-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="606ff-139">출력</span><span class="sxs-lookup"><span data-stu-id="606ff-139">OUTPUTS</span></span>

## <span data-ttu-id="606ff-140">상속자</span><span class="sxs-lookup"><span data-stu-id="606ff-140">NOTES</span></span>

## <span data-ttu-id="606ff-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="606ff-141">RELATED LINKS</span></span>

[<span data-ttu-id="606ff-142">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="606ff-142">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="606ff-143">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="606ff-143">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)


