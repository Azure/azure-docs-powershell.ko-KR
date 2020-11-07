---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 79d7482d51ffc7c03703dbf62e00fd9230f9976d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878854"
---
# <span data-ttu-id="9450d-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9450d-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="9450d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9450d-102">SYNOPSIS</span></span>
<span data-ttu-id="9450d-103">인스턴스 장애 조치 (Failover) 그룹의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9450d-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="9450d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9450d-104">SYNTAX</span></span>

### <span data-ttu-id="9450d-105">SetInstanceFailoverGroupDefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9450d-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9450d-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9450d-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9450d-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="9450d-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9450d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9450d-108">DESCRIPTION</span></span>
<span data-ttu-id="9450d-109">이 명령은 인스턴스 장애 조치 (Failover) 그룹의 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9450d-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="9450d-110">명령을 실행 하려면 인스턴스 장애 조치 그룹의 기본 영역을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9450d-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="9450d-111">인스턴스 장애 조치 (Failover) 그룹 기능을 미리 보는 동안에는 '-GracePeriodWithDataLossHours ' 매개 변수에 대해 1 시간 보다 크거나 같은 값만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9450d-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="9450d-112">예제의</span><span class="sxs-lookup"><span data-stu-id="9450d-112">EXAMPLES</span></span>

### <span data-ttu-id="9450d-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="9450d-113">Example 1</span></span>
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

<span data-ttu-id="9450d-114">장애 조치 (failover) 그룹에 파이핑 하 여 인스턴스 장애 조치 (failover) 그룹의 장애 정책을 ' 수동 '으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9450d-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="9450d-115">변수</span><span class="sxs-lookup"><span data-stu-id="9450d-115">PARAMETERS</span></span>

### <span data-ttu-id="9450d-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="9450d-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="9450d-117">보조 서버의 작동 중단이 읽기 전용 끝점의 자동 장애 조치를 트리거해야 하는지 여부</span><span class="sxs-lookup"><span data-stu-id="9450d-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="9450d-118">이 기능은 아직 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9450d-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="9450d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9450d-119">-DefaultProfile</span></span>
<span data-ttu-id="9450d-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9450d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9450d-121">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="9450d-121">-FailoverPolicy</span></span>
<span data-ttu-id="9450d-122">인스턴스 장애 조치 (Failover) 그룹의 장애 조치 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="9450d-122">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="9450d-123">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="9450d-123">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="9450d-124">기본 서버에서 작동 중지가 발생 하 고 데이터 손실 없이 장애 조치를 완료할 수 없는 경우 자동 장애 조치가 시작 되기 전의 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="9450d-124">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="9450d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9450d-125">-InputObject</span></span>
<span data-ttu-id="9450d-126">설정할 인스턴스 장애 조치 (Failover) 그룹 개체</span><span class="sxs-lookup"><span data-stu-id="9450d-126">The Instance Failover Group object to set</span></span>

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

### <span data-ttu-id="9450d-127">-위치</span><span class="sxs-lookup"><span data-stu-id="9450d-127">-Location</span></span>
<span data-ttu-id="9450d-128">인스턴스 장애 조치 (Failover) 그룹을 검색할 로컬 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9450d-128">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="9450d-129">-이름</span><span class="sxs-lookup"><span data-stu-id="9450d-129">-Name</span></span>
<span data-ttu-id="9450d-130">인스턴스 장애 조치 (Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9450d-130">The name of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="9450d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9450d-131">-ResourceGroupName</span></span>
<span data-ttu-id="9450d-132">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9450d-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="9450d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9450d-133">-ResourceId</span></span>
<span data-ttu-id="9450d-134">설정할 인스턴스 장애 조치 (Failover) 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9450d-134">The Resource ID of the Instance Failover Group to set.</span></span>

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

### <span data-ttu-id="9450d-135">-확인</span><span class="sxs-lookup"><span data-stu-id="9450d-135">-Confirm</span></span>
<span data-ttu-id="9450d-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9450d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9450d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9450d-137">-WhatIf</span></span>
<span data-ttu-id="9450d-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9450d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9450d-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9450d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9450d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9450d-140">CommonParameters</span></span>
<span data-ttu-id="9450d-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9450d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9450d-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9450d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9450d-143">입력</span><span class="sxs-lookup"><span data-stu-id="9450d-143">INPUTS</span></span>

### <span data-ttu-id="9450d-144">Microsoft. \*. AzureSqlInstanceFailoverGroupModel Failovergroup.</span><span class="sxs-lookup"><span data-stu-id="9450d-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="9450d-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9450d-145">System.String</span></span>

## <span data-ttu-id="9450d-146">출력</span><span class="sxs-lookup"><span data-stu-id="9450d-146">OUTPUTS</span></span>

### <span data-ttu-id="9450d-147">Microsoft. \*. AzureSqlInstanceFailoverGroupModel Failovergroup.</span><span class="sxs-lookup"><span data-stu-id="9450d-147">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="9450d-148">상속자</span><span class="sxs-lookup"><span data-stu-id="9450d-148">NOTES</span></span>

## <span data-ttu-id="9450d-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9450d-149">RELATED LINKS</span></span>
