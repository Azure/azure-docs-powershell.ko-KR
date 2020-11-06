---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: c5dd678a851e663b04746bb4a5780624ea4c5f40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535084"
---
# <span data-ttu-id="4635d-101">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4635d-101">New-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="4635d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4635d-102">SYNOPSIS</span></span>
<span data-ttu-id="4635d-103">이 명령은 새 Azure SQL 데이터베이스 장애 조치 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-103">This command creates a new Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4635d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4635d-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4635d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4635d-105">DESCRIPTION</span></span>
<span data-ttu-id="4635d-106">지정 된 서버에 대 한 새 Azure SQL 데이터베이스 장애 조치 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>
<span data-ttu-id="4635d-107">두 개의 Azure SQL Database TDS 끝점은 Failovergroupname (예: FailoverGroupName.database.windows.net) 및 FailoverGroupName. SqlDatabaseDnsSuffix에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="4635d-108">이러한 끝점을 사용 하 여 장애 조치 그룹의 기본 및 보조 서버에 각각 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="4635d-109">주 서버가 작동 중지에 영향을 받는 경우, 끝점 및 데이터베이스의 자동 장애 조치는 장애 조치 그룹의 장애 조치 정책 및 유예 기간에 따라 트리거됩니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>
<span data-ttu-id="4635d-110">새로 만든 장애 조치 (Failover) 그룹에는 데이터베이스가 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="4635d-111">장애 조치 (Failover) 그룹의 데이터베이스 집합을 제어 하려면 ' AzureRmSqlDatabaseToFailoverGroup ' 및 ' Remove-AzureRmSqlDatabaseFromFailoverGroup ' cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-111">To control the set of databases in a Failover Group, use the 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' cmdlets.</span></span>
<span data-ttu-id="4635d-112">장애 조치 (Failover) 그룹 기능을 미리 보는 동안에는 '-GracePeriodWithDataLossHours ' 매개 변수에 대해 1 시간 보다 크거나 같은 값만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-112">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="4635d-113">예제의</span><span class="sxs-lookup"><span data-stu-id="4635d-113">EXAMPLES</span></span>

### <span data-ttu-id="4635d-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="4635d-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="4635d-115">이 명령은 같은 리소스 그룹의 두 서버에 대해 장애 조치 정책으로 새 장애 조치 (failover) 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="4635d-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="4635d-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="4635d-117">이 명령은 서로 다른 리소스 그룹의 두 서버에 대해 장애 조치 정책 ' 수동 '을 사용 하 여 새 장애 조치 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="4635d-118">변수</span><span class="sxs-lookup"><span data-stu-id="4635d-118">PARAMETERS</span></span>

### <span data-ttu-id="4635d-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="4635d-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="4635d-120">보조 서버의 작동 중지가 읽기 전용 끝점의 자동 장애 조치를 트리거해야 하는지 여부</span><span class="sxs-lookup"><span data-stu-id="4635d-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="4635d-121">이 기능은 아직 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-121">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="4635d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4635d-122">-DefaultProfile</span></span>
<span data-ttu-id="4635d-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4635d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4635d-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="4635d-124">-FailoverGroupName</span></span>
<span data-ttu-id="4635d-125">만들 Azure SQL Database 장애 조치 (Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-125">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="4635d-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="4635d-126">-FailoverPolicy</span></span>
<span data-ttu-id="4635d-127">Azure SQL Database 장애 조치 (Failover) 그룹의 장애 조치 정책</span><span class="sxs-lookup"><span data-stu-id="4635d-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="4635d-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="4635d-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="4635d-129">기본 서버에서 작동 중지가 발생 하 고 데이터 손실 없이 장애 조치를 완료할 수 없는 경우 자동 장애 조치가 시작 되기 전의 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="4635d-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4635d-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="4635d-131">Azure SQL Database 장애 조치 (Failover) 그룹의 보조 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="4635d-132">-(-)-(서버 이름)</span><span class="sxs-lookup"><span data-stu-id="4635d-132">-PartnerServerName</span></span>
<span data-ttu-id="4635d-133">Azure SQL Database 장애 조치 (Failover) 그룹의 보조 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="4635d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4635d-134">-ResourceGroupName</span></span>
<span data-ttu-id="4635d-135">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="4635d-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4635d-136">-ServerName</span></span>
<span data-ttu-id="4635d-137">장애 조치 (Failover) 그룹의 기본 Azure SQL 데이터베이스 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="4635d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4635d-138">CommonParameters</span></span>
<span data-ttu-id="4635d-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4635d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4635d-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4635d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4635d-141">입력</span><span class="sxs-lookup"><span data-stu-id="4635d-141">INPUTS</span></span>

### <span data-ttu-id="4635d-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4635d-142">System.String</span></span>

## <span data-ttu-id="4635d-143">출력</span><span class="sxs-lookup"><span data-stu-id="4635d-143">OUTPUTS</span></span>

### <span data-ttu-id="4635d-144">AzureSqlFailoverGroupModel (\*. \*.)</span><span class="sxs-lookup"><span data-stu-id="4635d-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="4635d-145">상속자</span><span class="sxs-lookup"><span data-stu-id="4635d-145">NOTES</span></span>

## <span data-ttu-id="4635d-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4635d-146">RELATED LINKS</span></span>

[<span data-ttu-id="4635d-147">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4635d-147">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4635d-148">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4635d-148">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4635d-149">추가-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4635d-149">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="4635d-150">제거-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4635d-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="4635d-151">스위치-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4635d-151">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4635d-152">제거-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4635d-152">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4635d-153">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="4635d-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
