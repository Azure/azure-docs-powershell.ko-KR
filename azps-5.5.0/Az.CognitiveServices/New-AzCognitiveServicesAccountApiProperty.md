---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 97cf393d0d95dbc9ecfec06f53795713f59aecbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205040"
---
# <span data-ttu-id="38be5-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="38be5-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="38be5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38be5-102">SYNOPSIS</span></span>
<span data-ttu-id="38be5-103">Cognitive Services 계정 ApiProperties의 새 인스턴스 생성</span><span class="sxs-lookup"><span data-stu-id="38be5-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="38be5-104">구문</span><span class="sxs-lookup"><span data-stu-id="38be5-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38be5-105">설명</span><span class="sxs-lookup"><span data-stu-id="38be5-105">DESCRIPTION</span></span>
<span data-ttu-id="38be5-106">Cognitive Services 계정 ApiProperties의 새 인스턴스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="38be5-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="38be5-107">ApiProperties는 새 계정을 만들거나 기존 계정을 업데이트할 때 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38be5-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="38be5-108">ApiProperties는 특정 계정 유형에 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="38be5-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="38be5-109">예제</span><span class="sxs-lookup"><span data-stu-id="38be5-109">EXAMPLES</span></span>

### <span data-ttu-id="38be5-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="38be5-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="38be5-111">위의 예제에서는 API 속성 "QnaRuntimeEndpoint"를 사용하여 QnAMaker 계정을 만들 것입니다.</span><span class="sxs-lookup"><span data-stu-id="38be5-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="38be5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38be5-112">PARAMETERS</span></span>

### <span data-ttu-id="38be5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38be5-113">-DefaultProfile</span></span>
<span data-ttu-id="38be5-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38be5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38be5-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38be5-115">-Confirm</span></span>
<span data-ttu-id="38be5-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="38be5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38be5-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38be5-117">-WhatIf</span></span>
<span data-ttu-id="38be5-118">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="38be5-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38be5-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38be5-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38be5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38be5-120">CommonParameters</span></span>
<span data-ttu-id="38be5-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="38be5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38be5-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38be5-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38be5-123">입력</span><span class="sxs-lookup"><span data-stu-id="38be5-123">INPUTS</span></span>

### <span data-ttu-id="38be5-124">없음</span><span class="sxs-lookup"><span data-stu-id="38be5-124">None</span></span>

## <span data-ttu-id="38be5-125">출력</span><span class="sxs-lookup"><span data-stu-id="38be5-125">OUTPUTS</span></span>

### <span data-ttu-id="38be5-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="38be5-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="38be5-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="38be5-127">NOTES</span></span>

## <span data-ttu-id="38be5-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38be5-128">RELATED LINKS</span></span>
