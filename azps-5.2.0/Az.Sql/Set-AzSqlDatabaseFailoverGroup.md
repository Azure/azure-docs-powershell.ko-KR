---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 8b78cfc7a2934b4670702562941ea0e00c2a70c8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354789"
---
# <span data-ttu-id="2ebbb-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2ebbb-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="2ebbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ebbb-102">SYNOPSIS</span></span>
<span data-ttu-id="2ebbb-103">Azure SQL 데이터베이스 장애 조치(failover) 그룹의 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="2ebbb-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="2ebbb-104">구문</span><span class="sxs-lookup"><span data-stu-id="2ebbb-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ebbb-105">설명</span><span class="sxs-lookup"><span data-stu-id="2ebbb-105">DESCRIPTION</span></span>
<span data-ttu-id="2ebbb-106">이 명령은 Azure SQL 데이터베이스 장애 조치(failover) 그룹의 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="2ebbb-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="2ebbb-107">장애 조치 그룹의 주 서버를 사용하여 명령을 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ebbb-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="2ebbb-108">그룹의 데이터베이스 집합을 제어하려면 'Add-AzSqlDatabaseToFailoverGroup' 및 'Remove-AzSqlDatabaseFromFailoverGroup'을 대신 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="2ebbb-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="2ebbb-109">장애 조치 그룹 기능을 미리 볼 때 '-GracePeriodWithDataLossHours' 매개 변수에 대해 1시간보다 크거나 같은 값만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ebbb-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="2ebbb-110">예제</span><span class="sxs-lookup"><span data-stu-id="2ebbb-110">EXAMPLES</span></span>

### <span data-ttu-id="2ebbb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2ebbb-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="2ebbb-112">장애 조치 그룹의 장애 조치(failover) 정책을 '자동'으로 설정</span><span class="sxs-lookup"><span data-stu-id="2ebbb-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="2ebbb-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="2ebbb-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="2ebbb-114">장애 조치(failover) 그룹에서 파이핑하여 장애 조치(failover) 그룹의 장애 조치(failover) 정책을 '수동'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2ebbb-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="2ebbb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ebbb-115">PARAMETERS</span></span>

### <span data-ttu-id="2ebbb-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="2ebbb-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="2ebbb-117">보조 서버의 중단이 읽기 전용 엔드포인트의 자동 장애 조치(failover)를 트리거해야 하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="2ebbb-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ebbb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ebbb-118">-DefaultProfile</span></span>
<span data-ttu-id="2ebbb-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2ebbb-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ebbb-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="2ebbb-120">-FailoverGroupName</span></span>
<span data-ttu-id="2ebbb-121">Azure SQL 데이터베이스 장애 조치(failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ebbb-121">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="2ebbb-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="2ebbb-122">-FailoverPolicy</span></span>
<span data-ttu-id="2ebbb-123">Azure SQL 데이터베이스 장애 조치(failover) 그룹의 장애 조치(failover) 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="2ebbb-123">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ebbb-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="2ebbb-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="2ebbb-125">주 서버에서 정전이 발생하는 경우 자동 장애 조치(failover)가 시작되기 전의 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="2ebbb-125">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="2ebbb-126">이는 Azure SQL 데이터베이스가 유예 기간이 만료되기 전에 자동 장애 조치(failover)를 시작하지 않는다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2ebbb-126">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="2ebbb-127">AllowDataLoss 옵션을 사용하는 장애 조치(failover) 작업은 비동기 동기화의 특성으로 인해 데이터 손실이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ebbb-127">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ebbb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ebbb-128">-ResourceGroupName</span></span>
<span data-ttu-id="2ebbb-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ebbb-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="2ebbb-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2ebbb-130">-ServerName</span></span>
<span data-ttu-id="2ebbb-131">장애 조치 그룹의 기본 Azure SQL 데이터베이스 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ebbb-131">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="2ebbb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ebbb-132">CommonParameters</span></span>
<span data-ttu-id="2ebbb-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2ebbb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ebbb-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2ebbb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ebbb-135">입력</span><span class="sxs-lookup"><span data-stu-id="2ebbb-135">INPUTS</span></span>

### <span data-ttu-id="2ebbb-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2ebbb-136">System.String</span></span>

## <span data-ttu-id="2ebbb-137">출력</span><span class="sxs-lookup"><span data-stu-id="2ebbb-137">OUTPUTS</span></span>

### <span data-ttu-id="2ebbb-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="2ebbb-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="2ebbb-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2ebbb-139">NOTES</span></span>

## <span data-ttu-id="2ebbb-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ebbb-140">RELATED LINKS</span></span>

[<span data-ttu-id="2ebbb-141">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2ebbb-141">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="2ebbb-142">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2ebbb-142">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="2ebbb-143">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2ebbb-143">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="2ebbb-144">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2ebbb-144">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="2ebbb-145">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2ebbb-145">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="2ebbb-146">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2ebbb-146">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="2ebbb-147">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="2ebbb-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
