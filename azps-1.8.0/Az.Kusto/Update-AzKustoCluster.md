---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 890ec07cecd46badaccc1c2140290fd8042d319b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867778"
---
# <span data-ttu-id="a24e0-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="a24e0-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="a24e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a24e0-102">SYNOPSIS</span></span>
<span data-ttu-id="a24e0-103">기존 Kusto 클러스터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a24e0-103">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="a24e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a24e0-104">SYNTAX</span></span>

### <span data-ttu-id="a24e0-105">ByNameAndResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="a24e0-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>] [-Capacity <Int32>]
 [-Tier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a24e0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a24e0-106">ByResourceId</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a24e0-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a24e0-107">ByInputObject</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-InputObject] <PSKustoCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a24e0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a24e0-108">DESCRIPTION</span></span>
<span data-ttu-id="a24e0-109">기존 Kusto 클러스터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a24e0-109">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="a24e0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a24e0-110">EXAMPLES</span></span>

### <span data-ttu-id="a24e0-111">예제 1-이름으로 기존 클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="a24e0-111">Example 1 - Update an existing cluster by name</span></span>

```
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Sku D14_v2

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Sku               : D14_v2
Capacity          : 5
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="a24e0-112">위 명령은 리소스 그룹 "testrg"에서 찾은 Kusto 클러스터 "mykustocluster"의 계층을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a24e0-112">The above command updates the tier of the Kusto cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="a24e0-113">예제 2-파이핑을 기준으로 기존 클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="a24e0-113">Example 2 - Update an existing cluster by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Update-AzKustoCluster -Sku D14_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D14_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="a24e0-114">위 명령에서는 cmdlet을 사용 하 여 리소스 그룹 "testrg"에 있는 Kusto 클러스터 "mykustocluster"를 가져온 `Get-AzKustoCluster` 다음 결과를 파이프 하 여 `Update-AzKustoCluster` 클러스터의 계층을 "standard"로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a24e0-114">The above command gets the Kusto cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Update-AzKustoCluster` to update the cluster's tier to "standard".</span></span>

## <span data-ttu-id="a24e0-115">변수</span><span class="sxs-lookup"><span data-stu-id="a24e0-115">PARAMETERS</span></span>

### <span data-ttu-id="a24e0-116">용량</span><span class="sxs-lookup"><span data-stu-id="a24e0-116">-Capacity</span></span>
<span data-ttu-id="a24e0-117">VM의 인스턴스 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="a24e0-117">The instance number of the VM.</span></span>

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

### <span data-ttu-id="a24e0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a24e0-118">-DefaultProfile</span></span>
<span data-ttu-id="a24e0-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a24e0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a24e0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a24e0-120">-InputObject</span></span>
<span data-ttu-id="a24e0-121">클러스터 개체를 위한 kusto</span><span class="sxs-lookup"><span data-stu-id="a24e0-121">Kusto cluster object.</span></span>

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

### <span data-ttu-id="a24e0-122">-이름</span><span class="sxs-lookup"><span data-stu-id="a24e0-122">-Name</span></span>
<span data-ttu-id="a24e0-123">업데이트할 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a24e0-123">Name of cluster to be updated.</span></span>

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

### <span data-ttu-id="a24e0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a24e0-124">-ResourceGroupName</span></span>
<span data-ttu-id="a24e0-125">클러스터가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a24e0-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="a24e0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a24e0-126">-ResourceId</span></span>
<span data-ttu-id="a24e0-127">클러스터 ResourceID에 대 한 kusto</span><span class="sxs-lookup"><span data-stu-id="a24e0-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="a24e0-128">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="a24e0-128">-SkuName</span></span>
<span data-ttu-id="a24e0-129">클러스터를 만드는 데 사용 되는 Sku의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a24e0-129">Name of the Sku used to create the cluster</span></span>

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

### <span data-ttu-id="a24e0-130">-티어</span><span class="sxs-lookup"><span data-stu-id="a24e0-130">-Tier</span></span>
<span data-ttu-id="a24e0-131">클러스터를 만드는 데 사용 되는 계층 이름</span><span class="sxs-lookup"><span data-stu-id="a24e0-131">Name of the Tier used to create the cluster</span></span>

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

### <span data-ttu-id="a24e0-132">-확인</span><span class="sxs-lookup"><span data-stu-id="a24e0-132">-Confirm</span></span>
<span data-ttu-id="a24e0-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a24e0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a24e0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a24e0-134">-WhatIf</span></span>
<span data-ttu-id="a24e0-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a24e0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a24e0-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a24e0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a24e0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a24e0-137">CommonParameters</span></span>
<span data-ttu-id="a24e0-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a24e0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a24e0-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a24e0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a24e0-140">입력</span><span class="sxs-lookup"><span data-stu-id="a24e0-140">INPUTS</span></span>

### <span data-ttu-id="a24e0-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a24e0-141">System.String</span></span>

### <span data-ttu-id="a24e0-142">PSKustoCluster를 위한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="a24e0-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="a24e0-143">출력</span><span class="sxs-lookup"><span data-stu-id="a24e0-143">OUTPUTS</span></span>

### <span data-ttu-id="a24e0-144">PSKustoCluster를 위한 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="a24e0-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="a24e0-145">상속자</span><span class="sxs-lookup"><span data-stu-id="a24e0-145">NOTES</span></span>

## <span data-ttu-id="a24e0-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a24e0-146">RELATED LINKS</span></span>
