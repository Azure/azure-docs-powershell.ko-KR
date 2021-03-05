---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 3031878e30307cd5ff733de6177bc3c65c61a5bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967328"
---
# <span data-ttu-id="ec7bd-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ec7bd-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="ec7bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec7bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ec7bd-103">인스턴스 장애 조치(Failover) 그룹의 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="ec7bd-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec7bd-104">SYNTAX</span></span>

### <span data-ttu-id="ec7bd-105">SetInstanceFailoverGroupDefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ec7bd-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec7bd-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ec7bd-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec7bd-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="ec7bd-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec7bd-108">설명</span><span class="sxs-lookup"><span data-stu-id="ec7bd-108">DESCRIPTION</span></span>
<span data-ttu-id="ec7bd-109">이 명령은 인스턴스 장애 조치 그룹 구성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="ec7bd-110">인스턴스 장애 조치(Failover) 그룹의 기본 지역을 사용하여 명령을 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="ec7bd-111">인스턴스 장애 조치 그룹 기능 미리 보기 동안 '-GracePeriodWithDataLosHours' 매개 변수에 대해 1시간보다 크거나 같은 값만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="ec7bd-112">예제</span><span class="sxs-lookup"><span data-stu-id="ec7bd-112">EXAMPLES</span></span>

### <span data-ttu-id="ec7bd-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec7bd-113">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Set-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Manual
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

<span data-ttu-id="ec7bd-114">장애 조치(Failover) 그룹에서 피핑하여 인스턴스 장애 조치(Failover) 그룹의 장애 조치(failover) 정책을 '수동'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="ec7bd-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ec7bd-115">PARAMETERS</span></span>

### <span data-ttu-id="ec7bd-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="ec7bd-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="ec7bd-117">보조 서버의 중단이 읽기 전용 엔드포인트의 자동 장애 조치(failover)를 트리거해야 하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="ec7bd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec7bd-118">-DefaultProfile</span></span>
<span data-ttu-id="ec7bd-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec7bd-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="ec7bd-120">-FailoverPolicy</span></span>
<span data-ttu-id="ec7bd-121">인스턴스 장애 조치 그룹의 장애 조치(failover) 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-121">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="ec7bd-122">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="ec7bd-122">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="ec7bd-123">주 서버에서 정전이 발생하고 데이터 손실 없이 장애 조치(failover)를 완료할 수 없는 경우 자동 장애 조치(failover)가 시작되기 전의 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-123">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="ec7bd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec7bd-124">-InputObject</span></span>
<span data-ttu-id="ec7bd-125">설정할 인스턴스 장애 조치 그룹 개체</span><span class="sxs-lookup"><span data-stu-id="ec7bd-125">The Instance Failover Group object to set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec7bd-126">-Location</span><span class="sxs-lookup"><span data-stu-id="ec7bd-126">-Location</span></span>
<span data-ttu-id="ec7bd-127">인스턴스 장애 조치(Failover) 그룹을 검색할 로컬 지역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet, SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec7bd-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ec7bd-128">-Name</span></span>
<span data-ttu-id="ec7bd-129">인스턴스 장애 조치(Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-129">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec7bd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec7bd-130">-ResourceGroupName</span></span>
<span data-ttu-id="ec7bd-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec7bd-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec7bd-132">-ResourceId</span></span>
<span data-ttu-id="ec7bd-133">설정할 인스턴스 장애 조치 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-133">The Resource ID of the Instance Failover Group to set.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec7bd-134">-확인</span><span class="sxs-lookup"><span data-stu-id="ec7bd-134">-Confirm</span></span>
<span data-ttu-id="ec7bd-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec7bd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec7bd-136">-WhatIf</span></span>
<span data-ttu-id="ec7bd-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec7bd-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec7bd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec7bd-139">CommonParameters</span></span>
<span data-ttu-id="ec7bd-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec7bd-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec7bd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec7bd-142">입력</span><span class="sxs-lookup"><span data-stu-id="ec7bd-142">INPUTS</span></span>

### <span data-ttu-id="ec7bd-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="ec7bd-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="ec7bd-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ec7bd-144">System.String</span></span>

## <span data-ttu-id="ec7bd-145">출력</span><span class="sxs-lookup"><span data-stu-id="ec7bd-145">OUTPUTS</span></span>

### <span data-ttu-id="ec7bd-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="ec7bd-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="ec7bd-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec7bd-147">NOTES</span></span>

## <span data-ttu-id="ec7bd-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec7bd-148">RELATED LINKS</span></span>
