---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: 9018dab5f09bbab6a3fb1197ee8aabd09141e664
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014672"
---
# <span data-ttu-id="224d4-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="224d4-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="224d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="224d4-102">SYNOPSIS</span></span>
<span data-ttu-id="224d4-103">데이터베이스에 대한 가격 책정 계층 힌트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="224d4-104">구문</span><span class="sxs-lookup"><span data-stu-id="224d4-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="224d4-105">설명</span><span class="sxs-lookup"><span data-stu-id="224d4-105">DESCRIPTION</span></span>
<span data-ttu-id="224d4-106">**Get-AzSqlDatabaseUpgradeHint** cmdlet은 Azure SQL 업그레이드하기 위한 가격 책정 계층 힌트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="224d4-107">웹 및 비즈니스 가격 책정 계층에 있는 데이터베이스는 새 기본, 표준 또는 프리미엄 가격 책정 계층으로 업그레이드할 힌트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="224d4-108">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="224d4-109">예제</span><span class="sxs-lookup"><span data-stu-id="224d4-109">EXAMPLES</span></span>

### <span data-ttu-id="224d4-110">예제 1: 서버의 모든 데이터베이스에 대한 권장 사항 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="224d4-111">이 명령은 Server01이라는 서버의 모든 데이터베이스에 대한 업그레이드 힌트를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="224d4-112">예제 2: 특정 데이터베이스에 대한 권장 사항 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="224d4-113">이 명령은 특정 데이터베이스에 대한 업그레이드 힌트를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="224d4-114">예제 3: 탄력적 데이터베이스 풀에 없는 모든 데이터베이스에 대한 권장 사항 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="224d4-115">이 명령은 탄력적 데이터베이스 풀에 없는 모든 데이터베이스에 대한 업그레이드 힌트를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="224d4-116">예제 4: 필터링을 사용하여 서버의 모든 데이터베이스에 대한 권장 사항 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="224d4-117">이 명령은 "Database"로 시작하는 Server01이라는 서버의 모든 데이터베이스에 대한 업그레이드 힌트를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="224d4-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="224d4-118">PARAMETERS</span></span>

### <span data-ttu-id="224d4-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="224d4-119">-DatabaseName</span></span>
<span data-ttu-id="224d4-120">이 cmdlet에서 업그레이드 힌트를 SQL 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="224d4-121">데이터베이스를 지정하지 않으면 이 cmdlet은 논리 서버의 모든 데이터베이스에 대한 힌트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="224d4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="224d4-122">-DefaultProfile</span></span>
<span data-ttu-id="224d4-123">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="224d4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="224d4-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="224d4-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="224d4-125">탄력적 데이터베이스 풀의 데이터베이스가 반환된 권장 사항에서 제외되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

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

### <span data-ttu-id="224d4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="224d4-126">-ResourceGroupName</span></span>
<span data-ttu-id="224d4-127">데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="224d4-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="224d4-128">-ServerName</span></span>
<span data-ttu-id="224d4-129">이 cmdlet에서 업그레이드 힌트를 얻을 데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="224d4-130">-확인</span><span class="sxs-lookup"><span data-stu-id="224d4-130">-Confirm</span></span>
<span data-ttu-id="224d4-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="224d4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="224d4-132">-WhatIf</span></span>
<span data-ttu-id="224d4-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="224d4-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="224d4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="224d4-135">CommonParameters</span></span>
<span data-ttu-id="224d4-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="224d4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="224d4-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="224d4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="224d4-138">입력</span><span class="sxs-lookup"><span data-stu-id="224d4-138">INPUTS</span></span>

### <span data-ttu-id="224d4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="224d4-139">System.String</span></span>

### <span data-ttu-id="224d4-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="224d4-140">System.Boolean</span></span>

## <span data-ttu-id="224d4-141">출력</span><span class="sxs-lookup"><span data-stu-id="224d4-141">OUTPUTS</span></span>

### <span data-ttu-id="224d4-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="224d4-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="224d4-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="224d4-143">NOTES</span></span>

## <span data-ttu-id="224d4-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="224d4-144">RELATED LINKS</span></span>

[<span data-ttu-id="224d4-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="224d4-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="224d4-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="224d4-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)


