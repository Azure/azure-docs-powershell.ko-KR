---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/test-azmlopclustersystemservicesupdateavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Test-AzMlOpClusterSystemServicesUpdateAvailability.md
ms.openlocfilehash: d05f8b746dbd212c834e3554639340fa6075c216
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867498"
---
# <span data-ttu-id="5260c-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="5260c-101">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>

## <span data-ttu-id="5260c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5260c-102">SYNOPSIS</span></span>
<span data-ttu-id="5260c-103">Operationalization 클러스터와 연결 된 시스템 서비스에 사용할 수 있는 업데이트가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5260c-103">Checks if there are updates available for the system services associated with an operationalization cluster.</span></span>

## <span data-ttu-id="5260c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5260c-104">SYNTAX</span></span>

### <span data-ttu-id="5260c-105">TestByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5260c-105">TestByNameAndResourceGroup</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5260c-106">TestByInputObject</span><span class="sxs-lookup"><span data-stu-id="5260c-106">TestByInputObject</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5260c-107">TestByResourceId</span><span class="sxs-lookup"><span data-stu-id="5260c-107">TestByResourceId</span></span>
```
Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5260c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5260c-108">DESCRIPTION</span></span>
<span data-ttu-id="5260c-109">시스템 서비스는 operationalization 클러스터와는 별개로 업데이트를 받습니다.</span><span class="sxs-lookup"><span data-stu-id="5260c-109">System services receive updates independently from the operationalization cluster.</span></span> <span data-ttu-id="5260c-110">이 cmdlet을 사용 하면 사용자가 AzMlOpClusterSystemServicesUpdate를 호출할 때이를 알 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5260c-110">Using this cmdlet will let the user know if Invoke-AzMlOpClusterSystemServicesUpdate.</span></span>

## <span data-ttu-id="5260c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="5260c-111">EXAMPLES</span></span>

### <span data-ttu-id="5260c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="5260c-112">Example 1</span></span>
```
PS C:\> Test-AzMlOpClusterSystemServicesUpdateAvailability -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="5260c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="5260c-113">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

### <span data-ttu-id="5260c-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="5260c-114">Example 3</span></span>
```
PS C:\> Find-AzResource -ResourceType Microsoft.MachineLearningCompute/operationalizationClusters | Test-AzMlOpClusterSystemServicesUpdateAvailability
```

## <span data-ttu-id="5260c-115">변수</span><span class="sxs-lookup"><span data-stu-id="5260c-115">PARAMETERS</span></span>

### <span data-ttu-id="5260c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5260c-116">-DefaultProfile</span></span>
<span data-ttu-id="5260c-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5260c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5260c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5260c-118">-InputObject</span></span>
<span data-ttu-id="5260c-119">Operationalization cluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5260c-119">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: TestByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5260c-120">-이름</span><span class="sxs-lookup"><span data-stu-id="5260c-120">-Name</span></span>
<span data-ttu-id="5260c-121">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5260c-121">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5260c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5260c-122">-ResourceGroupName</span></span>
<span data-ttu-id="5260c-123">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5260c-123">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5260c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5260c-124">-ResourceId</span></span>
<span data-ttu-id="5260c-125">Operationalization 클러스터에 대 한 Azure 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="5260c-125">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5260c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5260c-126">CommonParameters</span></span>
<span data-ttu-id="5260c-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5260c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5260c-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5260c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5260c-129">입력</span><span class="sxs-lookup"><span data-stu-id="5260c-129">INPUTS</span></span>

### <span data-ttu-id="5260c-130">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="5260c-130">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="5260c-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5260c-131">System.String</span></span>

## <span data-ttu-id="5260c-132">출력</span><span class="sxs-lookup"><span data-stu-id="5260c-132">OUTPUTS</span></span>

### <span data-ttu-id="5260c-133">MachineLearningCompute. PSCheckSystemServicesUpdatesAvailableResponse/.</span><span class="sxs-lookup"><span data-stu-id="5260c-133">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSCheckSystemServicesUpdatesAvailableResponse</span></span>

## <span data-ttu-id="5260c-134">상속자</span><span class="sxs-lookup"><span data-stu-id="5260c-134">NOTES</span></span>

## <span data-ttu-id="5260c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5260c-135">RELATED LINKS</span></span>
