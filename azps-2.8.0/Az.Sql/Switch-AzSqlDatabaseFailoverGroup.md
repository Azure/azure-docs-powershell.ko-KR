---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 15b0026158f3942ffbb9ff1d426104cffcb18a28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874034"
---
# <span data-ttu-id="03b6c-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="03b6c-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="03b6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="03b6c-103">Azure SQL 데이터베이스 장애 조치 그룹의 장애 조치를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="03b6c-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="03b6c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03b6c-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03b6c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="03b6c-105">DESCRIPTION</span></span>
<span data-ttu-id="03b6c-106">이 명령은 장애 조치 (Failover) 그룹에 있는 서버의 역할을 전환 하 고 모든 보조 데이터베이스를 주 역할로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="03b6c-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="03b6c-107">DNS 클라이언트 캐시를 새로 고치면 모든 새 TDS 세션이 자동으로 보조 서버로 다시 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b6c-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="03b6c-108">원본 주 서버가 다시 온라인 상태가 되 면 이전의 모든 주 데이터베이스가 보조 역할로 전환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="03b6c-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="03b6c-109">이 명령을 실행 하려면 장애 조치 그룹의 보조 서버를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="03b6c-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="03b6c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="03b6c-110">EXAMPLES</span></span>

### <span data-ttu-id="03b6c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="03b6c-111">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="03b6c-112">장애 조치 (Failover) 그룹의 파이핑에서 데이터 손실을 허용 하는 장애 조치 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="03b6c-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="03b6c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="03b6c-113">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="03b6c-114">데이터 손실 또는 실패 및 롤백 없이 성공할 수 있는 최상의 장애 조치 작업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="03b6c-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="03b6c-115">변수</span><span class="sxs-lookup"><span data-stu-id="03b6c-115">PARAMETERS</span></span>

### <span data-ttu-id="03b6c-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="03b6c-116">-AllowDataLoss</span></span>
<span data-ttu-id="03b6c-117">장애 조치를 완료 하면 데이터 손실이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03b6c-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="03b6c-118">이렇게 하면 기본 데이터베이스를 사용할 수 없는 경우에도 장애 조치를 진행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03b6c-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03b6c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03b6c-119">-AsJob</span></span>
<span data-ttu-id="03b6c-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="03b6c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03b6c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03b6c-121">-DefaultProfile</span></span>
<span data-ttu-id="03b6c-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="03b6c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03b6c-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="03b6c-123">-FailoverGroupName</span></span>
<span data-ttu-id="03b6c-124">Azure SQL Database 장애 조치 (Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03b6c-124">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03b6c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03b6c-125">-ResourceGroupName</span></span>
<span data-ttu-id="03b6c-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03b6c-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="03b6c-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="03b6c-127">-ServerName</span></span>
<span data-ttu-id="03b6c-128">장애 조치 (Failover) 그룹의 보조 Azure SQL 데이터베이스 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03b6c-128">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="03b6c-129">-확인</span><span class="sxs-lookup"><span data-stu-id="03b6c-129">-Confirm</span></span>
<span data-ttu-id="03b6c-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="03b6c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03b6c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03b6c-131">-WhatIf</span></span>
<span data-ttu-id="03b6c-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="03b6c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03b6c-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03b6c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03b6c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b6c-134">CommonParameters</span></span>
<span data-ttu-id="03b6c-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03b6c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b6c-136">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="03b6c-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b6c-137">입력</span><span class="sxs-lookup"><span data-stu-id="03b6c-137">INPUTS</span></span>

### <span data-ttu-id="03b6c-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="03b6c-138">System.String</span></span>

## <span data-ttu-id="03b6c-139">출력</span><span class="sxs-lookup"><span data-stu-id="03b6c-139">OUTPUTS</span></span>

### <span data-ttu-id="03b6c-140">AzureSqlFailoverGroupModel (\*. \*.)</span><span class="sxs-lookup"><span data-stu-id="03b6c-140">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="03b6c-141">상속자</span><span class="sxs-lookup"><span data-stu-id="03b6c-141">NOTES</span></span>

## <span data-ttu-id="03b6c-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03b6c-142">RELATED LINKS</span></span>

[<span data-ttu-id="03b6c-143">새로운 AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="03b6c-143">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="03b6c-144">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="03b6c-144">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="03b6c-145">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="03b6c-145">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="03b6c-146">추가-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="03b6c-146">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="03b6c-147">제거-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="03b6c-147">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="03b6c-148">제거-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="03b6c-148">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="03b6c-149">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="03b6c-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
