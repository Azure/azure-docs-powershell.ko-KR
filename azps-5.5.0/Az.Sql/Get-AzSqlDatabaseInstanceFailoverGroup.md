---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: bd2a157a1fb05baf0fa6e02b061462718ffad314
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188961"
---
# <span data-ttu-id="ccca4-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ccca4-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="ccca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccca4-102">SYNOPSIS</span></span>
<span data-ttu-id="ccca4-103">인스턴스 장애 조치(failover) 그룹을 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ccca4-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="ccca4-104">구문</span><span class="sxs-lookup"><span data-stu-id="ccca4-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccca4-105">설명</span><span class="sxs-lookup"><span data-stu-id="ccca4-105">DESCRIPTION</span></span>
<span data-ttu-id="ccca4-106">특정 인스턴스 장애 조치(failover) 그룹을 얻거나 사용자의 구독에 속한 지역의 인스턴스 장애 조치(failover) 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ccca4-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="ccca4-107">인스턴스 장애 조치 그룹의 두 지역 중 하나를 사용하여 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ccca4-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="ccca4-108">반환된 값은 인스턴스 장애 조치(failover) 그룹과 관련한 해당 지역의 Managed Instance 상태를 반영합니다.</span><span class="sxs-lookup"><span data-stu-id="ccca4-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="ccca4-109">예제</span><span class="sxs-lookup"><span data-stu-id="ccca4-109">EXAMPLES</span></span>

### <span data-ttu-id="ccca4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ccca4-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location
Output:
{
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
}
```

<span data-ttu-id="ccca4-111">지역의 모든 장애 조치(failover) 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ccca4-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="ccca4-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="ccca4-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg
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

<span data-ttu-id="ccca4-113">특정 인스턴스 장애 조치(failover) 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ccca4-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="ccca4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccca4-114">PARAMETERS</span></span>

### <span data-ttu-id="ccca4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccca4-115">-DefaultProfile</span></span>
<span data-ttu-id="ccca4-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ccca4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccca4-117">-Location</span><span class="sxs-lookup"><span data-stu-id="ccca4-117">-Location</span></span>
<span data-ttu-id="ccca4-118">인스턴스 장애 조치(failover) 그룹을 검색할 로컬 지역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ccca4-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="ccca4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ccca4-119">-Name</span></span>
<span data-ttu-id="ccca4-120">검색할 인스턴스 장애 조치 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ccca4-120">The name of the Instance Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccca4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccca4-121">-ResourceGroupName</span></span>
<span data-ttu-id="ccca4-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ccca4-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="ccca4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccca4-123">CommonParameters</span></span>
<span data-ttu-id="ccca4-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ccca4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccca4-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ccca4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccca4-126">입력</span><span class="sxs-lookup"><span data-stu-id="ccca4-126">INPUTS</span></span>

### <span data-ttu-id="ccca4-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ccca4-127">System.String</span></span>

## <span data-ttu-id="ccca4-128">출력</span><span class="sxs-lookup"><span data-stu-id="ccca4-128">OUTPUTS</span></span>

### <span data-ttu-id="ccca4-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="ccca4-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="ccca4-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ccca4-130">NOTES</span></span>

## <span data-ttu-id="ccca4-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccca4-131">RELATED LINKS</span></span>
