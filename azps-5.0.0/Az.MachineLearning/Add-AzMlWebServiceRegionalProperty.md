---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: c9d7f205da9adbe199f2c8e33685612fd547feb7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218941"
---
# <span data-ttu-id="8d70c-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="8d70c-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="8d70c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d70c-102">SYNOPSIS</span></span>
<span data-ttu-id="8d70c-103">지역 웹 서비스 속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d70c-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="8d70c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d70c-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d70c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8d70c-105">DESCRIPTION</span></span>
<span data-ttu-id="8d70c-106">기존 웹 서비스에 대 한 Azure 기계 학습 국가별 속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d70c-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="8d70c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8d70c-107">EXAMPLES</span></span>

### <span data-ttu-id="8d70c-108">예제 1: 미국 중부 US에 대 한 새 국가별 속성 추가</span><span class="sxs-lookup"><span data-stu-id="8d70c-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="8d70c-109">이 예제 명령은 "서쪽 중부 US" 지역의 웹 서비스에 대 한 국가별 속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d70c-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="8d70c-110">변수</span><span class="sxs-lookup"><span data-stu-id="8d70c-110">PARAMETERS</span></span>

### <span data-ttu-id="8d70c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d70c-111">-DefaultProfile</span></span>
<span data-ttu-id="8d70c-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8d70c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d70c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8d70c-113">-Force</span></span>
<span data-ttu-id="8d70c-114">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d70c-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8d70c-115">-이름</span><span class="sxs-lookup"><span data-stu-id="8d70c-115">-Name</span></span>
<span data-ttu-id="8d70c-116">웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d70c-116">The name for the web service.</span></span>

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

### <span data-ttu-id="8d70c-117">-지역</span><span class="sxs-lookup"><span data-stu-id="8d70c-117">-Region</span></span>
<span data-ttu-id="8d70c-118">웹 서비스 속성을 만들 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="8d70c-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="8d70c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d70c-119">-ResourceGroupName</span></span>
<span data-ttu-id="8d70c-120">웹 서비스가 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="8d70c-120">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="8d70c-121">-확인</span><span class="sxs-lookup"><span data-stu-id="8d70c-121">-Confirm</span></span>
<span data-ttu-id="8d70c-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d70c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d70c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d70c-123">-WhatIf</span></span>
<span data-ttu-id="8d70c-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8d70c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d70c-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d70c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d70c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d70c-126">CommonParameters</span></span>
<span data-ttu-id="8d70c-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d70c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d70c-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d70c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d70c-129">입력</span><span class="sxs-lookup"><span data-stu-id="8d70c-129">INPUTS</span></span>

### <span data-ttu-id="8d70c-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d70c-130">System.String</span></span>

## <span data-ttu-id="8d70c-131">출력</span><span class="sxs-lookup"><span data-stu-id="8d70c-131">OUTPUTS</span></span>

### <span data-ttu-id="8d70c-132">MachineLearning. WebServices의 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="8d70c-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="8d70c-133">상속자</span><span class="sxs-lookup"><span data-stu-id="8d70c-133">NOTES</span></span>
<span data-ttu-id="8d70c-134">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="8d70c-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="8d70c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d70c-135">RELATED LINKS</span></span>
