---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 8b78cfc7a2934b4670702562941ea0e00c2a70c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226503"
---
# <span data-ttu-id="da7a1-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="da7a1-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="da7a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da7a1-102">SYNOPSIS</span></span>
<span data-ttu-id="da7a1-103">Azure SQL Database 장애 조치 (Failover) 그룹의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a1-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="da7a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="da7a1-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da7a1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="da7a1-105">DESCRIPTION</span></span>
<span data-ttu-id="da7a1-106">이 명령은 Azure SQL Database 장애 조치 (Failover) 그룹의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a1-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="da7a1-107">명령 실행을 위해 장애 조치 그룹의 주 서버를 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a1-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="da7a1-108">그룹의 데이터베이스 집합을 제어 하려면 ' AzSqlDatabaseToFailoverGroup ' 및 ' Remove-AzSqlDatabaseFromFailoverGroup '을 대신 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a1-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="da7a1-109">장애 조치 (Failover) 그룹 기능을 미리 보는 동안에는 '-GracePeriodWithDataLossHours ' 매개 변수에 대해 1 시간 보다 크거나 같은 값만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="da7a1-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="da7a1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="da7a1-110">EXAMPLES</span></span>

### <span data-ttu-id="da7a1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="da7a1-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="da7a1-112">장애 조치 그룹의 장애 조치 정책을 ' 자동 '으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a1-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="da7a1-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="da7a1-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="da7a1-114">장애 조치 (failover) 그룹의 파이프를 통해 장애 조치 그룹의 장애 조치 정책을 ' 수동 '으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a1-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="da7a1-115">변수</span><span class="sxs-lookup"><span data-stu-id="da7a1-115">PARAMETERS</span></span>

### <span data-ttu-id="da7a1-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="da7a1-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="da7a1-117">보조 서버의 작동 중단이 읽기 전용 끝점의 자동 장애 조치를 트리거해야 하는지 여부</span><span class="sxs-lookup"><span data-stu-id="da7a1-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="da7a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da7a1-118">-DefaultProfile</span></span>
<span data-ttu-id="da7a1-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="da7a1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da7a1-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="da7a1-120">-FailoverGroupName</span></span>
<span data-ttu-id="da7a1-121">Azure SQL Database 장애 조치 (Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da7a1-121">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="da7a1-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="da7a1-122">-FailoverPolicy</span></span>
<span data-ttu-id="da7a1-123">Azure SQL Database 장애 조치 (Failover) 그룹의 장애 조치 정책</span><span class="sxs-lookup"><span data-stu-id="da7a1-123">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="da7a1-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="da7a1-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="da7a1-125">기본 서버에서 정전이 발생 하는 경우 자동 장애 조치가 시작 되는 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="da7a1-125">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="da7a1-126">이는 유예 기간이 만료 되기 전에 Azure SQL Database가 자동 장애 조치를 시작 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="da7a1-126">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="da7a1-127">AllowDataLoss 옵션을 사용 하는 장애 조치 작업으로 인해 비동기 동기화의 특성상 데이터가 손실 될 수 있다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="da7a1-127">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="da7a1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da7a1-128">-ResourceGroupName</span></span>
<span data-ttu-id="da7a1-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da7a1-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="da7a1-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="da7a1-130">-ServerName</span></span>
<span data-ttu-id="da7a1-131">장애 조치 (Failover) 그룹의 기본 Azure SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da7a1-131">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="da7a1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7a1-132">CommonParameters</span></span>
<span data-ttu-id="da7a1-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="da7a1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7a1-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="da7a1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7a1-135">입력</span><span class="sxs-lookup"><span data-stu-id="da7a1-135">INPUTS</span></span>

### <span data-ttu-id="da7a1-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="da7a1-136">System.String</span></span>

## <span data-ttu-id="da7a1-137">출력</span><span class="sxs-lookup"><span data-stu-id="da7a1-137">OUTPUTS</span></span>

### <span data-ttu-id="da7a1-138">AzureSqlFailoverGroupModel (\*. \*.)</span><span class="sxs-lookup"><span data-stu-id="da7a1-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="da7a1-139">상속자</span><span class="sxs-lookup"><span data-stu-id="da7a1-139">NOTES</span></span>

## <span data-ttu-id="da7a1-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da7a1-140">RELATED LINKS</span></span>

[<span data-ttu-id="da7a1-141">새로운 AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="da7a1-141">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="da7a1-142">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="da7a1-142">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="da7a1-143">추가-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="da7a1-143">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="da7a1-144">제거-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="da7a1-144">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="da7a1-145">스위치-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="da7a1-145">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="da7a1-146">제거-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="da7a1-146">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="da7a1-147">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="da7a1-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
