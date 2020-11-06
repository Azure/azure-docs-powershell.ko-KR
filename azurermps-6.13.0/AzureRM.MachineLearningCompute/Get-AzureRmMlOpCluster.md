---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/get-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Get-AzureRmMlOpCluster.md
ms.openlocfilehash: 746dde8dd3460add5eb6a20e4a9b771873dac0e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530239"
---
# <span data-ttu-id="68944-101">Get-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="68944-101">Get-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="68944-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68944-102">SYNOPSIS</span></span>
<span data-ttu-id="68944-103">Operationalization 클러스터 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68944-103">Gets an operationalization cluster object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68944-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68944-104">SYNTAX</span></span>

### <span data-ttu-id="68944-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="68944-105">GetByName</span></span>
```
Get-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68944-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="68944-106">GetByResourceGroup</span></span>
```
Get-AzureRmMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68944-107">설명은</span><span class="sxs-lookup"><span data-stu-id="68944-107">DESCRIPTION</span></span>
<span data-ttu-id="68944-108">이름 또는 리소스 그룹별 또는 구독을 기준으로 operationalization cluster 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68944-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="68944-109">예제의</span><span class="sxs-lookup"><span data-stu-id="68944-109">EXAMPLES</span></span>

### <span data-ttu-id="68944-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="68944-110">Example 1</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="68944-111">이름으로 특정 operationalization 클러스터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68944-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="68944-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="68944-112">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="68944-113">리소스 그룹의 모든 operationalization 클러스터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68944-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="68944-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="68944-114">Example 3</span></span>
```
PS C:\> Get-AzureRmMlOpCluster
```

<span data-ttu-id="68944-115">구독에 있는 모든 operationalization 클러스터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="68944-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="68944-116">변수</span><span class="sxs-lookup"><span data-stu-id="68944-116">PARAMETERS</span></span>

### <span data-ttu-id="68944-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68944-117">-DefaultProfile</span></span>
<span data-ttu-id="68944-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68944-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68944-119">-이름</span><span class="sxs-lookup"><span data-stu-id="68944-119">-Name</span></span>
<span data-ttu-id="68944-120">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68944-120">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68944-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68944-121">-ResourceGroupName</span></span>
<span data-ttu-id="68944-122">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68944-122">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68944-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68944-123">CommonParameters</span></span>
<span data-ttu-id="68944-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68944-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68944-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68944-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68944-126">입력</span><span class="sxs-lookup"><span data-stu-id="68944-126">INPUTS</span></span>

### <span data-ttu-id="68944-127">않아야</span><span class="sxs-lookup"><span data-stu-id="68944-127">None</span></span>

## <span data-ttu-id="68944-128">출력</span><span class="sxs-lookup"><span data-stu-id="68944-128">OUTPUTS</span></span>

### <span data-ttu-id="68944-129">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="68944-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="68944-130">상속자</span><span class="sxs-lookup"><span data-stu-id="68944-130">NOTES</span></span>

## <span data-ttu-id="68944-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68944-131">RELATED LINKS</span></span>
