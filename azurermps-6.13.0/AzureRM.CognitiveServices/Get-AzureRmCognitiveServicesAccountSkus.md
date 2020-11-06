---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountskus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: e1bacc62ca7efc3bd453be93196e83b0b6d67853
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532487"
---
# <span data-ttu-id="e68ef-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="e68ef-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="e68ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e68ef-102">SYNOPSIS</span></span>
<span data-ttu-id="e68ef-103">계정에 사용할 수 있는 Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e68ef-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e68ef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e68ef-104">SYNTAX</span></span>

### <span data-ttu-id="e68ef-105">Geta 서 Uswithaccount (기본값)</span><span class="sxs-lookup"><span data-stu-id="e68ef-105">GetSkusWithAccount (Default)</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e68ef-106">Geta 서 Uswithfilter</span><span class="sxs-lookup"><span data-stu-id="e68ef-106">GetSkusWithFilter</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e68ef-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e68ef-107">DESCRIPTION</span></span>
<span data-ttu-id="e68ef-108">**AzureRmCognitiveServicesAccountSkus** Cmdlet은 인식 서비스 계정에 사용할 수 있는 sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e68ef-108">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="e68ef-109">SKU는 거래처에 대 한 계층 계획입니다.</span><span class="sxs-lookup"><span data-stu-id="e68ef-109">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="e68ef-110">계정에 대 한 가격, 통화 제한 및 요금을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="e68ef-110">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="e68ef-111">F0 SKU는 무료 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="e68ef-111">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="e68ef-112">유료 계층에는 S0, S1, S2 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e68ef-112">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="e68ef-113">예제의</span><span class="sxs-lookup"><span data-stu-id="e68ef-113">EXAMPLES</span></span>

### <span data-ttu-id="e68ef-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="e68ef-114">Example 1</span></span>
```powershell
PS C:\> (Get-AzureRmCognitiveServicesAccountSkus -ResourceGroupName cognitive-services-resource-group -Name myluis).Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="e68ef-115">변수</span><span class="sxs-lookup"><span data-stu-id="e68ef-115">PARAMETERS</span></span>

### <span data-ttu-id="e68ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e68ef-116">-DefaultProfile</span></span>
<span data-ttu-id="e68ef-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e68ef-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e68ef-118">-위치</span><span class="sxs-lookup"><span data-stu-id="e68ef-118">-Location</span></span>
<span data-ttu-id="e68ef-119">인식 서비스 계정 위치.</span><span class="sxs-lookup"><span data-stu-id="e68ef-119">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e68ef-120">-이름</span><span class="sxs-lookup"><span data-stu-id="e68ef-120">-Name</span></span>
<span data-ttu-id="e68ef-121">계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e68ef-121">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e68ef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e68ef-122">-ResourceGroupName</span></span>
<span data-ttu-id="e68ef-123">계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e68ef-123">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e68ef-124">-Type</span><span class="sxs-lookup"><span data-stu-id="e68ef-124">-Type</span></span>
<span data-ttu-id="e68ef-125">인식 서비스 계정 유형.</span><span class="sxs-lookup"><span data-stu-id="e68ef-125">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e68ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e68ef-126">CommonParameters</span></span>
<span data-ttu-id="e68ef-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e68ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e68ef-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e68ef-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e68ef-129">입력</span><span class="sxs-lookup"><span data-stu-id="e68ef-129">INPUTS</span></span>

### <span data-ttu-id="e68ef-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e68ef-130">System.String</span></span>

## <span data-ttu-id="e68ef-131">출력</span><span class="sxs-lookup"><span data-stu-id="e68ef-131">OUTPUTS</span></span>

### <span data-ttu-id="e68ef-132">CognitiveServices. PSCognitiveServicesSkus/. \*</span><span class="sxs-lookup"><span data-stu-id="e68ef-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="e68ef-133">상속자</span><span class="sxs-lookup"><span data-stu-id="e68ef-133">NOTES</span></span>

## <span data-ttu-id="e68ef-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e68ef-134">RELATED LINKS</span></span>
