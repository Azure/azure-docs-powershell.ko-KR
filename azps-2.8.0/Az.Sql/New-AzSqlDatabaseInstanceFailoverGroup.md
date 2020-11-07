---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 04ed033559abe6fe6a60922f7b11a498ff4026bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873884"
---
# <span data-ttu-id="72fcd-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="72fcd-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="72fcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72fcd-102">SYNOPSIS</span></span>
<span data-ttu-id="72fcd-103">이 명령은 새 Azure SQL 데이터베이스 인스턴스 장애 조치 (Failover) 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="72fcd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="72fcd-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup -Name <String> [-PartnerResourceGroupName <String>] [-PartnerSubscriptionId <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72fcd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="72fcd-105">DESCRIPTION</span></span>
<span data-ttu-id="72fcd-106">지정 된 영역 간에 관리 되는 인스턴스 쌍이 있는 새 Azure SQL 데이터베이스 인스턴스 장애 조치 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="72fcd-107">SqlDatabaseDnsSuffix (예: Name.database.windows.net) 및 SqlDatabaseDnsSuffix와 같은 두 개의 Azure SQL 데이터베이스 TDS 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="72fcd-108">이러한 끝점은 장애 조치 그룹의 기본 영역과 보조 영역에 각각 연결 하는 데 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="72fcd-109">기본 영역이 작동 중지의 영향을 받는 경우 끝점 및 데이터베이스의 자동 장애 조치는 인스턴스 장애 조치 그룹의 장애 조치 정책 및 유예 기간에 따라 트리거됩니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="72fcd-110">인스턴스 장애 조치 (Failover) 그룹 기능을 미리 보는 동안에는 '-GracePeriodWithDataLossHours ' 매개 변수에 대해 1 시간 보다 크거나 같은 값만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="72fcd-111">예제의</span><span class="sxs-lookup"><span data-stu-id="72fcd-111">EXAMPLES</span></span>

### <span data-ttu-id="72fcd-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="72fcd-112">Example 1</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="72fcd-113">이 명령은 관리 되는 인스턴스 쌍에 대해 장애 조치 정책 ' 자동 '을 사용 하 여 새 인스턴스 장애 조치 (Failover) 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="72fcd-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="72fcd-114">Example 2</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Manual
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Manual
FailoverWithDataLossGracePeriodHours  : 
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="72fcd-115">이 명령은 관리 되는 인스턴스 쌍에 대해 장애 조치 정책 ' 수동 '을 사용 하 여 새 인스턴스 장애 조치 (Failover) 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

## <span data-ttu-id="72fcd-116">변수</span><span class="sxs-lookup"><span data-stu-id="72fcd-116">PARAMETERS</span></span>

### <span data-ttu-id="72fcd-117">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="72fcd-117">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="72fcd-118">보조 서버의 작동 중지가 읽기 전용 끝점의 자동 장애 조치를 트리거해야 하는지 여부</span><span class="sxs-lookup"><span data-stu-id="72fcd-118">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="72fcd-119">이 기능은 아직 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-119">This feature is not yet supported.</span></span>

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fcd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72fcd-120">-DefaultProfile</span></span>
<span data-ttu-id="72fcd-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72fcd-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="72fcd-122">-FailoverPolicy</span></span>
<span data-ttu-id="72fcd-123">인스턴스 장애 조치 (Failover) 그룹의 장애 조치 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-123">The failover policy of the Instance Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fcd-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="72fcd-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="72fcd-125">기본 서버에서 작동 중지가 발생 하 고 데이터 손실 없이 장애 조치를 완료할 수 없는 경우 자동 장애 조치가 시작 되기 전의 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-125">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fcd-126">-위치</span><span class="sxs-lookup"><span data-stu-id="72fcd-126">-Location</span></span>
<span data-ttu-id="72fcd-127">인스턴스 장애 조치 (Failover) 그룹을 검색할 로컬 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fcd-128">-이름</span><span class="sxs-lookup"><span data-stu-id="72fcd-128">-Name</span></span>
<span data-ttu-id="72fcd-129">만들 Azure SQL Database 장애 조치 (Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-129">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fcd-130">-단일 기능을 위한 인스턴스</span><span class="sxs-lookup"><span data-stu-id="72fcd-130">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="72fcd-131">파트너 영역에서 인스턴스 장애 조치 (Failover) 그룹에 추가할 관리 되는 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-131">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fcd-132">-또는 지역</span><span class="sxs-lookup"><span data-stu-id="72fcd-132">-PartnerRegion</span></span>
<span data-ttu-id="72fcd-133">인스턴스 장애 조치 (Failover) 그룹의 파트너 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-133">The name of the partner region of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fcd-134">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72fcd-134">-PartnerResourceGroupName</span></span>
<span data-ttu-id="72fcd-135">인스턴스 장애 조치 (Failover) 그룹의 보조 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-135">The name of the secondary resource group of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fcd-136">-(또는)-(Subscriptionid)</span><span class="sxs-lookup"><span data-stu-id="72fcd-136">-PartnerSubscriptionId</span></span>
<span data-ttu-id="72fcd-137">인스턴스 장애 조치 (Failover) 그룹의 보조 관리 인스턴스에 대 한 구독 id입니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-137">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="72fcd-138">이 매개 변수는 교차 구독 설정에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-138">This parameter is only needed for cross-subscription setup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fcd-139">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="72fcd-139">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="72fcd-140">로컬 지역에서 인스턴스 장애 조치 (Failover) 그룹에 추가할 관리 되는 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-140">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fcd-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72fcd-141">-ResourceGroupName</span></span>
<span data-ttu-id="72fcd-142">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-142">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fcd-143">-확인</span><span class="sxs-lookup"><span data-stu-id="72fcd-143">-Confirm</span></span>
<span data-ttu-id="72fcd-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fcd-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72fcd-145">-WhatIf</span></span>
<span data-ttu-id="72fcd-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72fcd-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72fcd-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72fcd-148">CommonParameters</span></span>
<span data-ttu-id="72fcd-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="72fcd-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72fcd-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72fcd-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72fcd-151">입력</span><span class="sxs-lookup"><span data-stu-id="72fcd-151">INPUTS</span></span>

### <span data-ttu-id="72fcd-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="72fcd-152">System.String</span></span>

## <span data-ttu-id="72fcd-153">출력</span><span class="sxs-lookup"><span data-stu-id="72fcd-153">OUTPUTS</span></span>

### <span data-ttu-id="72fcd-154">Microsoft. \*. AzureSqlInstanceFailoverGroupModel Failovergroup.</span><span class="sxs-lookup"><span data-stu-id="72fcd-154">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="72fcd-155">상속자</span><span class="sxs-lookup"><span data-stu-id="72fcd-155">NOTES</span></span>

## <span data-ttu-id="72fcd-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="72fcd-156">RELATED LINKS</span></span>
