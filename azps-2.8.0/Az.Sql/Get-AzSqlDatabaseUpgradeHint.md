---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: adf689396930b57b18c53d5ac6d98478ab6f952a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873689"
---
# <span data-ttu-id="450a0-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="450a0-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="450a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="450a0-102">SYNOPSIS</span></span>
<span data-ttu-id="450a0-103">데이터베이스에 대 한 가격 계층 힌트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="450a0-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="450a0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="450a0-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="450a0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="450a0-105">DESCRIPTION</span></span>
<span data-ttu-id="450a0-106">**AzSqlDatabaseUpgradeHint** Cmdlet은 Azure SQL 데이터베이스 업그레이드에 대 한 가격 계층 힌트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="450a0-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="450a0-107">웹 및 비즈니스 가격 책정 계층에 남아 있는 데이터베이스는 새로운 기본, 표준 또는 프리미엄 가격 책정 계층으로 업그레이드 하는 힌트를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="450a0-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="450a0-108">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="450a0-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="450a0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="450a0-109">EXAMPLES</span></span>

### <span data-ttu-id="450a0-110">예제 1: 서버의 모든 데이터베이스에 대 한 권장 사항 보기</span><span class="sxs-lookup"><span data-stu-id="450a0-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="450a0-111">이 명령은 Server01 이라는 서버의 모든 데이터베이스에 대 한 업그레이드 힌트를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="450a0-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="450a0-112">예제 2: 특정 데이터베이스에 대 한 권장 사항 보기</span><span class="sxs-lookup"><span data-stu-id="450a0-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="450a0-113">이 명령은 특정 데이터베이스에 대 한 업그레이드 힌트를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="450a0-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="450a0-114">예제 3: 탄력적 데이터베이스 풀에 없는 모든 데이터베이스에 대 한 권장 사항 가져오기</span><span class="sxs-lookup"><span data-stu-id="450a0-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="450a0-115">이 명령은 탄력적 데이터베이스 풀에 없는 모든 데이터베이스에 대 한 업그레이드 힌트를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="450a0-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="450a0-116">예제 4: 필터링을 사용 하 여 서버의 모든 데이터베이스에 대 한 권장 사항 보기</span><span class="sxs-lookup"><span data-stu-id="450a0-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="450a0-117">이 명령은 "Database"로 시작 하는 Server01 이라는 서버의 모든 데이터베이스에 대 한 업그레이드 힌트를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="450a0-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="450a0-118">변수</span><span class="sxs-lookup"><span data-stu-id="450a0-118">PARAMETERS</span></span>

### <span data-ttu-id="450a0-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="450a0-119">-DatabaseName</span></span>
<span data-ttu-id="450a0-120">이 cmdlet이 업그레이드 힌트를 가져오는 SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="450a0-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="450a0-121">데이터베이스를 지정 하지 않으면이 cmdlet은 논리 서버의 모든 데이터베이스에 대 한 힌트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="450a0-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="450a0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="450a0-122">-DefaultProfile</span></span>
<span data-ttu-id="450a0-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="450a0-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="450a0-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="450a0-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="450a0-125">탄력적 데이터베이스 풀의 데이터베이스가 반환 된 권장 사항에서 제외 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="450a0-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="450a0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="450a0-126">-ResourceGroupName</span></span>
<span data-ttu-id="450a0-127">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="450a0-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="450a0-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="450a0-128">-ServerName</span></span>
<span data-ttu-id="450a0-129">이 cmdlet이 업그레이드 힌트를 가져오는 데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="450a0-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="450a0-130">-확인</span><span class="sxs-lookup"><span data-stu-id="450a0-130">-Confirm</span></span>
<span data-ttu-id="450a0-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="450a0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="450a0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="450a0-132">-WhatIf</span></span>
<span data-ttu-id="450a0-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="450a0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="450a0-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="450a0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="450a0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450a0-135">CommonParameters</span></span>
<span data-ttu-id="450a0-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="450a0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450a0-137">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="450a0-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450a0-138">입력</span><span class="sxs-lookup"><span data-stu-id="450a0-138">INPUTS</span></span>

### <span data-ttu-id="450a0-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="450a0-139">System.String</span></span>

### <span data-ttu-id="450a0-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="450a0-140">System.Boolean</span></span>

## <span data-ttu-id="450a0-141">출력</span><span class="sxs-lookup"><span data-stu-id="450a0-141">OUTPUTS</span></span>

### <span data-ttu-id="450a0-142">LegacySdk. RecommendedDatabaseProperties를 모두 보세요.</span><span class="sxs-lookup"><span data-stu-id="450a0-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="450a0-143">상속자</span><span class="sxs-lookup"><span data-stu-id="450a0-143">NOTES</span></span>

## <span data-ttu-id="450a0-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="450a0-144">RELATED LINKS</span></span>

[<span data-ttu-id="450a0-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="450a0-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="450a0-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="450a0-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)


