---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpClusterKey.md
ms.openlocfilehash: d8b8a333b4d009ee1b40a8b4ddc6ed49850f1a11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867542"
---
# <span data-ttu-id="e5e76-101">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="e5e76-101">Get-AzMlOpClusterKey</span></span>

## <span data-ttu-id="e5e76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5e76-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e76-103">Operationalization 클러스터와 연결 된 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e5e76-103">Gets the access keys associated with an operationalization cluster.</span></span>

## <span data-ttu-id="e5e76-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5e76-104">SYNTAX</span></span>

### <span data-ttu-id="e5e76-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5e76-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlOpClusterKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5e76-106">GetByInputObject</span><span class="sxs-lookup"><span data-stu-id="e5e76-106">GetByInputObject</span></span>
```
Get-AzMlOpClusterKey -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5e76-107">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e5e76-107">GetByResourceId</span></span>
```
Get-AzMlOpClusterKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5e76-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e5e76-108">DESCRIPTION</span></span>
<span data-ttu-id="e5e76-109">클러스터 속성을 가져올 때 저장소 계정, 컨테이너 레지스트리 및 operationalization 클러스터와 연결 된 기타 서비스의 키가 반환 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5e76-109">The keys for the storage account, container registry, and other services associated with the operationalization cluster are not returned when getting the cluster properties.</span></span> <span data-ttu-id="e5e76-110">키를 검색 하기 위한 특정 호출은 중요 한 정보 이기 때문에 이루어져야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5e76-110">A specific call to retrieve the keys must be made since they are sensitive information.</span></span>

## <span data-ttu-id="e5e76-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e5e76-111">EXAMPLES</span></span>

### <span data-ttu-id="e5e76-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="e5e76-112">Example 1</span></span>
```
PS C:\> Get-AzMlOpClusterKey -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="e5e76-113">Operationalization 클러스터와 연결 된 서비스에 대 한 비밀 키를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5e76-113">Returns the secret keys for the services associated with the operationalization cluster.</span></span>

## <span data-ttu-id="e5e76-114">변수</span><span class="sxs-lookup"><span data-stu-id="e5e76-114">PARAMETERS</span></span>

### <span data-ttu-id="e5e76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e76-115">-DefaultProfile</span></span>
<span data-ttu-id="e5e76-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5e76-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5e76-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5e76-117">-InputObject</span></span>
<span data-ttu-id="e5e76-118">Operationalization cluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e5e76-118">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: GetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e76-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e5e76-119">-Name</span></span>
<span data-ttu-id="e5e76-120">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5e76-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e76-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5e76-121">-ResourceGroupName</span></span>
<span data-ttu-id="e5e76-122">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5e76-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e76-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5e76-123">-ResourceId</span></span>
<span data-ttu-id="e5e76-124">Operationalization 클러스터에 대 한 Azure 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e5e76-124">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e76-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e76-125">CommonParameters</span></span>
<span data-ttu-id="e5e76-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5e76-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e76-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5e76-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e76-128">입력</span><span class="sxs-lookup"><span data-stu-id="e5e76-128">INPUTS</span></span>

### <span data-ttu-id="e5e76-129">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="e5e76-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="e5e76-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e5e76-130">System.String</span></span>

## <span data-ttu-id="e5e76-131">출력</span><span class="sxs-lookup"><span data-stu-id="e5e76-131">OUTPUTS</span></span>

### <span data-ttu-id="e5e76-132">MachineLearningCompute. PSOperationalizationClusterCredentials/.</span><span class="sxs-lookup"><span data-stu-id="e5e76-132">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationClusterCredentials</span></span>

## <span data-ttu-id="e5e76-133">상속자</span><span class="sxs-lookup"><span data-stu-id="e5e76-133">NOTES</span></span>

## <span data-ttu-id="e5e76-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5e76-134">RELATED LINKS</span></span>
