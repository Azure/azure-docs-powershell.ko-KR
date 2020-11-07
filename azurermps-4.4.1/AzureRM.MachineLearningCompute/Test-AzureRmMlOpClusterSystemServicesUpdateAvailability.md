---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 067fdf88b7a7b29007f81ab26590ffaa542ac7e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703360"
---
# <span data-ttu-id="c0416-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="c0416-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="c0416-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0416-102">SYNOPSIS</span></span>
<span data-ttu-id="c0416-103">Operationalization 클러스터와 연결 된 시스템 서비스에 사용할 수 있는 업데이트가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0416-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0416-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c0416-104">SYNTAX</span></span>

### <span data-ttu-id="c0416-105">Cmdlet 입력 매개 변수에서 업데이트 가용성을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0416-105">Test for update availability from cmdlet input parameters.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
```

### <span data-ttu-id="c0416-106">OperationalizationCluster 인스턴스 정의의 업데이트 가용성을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0416-106">Test for update availability from an OperationalizationCluster instance definition.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
```

### <span data-ttu-id="c0416-107">Azure 리소스 id의 업데이트 가용성을 테스트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0416-107">Test for update availability from an Azure resouce id.</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
```

## <span data-ttu-id="c0416-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c0416-108">DESCRIPTION</span></span>
<span data-ttu-id="c0416-109">시스템 서비스는 operationalization 클러스터와는 별개로 업데이트를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="c0416-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="c0416-110">이 cmdlet을 사용 하면 사용자가 AzureRmMlOpClusterSystemServicesUpdate를 호출할 때이를 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0416-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="c0416-111">예제의</span><span class="sxs-lookup"><span data-stu-id="c0416-111">EXAMPLES</span></span>

### <span data-ttu-id="c0416-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="c0416-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="c0416-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c0416-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="c0416-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="c0416-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="c0416-115">변수</span><span class="sxs-lookup"><span data-stu-id="c0416-115">PARAMETERS</span></span>

### <span data-ttu-id="c0416-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0416-116">-InputObject</span></span>
<span data-ttu-id="c0416-117">Operationalization cluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c0416-117">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Test for update availability from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0416-118">-이름</span><span class="sxs-lookup"><span data-stu-id="c0416-118">-Name</span></span>
<span data-ttu-id="c0416-119">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0416-119">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0416-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0416-120">-ResourceGroupName</span></span>
<span data-ttu-id="c0416-121">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0416-121">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0416-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0416-122">-ResourceId</span></span>
<span data-ttu-id="c0416-123">Operationalization 클러스터에 대 한 Azure 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="c0416-123">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Test for update availability from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="c0416-124">입력</span><span class="sxs-lookup"><span data-stu-id="c0416-124">INPUTS</span></span>

### <span data-ttu-id="c0416-125">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="c0416-125">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="c0416-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c0416-126">System.String</span></span>


## <span data-ttu-id="c0416-127">출력</span><span class="sxs-lookup"><span data-stu-id="c0416-127">OUTPUTS</span></span>

### <span data-ttu-id="c0416-128">MachineLearningCompute. PSCheckSystemServicesUpdatesAvailableResponse/.</span><span class="sxs-lookup"><span data-stu-id="c0416-128">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>


## <span data-ttu-id="c0416-129">상속자</span><span class="sxs-lookup"><span data-stu-id="c0416-129">NOTES</span></span>

## <span data-ttu-id="c0416-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0416-130">RELATED LINKS</span></span>

