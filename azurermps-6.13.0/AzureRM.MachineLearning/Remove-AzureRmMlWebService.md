---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: c1d6ae6c1396e23398bc1b52f4f32458999072a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530922"
---
# <span data-ttu-id="d491c-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="d491c-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="d491c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d491c-102">SYNOPSIS</span></span>
<span data-ttu-id="d491c-103">웹 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d491c-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d491c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d491c-104">SYNTAX</span></span>

### <span data-ttu-id="d491c-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d491c-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d491c-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="d491c-106">RemoveByObject</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d491c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d491c-107">DESCRIPTION</span></span>
<span data-ttu-id="d491c-108">리소스 그룹 및 이름에서 참조 하는 Azure 기계 학습 웹 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d491c-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="d491c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d491c-109">EXAMPLES</span></span>

### <span data-ttu-id="d491c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d491c-110">Example 1</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="d491c-111">변수</span><span class="sxs-lookup"><span data-stu-id="d491c-111">PARAMETERS</span></span>

### <span data-ttu-id="d491c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d491c-112">-DefaultProfile</span></span>
<span data-ttu-id="d491c-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d491c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d491c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d491c-114">-Force</span></span>
<span data-ttu-id="d491c-115">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d491c-115">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d491c-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="d491c-116">-MlWebService</span></span>
<span data-ttu-id="d491c-117">제거할 웹 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="d491c-117">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d491c-118">-이름</span><span class="sxs-lookup"><span data-stu-id="d491c-118">-Name</span></span>
<span data-ttu-id="d491c-119">제거할 웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d491c-119">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d491c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d491c-120">-ResourceGroupName</span></span>
<span data-ttu-id="d491c-121">웹 서비스의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="d491c-121">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d491c-122">-확인</span><span class="sxs-lookup"><span data-stu-id="d491c-122">-Confirm</span></span>
<span data-ttu-id="d491c-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d491c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d491c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d491c-124">-WhatIf</span></span>
<span data-ttu-id="d491c-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d491c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d491c-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d491c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d491c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d491c-127">CommonParameters</span></span>
<span data-ttu-id="d491c-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d491c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d491c-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d491c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d491c-130">입력</span><span class="sxs-lookup"><span data-stu-id="d491c-130">INPUTS</span></span>

### <span data-ttu-id="d491c-131">MachineLearning. WebServices의 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="d491c-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="d491c-132">매개 변수: MlWebService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d491c-132">Parameters: MlWebService (ByValue)</span></span>

## <span data-ttu-id="d491c-133">출력</span><span class="sxs-lookup"><span data-stu-id="d491c-133">OUTPUTS</span></span>

### <span data-ttu-id="d491c-134">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="d491c-134">System.Void</span></span>

## <span data-ttu-id="d491c-135">상속자</span><span class="sxs-lookup"><span data-stu-id="d491c-135">NOTES</span></span>
<span data-ttu-id="d491c-136">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="d491c-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d491c-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d491c-137">RELATED LINKS</span></span>
