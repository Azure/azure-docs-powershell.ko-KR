---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: fc89ff40c36fc444eec23089288849aa5ffe592c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537120"
---
# <span data-ttu-id="24b8c-101">Update-AzureRmMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="24b8c-101">Update-AzureRmMlOpClusterSystemService</span></span>

## <span data-ttu-id="24b8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="24b8c-103">Operationalization 클러스터의 시스템 서비스에서 업데이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b8c-103">Starts an update on the operationalization cluster's system services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24b8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24b8c-104">SYNTAX</span></span>

### <span data-ttu-id="24b8c-105">Cmdlet 입력 매개 변수에서 시스템 서비스 업데이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b8c-105">Start a system services update from cmdlet input parameters.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="24b8c-106">PSOperationalizationCluster 인스턴스 정의에서 시스템 서비스 업데이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b8c-106">Start a system services update from an PSOperationalizationCluster instance definition.</span></span>
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="24b8c-107">Azure 리소스 id에서 시스템 서비스 업데이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b8c-107">Start a system services update from an Azure resouce id.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="24b8c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="24b8c-108">DESCRIPTION</span></span>
<span data-ttu-id="24b8c-109">시스템 서비스는 operationalization 클러스터와 독립적으로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24b8c-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="24b8c-110">시스템 서비스에서 업데이트를 시작 하려면이 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b8c-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="24b8c-111">업데이트를 사용할 수 없는 경우 업데이트는 계속 시작 되 고 성공적으로 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24b8c-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="24b8c-112">업데이트가 완료 되 면 시작, 완료 및 성공한 경우 보고서를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b8c-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="24b8c-113">예제의</span><span class="sxs-lookup"><span data-stu-id="24b8c-113">EXAMPLES</span></span>

### <span data-ttu-id="24b8c-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="24b8c-114">Example 1</span></span>
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="24b8c-115">지정 된 클러스터에서 시스템 서비스 업데이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b8c-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="24b8c-116">변수</span><span class="sxs-lookup"><span data-stu-id="24b8c-116">PARAMETERS</span></span>

### <span data-ttu-id="24b8c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24b8c-117">-InputObject</span></span>
<span data-ttu-id="24b8c-118">Operationalization cluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="24b8c-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Start a system services update from an PSOperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24b8c-119">-확인</span><span class="sxs-lookup"><span data-stu-id="24b8c-119">-Confirm</span></span>
<span data-ttu-id="24b8c-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b8c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24b8c-121">-이름</span><span class="sxs-lookup"><span data-stu-id="24b8c-121">-Name</span></span>
<span data-ttu-id="24b8c-122">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24b8c-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b8c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24b8c-123">-ResourceGroupName</span></span>
<span data-ttu-id="24b8c-124">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24b8c-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24b8c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24b8c-125">-ResourceId</span></span>
<span data-ttu-id="24b8c-126">Operationalization 클러스터에 대 한 Azure 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="24b8c-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24b8c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24b8c-127">-WhatIf</span></span>
<span data-ttu-id="24b8c-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24b8c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24b8c-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24b8c-129">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="24b8c-130">입력</span><span class="sxs-lookup"><span data-stu-id="24b8c-130">INPUTS</span></span>

### <span data-ttu-id="24b8c-131">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="24b8c-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="24b8c-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24b8c-132">System.String</span></span>


## <span data-ttu-id="24b8c-133">출력</span><span class="sxs-lookup"><span data-stu-id="24b8c-133">OUTPUTS</span></span>

### <span data-ttu-id="24b8c-134">MachineLearningCompute. PSUpdateSystemServicesResponse/.</span><span class="sxs-lookup"><span data-stu-id="24b8c-134">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>


## <span data-ttu-id="24b8c-135">상속자</span><span class="sxs-lookup"><span data-stu-id="24b8c-135">NOTES</span></span>

## <span data-ttu-id="24b8c-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24b8c-136">RELATED LINKS</span></span>

