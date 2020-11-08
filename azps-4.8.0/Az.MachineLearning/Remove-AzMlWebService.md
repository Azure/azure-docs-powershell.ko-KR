---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 4a59508cc816f3301d76b1d982f52108247b50a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211667"
---
# <span data-ttu-id="05013-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="05013-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="05013-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05013-102">SYNOPSIS</span></span>
<span data-ttu-id="05013-103">웹 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="05013-103">Deletes a web service.</span></span>

## <span data-ttu-id="05013-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05013-104">SYNTAX</span></span>

### <span data-ttu-id="05013-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="05013-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05013-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="05013-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05013-107">설명은</span><span class="sxs-lookup"><span data-stu-id="05013-107">DESCRIPTION</span></span>
<span data-ttu-id="05013-108">리소스 그룹 및 이름에서 참조 하는 Azure 기계 학습 웹 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="05013-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="05013-109">예제의</span><span class="sxs-lookup"><span data-stu-id="05013-109">EXAMPLES</span></span>

### <span data-ttu-id="05013-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="05013-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="05013-111">변수</span><span class="sxs-lookup"><span data-stu-id="05013-111">PARAMETERS</span></span>

### <span data-ttu-id="05013-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05013-112">-DefaultProfile</span></span>
<span data-ttu-id="05013-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="05013-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05013-114">-Force</span><span class="sxs-lookup"><span data-stu-id="05013-114">-Force</span></span>
<span data-ttu-id="05013-115">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05013-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="05013-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="05013-116">-MlWebService</span></span>
<span data-ttu-id="05013-117">제거할 웹 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="05013-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="05013-118">-이름</span><span class="sxs-lookup"><span data-stu-id="05013-118">-Name</span></span>
<span data-ttu-id="05013-119">제거할 웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05013-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="05013-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05013-120">-ResourceGroupName</span></span>
<span data-ttu-id="05013-121">웹 서비스의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="05013-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="05013-122">-확인</span><span class="sxs-lookup"><span data-stu-id="05013-122">-Confirm</span></span>
<span data-ttu-id="05013-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="05013-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05013-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05013-124">-WhatIf</span></span>
<span data-ttu-id="05013-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="05013-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05013-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05013-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05013-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05013-127">CommonParameters</span></span>
<span data-ttu-id="05013-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05013-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05013-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05013-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05013-130">입력</span><span class="sxs-lookup"><span data-stu-id="05013-130">INPUTS</span></span>

### <span data-ttu-id="05013-131">MachineLearning. WebServices의 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="05013-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="05013-132">출력</span><span class="sxs-lookup"><span data-stu-id="05013-132">OUTPUTS</span></span>

### <span data-ttu-id="05013-133">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="05013-133">System.Void</span></span>

## <span data-ttu-id="05013-134">상속자</span><span class="sxs-lookup"><span data-stu-id="05013-134">NOTES</span></span>
<span data-ttu-id="05013-135">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="05013-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="05013-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05013-136">RELATED LINKS</span></span>
