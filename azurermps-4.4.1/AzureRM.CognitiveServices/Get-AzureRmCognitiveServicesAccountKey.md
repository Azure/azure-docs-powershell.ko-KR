---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: f9b9f48d671bd0cbae0b7f8a26eccb21f372c4ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531155"
---
# <span data-ttu-id="219c6-101">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="219c6-101">Get-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="219c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="219c6-102">SYNOPSIS</span></span>
<span data-ttu-id="219c6-103">계정에 대 한 API 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="219c6-103">Gets the API keys for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="219c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="219c6-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="219c6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="219c6-105">DESCRIPTION</span></span>
<span data-ttu-id="219c6-106">**AzureRmCognitiveServicesAccountKey** cmdlet은 프로 비전 된 인식 서비스 계정에 대 한 API 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="219c6-106">The **Get-AzureRmCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>

<span data-ttu-id="219c6-107">인지 서비스 계정에는 Key1 및 Key2의 두 가지 API 키가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="219c6-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="219c6-108">키를 사용 하면 인식 서비스 계정 끝점과 상호 작용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="219c6-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>

<span data-ttu-id="219c6-109">New-AzureRmCognitiveServicesAccountKey를 사용 하 여 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="219c6-109">Use New-AzureRmCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="219c6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="219c6-110">EXAMPLES</span></span>

## <span data-ttu-id="219c6-111">변수</span><span class="sxs-lookup"><span data-stu-id="219c6-111">PARAMETERS</span></span>

### <span data-ttu-id="219c6-112">-이름</span><span class="sxs-lookup"><span data-stu-id="219c6-112">-Name</span></span>
<span data-ttu-id="219c6-113">계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="219c6-113">Specifies the name of the account.</span></span>
<span data-ttu-id="219c6-114">이 cmdlet은이 계정에 대 한 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="219c6-114">This cmdlet gets the keys for this account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="219c6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="219c6-115">-ResourceGroupName</span></span>
<span data-ttu-id="219c6-116">계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="219c6-116">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="219c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="219c6-117">-DefaultProfile</span></span>
<span data-ttu-id="219c6-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="219c6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219c6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="219c6-119">CommonParameters</span></span>
<span data-ttu-id="219c6-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="219c6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="219c6-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="219c6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="219c6-122">입력</span><span class="sxs-lookup"><span data-stu-id="219c6-122">INPUTS</span></span>

## <span data-ttu-id="219c6-123">출력</span><span class="sxs-lookup"><span data-stu-id="219c6-123">OUTPUTS</span></span>

### <span data-ttu-id="219c6-124">CognitiveServices. PSCognitiveServicesAccountKeys/. \*</span><span class="sxs-lookup"><span data-stu-id="219c6-124">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="219c6-125">상속자</span><span class="sxs-lookup"><span data-stu-id="219c6-125">NOTES</span></span>

## <span data-ttu-id="219c6-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="219c6-126">RELATED LINKS</span></span>

[<span data-ttu-id="219c6-127">새로운 AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="219c6-127">New-AzureRmCognitiveServicesAccountKey</span></span>](./New-AzureRmCognitiveServicesAccountKey.md)


