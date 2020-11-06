---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpClusterKey.md
ms.openlocfilehash: cdf8c04a3d3b3b9fc50e571642bc14352d976b84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532776"
---
# <span data-ttu-id="5d6ab-101">Get-AzureRmMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="5d6ab-101">Get-AzureRmMlOpClusterKey</span></span>

## <span data-ttu-id="5d6ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d6ab-102">SYNOPSIS</span></span>
<span data-ttu-id="5d6ab-103">Operationalization 클러스터와 연결 된 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d6ab-103">Gets the access keys associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d6ab-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5d6ab-104">SYNTAX</span></span>

### <span data-ttu-id="5d6ab-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5d6ab-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d6ab-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="5d6ab-106">GetByInputObject</span></span>
```
Get-AzureRmMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d6ab-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5d6ab-107">GetByResourceId</span></span>
```
Get-AzureRmMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d6ab-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5d6ab-108">DESCRIPTION</span></span>
<span data-ttu-id="5d6ab-109">클러스터 속성을 가져올 때 저장소 계정, 컨테이너 레지스트리 및 operationalization 클러스터와 연결 된 기타 서비스의 키가 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d6ab-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="5d6ab-110">키를 검색 하기 위한 특정 호출은 중요 한 정보 이기 때문에 이루어져야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d6ab-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="5d6ab-111">예제의</span><span class="sxs-lookup"><span data-stu-id="5d6ab-111">EXAMPLES</span></span>

### <span data-ttu-id="5d6ab-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="5d6ab-112">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="5d6ab-113">Operationalization 클러스터와 연결 된 서비스에 대 한 비밀 키를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d6ab-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="5d6ab-114">변수</span><span class="sxs-lookup"><span data-stu-id="5d6ab-114">PARAMETERS</span></span>

### <span data-ttu-id="5d6ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d6ab-115">-DefaultProfile</span></span>
<span data-ttu-id="5d6ab-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d6ab-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d6ab-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d6ab-117">-InputObject</span></span>
<span data-ttu-id="5d6ab-118">Operationalization cluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5d6ab-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: GetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d6ab-119">-이름</span><span class="sxs-lookup"><span data-stu-id="5d6ab-119">-Name</span></span>
<span data-ttu-id="5d6ab-120">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d6ab-120">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d6ab-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d6ab-121">-ResourceGroupName</span></span>
<span data-ttu-id="5d6ab-122">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d6ab-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d6ab-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d6ab-123">-ResourceId</span></span>
<span data-ttu-id="5d6ab-124">Operationalization 클러스터에 대 한 Azure 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="5d6ab-124">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d6ab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d6ab-125">CommonParameters</span></span>
<span data-ttu-id="5d6ab-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d6ab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d6ab-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d6ab-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d6ab-128">입력</span><span class="sxs-lookup"><span data-stu-id="5d6ab-128">INPUTS</span></span>

### <span data-ttu-id="5d6ab-129">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="5d6ab-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="5d6ab-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5d6ab-130">System.String</span></span>

## <span data-ttu-id="5d6ab-131">출력</span><span class="sxs-lookup"><span data-stu-id="5d6ab-131">OUTPUTS</span></span>

### <span data-ttu-id="5d6ab-132">MachineLearningCompute. PSOperationalizationClusterCredentials/.</span><span class="sxs-lookup"><span data-stu-id="5d6ab-132">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="5d6ab-133">상속자</span><span class="sxs-lookup"><span data-stu-id="5d6ab-133">NOTES</span></span>

## <span data-ttu-id="5d6ab-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d6ab-134">RELATED LINKS</span></span>

