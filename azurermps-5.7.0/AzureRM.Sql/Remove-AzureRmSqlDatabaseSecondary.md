---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: d326abcd7cc0aee627d56250ac63d68549be610d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533575"
---
# <span data-ttu-id="046d1-101">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="046d1-101">Remove-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="046d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="046d1-102">SYNOPSIS</span></span>
<span data-ttu-id="046d1-103">SQL 데이터베이스와 지정 된 보조 데이터베이스 간의 데이터 복제를 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="046d1-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="046d1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="046d1-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="046d1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="046d1-105">DESCRIPTION</span></span>
<span data-ttu-id="046d1-106">**AzureRmSqlDatabaseSecondary** cmdlet은 지리적 복제 링크를 강제로 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="046d1-106">The **Remove-AzureRmSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="046d1-107">이 cmdlet은 Stop-AzureSqlDatabaseCopy cmdlet을 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="046d1-107">This cmdlet replaces the Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="046d1-108">종료 하기 전에 복제 동기화가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="046d1-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="046d1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="046d1-109">EXAMPLES</span></span>

## <span data-ttu-id="046d1-110">변수</span><span class="sxs-lookup"><span data-stu-id="046d1-110">PARAMETERS</span></span>

### <span data-ttu-id="046d1-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="046d1-111">-DatabaseName</span></span>
<span data-ttu-id="046d1-112">이 cmdlet이 제거 하는 복제 링크가 있는 기본 Azure SQL 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="046d1-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="046d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="046d1-113">-DefaultProfile</span></span>
<span data-ttu-id="046d1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="046d1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="046d1-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="046d1-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="046d1-116">파트너 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="046d1-116">Specifies the name of the partner  resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046d1-117">-(-)-(서버 이름)</span><span class="sxs-lookup"><span data-stu-id="046d1-117">-PartnerServerName</span></span>
<span data-ttu-id="046d1-118">파트너 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="046d1-118">Specifies the name of the partner SQL Server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046d1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="046d1-119">-ResourceGroupName</span></span>
<span data-ttu-id="046d1-120">제거할 복제 링크와 연결 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="046d1-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="046d1-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="046d1-121">-ServerName</span></span>
<span data-ttu-id="046d1-122">제거할 복제 링크가 있는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="046d1-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="046d1-123">-확인</span><span class="sxs-lookup"><span data-stu-id="046d1-123">-Confirm</span></span>
<span data-ttu-id="046d1-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="046d1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="046d1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="046d1-125">-WhatIf</span></span>
<span data-ttu-id="046d1-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="046d1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="046d1-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="046d1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="046d1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="046d1-128">CommonParameters</span></span>
<span data-ttu-id="046d1-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="046d1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="046d1-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="046d1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="046d1-131">입력</span><span class="sxs-lookup"><span data-stu-id="046d1-131">INPUTS</span></span>

###  
<span data-ttu-id="046d1-132">Primary 또는 보조 데이터베이스용 **데이터베이스** 개체의 인스턴스를이 cmdlet으로 파이프 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="046d1-132">You can pipe instances of the **Database** object for the primary or secondary database to this cmdlet.</span></span>

## <span data-ttu-id="046d1-133">출력</span><span class="sxs-lookup"><span data-stu-id="046d1-133">OUTPUTS</span></span>

###  
<span data-ttu-id="046d1-134">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="046d1-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="046d1-135">상속자</span><span class="sxs-lookup"><span data-stu-id="046d1-135">NOTES</span></span>

## <span data-ttu-id="046d1-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="046d1-136">RELATED LINKS</span></span>

[<span data-ttu-id="046d1-137">새로운 AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="046d1-137">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="046d1-138">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="046d1-138">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="046d1-139">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="046d1-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
