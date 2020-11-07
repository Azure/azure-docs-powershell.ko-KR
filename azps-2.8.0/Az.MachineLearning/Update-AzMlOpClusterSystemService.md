---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlopclustersystemservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
ms.openlocfilehash: 0e673cd74d87cee990130c1fd58b9049eec9ff15
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689413"
---
# <span data-ttu-id="7b423-101">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="7b423-101">Update-AzMlOpClusterSystemService</span></span>

## <span data-ttu-id="7b423-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b423-102">SYNOPSIS</span></span>
<span data-ttu-id="7b423-103">Operationalization 클러스터의 시스템 서비스에서 업데이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b423-103">Starts an update on the operationalization cluster's system services.</span></span>

## <span data-ttu-id="7b423-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7b423-104">SYNTAX</span></span>

### <span data-ttu-id="7b423-105">StartUpdateWithNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7b423-105">StartUpdateWithNameAndResourceGroup</span></span>
```
Update-AzMlOpClusterSystemService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b423-106">StartUpdateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="7b423-106">StartUpdateWithInputObject</span></span>
```
Update-AzMlOpClusterSystemService -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b423-107">StartUpdateWithResourceId</span><span class="sxs-lookup"><span data-stu-id="7b423-107">StartUpdateWithResourceId</span></span>
```
Update-AzMlOpClusterSystemService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b423-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7b423-108">DESCRIPTION</span></span>
<span data-ttu-id="7b423-109">시스템 서비스는 operationalization 클러스터와 독립적으로 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b423-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="7b423-110">시스템 서비스에서 업데이트를 시작 하려면이 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b423-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="7b423-111">업데이트를 사용할 수 없는 경우 업데이트는 계속 시작 되 고 성공적으로 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b423-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="7b423-112">업데이트가 완료 되 면 시작, 완료 및 성공한 경우 보고서를 보고 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b423-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="7b423-113">예제의</span><span class="sxs-lookup"><span data-stu-id="7b423-113">EXAMPLES</span></span>

### <span data-ttu-id="7b423-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="7b423-114">Example 1</span></span>
```
PS C:\> Update-AzMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="7b423-115">지정 된 클러스터에서 시스템 서비스 업데이트를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b423-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="7b423-116">변수</span><span class="sxs-lookup"><span data-stu-id="7b423-116">PARAMETERS</span></span>

### <span data-ttu-id="7b423-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b423-117">-DefaultProfile</span></span>
<span data-ttu-id="7b423-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b423-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b423-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b423-119">-InputObject</span></span>
<span data-ttu-id="7b423-120">Operationalization cluster 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7b423-120">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: StartUpdateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b423-121">-이름</span><span class="sxs-lookup"><span data-stu-id="7b423-121">-Name</span></span>
<span data-ttu-id="7b423-122">Operationalization 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b423-122">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b423-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b423-123">-ResourceGroupName</span></span>
<span data-ttu-id="7b423-124">Operationalization 클러스터에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b423-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b423-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b423-125">-ResourceId</span></span>
<span data-ttu-id="7b423-126">Operationalization 클러스터에 대 한 Azure 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="7b423-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b423-127">-확인</span><span class="sxs-lookup"><span data-stu-id="7b423-127">-Confirm</span></span>
<span data-ttu-id="7b423-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b423-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b423-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b423-129">-WhatIf</span></span>
<span data-ttu-id="7b423-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b423-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b423-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b423-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b423-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b423-132">CommonParameters</span></span>
<span data-ttu-id="7b423-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b423-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b423-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b423-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b423-135">입력</span><span class="sxs-lookup"><span data-stu-id="7b423-135">INPUTS</span></span>

### <span data-ttu-id="7b423-136">MachineLearningCompute. PSOperationalizationCluster/.</span><span class="sxs-lookup"><span data-stu-id="7b423-136">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="7b423-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7b423-137">System.String</span></span>

## <span data-ttu-id="7b423-138">출력</span><span class="sxs-lookup"><span data-stu-id="7b423-138">OUTPUTS</span></span>

### <span data-ttu-id="7b423-139">MachineLearningCompute. PSUpdateSystemServicesResponse/.</span><span class="sxs-lookup"><span data-stu-id="7b423-139">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>

## <span data-ttu-id="7b423-140">상속자</span><span class="sxs-lookup"><span data-stu-id="7b423-140">NOTES</span></span>

## <span data-ttu-id="7b423-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b423-141">RELATED LINKS</span></span>
