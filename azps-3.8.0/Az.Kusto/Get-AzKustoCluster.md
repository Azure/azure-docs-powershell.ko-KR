---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: 6e24eaee77e8965ea34cbfcd8c169d675bce56d8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034596"
---
# <span data-ttu-id="26fd5-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="26fd5-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="26fd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26fd5-102">SYNOPSIS</span></span>
<span data-ttu-id="26fd5-103">모든 Kusto 리소스 그룹의 클러스터를 나열 하거나 특정 kusto 클러스터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26fd5-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="26fd5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26fd5-104">SYNTAX</span></span>

### <span data-ttu-id="26fd5-105">Byclusterorresourcegrou구독 (기본값)</span><span class="sxs-lookup"><span data-stu-id="26fd5-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26fd5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="26fd5-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26fd5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="26fd5-107">DESCRIPTION</span></span>
<span data-ttu-id="26fd5-108">모든 Kusto 리소스 그룹의 클러스터를 나열 하거나 특정 kusto 클러스터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26fd5-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="26fd5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="26fd5-109">EXAMPLES</span></span>

### <span data-ttu-id="26fd5-110">예제 1-리소스 그룹에 모든 Kusto 클러스터 나열</span><span class="sxs-lookup"><span data-stu-id="26fd5-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="26fd5-111">유형: Microsoft. Kusto/클러스터 Id:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup: testrg Name: mykustocluster1 Location: 중부 US 용량: 3 Sku: D13_v2 ProvisioningState: 성공 상태: 실행 태그: {} Uri: https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster1.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="26fd5-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net</span></span>

<span data-ttu-id="26fd5-112">유형: Microsoft. Kusto/클러스터 Id:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup: testrg Name: mykustocluster2 Location: 중부 US 용량: 5 Sku: D13_v2 ProvisioningState: 성공 상태: 실행 태그: {} Uri: https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster2.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="26fd5-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster2.centralus.kusto.windows.net</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="26fd5-113">위의 명령은 리소스 그룹 "testrg"에 모든 Kusto 클러스터를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="26fd5-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="26fd5-114">예제 2-이름으로 특정 Kusto 클러스터 가져오기</span><span class="sxs-lookup"><span data-stu-id="26fd5-114">Example 2 - Get a specific Kusto cluster by name</span></span>

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

<span data-ttu-id="26fd5-115">위의 명령은 리소스 그룹 "testrg"에서 "mykustocluster" 이라는 Kusto 클러스터를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="26fd5-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="26fd5-116">예제 3-리소스 id를 기준으로 특정 Kusto 클러스터 가져오기</span><span class="sxs-lookup"><span data-stu-id="26fd5-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

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

<span data-ttu-id="26fd5-117">위의 명령은 리소스 그룹 "testrg"에서 "mykustocluster" 이라는 Kusto 클러스터를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="26fd5-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="26fd5-118">변수</span><span class="sxs-lookup"><span data-stu-id="26fd5-118">PARAMETERS</span></span>

### <span data-ttu-id="26fd5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26fd5-119">-DefaultProfile</span></span>
<span data-ttu-id="26fd5-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26fd5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26fd5-121">-이름</span><span class="sxs-lookup"><span data-stu-id="26fd5-121">-Name</span></span>
<span data-ttu-id="26fd5-122">특정 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26fd5-122">Name of a specific cluster.</span></span>

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

### <span data-ttu-id="26fd5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26fd5-123">-ResourceGroupName</span></span>
<span data-ttu-id="26fd5-124">사용자가 클러스터를 검색 하려는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26fd5-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

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

### <span data-ttu-id="26fd5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26fd5-125">-ResourceId</span></span>
<span data-ttu-id="26fd5-126">클러스터 ResourceID에 대 한 kusto</span><span class="sxs-lookup"><span data-stu-id="26fd5-126">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="26fd5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26fd5-127">CommonParameters</span></span>
<span data-ttu-id="26fd5-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26fd5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26fd5-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26fd5-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26fd5-130">입력</span><span class="sxs-lookup"><span data-stu-id="26fd5-130">INPUTS</span></span>

### <span data-ttu-id="26fd5-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="26fd5-131">System.String</span></span>

## <span data-ttu-id="26fd5-132">출력</span><span class="sxs-lookup"><span data-stu-id="26fd5-132">OUTPUTS</span></span>

### <span data-ttu-id="26fd5-133">PSKustoCluster를 위한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="26fd5-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="26fd5-134">상속자</span><span class="sxs-lookup"><span data-stu-id="26fd5-134">NOTES</span></span>

## <span data-ttu-id="26fd5-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26fd5-135">RELATED LINKS</span></span>
