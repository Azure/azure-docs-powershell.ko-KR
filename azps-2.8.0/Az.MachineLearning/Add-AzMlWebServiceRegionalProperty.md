---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: 877ef93dbecf3510887a24cb0b5dfe65948658f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689454"
---
# <span data-ttu-id="10915-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="10915-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="10915-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10915-102">SYNOPSIS</span></span>
<span data-ttu-id="10915-103">지역 웹 서비스 속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="10915-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="10915-104">구문과</span><span class="sxs-lookup"><span data-stu-id="10915-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10915-105">설명은</span><span class="sxs-lookup"><span data-stu-id="10915-105">DESCRIPTION</span></span>
<span data-ttu-id="10915-106">기존 웹 서비스에 대 한 Azure 기계 학습 국가별 속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="10915-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="10915-107">예제의</span><span class="sxs-lookup"><span data-stu-id="10915-107">EXAMPLES</span></span>

### <span data-ttu-id="10915-108">예제 1: 미국 중부 US에 대 한 새 국가별 속성 추가</span><span class="sxs-lookup"><span data-stu-id="10915-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="10915-109">이 예제 명령은 "서쪽 중부 US" 지역의 웹 서비스에 대 한 국가별 속성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="10915-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="10915-110">변수</span><span class="sxs-lookup"><span data-stu-id="10915-110">PARAMETERS</span></span>

### <span data-ttu-id="10915-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10915-111">-DefaultProfile</span></span>
<span data-ttu-id="10915-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="10915-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10915-113">-Force</span><span class="sxs-lookup"><span data-stu-id="10915-113">-Force</span></span>
<span data-ttu-id="10915-114">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10915-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="10915-115">-이름</span><span class="sxs-lookup"><span data-stu-id="10915-115">-Name</span></span>
<span data-ttu-id="10915-116">웹 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="10915-116">The name for the web service.</span></span>

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

### <span data-ttu-id="10915-117">-지역</span><span class="sxs-lookup"><span data-stu-id="10915-117">-Region</span></span>
<span data-ttu-id="10915-118">웹 서비스 속성을 만들 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="10915-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="10915-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10915-119">-ResourceGroupName</span></span>
<span data-ttu-id="10915-120">웹 서비스가 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="10915-120">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="10915-121">-확인</span><span class="sxs-lookup"><span data-stu-id="10915-121">-Confirm</span></span>
<span data-ttu-id="10915-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="10915-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10915-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10915-123">-WhatIf</span></span>
<span data-ttu-id="10915-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="10915-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10915-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10915-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10915-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10915-126">CommonParameters</span></span>
<span data-ttu-id="10915-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="10915-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10915-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10915-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10915-129">입력</span><span class="sxs-lookup"><span data-stu-id="10915-129">INPUTS</span></span>

### <span data-ttu-id="10915-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="10915-130">System.String</span></span>

## <span data-ttu-id="10915-131">출력</span><span class="sxs-lookup"><span data-stu-id="10915-131">OUTPUTS</span></span>

### <span data-ttu-id="10915-132">MachineLearning. WebServices의 웹 서비스</span><span class="sxs-lookup"><span data-stu-id="10915-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="10915-133">상속자</span><span class="sxs-lookup"><span data-stu-id="10915-133">NOTES</span></span>
<span data-ttu-id="10915-134">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="10915-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="10915-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10915-135">RELATED LINKS</span></span>
