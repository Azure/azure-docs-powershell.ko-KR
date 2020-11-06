---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 230c47e67610cdeea629097f26c73cb2774c5384
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531767"
---
# <span data-ttu-id="227cc-101">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="227cc-101">Get-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="227cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="227cc-102">SYNOPSIS</span></span>
<span data-ttu-id="227cc-103">계정에 대 한 API 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="227cc-103">Gets the API keys for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="227cc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="227cc-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="227cc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="227cc-105">DESCRIPTION</span></span>
<span data-ttu-id="227cc-106">**AzureRmCognitiveServicesAccountKey** cmdlet은 프로 비전 된 인식 서비스 계정에 대 한 API 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="227cc-106">The **Get-AzureRmCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>

<span data-ttu-id="227cc-107">인지 서비스 계정에는 Key1 및 Key2의 두 가지 API 키가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="227cc-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="227cc-108">키를 사용 하면 인식 서비스 계정 끝점과 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="227cc-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>

<span data-ttu-id="227cc-109">New-AzureRmCognitiveServicesAccountKey를 사용 하 여 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="227cc-109">Use New-AzureRmCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="227cc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="227cc-110">EXAMPLES</span></span>

## <span data-ttu-id="227cc-111">변수</span><span class="sxs-lookup"><span data-stu-id="227cc-111">PARAMETERS</span></span>

### <span data-ttu-id="227cc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="227cc-112">-DefaultProfile</span></span>
<span data-ttu-id="227cc-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="227cc-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="227cc-114">-이름</span><span class="sxs-lookup"><span data-stu-id="227cc-114">-Name</span></span>
<span data-ttu-id="227cc-115">계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="227cc-115">Specifies the name of the account.</span></span>
<span data-ttu-id="227cc-116">이 cmdlet은이 계정에 대 한 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="227cc-116">This cmdlet gets the keys for this account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="227cc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="227cc-117">-ResourceGroupName</span></span>
<span data-ttu-id="227cc-118">계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="227cc-118">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="227cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="227cc-119">CommonParameters</span></span>
<span data-ttu-id="227cc-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="227cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="227cc-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="227cc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="227cc-122">입력</span><span class="sxs-lookup"><span data-stu-id="227cc-122">INPUTS</span></span>

### <span data-ttu-id="227cc-123">않아야</span><span class="sxs-lookup"><span data-stu-id="227cc-123">None</span></span>
<span data-ttu-id="227cc-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="227cc-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="227cc-125">출력</span><span class="sxs-lookup"><span data-stu-id="227cc-125">OUTPUTS</span></span>

### <span data-ttu-id="227cc-126">CognitiveServices. PSCognitiveServicesAccountKeys/. \*</span><span class="sxs-lookup"><span data-stu-id="227cc-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="227cc-127">상속자</span><span class="sxs-lookup"><span data-stu-id="227cc-127">NOTES</span></span>

## <span data-ttu-id="227cc-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="227cc-128">RELATED LINKS</span></span>

[<span data-ttu-id="227cc-129">새로운 AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="227cc-129">New-AzureRmCognitiveServicesAccountKey</span></span>](./New-AzureRmCognitiveServicesAccountKey.md)


