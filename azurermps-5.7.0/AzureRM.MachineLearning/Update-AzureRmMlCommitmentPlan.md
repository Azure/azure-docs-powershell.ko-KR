---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/update-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 0cda9ee6f6a93a43234835104130ea39782f36d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530491"
---
# <span data-ttu-id="04d36-101">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="04d36-101">Update-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="04d36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04d36-102">SYNOPSIS</span></span>
<span data-ttu-id="04d36-103">기존 약정 계획 리소스의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d36-103">Updates properties of an existing commitment plan resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04d36-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04d36-104">SYNTAX</span></span>

```
Update-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04d36-105">설명은</span><span class="sxs-lookup"><span data-stu-id="04d36-105">DESCRIPTION</span></span>
<span data-ttu-id="04d36-106">기존 약정 계획 리소스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d36-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="04d36-107">약정 계획의 대부분의 속성은 변경 불가능 하며 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04d36-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="04d36-108">수정할 수 있는 속성에는 Sku (한 SKU에서 다른 SKU로 약정 계획을 마이그레이션할 수 있음) 및 태그가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04d36-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="04d36-109">예제의</span><span class="sxs-lookup"><span data-stu-id="04d36-109">EXAMPLES</span></span>

### <span data-ttu-id="04d36-110">예제 1: 약정 계획 업데이트</span><span class="sxs-lookup"><span data-stu-id="04d36-110">Example 1: Update a commitment plan</span></span>
```
Update-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="04d36-111">변수</span><span class="sxs-lookup"><span data-stu-id="04d36-111">PARAMETERS</span></span>

### <span data-ttu-id="04d36-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04d36-112">-DefaultProfile</span></span>
<span data-ttu-id="04d36-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="04d36-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04d36-114">-Force</span><span class="sxs-lookup"><span data-stu-id="04d36-114">-Force</span></span>
<span data-ttu-id="04d36-115">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04d36-115">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d36-116">-이름</span><span class="sxs-lookup"><span data-stu-id="04d36-116">-Name</span></span>
<span data-ttu-id="04d36-117">Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04d36-117">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d36-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04d36-118">-ResourceGroupName</span></span>
<span data-ttu-id="04d36-119">Azure ML 약정 계획에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04d36-119">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d36-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="04d36-120">-SkuCapacity</span></span>
<span data-ttu-id="04d36-121">Azure ML 약정 계획을 업데이트할 때 사용할 SKU의 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="04d36-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d36-122">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="04d36-122">-SkuName</span></span>
<span data-ttu-id="04d36-123">Azure ML 약정 계획을 업데이트할 때 사용할 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04d36-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d36-124">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="04d36-124">-SkuTier</span></span>
<span data-ttu-id="04d36-125">Azure ML 약정 계획을 업데이트할 때 사용할 SKU의 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="04d36-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d36-126">태그</span><span class="sxs-lookup"><span data-stu-id="04d36-126">-Tag</span></span>
<span data-ttu-id="04d36-127">약정 계획 리소스의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="04d36-127">Tags for the commitment plan resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d36-128">-확인</span><span class="sxs-lookup"><span data-stu-id="04d36-128">-Confirm</span></span>
<span data-ttu-id="04d36-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d36-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04d36-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04d36-130">-WhatIf</span></span>
<span data-ttu-id="04d36-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="04d36-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04d36-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04d36-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04d36-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d36-133">CommonParameters</span></span>
<span data-ttu-id="04d36-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d36-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d36-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04d36-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d36-136">입력</span><span class="sxs-lookup"><span data-stu-id="04d36-136">INPUTS</span></span>

### <span data-ttu-id="04d36-137">않아야</span><span class="sxs-lookup"><span data-stu-id="04d36-137">None</span></span>
<span data-ttu-id="04d36-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04d36-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04d36-139">출력</span><span class="sxs-lookup"><span data-stu-id="04d36-139">OUTPUTS</span></span>

### <span data-ttu-id="04d36-140">MachineLearning. CommitmentPlans. \ CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="04d36-140">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="04d36-141">상속자</span><span class="sxs-lookup"><span data-stu-id="04d36-141">NOTES</span></span>
<span data-ttu-id="04d36-142">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="04d36-142">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="04d36-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04d36-143">RELATED LINKS</span></span>
