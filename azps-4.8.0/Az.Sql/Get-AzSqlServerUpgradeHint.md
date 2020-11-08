---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
ms.openlocfilehash: 841de793c6e0c6d9213be262576dbd4f407fd947
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048664"
---
# <span data-ttu-id="61287-101">Get-AzSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="61287-101">Get-AzSqlServerUpgradeHint</span></span>

## <span data-ttu-id="61287-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61287-102">SYNOPSIS</span></span>
<span data-ttu-id="61287-103">Azure SQL 데이터베이스 서버 업그레이드에 대 한 가격 책정 계층 힌트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="61287-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

## <span data-ttu-id="61287-104">구문과</span><span class="sxs-lookup"><span data-stu-id="61287-104">SYNTAX</span></span>

```
Get-AzSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61287-105">설명은</span><span class="sxs-lookup"><span data-stu-id="61287-105">DESCRIPTION</span></span>
<span data-ttu-id="61287-106">**AzSqlServerUpgradeHint** Cmdlet은 Azure SQL 데이터베이스 서버를 업그레이드 하기 위한 가격 계층 힌트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="61287-106">The **Get-AzSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="61287-107">힌트에는 탄력적 데이터베이스 풀 및 독립 실행형 데이터베이스 힌트가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="61287-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="61287-108">웹 및 비즈니스 가격 책정 계층에 남아 있는 데이터베이스에는 새 기본, 표준 또는 프리미엄 가격 책정 계층으로 업그레이드 하거나 탄력적 데이터베이스 풀로 이동 하는 힌트가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="61287-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="61287-109">이 cmdlet은 지정 된 서버에서 호스팅되는 모든 데이터베이스에 대 한 힌트를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="61287-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="61287-110">예제의</span><span class="sxs-lookup"><span data-stu-id="61287-110">EXAMPLES</span></span>

### <span data-ttu-id="61287-111">예제 1: 통합 권장 구성 가져오기</span><span class="sxs-lookup"><span data-stu-id="61287-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="61287-112">이 명령은 Server01 이라는 서버의 모든 데이터베이스에 대해 권장 되는 추천 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="61287-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="61287-113">변수</span><span class="sxs-lookup"><span data-stu-id="61287-113">PARAMETERS</span></span>

### <span data-ttu-id="61287-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61287-114">-DefaultProfile</span></span>
<span data-ttu-id="61287-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="61287-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61287-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="61287-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="61287-117">탄력적 데이터베이스 풀에 포함 된 데이터베이스를 반환 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="61287-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="61287-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61287-118">-ResourceGroupName</span></span>
<span data-ttu-id="61287-119">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61287-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="61287-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="61287-120">-ServerName</span></span>
<span data-ttu-id="61287-121">이 cmdlet이 업그레이드 힌트를 가져오는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="61287-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="61287-122">-확인</span><span class="sxs-lookup"><span data-stu-id="61287-122">-Confirm</span></span>
<span data-ttu-id="61287-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="61287-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61287-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61287-124">-WhatIf</span></span>
<span data-ttu-id="61287-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="61287-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61287-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61287-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61287-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61287-127">CommonParameters</span></span>
<span data-ttu-id="61287-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="61287-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61287-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="61287-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61287-130">입력</span><span class="sxs-lookup"><span data-stu-id="61287-130">INPUTS</span></span>

### <span data-ttu-id="61287-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="61287-131">System.String</span></span>

### <span data-ttu-id="61287-132">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="61287-132">System.Boolean</span></span>

## <span data-ttu-id="61287-133">출력</span><span class="sxs-lookup"><span data-stu-id="61287-133">OUTPUTS</span></span>

### <span data-ttu-id="61287-134">ServiceTierAdvisor를 통해 UpgradeServerHint를 자동으로</span><span class="sxs-lookup"><span data-stu-id="61287-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="61287-135">상속자</span><span class="sxs-lookup"><span data-stu-id="61287-135">NOTES</span></span>

## <span data-ttu-id="61287-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61287-136">RELATED LINKS</span></span>

[<span data-ttu-id="61287-137">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="61287-137">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="61287-138">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="61287-138">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

[<span data-ttu-id="61287-139">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="61287-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


