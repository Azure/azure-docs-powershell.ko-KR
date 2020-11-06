---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: 4dfa855bba7318e85eb855e35227070a55d4ed73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534008"
---
# <span data-ttu-id="26403-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="26403-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="26403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26403-102">SYNOPSIS</span></span>
<span data-ttu-id="26403-103">Operationalization 클러스터와 연결 된 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26403-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26403-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26403-104">SYNTAX</span></span>

### <span data-ttu-id="26403-105">Cmdlet 입력 매개 변수에서 operationalization 클러스터의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26403-105">Get operationalization cluster's keys from cmdlet input parameters.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="26403-106">OperationalizationCluster 인스턴스 정의에서 operationalization 클러스터의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26403-106">Get operationalization cluster's keys from an OperationalizationCluster instance definition.</span></span>
```
Get-AzureRmMlOpClusterKey -Cluster <PSOperationalizationCluster>
```

### <span data-ttu-id="26403-107">Azure 리소스 id에서 operationalization 클러스터의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26403-107">Get operationalization cluster's keys from an Azure resource id.</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String>
```

## <span data-ttu-id="26403-108">설명은</span><span class="sxs-lookup"><span data-stu-id="26403-108">DESCRIPTION</span></span>
<span data-ttu-id="26403-109">클러스터 속성을 가져올 때 저장소 계정, 컨테이너 레지스트리 및 operationalization 클러스터와 연결 된 기타 서비스의 키가 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26403-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="26403-110">키를 검색 하기 위한 특정 호출은 중요 한 정보 이기 때문에 이루어져야 합니다.</span><span class="sxs-lookup"><span data-stu-id="26403-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="26403-111">예제의</span><span class="sxs-lookup"><span data-stu-id="26403-111">EXAMPLES</span></span>

### <span data-ttu-id="26403-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="26403-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="26403-113">Operationalization 클러스터와 연결 된 서비스에 대 한 비밀 키를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="26403-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="26403-114">변수</span><span class="sxs-lookup"><span data-stu-id="26403-114">PARAMETERS</span></span>

### <span data-ttu-id="26403-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26403-115">-InputObject</span></span>
<span data-ttu-id="26403-116">Operationalization cluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="26403-116">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Get operationalization cluster's keys from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26403-117">-이름</span><span class="sxs-lookup"><span data-stu-id="26403-117">-Name</span></span>
<span data-ttu-id="26403-118">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26403-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26403-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26403-119">-ResourceGroupName</span></span>
<span data-ttu-id="26403-120">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26403-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26403-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26403-121">-ResourceId</span></span>
<span data-ttu-id="26403-122">Operationalization 클러스터에 대 한 Azure 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="26403-122">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get operationalization cluster's keys from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="26403-123">입력</span><span class="sxs-lookup"><span data-stu-id="26403-123">INPUTS</span></span>

### <span data-ttu-id="26403-124">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="26403-124">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="26403-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="26403-125">System.String</span></span>


## <span data-ttu-id="26403-126">출력</span><span class="sxs-lookup"><span data-stu-id="26403-126">OUTPUTS</span></span>

### <span data-ttu-id="26403-127">MachineLearningCompute. PSOperationalizationClusterCredentials/.</span><span class="sxs-lookup"><span data-stu-id="26403-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>


## <span data-ttu-id="26403-128">상속자</span><span class="sxs-lookup"><span data-stu-id="26403-128">NOTES</span></span>

## <span data-ttu-id="26403-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26403-129">RELATED LINKS</span></span>

