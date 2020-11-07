---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: 33272012d81160a055bcd5d1eb0ef617787eed1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867810"
---
# <span data-ttu-id="24fbe-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="24fbe-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="24fbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24fbe-102">SYNOPSIS</span></span>
<span data-ttu-id="24fbe-103">기존 클러스터에 새 Kusto 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24fbe-103">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="24fbe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24fbe-104">SYNTAX</span></span>

### <span data-ttu-id="24fbe-105">ByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="24fbe-105">ByNameAndResourceGroup (Default)</span></span>
```
New-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fbe-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="24fbe-106">ByResourceId</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24fbe-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="24fbe-107">ByInputObject</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-InputObject] <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="24fbe-108">설명은</span><span class="sxs-lookup"><span data-stu-id="24fbe-108">DESCRIPTION</span></span>
<span data-ttu-id="24fbe-109">기존 클러스터에 새 Kusto 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24fbe-109">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="24fbe-110">예제의</span><span class="sxs-lookup"><span data-stu-id="24fbe-110">EXAMPLES</span></span>

### <span data-ttu-id="24fbe-111">예제 1-이름으로 새 Kusto 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="24fbe-111">Example 1 - Create a new Kusto database by name</span></span>

```
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 4 -HotCachePeriodInDays 2

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 4
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="24fbe-112">위의 명령은 리소스 그룹 "testrg"에 있는 기존 클러스터 "mykustocluster"에 "mykustodatabase" 이라는 새 Kusto 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24fbe-112">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="24fbe-113">변수</span><span class="sxs-lookup"><span data-stu-id="24fbe-113">PARAMETERS</span></span>

### <span data-ttu-id="24fbe-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="24fbe-114">-ClusterName</span></span>
<span data-ttu-id="24fbe-115">데이터베이스를 만드는 데 사용할 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24fbe-115">Name of cluster under which you want to create the database.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fbe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24fbe-116">-DefaultProfile</span></span>
<span data-ttu-id="24fbe-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24fbe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24fbe-118">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="24fbe-118">-HotCachePeriodInDays</span></span>
<span data-ttu-id="24fbe-119">빠른 쿼리를 위해 캐시에 유지할 데이터 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="24fbe-119">The number of days of data that should be kept in cache for fast queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fbe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24fbe-120">-InputObject</span></span>
<span data-ttu-id="24fbe-121">클러스터 개체를 위한 kusto</span><span class="sxs-lookup"><span data-stu-id="24fbe-121">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24fbe-122">-이름</span><span class="sxs-lookup"><span data-stu-id="24fbe-122">-Name</span></span>
<span data-ttu-id="24fbe-123">만들 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24fbe-123">Name of the database to be created.</span></span>

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

### <span data-ttu-id="24fbe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24fbe-124">-ResourceGroupName</span></span>
<span data-ttu-id="24fbe-125">클러스터가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24fbe-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fbe-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24fbe-126">-ResourceId</span></span>
<span data-ttu-id="24fbe-127">클러스터 ResourceID에 대 한 kusto</span><span class="sxs-lookup"><span data-stu-id="24fbe-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24fbe-128">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="24fbe-128">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="24fbe-129">쿼리에 대 한 액세스를 중지 하기 전에 데이터를 유지 해야 하는 날짜 수입니다.</span><span class="sxs-lookup"><span data-stu-id="24fbe-129">The number of days data should be kept before it stops being accessible to queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fbe-130">-확인</span><span class="sxs-lookup"><span data-stu-id="24fbe-130">-Confirm</span></span>
<span data-ttu-id="24fbe-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24fbe-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24fbe-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24fbe-132">-WhatIf</span></span>
<span data-ttu-id="24fbe-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24fbe-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24fbe-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24fbe-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24fbe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24fbe-135">CommonParameters</span></span>
<span data-ttu-id="24fbe-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24fbe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24fbe-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24fbe-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24fbe-138">입력</span><span class="sxs-lookup"><span data-stu-id="24fbe-138">INPUTS</span></span>

### <span data-ttu-id="24fbe-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24fbe-139">System.String</span></span>

### <span data-ttu-id="24fbe-140">PSKustoCluster를 위한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="24fbe-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="24fbe-141">출력</span><span class="sxs-lookup"><span data-stu-id="24fbe-141">OUTPUTS</span></span>

### <span data-ttu-id="24fbe-142">PSKustoDatabase를 위한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="24fbe-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="24fbe-143">상속자</span><span class="sxs-lookup"><span data-stu-id="24fbe-143">NOTES</span></span>

## <span data-ttu-id="24fbe-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24fbe-144">RELATED LINKS</span></span>
