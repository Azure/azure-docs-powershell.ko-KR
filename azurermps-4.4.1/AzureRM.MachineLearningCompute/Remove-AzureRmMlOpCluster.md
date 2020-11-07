---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 63e401c09a2d224b53d260855990198a409d4846
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703107"
---
# <span data-ttu-id="fbe16-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="fbe16-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="fbe16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbe16-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe16-103">Operationalization 클러스터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe16-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbe16-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fbe16-104">SYNTAX</span></span>

### <span data-ttu-id="fbe16-105">Cmdlet 입력 매개 변수에서 operationalization 클러스터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe16-105">Remove an operationalization cluster from cmdlet input parameters.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fbe16-106">OperationalizationCluster 인스턴스 정의에서 operationalization 클러스터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe16-106">Remove an operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fbe16-107">Azure 리소스 id에서 operationalization 클러스터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe16-107">Remove an operationalization cluster from an Azure resouce id.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="fbe16-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fbe16-108">DESCRIPTION</span></span>
<span data-ttu-id="fbe16-109">Operationalization 클러스터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe16-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="fbe16-110">클러스터와 연결 된 일부 리소스가 모두 제거 되지 않았을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe16-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="fbe16-111">예를 들어 Azure 컨테이너 서비스는 제거 되지만 연결 된 Vm에는 없는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fbe16-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="fbe16-112">저장소 계정, 컨테이너 레지스트리 및 application insights가 진단 정보에 대해서는 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe16-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="fbe16-113">예제의</span><span class="sxs-lookup"><span data-stu-id="fbe16-113">EXAMPLES</span></span>

### <span data-ttu-id="fbe16-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="fbe16-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="fbe16-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="fbe16-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster 
```

## <span data-ttu-id="fbe16-116">변수</span><span class="sxs-lookup"><span data-stu-id="fbe16-116">PARAMETERS</span></span>

### <span data-ttu-id="fbe16-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbe16-117">-InputObject</span></span>
<span data-ttu-id="fbe16-118">Operationalization cluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="fbe16-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Remove an operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe16-119">-확인</span><span class="sxs-lookup"><span data-stu-id="fbe16-119">-Confirm</span></span>
<span data-ttu-id="fbe16-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fbe16-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe16-121">-이름</span><span class="sxs-lookup"><span data-stu-id="fbe16-121">-Name</span></span>
<span data-ttu-id="fbe16-122">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbe16-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe16-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbe16-123">-ResourceGroupName</span></span>
<span data-ttu-id="fbe16-124">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fbe16-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe16-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbe16-125">-ResourceId</span></span>
<span data-ttu-id="fbe16-126">Operationalization 클러스터에 대 한 Azure 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="fbe16-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe16-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe16-127">-WhatIf</span></span>
<span data-ttu-id="fbe16-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fbe16-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbe16-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fbe16-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="fbe16-130">입력</span><span class="sxs-lookup"><span data-stu-id="fbe16-130">INPUTS</span></span>

### <span data-ttu-id="fbe16-131">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="fbe16-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="fbe16-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fbe16-132">System.String</span></span>


## <span data-ttu-id="fbe16-133">출력</span><span class="sxs-lookup"><span data-stu-id="fbe16-133">OUTPUTS</span></span>

### <span data-ttu-id="fbe16-134">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="fbe16-134">System.Void</span></span>


## <span data-ttu-id="fbe16-135">상속자</span><span class="sxs-lookup"><span data-stu-id="fbe16-135">NOTES</span></span>

## <span data-ttu-id="fbe16-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fbe16-136">RELATED LINKS</span></span>

