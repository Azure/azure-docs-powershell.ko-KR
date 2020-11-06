---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: 4d7365a2a7a8d11fc1032f182409bd462931be3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530492"
---
# <span data-ttu-id="9d72e-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="9d72e-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="9d72e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d72e-102">SYNOPSIS</span></span>
<span data-ttu-id="9d72e-103">웹 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d72e-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d72e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9d72e-104">SYNTAX</span></span>

### <span data-ttu-id="9d72e-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9d72e-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d72e-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="9d72e-106">RemoveByObject</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d72e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9d72e-107">DESCRIPTION</span></span>
<span data-ttu-id="9d72e-108">리소스 그룹 및 이름에서 참조 하는 Azure 기계 학습 웹 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d72e-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="9d72e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9d72e-109">EXAMPLES</span></span>

### <span data-ttu-id="9d72e-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9d72e-110">--------------------------  Example 1  --------------------------</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="9d72e-111">변수</span><span class="sxs-lookup"><span data-stu-id="9d72e-111">PARAMETERS</span></span>

### <span data-ttu-id="9d72e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d72e-112">-DefaultProfile</span></span>
<span data-ttu-id="9d72e-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9d72e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d72e-114">-Force</span><span class="sxs-lookup"><span data-stu-id="9d72e-114">-Force</span></span>
<span data-ttu-id="9d72e-115">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d72e-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9d72e-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="9d72e-116">-MlWebService</span></span>
<span data-ttu-id="9d72e-117">제거할 웹 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="9d72e-117">The web service to be removed.</span></span>

```yaml
Type: WebService
Parameter Sets: RemoveByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d72e-118">-이름</span><span class="sxs-lookup"><span data-stu-id="9d72e-118">-Name</span></span>
<span data-ttu-id="9d72e-119">제거할 웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9d72e-119">The name of the web service to be removed.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d72e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d72e-120">-ResourceGroupName</span></span>
<span data-ttu-id="9d72e-121">웹 서비스의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="9d72e-121">The resource group of the web service.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d72e-122">-확인</span><span class="sxs-lookup"><span data-stu-id="9d72e-122">-Confirm</span></span>
<span data-ttu-id="9d72e-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d72e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d72e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d72e-124">-WhatIf</span></span>
<span data-ttu-id="9d72e-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9d72e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d72e-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d72e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d72e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d72e-127">CommonParameters</span></span>
<span data-ttu-id="9d72e-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d72e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d72e-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d72e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d72e-130">입력</span><span class="sxs-lookup"><span data-stu-id="9d72e-130">INPUTS</span></span>

### <span data-ttu-id="9d72e-131">용</span><span class="sxs-lookup"><span data-stu-id="9d72e-131">WebService</span></span>
<span data-ttu-id="9d72e-132">' MlWebService ' 매개 변수는 파이프라인에서 ' WebService ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d72e-132">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="9d72e-133">출력</span><span class="sxs-lookup"><span data-stu-id="9d72e-133">OUTPUTS</span></span>

### <span data-ttu-id="9d72e-134">않아야</span><span class="sxs-lookup"><span data-stu-id="9d72e-134">None</span></span>

## <span data-ttu-id="9d72e-135">상속자</span><span class="sxs-lookup"><span data-stu-id="9d72e-135">NOTES</span></span>
<span data-ttu-id="9d72e-136">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="9d72e-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="9d72e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9d72e-137">RELATED LINKS</span></span>

