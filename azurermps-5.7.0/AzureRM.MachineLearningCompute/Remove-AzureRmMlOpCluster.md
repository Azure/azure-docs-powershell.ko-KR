---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/remove-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 9836856ffd663939de8ca0e28635d81785c9c898
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93711926"
---
# <span data-ttu-id="466e3-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="466e3-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="466e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="466e3-102">SYNOPSIS</span></span>
<span data-ttu-id="466e3-103">Operationalization 클러스터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="466e3-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="466e3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="466e3-104">SYNTAX</span></span>

### <span data-ttu-id="466e3-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="466e3-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeAllResources] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="466e3-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="466e3-106">RemoveByInputObject</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeAllResources] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="466e3-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="466e3-107">RemoveByResourceId</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeAllResources] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="466e3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="466e3-108">DESCRIPTION</span></span>
<span data-ttu-id="466e3-109">Operationalization 클러스터를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="466e3-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="466e3-110">클러스터와 연결 된 일부 리소스가 모두 제거 되지 않았을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="466e3-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="466e3-111">예를 들어 Azure 컨테이너 서비스는 제거 되지만 연결 된 Vm에는 없는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="466e3-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="466e3-112">저장소 계정, 컨테이너 레지스트리 및 application insights가 진단 정보에 대해서는 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="466e3-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="466e3-113">예제의</span><span class="sxs-lookup"><span data-stu-id="466e3-113">EXAMPLES</span></span>

### <span data-ttu-id="466e3-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="466e3-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="466e3-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="466e3-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster
```

## <span data-ttu-id="466e3-116">변수</span><span class="sxs-lookup"><span data-stu-id="466e3-116">PARAMETERS</span></span>

### <span data-ttu-id="466e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="466e3-117">-DefaultProfile</span></span>
<span data-ttu-id="466e3-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="466e3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="466e3-119">-IncludeAllResources 리소스</span><span class="sxs-lookup"><span data-stu-id="466e3-119">-IncludeAllResources</span></span>
<span data-ttu-id="466e3-120">클러스터를 사용 하 여 만든 모든 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="466e3-120">Removes all resources that were created with the cluster.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="466e3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="466e3-121">-InputObject</span></span>
<span data-ttu-id="466e3-122">Operationalization cluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="466e3-122">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: RemoveByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="466e3-123">-이름</span><span class="sxs-lookup"><span data-stu-id="466e3-123">-Name</span></span>
<span data-ttu-id="466e3-124">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="466e3-124">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="466e3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="466e3-125">-ResourceGroupName</span></span>
<span data-ttu-id="466e3-126">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="466e3-126">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="466e3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="466e3-127">-ResourceId</span></span>
<span data-ttu-id="466e3-128">Operationalization 클러스터에 대 한 Azure 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="466e3-128">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="466e3-129">-확인</span><span class="sxs-lookup"><span data-stu-id="466e3-129">-Confirm</span></span>
<span data-ttu-id="466e3-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="466e3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="466e3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="466e3-131">-WhatIf</span></span>
<span data-ttu-id="466e3-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="466e3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="466e3-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="466e3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="466e3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="466e3-134">CommonParameters</span></span>
<span data-ttu-id="466e3-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="466e3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="466e3-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="466e3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="466e3-137">입력</span><span class="sxs-lookup"><span data-stu-id="466e3-137">INPUTS</span></span>

### <span data-ttu-id="466e3-138">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="466e3-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="466e3-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="466e3-139">System.String</span></span>

## <span data-ttu-id="466e3-140">출력</span><span class="sxs-lookup"><span data-stu-id="466e3-140">OUTPUTS</span></span>

### <span data-ttu-id="466e3-141">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="466e3-141">System.Void</span></span>

## <span data-ttu-id="466e3-142">상속자</span><span class="sxs-lookup"><span data-stu-id="466e3-142">NOTES</span></span>

## <span data-ttu-id="466e3-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="466e3-143">RELATED LINKS</span></span>

