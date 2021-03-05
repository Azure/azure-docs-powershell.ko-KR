---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: a20f2196b6052befb74cd74366c96bf262cdd325
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992287"
---
# <span data-ttu-id="5bf32-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5bf32-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="5bf32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bf32-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf32-103">인스턴스 장애 조치(failover) 그룹의 장애 조치(failover)를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5bf32-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="5bf32-104">구문</span><span class="sxs-lookup"><span data-stu-id="5bf32-104">SYNTAX</span></span>

### <span data-ttu-id="5bf32-105">SwitchInstanceFailoverGroupDefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5bf32-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bf32-106">SwitchInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5bf32-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bf32-107">SwitchInstanceFailoverGroupByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5bf32-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bf32-108">설명</span><span class="sxs-lookup"><span data-stu-id="5bf32-108">DESCRIPTION</span></span>
<span data-ttu-id="5bf32-109">이 명령은 지정된 보조 지역으로 장애 조치(failover) 그룹으로 장애 조치(failover) 그룹에서 관리되는 인스턴스의 역할을 교환하여 새 주 지역으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5bf32-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="5bf32-110">기본 엔드포인트에 연결하는 모든 새 TDS 세션은 자동으로 새 주 지역으로 다시 라우팅됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bf32-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="5bf32-111">예제</span><span class="sxs-lookup"><span data-stu-id="5bf32-111">EXAMPLES</span></span>

### <span data-ttu-id="5bf32-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="5bf32-112">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup -AllowDataLoss
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

<span data-ttu-id="5bf32-113">인스턴스 장애 조치 그룹에서 파이핑하여 데이터 손실을 허용하는 장애 조치(failover) 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5bf32-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="5bf32-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="5bf32-114">Example 2</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup
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

<span data-ttu-id="5bf32-115">데이터를 잃지 않고 성공하거나 실패하고 롤백하는 최상의 장애 조치(failover) 작업을 발급합니다.</span><span class="sxs-lookup"><span data-stu-id="5bf32-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="5bf32-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5bf32-116">PARAMETERS</span></span>

### <span data-ttu-id="5bf32-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="5bf32-117">-AllowDataLoss</span></span>
<span data-ttu-id="5bf32-118">장애 조치(failover)를 완료하면 데이터가 손실될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bf32-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="5bf32-119">이렇게 하면 주 데이터베이스를 사용할 수 없는 경우에도 장애 조치(failover)가 진행될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5bf32-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="5bf32-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf32-120">-DefaultProfile</span></span>
<span data-ttu-id="5bf32-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5bf32-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bf32-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bf32-122">-InputObject</span></span>
<span data-ttu-id="5bf32-123">전환할 인스턴스 장애 조치 그룹 개체</span><span class="sxs-lookup"><span data-stu-id="5bf32-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SwitchInstanceFailoverGroupByInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bf32-124">-Location</span><span class="sxs-lookup"><span data-stu-id="5bf32-124">-Location</span></span>
<span data-ttu-id="5bf32-125">인스턴스 장애 조치(Failover) 그룹을 검색할 로컬 지역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bf32-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet, SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bf32-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5bf32-126">-Name</span></span>
<span data-ttu-id="5bf32-127">인스턴스 장애 조치(Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bf32-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bf32-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bf32-128">-ResourceGroupName</span></span>
<span data-ttu-id="5bf32-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5bf32-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bf32-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bf32-130">-ResourceId</span></span>
<span data-ttu-id="5bf32-131">전환할 인스턴스 장애 조치(Failover) 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5bf32-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bf32-132">-확인</span><span class="sxs-lookup"><span data-stu-id="5bf32-132">-Confirm</span></span>
<span data-ttu-id="5bf32-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5bf32-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bf32-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bf32-134">-WhatIf</span></span>
<span data-ttu-id="5bf32-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5bf32-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bf32-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5bf32-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bf32-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf32-137">CommonParameters</span></span>
<span data-ttu-id="5bf32-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5bf32-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf32-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5bf32-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf32-140">입력</span><span class="sxs-lookup"><span data-stu-id="5bf32-140">INPUTS</span></span>

### <span data-ttu-id="5bf32-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="5bf32-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="5bf32-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5bf32-142">System.String</span></span>

## <span data-ttu-id="5bf32-143">출력</span><span class="sxs-lookup"><span data-stu-id="5bf32-143">OUTPUTS</span></span>

### <span data-ttu-id="5bf32-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="5bf32-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="5bf32-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5bf32-145">NOTES</span></span>

## <span data-ttu-id="5bf32-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5bf32-146">RELATED LINKS</span></span>
