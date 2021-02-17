---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: d676958948b9197a64a08646e837287299107bfa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191156"
---
# <span data-ttu-id="e3520-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="e3520-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="e3520-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3520-102">SYNOPSIS</span></span>
<span data-ttu-id="e3520-103">클러스터 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e3520-103">Remove cluster resource.</span></span>

## <span data-ttu-id="e3520-104">구문</span><span class="sxs-lookup"><span data-stu-id="e3520-104">SYNTAX</span></span>

### <span data-ttu-id="e3520-105">ByObj(기본값)</span><span class="sxs-lookup"><span data-stu-id="e3520-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3520-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e3520-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3520-107">ById</span><span class="sxs-lookup"><span data-stu-id="e3520-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3520-108">설명</span><span class="sxs-lookup"><span data-stu-id="e3520-108">DESCRIPTION</span></span>
<span data-ttu-id="e3520-109">클러스터를 제거하면 클러스터의 노드 유형도 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3520-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="e3520-110">예제</span><span class="sxs-lookup"><span data-stu-id="e3520-110">EXAMPLES</span></span>

### <span data-ttu-id="e3520-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e3520-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="e3520-112">클러스터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e3520-112">Remove cluster.</span></span>

### <span data-ttu-id="e3520-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e3520-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="e3520-114">파이핑을 사용하여 클러스터를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e3520-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="e3520-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3520-115">PARAMETERS</span></span>

### <span data-ttu-id="e3520-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3520-116">-AsJob</span></span>
<span data-ttu-id="e3520-117">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="e3520-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e3520-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3520-118">-DefaultProfile</span></span>
<span data-ttu-id="e3520-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3520-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3520-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3520-120">-InputObject</span></span>
<span data-ttu-id="e3520-121">관리되는 클러스터 리소스</span><span class="sxs-lookup"><span data-stu-id="e3520-121">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3520-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e3520-122">-Name</span></span>
<span data-ttu-id="e3520-123">클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e3520-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3520-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3520-124">-PassThru</span></span>
<span data-ttu-id="e3520-125">{{ PassThru 설명 채우기 }}</span><span class="sxs-lookup"><span data-stu-id="e3520-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="e3520-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3520-126">-ResourceGroupName</span></span>
<span data-ttu-id="e3520-127">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e3520-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3520-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3520-128">-ResourceId</span></span>
<span data-ttu-id="e3520-129">관리되는 클러스터 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e3520-129">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3520-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3520-130">-Confirm</span></span>
<span data-ttu-id="e3520-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3520-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3520-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3520-132">-WhatIf</span></span>
<span data-ttu-id="e3520-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e3520-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3520-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3520-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3520-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3520-135">CommonParameters</span></span>
<span data-ttu-id="e3520-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3520-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3520-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3520-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3520-138">입력</span><span class="sxs-lookup"><span data-stu-id="e3520-138">INPUTS</span></span>

### <span data-ttu-id="e3520-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e3520-139">System.String</span></span>

## <span data-ttu-id="e3520-140">출력</span><span class="sxs-lookup"><span data-stu-id="e3520-140">OUTPUTS</span></span>

### <span data-ttu-id="e3520-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3520-141">System.Boolean</span></span>

## <span data-ttu-id="e3520-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e3520-142">NOTES</span></span>

## <span data-ttu-id="e3520-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3520-143">RELATED LINKS</span></span>
