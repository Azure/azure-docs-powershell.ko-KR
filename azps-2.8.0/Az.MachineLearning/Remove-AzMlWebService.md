---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 2ade770ea51f3b9cb83ff04fc5edf604cab5bb71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689421"
---
# <span data-ttu-id="16736-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="16736-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="16736-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16736-102">SYNOPSIS</span></span>
<span data-ttu-id="16736-103">웹 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="16736-103">Deletes a web service.</span></span>

## <span data-ttu-id="16736-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16736-104">SYNTAX</span></span>

### <span data-ttu-id="16736-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="16736-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16736-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="16736-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16736-107">설명은</span><span class="sxs-lookup"><span data-stu-id="16736-107">DESCRIPTION</span></span>
<span data-ttu-id="16736-108">리소스 그룹 및 이름에서 참조 하는 Azure 기계 학습 웹 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="16736-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="16736-109">예제의</span><span class="sxs-lookup"><span data-stu-id="16736-109">EXAMPLES</span></span>

### <span data-ttu-id="16736-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="16736-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="16736-111">변수</span><span class="sxs-lookup"><span data-stu-id="16736-111">PARAMETERS</span></span>

### <span data-ttu-id="16736-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16736-112">-DefaultProfile</span></span>
<span data-ttu-id="16736-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="16736-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16736-114">-Force</span><span class="sxs-lookup"><span data-stu-id="16736-114">-Force</span></span>
<span data-ttu-id="16736-115">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16736-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="16736-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="16736-116">-MlWebService</span></span>
<span data-ttu-id="16736-117">제거할 웹 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="16736-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="16736-118">-이름</span><span class="sxs-lookup"><span data-stu-id="16736-118">-Name</span></span>
<span data-ttu-id="16736-119">제거할 웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16736-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="16736-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16736-120">-ResourceGroupName</span></span>
<span data-ttu-id="16736-121">웹 서비스의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="16736-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="16736-122">-확인</span><span class="sxs-lookup"><span data-stu-id="16736-122">-Confirm</span></span>
<span data-ttu-id="16736-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="16736-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16736-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16736-124">-WhatIf</span></span>
<span data-ttu-id="16736-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="16736-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16736-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16736-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16736-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16736-127">CommonParameters</span></span>
<span data-ttu-id="16736-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16736-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16736-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16736-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16736-130">입력</span><span class="sxs-lookup"><span data-stu-id="16736-130">INPUTS</span></span>

### <span data-ttu-id="16736-131">MachineLearning. WebServices의 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="16736-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="16736-132">출력</span><span class="sxs-lookup"><span data-stu-id="16736-132">OUTPUTS</span></span>

### <span data-ttu-id="16736-133">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="16736-133">System.Void</span></span>

## <span data-ttu-id="16736-134">상속자</span><span class="sxs-lookup"><span data-stu-id="16736-134">NOTES</span></span>
<span data-ttu-id="16736-135">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="16736-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="16736-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16736-136">RELATED LINKS</span></span>
