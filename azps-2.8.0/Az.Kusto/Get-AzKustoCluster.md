---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: c5c7cdffc8b329fdff426f48f60869ca6821f32d
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401354"
---
# <span data-ttu-id="eb9f9-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="eb9f9-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="eb9f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb9f9-102">SYNOPSIS</span></span>
<span data-ttu-id="eb9f9-103">리소스 그룹의 모든 Kusto 클러스터를 나열하거나 특정 Kusto 클러스터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eb9f9-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="eb9f9-104">구문</span><span class="sxs-lookup"><span data-stu-id="eb9f9-104">SYNTAX</span></span>

### <span data-ttu-id="eb9f9-105">ByClusterOrResourceGroupOrSubscription(기본값)</span><span class="sxs-lookup"><span data-stu-id="eb9f9-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb9f9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="eb9f9-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb9f9-107">설명</span><span class="sxs-lookup"><span data-stu-id="eb9f9-107">DESCRIPTION</span></span>
<span data-ttu-id="eb9f9-108">리소스 그룹의 모든 Kusto 클러스터를 나열하거나 특정 Kusto 클러스터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eb9f9-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="eb9f9-109">예제</span><span class="sxs-lookup"><span data-stu-id="eb9f9-109">EXAMPLES</span></span>

### <span data-ttu-id="eb9f9-110">예제 1 - 리소스 그룹의 모든 Kusto 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="eb9f9-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="eb9f9-111">형식 : Microsoft.Kusto/Clusters ID : /subscriptions/xxxxxxxxx-xxxx-xxxx-xxxx-xxx/resourceGroups/testrg/providers/Microsoft..Kusto/Clusters/mykustocluster1 ResourceGroup : testrg Name : mykustocluster1 Location : Central US Capacity : 3 Sku : D13_v2 ProvisioningState : Succeeded State : Running Tag : {} Uri : `https://mykustocluster1.centralus.kusto.windows.net` DataIngestionUri : `https://ingest-mykustocluster1.centralus.kusto.windows.net`</span><span class="sxs-lookup"><span data-stu-id="eb9f9-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : `https://mykustocluster1.centralus.kusto.windows.net` DataIngestionUri  : `https://ingest-mykustocluster1.centralus.kusto.windows.net`</span></span>

<span data-ttu-id="eb9f9-112">형식 : Microsoft.Kusto/Clusters ID : /subscriptions/xxxxxxxxx-xxxx-xxxx-xxxx-xxx/resourceGroups/testrg/providers/Microsoft..Kusto/Clusters/mykustocluster2 ResourceGroup : testrg Name : mykustocluster2 Location : Central US Capacity : 5 Sku : D13_v2 ProvisioningState : Succeeded State : Running Tag : {} Uri : `https://mykustocluster2.centralus.kusto.windows.net` DataIngestionUri : `https://ingest-mykustocluster2.centralus.kusto.windows.net`</span><span class="sxs-lookup"><span data-stu-id="eb9f9-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : `https://mykustocluster2.centralus.kusto.windows.net` DataIngestionUri  : `https://ingest-mykustocluster2.centralus.kusto.windows.net`</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="eb9f9-113">위의 명령은 리소스 그룹 "testrg"의 모든 Kusto 클러스터를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9f9-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="eb9f9-114">예제 2 - 이름으로 특정 Kusto 클러스터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eb9f9-114">Example 2 - Get a specific Kusto cluster by name</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="eb9f9-115">위의 명령은 리소스 그룹 "testrg"에서 "mykustocluster"라는 Kusto 클러스터를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9f9-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="eb9f9-116">예제 3 - 리소스 ID로 특정 Kusto 클러스터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="eb9f9-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/clusters/mykustocluster
Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="eb9f9-117">위의 명령은 리소스 그룹 "testrg"에서 "mykustocluster"라는 Kusto 클러스터를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9f9-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="eb9f9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb9f9-118">PARAMETERS</span></span>

### <span data-ttu-id="eb9f9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb9f9-119">-DefaultProfile</span></span>
<span data-ttu-id="eb9f9-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eb9f9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb9f9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="eb9f9-121">-Name</span></span>
<span data-ttu-id="eb9f9-122">특정 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb9f9-122">Name of a specific cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9f9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb9f9-123">-ResourceGroupName</span></span>
<span data-ttu-id="eb9f9-124">사용자가 클러스터를 검색하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eb9f9-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

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

### <span data-ttu-id="eb9f9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb9f9-125">-ResourceId</span></span>
<span data-ttu-id="eb9f9-126">Kusto 클러스터 ResourceID.</span><span class="sxs-lookup"><span data-stu-id="eb9f9-126">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="eb9f9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb9f9-127">CommonParameters</span></span>
<span data-ttu-id="eb9f9-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="eb9f9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb9f9-129">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="eb9f9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb9f9-130">입력</span><span class="sxs-lookup"><span data-stu-id="eb9f9-130">INPUTS</span></span>

### <span data-ttu-id="eb9f9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="eb9f9-131">System.String</span></span>

## <span data-ttu-id="eb9f9-132">출력</span><span class="sxs-lookup"><span data-stu-id="eb9f9-132">OUTPUTS</span></span>

### <span data-ttu-id="eb9f9-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="eb9f9-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="eb9f9-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="eb9f9-134">NOTES</span></span>

## <span data-ttu-id="eb9f9-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eb9f9-135">RELATED LINKS</span></span>
