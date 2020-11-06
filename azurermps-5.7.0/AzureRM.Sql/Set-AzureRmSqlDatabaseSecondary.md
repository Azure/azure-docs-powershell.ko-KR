---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 2c1853de6eb11c304014ac45b5469c5699105824
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528739"
---
# <span data-ttu-id="a854c-101">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a854c-101">Set-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="a854c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a854c-102">SYNOPSIS</span></span>
<span data-ttu-id="a854c-103">장애 조치를 시작 하기 위해 보조 데이터베이스를 기본으로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a854c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a854c-104">SYNTAX</span></span>

### <span data-ttu-id="a854c-105">No옵션 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a854c-105">NoOptionsSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a854c-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="a854c-106">ByFailoverParams</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a854c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a854c-107">DESCRIPTION</span></span>
<span data-ttu-id="a854c-108">**AzureRmSqlDatabaseSecondary** cmdlet은 장애 조치를 시작 하기 위해 보조 데이터베이스를 기본으로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-108">The **Set-AzureRmSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="a854c-109">이 cmdlet은 일반 구성 명령으로 설계 되었지만 현재 장애 조치 (failover)를 시작 하도록 제한 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="a854c-110">중단 하는 동안 강제 장애 조치를 시작 하는 *AllowDataLoss* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="a854c-111">복구 드릴 등 계획 된 작업을 수행할 때이 매개 변수를 지정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="a854c-112">후자의 경우 보조 데이터베이스는 전환 되기 전에 기본을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="a854c-113">예제의</span><span class="sxs-lookup"><span data-stu-id="a854c-113">EXAMPLES</span></span>

## <span data-ttu-id="a854c-114">변수</span><span class="sxs-lookup"><span data-stu-id="a854c-114">PARAMETERS</span></span>

### <span data-ttu-id="a854c-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="a854c-115">-AllowDataLoss</span></span>
<span data-ttu-id="a854c-116">이 장애 조치 (failover) 작업으로 데이터 손실이 허용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-116">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a854c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a854c-117">-AsJob</span></span>
<span data-ttu-id="a854c-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a854c-118">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="a854c-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a854c-119">-DatabaseName</span></span>
<span data-ttu-id="a854c-120">Azure SQL 데이터베이스 보조의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-120">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="a854c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a854c-121">-DefaultProfile</span></span>
<span data-ttu-id="a854c-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a854c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a854c-123">-장애 조치</span><span class="sxs-lookup"><span data-stu-id="a854c-123">-Failover</span></span>
<span data-ttu-id="a854c-124">이 작업이 장애 조치 (failover) 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-124">Indicates that this operation is a failover.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a854c-125">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a854c-125">-PartnerResourceGroupName</span></span>
<span data-ttu-id="a854c-126">파트너 Azure SQL 데이터베이스가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-126">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="a854c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a854c-127">-ResourceGroupName</span></span>
<span data-ttu-id="a854c-128">Azure SQL 데이터베이스 보조를 할당 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-128">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="a854c-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a854c-129">-ServerName</span></span>
<span data-ttu-id="a854c-130">Azure SQL 데이터베이스 보조를 호스트 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-130">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="a854c-131">-확인</span><span class="sxs-lookup"><span data-stu-id="a854c-131">-Confirm</span></span>
<span data-ttu-id="a854c-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a854c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a854c-133">-WhatIf</span></span>
<span data-ttu-id="a854c-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a854c-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a854c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a854c-136">CommonParameters</span></span>
<span data-ttu-id="a854c-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a854c-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a854c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a854c-139">입력</span><span class="sxs-lookup"><span data-stu-id="a854c-139">INPUTS</span></span>

###  
<span data-ttu-id="a854c-140">보조 데이터베이스에 대해 **데이터베이스** 개체의 인스턴스를 파이프 하 여이 cmdlet에 대 한 주 데이터베이스를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-140">You can pipe instances of the **Database** object for the secondary database to fail over and make the primary database to this cmdlet.</span></span>

## <span data-ttu-id="a854c-141">출력</span><span class="sxs-lookup"><span data-stu-id="a854c-141">OUTPUTS</span></span>

###  
<span data-ttu-id="a854c-142">이 cmdlet은 **ReplicationLink** 를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a854c-142">This cmdlet returns a **ReplicationLink**.</span></span>

## <span data-ttu-id="a854c-143">상속자</span><span class="sxs-lookup"><span data-stu-id="a854c-143">NOTES</span></span>

## <span data-ttu-id="a854c-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a854c-144">RELATED LINKS</span></span>

[<span data-ttu-id="a854c-145">새로운 AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a854c-145">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="a854c-146">제거-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a854c-146">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="a854c-147">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="a854c-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
