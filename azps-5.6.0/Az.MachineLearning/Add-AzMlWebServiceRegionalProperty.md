---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: 8b645154e9aaa011fccf1fa01624481e44b4eebb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952352"
---
# <span data-ttu-id="f80ab-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="f80ab-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="f80ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f80ab-102">SYNOPSIS</span></span>
<span data-ttu-id="f80ab-103">지역 웹 서비스 속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f80ab-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="f80ab-104">구문</span><span class="sxs-lookup"><span data-stu-id="f80ab-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f80ab-105">설명</span><span class="sxs-lookup"><span data-stu-id="f80ab-105">DESCRIPTION</span></span>
<span data-ttu-id="f80ab-106">기존 웹 서비스에 대한 Azure Machine Learning 지역 속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f80ab-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="f80ab-107">예제</span><span class="sxs-lookup"><span data-stu-id="f80ab-107">EXAMPLES</span></span>

### <span data-ttu-id="f80ab-108">예제 1: 미국 중서부에 대한 새 지역 속성 추가</span><span class="sxs-lookup"><span data-stu-id="f80ab-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="f80ab-109">이 예제 명령은 "미국 중서부" 지역에 있는 웹 서비스에 대한 지역 속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f80ab-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="f80ab-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f80ab-110">PARAMETERS</span></span>

### <span data-ttu-id="f80ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f80ab-111">-DefaultProfile</span></span>
<span data-ttu-id="f80ab-112">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f80ab-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f80ab-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f80ab-113">-Force</span></span>
<span data-ttu-id="f80ab-114">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f80ab-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f80ab-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f80ab-115">-Name</span></span>
<span data-ttu-id="f80ab-116">웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f80ab-116">The name for the web service.</span></span>

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

### <span data-ttu-id="f80ab-117">-Region</span><span class="sxs-lookup"><span data-stu-id="f80ab-117">-Region</span></span>
<span data-ttu-id="f80ab-118">웹 서비스 속성을 만들 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="f80ab-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="f80ab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f80ab-119">-ResourceGroupName</span></span>
<span data-ttu-id="f80ab-120">웹 서비스가 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="f80ab-120">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="f80ab-121">-확인</span><span class="sxs-lookup"><span data-stu-id="f80ab-121">-Confirm</span></span>
<span data-ttu-id="f80ab-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f80ab-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f80ab-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f80ab-123">-WhatIf</span></span>
<span data-ttu-id="f80ab-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f80ab-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f80ab-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f80ab-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f80ab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f80ab-126">CommonParameters</span></span>
<span data-ttu-id="f80ab-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f80ab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f80ab-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f80ab-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f80ab-129">입력</span><span class="sxs-lookup"><span data-stu-id="f80ab-129">INPUTS</span></span>

### <span data-ttu-id="f80ab-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f80ab-130">System.String</span></span>

## <span data-ttu-id="f80ab-131">출력</span><span class="sxs-lookup"><span data-stu-id="f80ab-131">OUTPUTS</span></span>

### <span data-ttu-id="f80ab-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="f80ab-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="f80ab-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f80ab-133">NOTES</span></span>
<span data-ttu-id="f80ab-134">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="f80ab-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f80ab-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f80ab-135">RELATED LINKS</span></span>
