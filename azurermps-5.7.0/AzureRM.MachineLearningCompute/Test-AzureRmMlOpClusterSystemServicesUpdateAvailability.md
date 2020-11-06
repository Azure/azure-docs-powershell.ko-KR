---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/test-azurermmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Test-AzureRmMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: 9f531b67d2dc3cc6010a7677c96dc4ecf10fb5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530489"
---
# <span data-ttu-id="23683-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="23683-101">Test-AzureRmMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="23683-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23683-102">SYNOPSIS</span></span>
<span data-ttu-id="23683-103">Operationalization 클러스터와 연결 된 시스템 서비스에 사용할 수 있는 업데이트가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="23683-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23683-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23683-104">SYNTAX</span></span>

### <span data-ttu-id="23683-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="23683-105">TestByNameAndResourceGroup</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23683-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="23683-106">TestByInputObject</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23683-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="23683-107">TestByResourceId</span></span>
```
Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23683-108">설명은</span><span class="sxs-lookup"><span data-stu-id="23683-108">DESCRIPTION</span></span>
<span data-ttu-id="23683-109">시스템 서비스는 operationalization 클러스터와는 별개로 업데이트를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="23683-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="23683-110">이 cmdlet을 사용 하면 사용자가 AzureRmMlOpClusterSystemServicesUpdate를 호출할 때이를 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23683-110">Using this cmdlet will let the user know if Invoke-AzureRmMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="23683-111">예제의</span><span class="sxs-lookup"><span data-stu-id="23683-111">EXAMPLES</span></span>

### <span data-ttu-id="23683-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="23683-112">Example 1</span></span>
```
PS C:\> Test-AzureRmMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="23683-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="23683-113">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="23683-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="23683-114">Example 3</span></span>
```
PS C:\> Find-AzureRmResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzureRmMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="23683-115">변수</span><span class="sxs-lookup"><span data-stu-id="23683-115">PARAMETERS</span></span>

### <span data-ttu-id="23683-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23683-116">-DefaultProfile</span></span>
<span data-ttu-id="23683-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23683-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23683-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23683-118">-InputObject</span></span>
<span data-ttu-id="23683-119">Operationalization cluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="23683-119">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: TestByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23683-120">-이름</span><span class="sxs-lookup"><span data-stu-id="23683-120">-Name</span></span>
<span data-ttu-id="23683-121">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23683-121">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: TestByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23683-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23683-122">-ResourceGroupName</span></span>
<span data-ttu-id="23683-123">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23683-123">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: TestByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23683-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23683-124">-ResourceId</span></span>
<span data-ttu-id="23683-125">Operationalization 클러스터에 대 한 Azure 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="23683-125">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: TestByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23683-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23683-126">CommonParameters</span></span>
<span data-ttu-id="23683-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23683-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23683-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23683-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23683-129">입력</span><span class="sxs-lookup"><span data-stu-id="23683-129">INPUTS</span></span>

### <span data-ttu-id="23683-130">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="23683-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="23683-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="23683-131">System.String</span></span>

## <span data-ttu-id="23683-132">출력</span><span class="sxs-lookup"><span data-stu-id="23683-132">OUTPUTS</span></span>

### <span data-ttu-id="23683-133">MachineLearningCompute. PSCheckSystemServicesUpdatesAvailableResponse/.</span><span class="sxs-lookup"><span data-stu-id="23683-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="23683-134">상속자</span><span class="sxs-lookup"><span data-stu-id="23683-134">NOTES</span></span>

## <span data-ttu-id="23683-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23683-135">RELATED LINKS</span></span>

