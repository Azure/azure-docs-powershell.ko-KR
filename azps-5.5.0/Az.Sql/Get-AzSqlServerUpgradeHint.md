---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
ms.openlocfilehash: 841de793c6e0c6d9213be262576dbd4f407fd947
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201473"
---
# <span data-ttu-id="8e827-101">Get-AzSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="8e827-101">Get-AzSqlServerUpgradeHint</span></span>

## <span data-ttu-id="8e827-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e827-102">SYNOPSIS</span></span>
<span data-ttu-id="8e827-103">Azure SQL Database 서버를 업그레이드하기 위한 가격 책정 계층 힌트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8e827-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

## <span data-ttu-id="8e827-104">구문</span><span class="sxs-lookup"><span data-stu-id="8e827-104">SYNTAX</span></span>

```
Get-AzSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e827-105">설명</span><span class="sxs-lookup"><span data-stu-id="8e827-105">DESCRIPTION</span></span>
<span data-ttu-id="8e827-106">**Get-AzSqlServerUpgradeHint** cmdlet은 Azure SQL 데이터베이스 서버를 업그레이드하기 위한 가격 책정 계층 힌트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8e827-106">The **Get-AzSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="8e827-107">힌트에는 탄력적 데이터베이스 풀 및 독립 실행형 데이터베이스 힌트가 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8e827-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="8e827-108">Web 및 Business 가격 책정 계층에 있는 데이터베이스는 새 기본, 표준 또는 프리미엄 가격 책정 계층으로 업그레이드하거나 탄력적 데이터베이스 풀로 이동하는 힌트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8e827-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="8e827-109">이 cmdlet은 지정된 서버에 호스트되는 모든 데이터베이스에 대한 힌트를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8e827-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="8e827-110">예제</span><span class="sxs-lookup"><span data-stu-id="8e827-110">EXAMPLES</span></span>

### <span data-ttu-id="8e827-111">예제 1: 결합된 권장 사항 얻기</span><span class="sxs-lookup"><span data-stu-id="8e827-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="8e827-112">이 명령은 Server01이라는 서버의 모든 데이터베이스에 대한 결합된 권장 사항을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8e827-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="8e827-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e827-113">PARAMETERS</span></span>

### <span data-ttu-id="8e827-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e827-114">-DefaultProfile</span></span>
<span data-ttu-id="8e827-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8e827-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e827-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="8e827-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="8e827-117">탄력적 데이터베이스 풀에 포함된 데이터베이스를 반환해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8e827-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="8e827-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e827-118">-ResourceGroupName</span></span>
<span data-ttu-id="8e827-119">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8e827-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="8e827-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8e827-120">-ServerName</span></span>
<span data-ttu-id="8e827-121">이 cmdlet이 업그레이드 힌트를 얻을 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8e827-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="8e827-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e827-122">-Confirm</span></span>
<span data-ttu-id="8e827-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8e827-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e827-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e827-124">-WhatIf</span></span>
<span data-ttu-id="8e827-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8e827-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e827-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e827-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e827-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e827-127">CommonParameters</span></span>
<span data-ttu-id="8e827-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8e827-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e827-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8e827-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e827-130">입력</span><span class="sxs-lookup"><span data-stu-id="8e827-130">INPUTS</span></span>

### <span data-ttu-id="8e827-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8e827-131">System.String</span></span>

### <span data-ttu-id="8e827-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8e827-132">System.Boolean</span></span>

## <span data-ttu-id="8e827-133">출력</span><span class="sxs-lookup"><span data-stu-id="8e827-133">OUTPUTS</span></span>

### <span data-ttu-id="8e827-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="8e827-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="8e827-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8e827-135">NOTES</span></span>

## <span data-ttu-id="8e827-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e827-136">RELATED LINKS</span></span>

[<span data-ttu-id="8e827-137">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="8e827-137">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="8e827-138">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="8e827-138">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

[<span data-ttu-id="8e827-139">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="8e827-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


