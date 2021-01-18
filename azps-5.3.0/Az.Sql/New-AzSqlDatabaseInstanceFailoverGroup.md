---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 99be70e225dd607c580c4571f4ae332e7badf33a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495541"
---
# <span data-ttu-id="bea51-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="bea51-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="bea51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bea51-102">SYNOPSIS</span></span>
<span data-ttu-id="bea51-103">이 명령은 새 Azure SQL 데이터베이스 인스턴스 장애 조치(failover) 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="bea51-104">구문</span><span class="sxs-lookup"><span data-stu-id="bea51-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup [-Name] <String> [-PartnerResourceGroupName <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-PartnerSubscriptionId <String>] [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bea51-105">설명</span><span class="sxs-lookup"><span data-stu-id="bea51-105">DESCRIPTION</span></span>
<span data-ttu-id="bea51-106">명시된 Managed Instance 쌍을 SQL 지역 간에 새 Azure SQL 데이터베이스 인스턴스 장애 조치(failover) 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="bea51-107">Name.SqlDatabaseDnsSuffix(예: Name.database.windows.net) 및 Name.secondary.SqlDatabaseDnsSuffix에 두 개의 Azure SQL Database TDS 엔드포인트가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="bea51-108">이러한 엔드포인트는 장애 조치(failover) 그룹의 기본 및 보조 지역에 각각 연결하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="bea51-109">주 지역이 중단의 영향을 받는 경우 인스턴스 장애 조치(failover) 그룹의 장애 조치(failover) 정책 및 유예 기간에 따라 엔드포인트 및 데이터베이스의 자동 장애 조치(failover)가 트리거됩니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="bea51-110">인스턴스 장애 조치 그룹 기능의 미리 보기 동안 '-GracePeriodWithDataLossHours' 매개 변수에 대해 1시간보다 크거나 같은 값만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="bea51-111">예제</span><span class="sxs-lookup"><span data-stu-id="bea51-111">EXAMPLES</span></span>

### <span data-ttu-id="bea51-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="bea51-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="bea51-113">이 명령은 Managed Instance 쌍에 대한 장애 조치 정책 '자동'을 사용하여 새 인스턴스 장애 조치(failover) 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="bea51-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="bea51-114">Example 2</span></span>
```powershell
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

<span data-ttu-id="bea51-115">이 명령은 Managed Instance 쌍에 대한 장애 조치 정책 '수동'을 사용하여 새 인스턴스 장애 조치(failover) 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

### <span data-ttu-id="bea51-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="bea51-116">Example 3</span></span>

<span data-ttu-id="bea51-117">이 명령은 새 Azure SQL 데이터베이스 인스턴스 장애 조치(failover) 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-117">This command creates a new Azure SQL Database Instance Failover Group.</span></span> <span data-ttu-id="bea51-118">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="bea51-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1 -Location location -Name fgName -PartnerManagedInstanceName $partnerManagedInstance.Name -PartnerRegion $partnerRegion -PartnerResourceGroupName rg2 -PrimaryManagedInstanceName $managedInstance.Name -ResourceGroupName rg
```

## <span data-ttu-id="bea51-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bea51-119">PARAMETERS</span></span>

### <span data-ttu-id="bea51-120">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="bea51-120">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="bea51-121">보조 서버의 중단이 읽기 전용 엔드포인트의 자동 장애 조치(failover)를 트리거해야 하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-121">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="bea51-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea51-122">-DefaultProfile</span></span>
<span data-ttu-id="bea51-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bea51-124">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="bea51-124">-FailoverPolicy</span></span>
<span data-ttu-id="bea51-125">인스턴스 장애 조치 그룹의 장애 조치(failover) 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-125">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="bea51-126">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="bea51-126">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="bea51-127">주 서버에서 정전이 발생하고 데이터 손실 없이 장애 조치(failover)를 완료할 수 없는 경우 자동 장애 조치(failover)가 시작되기 전의 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-127">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea51-128">-Location</span><span class="sxs-lookup"><span data-stu-id="bea51-128">-Location</span></span>
<span data-ttu-id="bea51-129">인스턴스 장애 조치(failover) 그룹을 검색할 로컬 지역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-129">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea51-130">-Name</span><span class="sxs-lookup"><span data-stu-id="bea51-130">-Name</span></span>
<span data-ttu-id="bea51-131">만들 Azure SQL 데이터베이스 장애 조치(failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-131">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea51-132">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="bea51-132">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="bea51-133">인스턴스 장애 조치(failover) 그룹에 추가할 파트너 지역의 Managed Instance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-133">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="bea51-134">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="bea51-134">-PartnerRegion</span></span>
<span data-ttu-id="bea51-135">인스턴스 장애 조치 그룹의 파트너 지역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-135">The name of the partner region of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="bea51-136">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea51-136">-PartnerResourceGroupName</span></span>
<span data-ttu-id="bea51-137">인스턴스 장애 조치 그룹의 보조 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-137">The name of the secondary resource group of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="bea51-138">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bea51-138">-PartnerSubscriptionId</span></span>
<span data-ttu-id="bea51-139">인스턴스 장애 조치 그룹의 보조 Managed Instance의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-139">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="bea51-140">이 매개 변수는 구독 간 설정에만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-140">This parameter is only needed for cross-subscription setup</span></span>

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

### <span data-ttu-id="bea51-141">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="bea51-141">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="bea51-142">인스턴스 장애 조치(failover) 그룹에 추가할 로컬 지역의 Managed Instance의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-142">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="bea51-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea51-143">-ResourceGroupName</span></span>
<span data-ttu-id="bea51-144">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea51-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bea51-145">-Confirm</span></span>
<span data-ttu-id="bea51-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea51-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bea51-147">-WhatIf</span></span>
<span data-ttu-id="bea51-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bea51-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bea51-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea51-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea51-150">CommonParameters</span></span>
<span data-ttu-id="bea51-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bea51-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea51-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bea51-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea51-153">입력</span><span class="sxs-lookup"><span data-stu-id="bea51-153">INPUTS</span></span>

### <span data-ttu-id="bea51-154">System.String</span><span class="sxs-lookup"><span data-stu-id="bea51-154">System.String</span></span>

## <span data-ttu-id="bea51-155">출력</span><span class="sxs-lookup"><span data-stu-id="bea51-155">OUTPUTS</span></span>

### <span data-ttu-id="bea51-156">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="bea51-156">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="bea51-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bea51-157">NOTES</span></span>

## <span data-ttu-id="bea51-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bea51-158">RELATED LINKS</span></span>
