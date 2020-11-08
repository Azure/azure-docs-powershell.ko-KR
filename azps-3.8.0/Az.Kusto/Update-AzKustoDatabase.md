---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: 858578d36f2f913f903f86b9c556a93d30e2e3b3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034576"
---
# <span data-ttu-id="764d1-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="764d1-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="764d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="764d1-102">SYNOPSIS</span></span>
<span data-ttu-id="764d1-103">기존 Kusto를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="764d1-103">Update an existing Kusto database.</span></span>

## <span data-ttu-id="764d1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="764d1-104">SYNTAX</span></span>

### <span data-ttu-id="764d1-105">ByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="764d1-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="764d1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="764d1-106">ByResourceId</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="764d1-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="764d1-107">ByInputObject</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>]
 [-InputObject] <PSKustoDatabase> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="764d1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="764d1-108">DESCRIPTION</span></span>
<span data-ttu-id="764d1-109">기존 Kusto를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="764d1-109">Update an existing Kusto database.</span></span>

## <span data-ttu-id="764d1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="764d1-110">EXAMPLES</span></span>

### <span data-ttu-id="764d1-111">예제 1-이름으로 기존 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="764d1-111">Example 1 - Update an existing database by name</span></span>

```
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="764d1-112">위 명령은 리소스 그룹 "testrg"에 있는 클러스터 "mykustocluster"의 Kusto 삭제 기간을 "mykustodatabase" 데이터베이스에 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="764d1-112">The above command updates the soft deletion period of the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="764d1-113">예제 2-파이핑을 통해 기존 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="764d1-113">Example 2 - Update an existing database by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Update-AzKustoDatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="764d1-114">위 명령에서는 cmdlet을 사용 하 여 리소스 그룹 "testrg"에 있는 "mykustocluster" 클러스터의 Kusto database "mykustodatabase"를 가져온 `Get-AzKustoDatabase` 다음 결과를 파이프 하 여 `Update-AzKustoDatabase` 데이터베이스의 소프트 삭제 기간을 5 일로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="764d1-114">The above command gets the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Update-AzKustoDatabase` to update the database's soft deletion period to five days.</span></span>

## <span data-ttu-id="764d1-115">변수</span><span class="sxs-lookup"><span data-stu-id="764d1-115">PARAMETERS</span></span>

### <span data-ttu-id="764d1-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="764d1-116">-ClusterName</span></span>
<span data-ttu-id="764d1-117">데이터베이스가 있는 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="764d1-117">Name of cluster under which the database exists</span></span>

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

### <span data-ttu-id="764d1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="764d1-118">-DefaultProfile</span></span>
<span data-ttu-id="764d1-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="764d1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="764d1-120">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="764d1-120">-HotCachePeriodInDays</span></span>
<span data-ttu-id="764d1-121">빠른 쿼리를 위해 캐시에 데이터를 유지 해야 하는 날짜 수입니다.</span><span class="sxs-lookup"><span data-stu-id="764d1-121">The number of days that data should be kept in cache for fast queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="764d1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="764d1-122">-InputObject</span></span>
<span data-ttu-id="764d1-123">데이터베이스 개체에는 kusto가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="764d1-123">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="764d1-124">-이름</span><span class="sxs-lookup"><span data-stu-id="764d1-124">-Name</span></span>
<span data-ttu-id="764d1-125">업데이트할 데이터베이스의 이름</span><span class="sxs-lookup"><span data-stu-id="764d1-125">Name of the database to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="764d1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="764d1-126">-ResourceGroupName</span></span>
<span data-ttu-id="764d1-127">클러스터가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="764d1-127">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="764d1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="764d1-128">-ResourceId</span></span>
<span data-ttu-id="764d1-129">데이터베이스 ResourceID에 대 한 kusto</span><span class="sxs-lookup"><span data-stu-id="764d1-129">Kusto database ResourceID.</span></span>

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

### <span data-ttu-id="764d1-130">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="764d1-130">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="764d1-131">데이터에 대 한 액세스를 중지 하기 전에 유지 해야 하는 날짜 수입니다.</span><span class="sxs-lookup"><span data-stu-id="764d1-131">The number of days that data should be kept before it stops being accessible to queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="764d1-132">-확인</span><span class="sxs-lookup"><span data-stu-id="764d1-132">-Confirm</span></span>
<span data-ttu-id="764d1-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="764d1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="764d1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="764d1-134">-WhatIf</span></span>
<span data-ttu-id="764d1-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="764d1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="764d1-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="764d1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="764d1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="764d1-137">CommonParameters</span></span>
<span data-ttu-id="764d1-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="764d1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="764d1-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="764d1-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="764d1-140">입력</span><span class="sxs-lookup"><span data-stu-id="764d1-140">INPUTS</span></span>

### <span data-ttu-id="764d1-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="764d1-141">System.String</span></span>

### <span data-ttu-id="764d1-142">PSKustoDatabase를 위한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="764d1-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="764d1-143">출력</span><span class="sxs-lookup"><span data-stu-id="764d1-143">OUTPUTS</span></span>

### <span data-ttu-id="764d1-144">PSKustoDatabase를 위한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="764d1-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="764d1-145">상속자</span><span class="sxs-lookup"><span data-stu-id="764d1-145">NOTES</span></span>

## <span data-ttu-id="764d1-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="764d1-146">RELATED LINKS</span></span>
