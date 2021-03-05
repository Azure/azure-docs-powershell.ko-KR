---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 50e62158d4b24282753c726845e7dd88d492843c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981195"
---
# <span data-ttu-id="11b36-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="11b36-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="11b36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11b36-102">SYNOPSIS</span></span>
<span data-ttu-id="11b36-103">Cognitive Services 계정 ApiProperties의 새 인스턴스 생성</span><span class="sxs-lookup"><span data-stu-id="11b36-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="11b36-104">구문</span><span class="sxs-lookup"><span data-stu-id="11b36-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11b36-105">설명</span><span class="sxs-lookup"><span data-stu-id="11b36-105">DESCRIPTION</span></span>
<span data-ttu-id="11b36-106">Cognitive Services 계정 ApiProperties의 새 인스턴스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="11b36-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="11b36-107">ApiProperties는 새 계정을 만들거나 기존 계정을 업데이트할 때 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11b36-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="11b36-108">ApiProperties는 특정 계정 유형에 따라 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="11b36-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="11b36-109">예제</span><span class="sxs-lookup"><span data-stu-id="11b36-109">EXAMPLES</span></span>

### <span data-ttu-id="11b36-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="11b36-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="11b36-111">위의 예제에서는 API 속성 "QnaRuntimeEndpoint"를 사용하여 QnAMaker 계정을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="11b36-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="11b36-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="11b36-112">PARAMETERS</span></span>

### <span data-ttu-id="11b36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b36-113">-DefaultProfile</span></span>
<span data-ttu-id="11b36-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11b36-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11b36-115">-확인</span><span class="sxs-lookup"><span data-stu-id="11b36-115">-Confirm</span></span>
<span data-ttu-id="11b36-116">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="11b36-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11b36-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11b36-117">-WhatIf</span></span>
<span data-ttu-id="11b36-118">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="11b36-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11b36-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11b36-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11b36-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b36-120">CommonParameters</span></span>
<span data-ttu-id="11b36-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="11b36-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b36-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11b36-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b36-123">입력</span><span class="sxs-lookup"><span data-stu-id="11b36-123">INPUTS</span></span>

### <span data-ttu-id="11b36-124">없음</span><span class="sxs-lookup"><span data-stu-id="11b36-124">None</span></span>

## <span data-ttu-id="11b36-125">출력</span><span class="sxs-lookup"><span data-stu-id="11b36-125">OUTPUTS</span></span>

### <span data-ttu-id="11b36-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="11b36-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="11b36-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="11b36-127">NOTES</span></span>

## <span data-ttu-id="11b36-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11b36-128">RELATED LINKS</span></span>
