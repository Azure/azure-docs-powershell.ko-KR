---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 9e0af4c5110fe0732782293eb9d8c67fb7d89600
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878842"
---
# <span data-ttu-id="f2f21-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f2f21-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="f2f21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2f21-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f21-103">장애 조치를 시작 하기 위해 보조 데이터베이스를 기본으로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2f21-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="f2f21-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2f21-104">SYNTAX</span></span>

### <span data-ttu-id="f2f21-105">No옵션 집합 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f2f21-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2f21-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="f2f21-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2f21-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f2f21-107">DESCRIPTION</span></span>
<span data-ttu-id="f2f21-108">**AzSqlDatabaseSecondary** cmdlet은 장애 조치를 시작 하기 위해 보조 데이터베이스를 기본으로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2f21-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="f2f21-109">이 cmdlet은 일반 구성 명령으로 설계 되었지만 현재 장애 조치 (failover)를 시작 하도록 제한 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2f21-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="f2f21-110">중단 하는 동안 강제 장애 조치를 시작 하는 *AllowDataLoss* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2f21-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="f2f21-111">복구 드릴 등 계획 된 작업을 수행할 때이 매개 변수를 지정할 필요가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f2f21-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="f2f21-112">후자의 경우 보조 데이터베이스는 전환 되기 전에 기본을 동기화 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2f21-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="f2f21-113">예제의</span><span class="sxs-lookup"><span data-stu-id="f2f21-113">EXAMPLES</span></span>

### <span data-ttu-id="f2f21-114">1: 계획 된 장애 조치 시작</span><span class="sxs-lookup"><span data-stu-id="f2f21-114">1: Initiate a planned failover</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="f2f21-115">2: 강제 장애 조치 시작 (잠재적인 데이터 손실)</span><span class="sxs-lookup"><span data-stu-id="f2f21-115">2: Initiate a forced failover (with potential data loss)</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="f2f21-116">변수</span><span class="sxs-lookup"><span data-stu-id="f2f21-116">PARAMETERS</span></span>

### <span data-ttu-id="f2f21-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="f2f21-117">-AllowDataLoss</span></span>
<span data-ttu-id="f2f21-118">이 장애 조치 (failover) 작업으로 데이터 손실이 허용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f2f21-118">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f21-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2f21-119">-AsJob</span></span>
<span data-ttu-id="f2f21-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f2f21-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f21-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f2f21-121">-DatabaseName</span></span>
<span data-ttu-id="f2f21-122">Azure SQL 데이터베이스 보조의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2f21-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f21-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f21-123">-DefaultProfile</span></span>
<span data-ttu-id="f2f21-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f2f21-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2f21-125">-장애 조치</span><span class="sxs-lookup"><span data-stu-id="f2f21-125">-Failover</span></span>
<span data-ttu-id="f2f21-126">이 작업이 장애 조치 (failover) 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f2f21-126">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f21-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2f21-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="f2f21-128">파트너 Azure SQL 데이터베이스가 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2f21-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f21-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2f21-129">-ResourceGroupName</span></span>
<span data-ttu-id="f2f21-130">Azure SQL 데이터베이스 보조를 할당 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2f21-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="f2f21-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f2f21-131">-ServerName</span></span>
<span data-ttu-id="f2f21-132">Azure SQL 데이터베이스 보조를 호스트 하는 SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2f21-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="f2f21-133">-확인</span><span class="sxs-lookup"><span data-stu-id="f2f21-133">-Confirm</span></span>
<span data-ttu-id="f2f21-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2f21-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2f21-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2f21-135">-WhatIf</span></span>
<span data-ttu-id="f2f21-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f2f21-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2f21-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2f21-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2f21-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f21-138">CommonParameters</span></span>
<span data-ttu-id="f2f21-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2f21-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f21-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f2f21-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f21-141">입력</span><span class="sxs-lookup"><span data-stu-id="f2f21-141">INPUTS</span></span>

### <span data-ttu-id="f2f21-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f2f21-142">System.String</span></span>

## <span data-ttu-id="f2f21-143">출력</span><span class="sxs-lookup"><span data-stu-id="f2f21-143">OUTPUTS</span></span>

### <span data-ttu-id="f2f21-144">AzureReplicationLinkModel를 통해 서의.</span><span class="sxs-lookup"><span data-stu-id="f2f21-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="f2f21-145">상속자</span><span class="sxs-lookup"><span data-stu-id="f2f21-145">NOTES</span></span>

## <span data-ttu-id="f2f21-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2f21-146">RELATED LINKS</span></span>

[<span data-ttu-id="f2f21-147">새로운 AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f2f21-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="f2f21-148">제거-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f2f21-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="f2f21-149">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="f2f21-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)