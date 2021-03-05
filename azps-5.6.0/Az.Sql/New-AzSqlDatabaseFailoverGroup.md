---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: be1f2fc5c0aa2abda5f036580e377f05b26c2eb2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976304"
---
# <span data-ttu-id="5fb0a-101">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5fb0a-101">New-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="5fb0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fb0a-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb0a-103">이 명령은 새 Azure SQL 장애 조치(Failover) 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-103">This command creates a new Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="5fb0a-104">구문</span><span class="sxs-lookup"><span data-stu-id="5fb0a-104">SYNTAX</span></span>

```
New-AzSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fb0a-105">설명</span><span class="sxs-lookup"><span data-stu-id="5fb0a-105">DESCRIPTION</span></span>
<span data-ttu-id="5fb0a-106">지정된 서버에 SQL 데이터베이스 장애 조치(Failover) 그룹을 새로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>
<span data-ttu-id="5fb0a-107">Azure SQL 데이터베이스 TDS 엔드포인트는 FailoverGroupName.SqlDatabaseDnsSuffix(예: FailoverGroupName.database.windows.net) 및 FailoverGroupName.secondary.SqlDatabaseDnsSuffix에서 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="5fb0a-108">이러한 엔드포인트는 장애 조치(Failover) 그룹의 기본 및 보조 서버에 각각 연결하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="5fb0a-109">주 서버가 중단의 영향을 받는 경우 장애 조치(Failover) 그룹의 장애 조치(failover) 정책 및 유예 기간에 따라 엔드포인트 및 데이터베이스의 자동 장애 조치(failover)가 트리거됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>
<span data-ttu-id="5fb0a-110">새로 만든 장애 조치(Failover) 그룹에는 데이터베이스가 포함되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="5fb0a-111">장애 조치 그룹에서 데이터베이스 집합을 제어하려면 'Add-AzSqlDatabaseToFailoverGroup' 및 'Remove-AzSqlDatabaseFromFailoverGroup' cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-111">To control the set of databases in a Failover Group, use the 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' cmdlets.</span></span>
<span data-ttu-id="5fb0a-112">'-GracePeriodWithDataLosHours' 매개 변수에 대해 1시간보다 크거나 같은 값만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-112">Only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="5fb0a-113">예제</span><span class="sxs-lookup"><span data-stu-id="5fb0a-113">EXAMPLES</span></span>

### <span data-ttu-id="5fb0a-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="5fb0a-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="5fb0a-115">이 명령은 동일한 리소스 그룹의 두 서버에 대해 장애 조치(failover) 정책 '자동'이 있는 새 장애 조치(Failover) 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="5fb0a-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="5fb0a-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="5fb0a-117">이 명령은 서로 다른 리소스 그룹의 두 서버에 대해 장애 조치(failover) 정책 '수동'이 있는 새 장애 조치(Failover) 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="5fb0a-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5fb0a-118">PARAMETERS</span></span>

### <span data-ttu-id="5fb0a-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="5fb0a-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="5fb0a-120">보조 서버의 중단이 읽기 전용 엔드포인트의 자동 장애 조치(failover)를 트리거해야 하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="5fb0a-121">이 기능은 아직 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-121">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="5fb0a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fb0a-122">-DefaultProfile</span></span>
<span data-ttu-id="5fb0a-123">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5fb0a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fb0a-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="5fb0a-124">-FailoverGroupName</span></span>
<span data-ttu-id="5fb0a-125">만들 데이터베이스 장애 조치 SQL Azure의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-125">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb0a-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="5fb0a-126">-FailoverPolicy</span></span>
<span data-ttu-id="5fb0a-127">Azure 데이터베이스 장애 조치(failover) SQL 장애 조치(failover) 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="5fb0a-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="5fb0a-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="5fb0a-129">주 서버에서 정전이 발생하고 데이터 손실 없이 장애 조치(failover)를 완료할 수 없는 경우 자동 장애 조치(failover)가 시작되기 전의 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="5fb0a-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fb0a-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="5fb0a-131">Azure 데이터베이스 장애 조치(Failover) 그룹의 보조 SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb0a-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="5fb0a-132">-PartnerServerName</span></span>
<span data-ttu-id="5fb0a-133">Azure 데이터베이스 장애 조치(Failover) 그룹의 보조 SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fb0a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fb0a-134">-ResourceGroupName</span></span>
<span data-ttu-id="5fb0a-135">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="5fb0a-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5fb0a-136">-ServerName</span></span>
<span data-ttu-id="5fb0a-137">장애 조치(Failover) 그룹의 기본 Azure SQL 데이터베이스 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="5fb0a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb0a-138">CommonParameters</span></span>
<span data-ttu-id="5fb0a-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5fb0a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb0a-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fb0a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb0a-141">입력</span><span class="sxs-lookup"><span data-stu-id="5fb0a-141">INPUTS</span></span>

### <span data-ttu-id="5fb0a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5fb0a-142">System.String</span></span>

## <span data-ttu-id="5fb0a-143">출력</span><span class="sxs-lookup"><span data-stu-id="5fb0a-143">OUTPUTS</span></span>

### <span data-ttu-id="5fb0a-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="5fb0a-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="5fb0a-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5fb0a-145">NOTES</span></span>

## <span data-ttu-id="5fb0a-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5fb0a-146">RELATED LINKS</span></span>

[<span data-ttu-id="5fb0a-147">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5fb0a-147">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5fb0a-148">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5fb0a-148">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5fb0a-149">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5fb0a-149">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="5fb0a-150">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5fb0a-150">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="5fb0a-151">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5fb0a-151">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5fb0a-152">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5fb0a-152">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5fb0a-153">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="5fb0a-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
