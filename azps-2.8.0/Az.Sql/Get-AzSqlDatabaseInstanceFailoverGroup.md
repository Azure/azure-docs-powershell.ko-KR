---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: dbb0cb56c50025e6b257d801957b1a75479220f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873709"
---
# <span data-ttu-id="d07dd-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d07dd-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="d07dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d07dd-102">SYNOPSIS</span></span>
<span data-ttu-id="d07dd-103">인스턴스 장애 조치 (Failover) 그룹을 가져오거나 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d07dd-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="d07dd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d07dd-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d07dd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d07dd-105">DESCRIPTION</span></span>
<span data-ttu-id="d07dd-106">특정 인스턴스 장애 조치 그룹을 가져오거나 사용자의 구독 아래에 있는 영역의 인스턴스 장애 조치 (Failover) 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="d07dd-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="d07dd-107">인스턴스 장애 조치 (Failover) 그룹의 두 영역 중 하나를 사용 하 여 명령을 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d07dd-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="d07dd-108">반환 된 값은 인스턴스 장애 조치 (Failover) 그룹과 관련 하 여 해당 영역의 관리 되는 인스턴스에 대 한 상태를 반영 합니다.</span><span class="sxs-lookup"><span data-stu-id="d07dd-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="d07dd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d07dd-109">EXAMPLES</span></span>

### <span data-ttu-id="d07dd-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d07dd-110">Example 1</span></span>
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

<span data-ttu-id="d07dd-111">영역의 모든 장애 조치 (Failover) 그룹 나열</span><span class="sxs-lookup"><span data-stu-id="d07dd-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="d07dd-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="d07dd-112">Example 2</span></span>
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

<span data-ttu-id="d07dd-113">특정 인스턴스 장애 조치 (Failover) 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d07dd-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="d07dd-114">변수</span><span class="sxs-lookup"><span data-stu-id="d07dd-114">PARAMETERS</span></span>

### <span data-ttu-id="d07dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d07dd-115">-DefaultProfile</span></span>
<span data-ttu-id="d07dd-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d07dd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d07dd-117">-위치</span><span class="sxs-lookup"><span data-stu-id="d07dd-117">-Location</span></span>
<span data-ttu-id="d07dd-118">인스턴스 장애 조치 (Failover) 그룹을 검색할 로컬 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d07dd-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="d07dd-119">-이름</span><span class="sxs-lookup"><span data-stu-id="d07dd-119">-Name</span></span>
<span data-ttu-id="d07dd-120">검색할 인스턴스 장애 조치 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d07dd-120">The name of the Instance Failover Group to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d07dd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d07dd-121">-ResourceGroupName</span></span>
<span data-ttu-id="d07dd-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d07dd-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="d07dd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d07dd-123">CommonParameters</span></span>
<span data-ttu-id="d07dd-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d07dd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d07dd-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d07dd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d07dd-126">입력</span><span class="sxs-lookup"><span data-stu-id="d07dd-126">INPUTS</span></span>

### <span data-ttu-id="d07dd-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d07dd-127">System.String</span></span>

## <span data-ttu-id="d07dd-128">출력</span><span class="sxs-lookup"><span data-stu-id="d07dd-128">OUTPUTS</span></span>

### <span data-ttu-id="d07dd-129">Microsoft. \*. AzureSqlInstanceFailoverGroupModel Failovergroup.</span><span class="sxs-lookup"><span data-stu-id="d07dd-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="d07dd-130">상속자</span><span class="sxs-lookup"><span data-stu-id="d07dd-130">NOTES</span></span>

## <span data-ttu-id="d07dd-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d07dd-131">RELATED LINKS</span></span>
