---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 4a59508cc816f3301d76b1d982f52108247b50a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346214"
---
# <span data-ttu-id="2101f-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="2101f-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="2101f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2101f-102">SYNOPSIS</span></span>
<span data-ttu-id="2101f-103">웹 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="2101f-103">Deletes a web service.</span></span>

## <span data-ttu-id="2101f-104">구문</span><span class="sxs-lookup"><span data-stu-id="2101f-104">SYNTAX</span></span>

### <span data-ttu-id="2101f-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2101f-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2101f-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="2101f-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2101f-107">설명</span><span class="sxs-lookup"><span data-stu-id="2101f-107">DESCRIPTION</span></span>
<span data-ttu-id="2101f-108">리소스 그룹 및 이름으로 참조되는 Azure Machine Learning 웹 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="2101f-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="2101f-109">예제</span><span class="sxs-lookup"><span data-stu-id="2101f-109">EXAMPLES</span></span>

### <span data-ttu-id="2101f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2101f-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="2101f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2101f-111">PARAMETERS</span></span>

### <span data-ttu-id="2101f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2101f-112">-DefaultProfile</span></span>
<span data-ttu-id="2101f-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2101f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2101f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2101f-114">-Force</span></span>
<span data-ttu-id="2101f-115">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2101f-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2101f-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="2101f-116">-MlWebService</span></span>
<span data-ttu-id="2101f-117">제거할 웹 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="2101f-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="2101f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2101f-118">-Name</span></span>
<span data-ttu-id="2101f-119">제거할 웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2101f-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="2101f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2101f-120">-ResourceGroupName</span></span>
<span data-ttu-id="2101f-121">웹 서비스의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="2101f-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="2101f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2101f-122">-Confirm</span></span>
<span data-ttu-id="2101f-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2101f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2101f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2101f-124">-WhatIf</span></span>
<span data-ttu-id="2101f-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2101f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2101f-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2101f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2101f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2101f-127">CommonParameters</span></span>
<span data-ttu-id="2101f-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2101f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2101f-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2101f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2101f-130">입력</span><span class="sxs-lookup"><span data-stu-id="2101f-130">INPUTS</span></span>

### <span data-ttu-id="2101f-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="2101f-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="2101f-132">출력</span><span class="sxs-lookup"><span data-stu-id="2101f-132">OUTPUTS</span></span>

### <span data-ttu-id="2101f-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="2101f-133">System.Void</span></span>

## <span data-ttu-id="2101f-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2101f-134">NOTES</span></span>
<span data-ttu-id="2101f-135">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="2101f-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2101f-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2101f-136">RELATED LINKS</span></span>
