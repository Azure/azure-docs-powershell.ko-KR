---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: e37aff4f6f79a3aa0420c98811bc47b951bb4d3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533063"
---
# <span data-ttu-id="81c22-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="81c22-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="81c22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81c22-102">SYNOPSIS</span></span>
<span data-ttu-id="81c22-103">Operationalization 클러스터 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="81c22-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81c22-104">구문과</span><span class="sxs-lookup"><span data-stu-id="81c22-104">SYNTAX</span></span>

```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81c22-105">설명은</span><span class="sxs-lookup"><span data-stu-id="81c22-105">DESCRIPTION</span></span>
<span data-ttu-id="81c22-106">이름 또는 리소스 그룹별 또는 구독을 기준으로 operationalization cluster 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="81c22-106">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="81c22-107">예제의</span><span class="sxs-lookup"><span data-stu-id="81c22-107">EXAMPLES</span></span>

### <span data-ttu-id="81c22-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="81c22-108">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="81c22-109">이름으로 특정 operationalization 클러스터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="81c22-109">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="81c22-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="81c22-110">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="81c22-111">리소스 그룹의 모든 operationalization 클러스터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="81c22-111">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="81c22-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="81c22-112">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="81c22-113">구독에 있는 모든 operationalization 클러스터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="81c22-113">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="81c22-114">변수</span><span class="sxs-lookup"><span data-stu-id="81c22-114">PARAMETERS</span></span>

### <span data-ttu-id="81c22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c22-115">-DefaultProfile</span></span>
<span data-ttu-id="81c22-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81c22-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81c22-117">-이름</span><span class="sxs-lookup"><span data-stu-id="81c22-117">-Name</span></span>
<span data-ttu-id="81c22-118">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81c22-118">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Get an operationalization cluster by its name.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c22-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81c22-119">-ResourceGroupName</span></span>
<span data-ttu-id="81c22-120">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81c22-120">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c22-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c22-121">CommonParameters</span></span>
<span data-ttu-id="81c22-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="81c22-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c22-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81c22-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c22-124">입력</span><span class="sxs-lookup"><span data-stu-id="81c22-124">INPUTS</span></span>

### <span data-ttu-id="81c22-125">않아야</span><span class="sxs-lookup"><span data-stu-id="81c22-125">None</span></span>

## <span data-ttu-id="81c22-126">출력</span><span class="sxs-lookup"><span data-stu-id="81c22-126">OUTPUTS</span></span>

### <span data-ttu-id="81c22-127">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="81c22-127">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="81c22-128">MachineLearningCompute ' 1 [[Microsoft Azure. PSOperationalizationCluster, Microsoft Azure. MachineLearningCompute, Version = 0.1.0.0, Culture = 중립, PublicKeyToken = null]] 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="81c22-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster, Microsoft.Azure.Commands.MachineLearningCompute, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="81c22-129">상속자</span><span class="sxs-lookup"><span data-stu-id="81c22-129">NOTES</span></span>

## <span data-ttu-id="81c22-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81c22-130">RELATED LINKS</span></span>

