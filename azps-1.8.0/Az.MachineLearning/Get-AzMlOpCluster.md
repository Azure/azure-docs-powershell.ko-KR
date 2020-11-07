---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlOpCluster.md
ms.openlocfilehash: 24400b7a2c882cef81d818c5f5b94fca4235ec83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867549"
---
# <span data-ttu-id="7ab18-101">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="7ab18-101">Get-AzMlOpCluster</span></span>

## <span data-ttu-id="7ab18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ab18-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab18-103">Operationalization 클러스터 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ab18-103">Gets an operationalization cluster object.</span></span>

## <span data-ttu-id="7ab18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7ab18-104">SYNTAX</span></span>

### <span data-ttu-id="7ab18-105">GetByName</span><span class="sxs-lookup"><span data-stu-id="7ab18-105">GetByName</span></span>
```
Get-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ab18-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7ab18-106">GetByResourceGroup</span></span>
```
Get-AzMlOpCluster [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ab18-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7ab18-107">DESCRIPTION</span></span>
<span data-ttu-id="7ab18-108">이름 또는 리소스 그룹별 또는 구독을 기준으로 operationalization cluster 개체를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ab18-108">Gets an operationalization cluster object by name, or by resource group, or by subscription.</span></span>

## <span data-ttu-id="7ab18-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7ab18-109">EXAMPLES</span></span>

### <span data-ttu-id="7ab18-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7ab18-110">Example 1</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="7ab18-111">이름으로 특정 operationalization 클러스터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ab18-111">Gets a specific operationalization cluster by name.</span></span>

### <span data-ttu-id="7ab18-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="7ab18-112">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group
```

<span data-ttu-id="7ab18-113">리소스 그룹의 모든 operationalization 클러스터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ab18-113">Gets all the operationalization clusters in a resource group.</span></span>

### <span data-ttu-id="7ab18-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="7ab18-114">Example 3</span></span>
```
PS C:\> Get-AzMlOpCluster
```

<span data-ttu-id="7ab18-115">구독에 있는 모든 operationalization 클러스터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7ab18-115">Gets all the operationalization clusters in a subscription.</span></span>

## <span data-ttu-id="7ab18-116">변수</span><span class="sxs-lookup"><span data-stu-id="7ab18-116">PARAMETERS</span></span>

### <span data-ttu-id="7ab18-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab18-117">-DefaultProfile</span></span>
<span data-ttu-id="7ab18-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7ab18-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ab18-119">-이름</span><span class="sxs-lookup"><span data-stu-id="7ab18-119">-Name</span></span>
<span data-ttu-id="7ab18-120">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ab18-120">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="7ab18-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ab18-121">-ResourceGroupName</span></span>
<span data-ttu-id="7ab18-122">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ab18-122">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="7ab18-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab18-123">CommonParameters</span></span>
<span data-ttu-id="7ab18-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ab18-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab18-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ab18-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab18-126">입력</span><span class="sxs-lookup"><span data-stu-id="7ab18-126">INPUTS</span></span>

### <span data-ttu-id="7ab18-127">않아야</span><span class="sxs-lookup"><span data-stu-id="7ab18-127">None</span></span>

## <span data-ttu-id="7ab18-128">출력</span><span class="sxs-lookup"><span data-stu-id="7ab18-128">OUTPUTS</span></span>

### <span data-ttu-id="7ab18-129">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="7ab18-129">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="7ab18-130">상속자</span><span class="sxs-lookup"><span data-stu-id="7ab18-130">NOTES</span></span>

## <span data-ttu-id="7ab18-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ab18-131">RELATED LINKS</span></span>
