---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: 98936051ba3faa06d611fc8509faaa2b26998d29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689571"
---
# <span data-ttu-id="11ca6-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="11ca6-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="11ca6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="11ca6-103">모든 Kusto 클러스터의 데이터베이스를 나열 하거나 특정 Kusto 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11ca6-103">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="11ca6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11ca6-104">SYNTAX</span></span>

### <span data-ttu-id="11ca6-105">Byclusterorresourcegrou구독 (기본값)</span><span class="sxs-lookup"><span data-stu-id="11ca6-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoDatabase -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11ca6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="11ca6-106">ByResourceId</span></span>
```
Get-AzKustoDatabase [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="11ca6-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="11ca6-107">ByInputObject</span></span>
```
Get-AzKustoDatabase [-Name <String>] -InputObject <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11ca6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="11ca6-108">DESCRIPTION</span></span>
<span data-ttu-id="11ca6-109">모든 Kusto 클러스터의 데이터베이스를 나열 하거나 특정 Kusto 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="11ca6-109">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="11ca6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="11ca6-110">EXAMPLES</span></span>

### <span data-ttu-id="11ca6-111">예제 1-클러스터의 모든 Kname을 이름으로 하 여 데이터베이스에 나열</span><span class="sxs-lookup"><span data-stu-id="11ca6-111">Example 1 - List all Kusto databases in a cluster by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster

Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="11ca6-112">위의 명령은 리소스 그룹 "testrg"에 있는 "mykustocluster" 클러스터의 모든 Kusto 데이터베이스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ca6-112">The above command returns all Kusto databases in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="11ca6-113">예제 2-파이프를 기준으로 클러스터의 모든 데이터베이스에 모든 Kusto</span><span class="sxs-lookup"><span data-stu-id="11ca6-113">Example 2 - List all Kusto databases in a cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Get-AzKustoDatabase
Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="11ca6-114">위의 명령에서는 cmdlet을 사용 하 여 리소스 그룹 "testrg"에 있는 "mykustocluster" 이라는 이름의 클러스터에 대 한 Kusto를 가져오고 `Get-AzKustoCluster` , 결과를 cmdlet에 파이프 하 여 `Get-AzKustoDatabase` 해당 클러스터의 모든 데이터베이스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ca6-114">The above command will get the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and pipe the result to the `Get-AzKustoDatabase` cmdlet to list all databases in that cluster.</span></span>

### <span data-ttu-id="11ca6-115">예제 3-이름으로 특정 Kusto 데이터베이스 가져오기</span><span class="sxs-lookup"><span data-stu-id="11ca6-115">Example 3 - Get a specific Kusto database by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="11ca6-116">위 명령은 리소스 그룹 "testrg"에 있는 클러스터 "mykustocluster"에 있는 "mykustodatabase" 이라는 Kusto 데이터베이스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ca6-116">The above command returns the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="11ca6-117">변수</span><span class="sxs-lookup"><span data-stu-id="11ca6-117">PARAMETERS</span></span>

### <span data-ttu-id="11ca6-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="11ca6-118">-ClusterName</span></span>
<span data-ttu-id="11ca6-119">데이터베이스가 있는 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11ca6-119">Name of cluster under which the database exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11ca6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11ca6-120">-DefaultProfile</span></span>
<span data-ttu-id="11ca6-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11ca6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11ca6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11ca6-122">-InputObject</span></span>
<span data-ttu-id="11ca6-123">클러스터 개체를 위한 kusto</span><span class="sxs-lookup"><span data-stu-id="11ca6-123">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11ca6-124">-이름</span><span class="sxs-lookup"><span data-stu-id="11ca6-124">-Name</span></span>
<span data-ttu-id="11ca6-125">데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11ca6-125">the name of the database.</span></span>

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

### <span data-ttu-id="11ca6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11ca6-126">-ResourceGroupName</span></span>
<span data-ttu-id="11ca6-127">사용자가 클러스터를 검색 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11ca6-127">Name of resource group under which the user wants to retrieve the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11ca6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11ca6-128">-ResourceId</span></span>
<span data-ttu-id="11ca6-129">클러스터 ResourceID에 대 한 kusto</span><span class="sxs-lookup"><span data-stu-id="11ca6-129">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11ca6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11ca6-130">CommonParameters</span></span>
<span data-ttu-id="11ca6-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11ca6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11ca6-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11ca6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11ca6-133">입력</span><span class="sxs-lookup"><span data-stu-id="11ca6-133">INPUTS</span></span>

### <span data-ttu-id="11ca6-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="11ca6-134">System.String</span></span>

### <span data-ttu-id="11ca6-135">PSKustoCluster를 위한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="11ca6-135">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="11ca6-136">출력</span><span class="sxs-lookup"><span data-stu-id="11ca6-136">OUTPUTS</span></span>

### <span data-ttu-id="11ca6-137">PSKustoDatabase를 위한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="11ca6-137">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="11ca6-138">상속자</span><span class="sxs-lookup"><span data-stu-id="11ca6-138">NOTES</span></span>

## <span data-ttu-id="11ca6-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11ca6-139">RELATED LINKS</span></span>
