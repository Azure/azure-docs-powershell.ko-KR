---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 97cf393d0d95dbc9ecfec06f53795713f59aecbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213684"
---
# <span data-ttu-id="26e7a-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="26e7a-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="26e7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="26e7a-103">인지 서비스 계정 ApiProperties의 새 인스턴스를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e7a-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="26e7a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26e7a-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26e7a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="26e7a-105">DESCRIPTION</span></span>
<span data-ttu-id="26e7a-106">인지 서비스 계정 ApiProperties의 새 인스턴스를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e7a-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="26e7a-107">ApiProperties를 사용 하 여 새 계정을 만들거나 기존 계정을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26e7a-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="26e7a-108">ApiProperties은 특정 계정 유형에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e7a-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="26e7a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="26e7a-109">EXAMPLES</span></span>

### <span data-ttu-id="26e7a-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="26e7a-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="26e7a-111">위의 예에서는 API 속성 "QnaRuntimeEndpoint"을 사용 하 여 QnAMaker 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26e7a-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="26e7a-112">변수</span><span class="sxs-lookup"><span data-stu-id="26e7a-112">PARAMETERS</span></span>

### <span data-ttu-id="26e7a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e7a-113">-DefaultProfile</span></span>
<span data-ttu-id="26e7a-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26e7a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26e7a-115">-확인</span><span class="sxs-lookup"><span data-stu-id="26e7a-115">-Confirm</span></span>
<span data-ttu-id="26e7a-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e7a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26e7a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e7a-117">-WhatIf</span></span>
<span data-ttu-id="26e7a-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="26e7a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26e7a-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26e7a-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26e7a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e7a-120">CommonParameters</span></span>
<span data-ttu-id="26e7a-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e7a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e7a-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="26e7a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e7a-123">입력</span><span class="sxs-lookup"><span data-stu-id="26e7a-123">INPUTS</span></span>

### <span data-ttu-id="26e7a-124">않아야</span><span class="sxs-lookup"><span data-stu-id="26e7a-124">None</span></span>

## <span data-ttu-id="26e7a-125">출력</span><span class="sxs-lookup"><span data-stu-id="26e7a-125">OUTPUTS</span></span>

### <span data-ttu-id="26e7a-126">CognitiveServices. CognitiveServicesAccountApiProperties/.</span><span class="sxs-lookup"><span data-stu-id="26e7a-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="26e7a-127">상속자</span><span class="sxs-lookup"><span data-stu-id="26e7a-127">NOTES</span></span>

## <span data-ttu-id="26e7a-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26e7a-128">RELATED LINKS</span></span>
