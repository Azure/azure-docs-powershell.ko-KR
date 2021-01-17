---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: c9d7f205da9adbe199f2c8e33685612fd547feb7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386107"
---
# <span data-ttu-id="3c16f-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="3c16f-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="3c16f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c16f-102">SYNOPSIS</span></span>
<span data-ttu-id="3c16f-103">지역별 웹 서비스 속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3c16f-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="3c16f-104">구문</span><span class="sxs-lookup"><span data-stu-id="3c16f-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c16f-105">설명</span><span class="sxs-lookup"><span data-stu-id="3c16f-105">DESCRIPTION</span></span>
<span data-ttu-id="3c16f-106">기존 웹 서비스에 대한 Azure Machine Learning 지역 속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3c16f-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="3c16f-107">예제</span><span class="sxs-lookup"><span data-stu-id="3c16f-107">EXAMPLES</span></span>

### <span data-ttu-id="3c16f-108">예제 1: 미국 중서부에 대한 새 지역 속성 추가</span><span class="sxs-lookup"><span data-stu-id="3c16f-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="3c16f-109">이 예제 명령은 "미국 중서부" 지역에 웹 서비스에 대한 지역 속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3c16f-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="3c16f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c16f-110">PARAMETERS</span></span>

### <span data-ttu-id="3c16f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c16f-111">-DefaultProfile</span></span>
<span data-ttu-id="3c16f-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3c16f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c16f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3c16f-113">-Force</span></span>
<span data-ttu-id="3c16f-114">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c16f-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3c16f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3c16f-115">-Name</span></span>
<span data-ttu-id="3c16f-116">웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c16f-116">The name for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c16f-117">-Region</span><span class="sxs-lookup"><span data-stu-id="3c16f-117">-Region</span></span>
<span data-ttu-id="3c16f-118">웹 서비스 속성을 만들 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="3c16f-118">The region in which to create the web service properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c16f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c16f-119">-ResourceGroupName</span></span>
<span data-ttu-id="3c16f-120">웹 서비스가 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="3c16f-120">The resource group in which the web service belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c16f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c16f-121">-Confirm</span></span>
<span data-ttu-id="3c16f-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c16f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c16f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c16f-123">-WhatIf</span></span>
<span data-ttu-id="3c16f-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3c16f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c16f-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c16f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c16f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c16f-126">CommonParameters</span></span>
<span data-ttu-id="3c16f-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3c16f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c16f-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3c16f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c16f-129">입력</span><span class="sxs-lookup"><span data-stu-id="3c16f-129">INPUTS</span></span>

### <span data-ttu-id="3c16f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3c16f-130">System.String</span></span>

## <span data-ttu-id="3c16f-131">출력</span><span class="sxs-lookup"><span data-stu-id="3c16f-131">OUTPUTS</span></span>

### <span data-ttu-id="3c16f-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="3c16f-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="3c16f-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3c16f-133">NOTES</span></span>
<span data-ttu-id="3c16f-134">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="3c16f-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3c16f-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c16f-135">RELATED LINKS</span></span>
