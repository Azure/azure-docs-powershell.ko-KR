---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a8ad9a3925ccf1c0f56ce9be6a962d667f122307
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992306"
---
# <span data-ttu-id="f1685-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f1685-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="f1685-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1685-102">SYNOPSIS</span></span>
<span data-ttu-id="f1685-103">Azure 데이터베이스 장애 조치(failover) 그룹의 장애 조치(failover)SQL 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="f1685-104">구문</span><span class="sxs-lookup"><span data-stu-id="f1685-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1685-105">설명</span><span class="sxs-lookup"><span data-stu-id="f1685-105">DESCRIPTION</span></span>
<span data-ttu-id="f1685-106">이 명령은 장애 조치(Failover) 그룹의 서버 역할을 교환하고 모든 보조 데이터베이스를 주 역할로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="f1685-107">모든 새 TDS 세션은 DNS 클라이언트 캐시를 새로 고침한 후 보조 서버로 자동으로 다시 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="f1685-108">원래 주 서버가 다시 온라인이면 이전의 모든 주 데이터베이스가 보조 역할로 전환됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="f1685-109">장애 조치(Failover) 그룹의 보조 서버를 사용하여 이 명령을 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-109">The Failover Group's secondary server must be used to execute this command.</span></span>
<span data-ttu-id="f1685-110">AllowDataLoss 매개 변수를 지정하지 않으면 이 명령은 두 역할이 모두 전환될 때까지 대기합니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-110">If the AllowDataLoss parameter is not specified, this command waits until both roles are switched.</span></span> <span data-ttu-id="f1685-111">AllowDataLoss 매개 변수가 지정되어 있는 경우 명령은 새 주에서 해당 역할을 가정할 때까지만 대기합니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-111">If the AllowDataLoss parameter is specified, the command only waits until the new primary assumes its role.</span></span>

## <span data-ttu-id="f1685-112">예제</span><span class="sxs-lookup"><span data-stu-id="f1685-112">EXAMPLES</span></span>

### <span data-ttu-id="f1685-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="f1685-113">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="f1685-114">장애 조치(Failover) 그룹에서 파이핑하여 데이터 손실을 허용하는 장애 조치(failover) 작업을 발급합니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-114">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="f1685-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="f1685-115">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="f1685-116">데이터를 잃지 않고 성공하거나 실패하고 롤백하는 최상의 장애 조치(failover) 작업을 발급합니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-116">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="f1685-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f1685-117">PARAMETERS</span></span>

### <span data-ttu-id="f1685-118">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="f1685-118">-AllowDataLoss</span></span>
<span data-ttu-id="f1685-119">장애 조치(failover)를 완료하면 데이터가 손실될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-119">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="f1685-120">이렇게 하면 주 데이터베이스를 사용할 수 없는 경우에도 장애 조치(failover)가 진행될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-120">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="f1685-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1685-121">-AsJob</span></span>
<span data-ttu-id="f1685-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f1685-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1685-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1685-123">-DefaultProfile</span></span>
<span data-ttu-id="f1685-124">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f1685-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1685-125">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="f1685-125">-FailoverGroupName</span></span>
<span data-ttu-id="f1685-126">Azure 데이터베이스 장애 조치(failover) SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-126">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="f1685-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1685-127">-ResourceGroupName</span></span>
<span data-ttu-id="f1685-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="f1685-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f1685-129">-ServerName</span></span>
<span data-ttu-id="f1685-130">장애 조치(Failover) 그룹의 보조 Azure SQL 데이터베이스 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-130">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="f1685-131">-확인</span><span class="sxs-lookup"><span data-stu-id="f1685-131">-Confirm</span></span>
<span data-ttu-id="f1685-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1685-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1685-133">-WhatIf</span></span>
<span data-ttu-id="f1685-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1685-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1685-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1685-136">CommonParameters</span></span>
<span data-ttu-id="f1685-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1685-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1685-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1685-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1685-139">입력</span><span class="sxs-lookup"><span data-stu-id="f1685-139">INPUTS</span></span>

### <span data-ttu-id="f1685-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f1685-140">System.String</span></span>

## <span data-ttu-id="f1685-141">출력</span><span class="sxs-lookup"><span data-stu-id="f1685-141">OUTPUTS</span></span>

### <span data-ttu-id="f1685-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="f1685-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="f1685-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1685-143">NOTES</span></span>

## <span data-ttu-id="f1685-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1685-144">RELATED LINKS</span></span>

[<span data-ttu-id="f1685-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f1685-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f1685-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f1685-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f1685-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f1685-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f1685-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f1685-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="f1685-149">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f1685-149">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="f1685-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="f1685-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="f1685-151">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="f1685-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
