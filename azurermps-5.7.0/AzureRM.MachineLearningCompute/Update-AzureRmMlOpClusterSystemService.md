---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/update-azurermmlopclustersystemservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: 01f826746b92dd5aa82416e8207305b945ddb711
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703047"
---
# <span data-ttu-id="a6022-101">Update-AzureRmMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="a6022-101">Update-AzureRmMlOpClusterSystemService</span></span>

## <span data-ttu-id="a6022-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6022-102">SYNOPSIS</span></span>
<span data-ttu-id="a6022-103">Operationalization 클러스터의 시스템 서비스에서 업데이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6022-103">Starts an update on the operationalization cluster's system services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6022-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a6022-104">SYNTAX</span></span>

### <span data-ttu-id="a6022-105">StartUpdateWithNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a6022-105">StartUpdateWithNameAndResourceGroup</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6022-106">StartUpdateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="a6022-106">StartUpdateWithInputObject</span></span>
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6022-107">StartUpdateWithResourceId</span><span class="sxs-lookup"><span data-stu-id="a6022-107">StartUpdateWithResourceId</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6022-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a6022-108">DESCRIPTION</span></span>
<span data-ttu-id="a6022-109">시스템 서비스는 operationalization 클러스터와 독립적으로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6022-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="a6022-110">시스템 서비스에서 업데이트를 시작 하려면이 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6022-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="a6022-111">업데이트를 사용할 수 없는 경우 업데이트는 계속 시작 되 고 성공적으로 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6022-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="a6022-112">업데이트가 완료 되 면 시작, 완료 및 성공한 경우 보고서를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6022-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="a6022-113">예제의</span><span class="sxs-lookup"><span data-stu-id="a6022-113">EXAMPLES</span></span>

### <span data-ttu-id="a6022-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="a6022-114">Example 1</span></span>
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="a6022-115">지정 된 클러스터에서 시스템 서비스 업데이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6022-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="a6022-116">변수</span><span class="sxs-lookup"><span data-stu-id="a6022-116">PARAMETERS</span></span>

### <span data-ttu-id="a6022-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6022-117">-DefaultProfile</span></span>
<span data-ttu-id="a6022-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6022-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6022-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6022-119">-InputObject</span></span>
<span data-ttu-id="a6022-120">Operationalization cluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a6022-120">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: StartUpdateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6022-121">-이름</span><span class="sxs-lookup"><span data-stu-id="a6022-121">-Name</span></span>
<span data-ttu-id="a6022-122">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6022-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6022-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6022-123">-ResourceGroupName</span></span>
<span data-ttu-id="a6022-124">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a6022-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6022-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6022-125">-ResourceId</span></span>
<span data-ttu-id="a6022-126">Operationalization 클러스터에 대 한 Azure 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a6022-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: StartUpdateWithResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6022-127">-확인</span><span class="sxs-lookup"><span data-stu-id="a6022-127">-Confirm</span></span>
<span data-ttu-id="a6022-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6022-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6022-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6022-129">-WhatIf</span></span>
<span data-ttu-id="a6022-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a6022-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6022-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6022-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6022-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6022-132">CommonParameters</span></span>
<span data-ttu-id="a6022-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6022-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6022-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6022-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6022-135">입력</span><span class="sxs-lookup"><span data-stu-id="a6022-135">INPUTS</span></span>

### <span data-ttu-id="a6022-136">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="a6022-136">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="a6022-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a6022-137">System.String</span></span>

## <span data-ttu-id="a6022-138">출력</span><span class="sxs-lookup"><span data-stu-id="a6022-138">OUTPUTS</span></span>

### <span data-ttu-id="a6022-139">MachineLearningCompute. PSUpdateSystemServicesResponse/.</span><span class="sxs-lookup"><span data-stu-id="a6022-139">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>

## <span data-ttu-id="a6022-140">상속자</span><span class="sxs-lookup"><span data-stu-id="a6022-140">NOTES</span></span>

## <span data-ttu-id="a6022-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6022-141">RELATED LINKS</span></span>

