---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareprovidersharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
ms.openlocfilehash: a94d879573be2d640269510283e341cbad8aa052
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034630"
---
# <span data-ttu-id="bd365-101">Get-AzDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="bd365-101">Get-AzDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="bd365-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd365-102">SYNOPSIS</span></span>
<span data-ttu-id="bd365-103">공급자 측의 소비자 공유 구독에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bd365-103">Gets information about consumer share subscriptions on provider side.</span></span>

## <span data-ttu-id="bd365-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bd365-104">SYNTAX</span></span>

### <span data-ttu-id="bd365-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bd365-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareProviderShareSubscription -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-ShareSubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd365-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd365-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Get-AzDataShareProviderShareSubscription [-ShareSubscriptionId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd365-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bd365-107">DESCRIPTION</span></span>
<span data-ttu-id="bd365-108">**AzDataShareProviderSubscription** cmdlet은 공급자 측의 소비자 공유 구독에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bd365-108">The **Get-AzDataShareProviderSubscription** cmdlet gets information about consumer share subscriptions on provider side.</span></span> <span data-ttu-id="bd365-109">공유 subscrption id를 지정 하는 경우이 cmdlet은 공유 구독에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bd365-109">If you specify the share subscrption id, this cmdlet gets information about the share subscription.</span></span> <span data-ttu-id="bd365-110">공유 구독 id를 지정 하지 않으면이 cmdlet은 공유와 연결 된 모든 소비자 공유 구독에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bd365-110">If you do not specify the share subscription id, this cmdlet gets information about all the consumer share subscriptions in associated with the share.</span></span>

## <span data-ttu-id="bd365-111">예제의</span><span class="sxs-lookup"><span data-stu-id="bd365-111">EXAMPLES</span></span>

### <span data-ttu-id="bd365-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="bd365-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareProviderShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -ShareSubscriptionId "/subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a"

Company                   : ADS Test
CreatedAt                 : 6/30/2019 12:42:12 AM
CreatedBy                 : adstest@microsoft.com
SharedAt                  : 6/30/2019 12:41:37 AM
SharedBy                  : adsprovider@microsoft.com
ShareSubscriptionObjectId : 505c3500-b2ff-46ab-96bf-50f5ec89d75a
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a
Name                      : AdsShareSubscription
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="bd365-113">이 명령은 데이터 공유 계정 WikiAds에서 공유 공유와 연결 된 소비자 공유 구독에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd365-113">This commands provides information about consumer share subscription associated with share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="bd365-114">변수</span><span class="sxs-lookup"><span data-stu-id="bd365-114">PARAMETERS</span></span>

### <span data-ttu-id="bd365-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bd365-115">-AccountName</span></span>
<span data-ttu-id="bd365-116">Azure DataShare 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd365-116">Azure DataShare Account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd365-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd365-117">-DefaultProfile</span></span>
<span data-ttu-id="bd365-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd365-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd365-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd365-119">-ResourceGroupName</span></span>
<span data-ttu-id="bd365-120">Azure DataShare 계정의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="bd365-120">The resource group of the Azure DataShare Account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd365-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd365-121">-ResourceId</span></span>
<span data-ttu-id="bd365-122">공유의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="bd365-122">The resource id of the share</span></span>

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd365-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="bd365-123">-ShareName</span></span>
<span data-ttu-id="bd365-124">Azure DataShare 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd365-124">Azure DataShare name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd365-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd365-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="bd365-126">소비자 공유 구독의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="bd365-126">The id of consumer share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd365-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd365-127">CommonParameters</span></span>
<span data-ttu-id="bd365-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd365-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd365-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd365-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd365-130">입력</span><span class="sxs-lookup"><span data-stu-id="bd365-130">INPUTS</span></span>

### <span data-ttu-id="bd365-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bd365-131">System.String</span></span>

## <span data-ttu-id="bd365-132">출력</span><span class="sxs-lookup"><span data-stu-id="bd365-132">OUTPUTS</span></span>

### <span data-ttu-id="bd365-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="bd365-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="bd365-134">상속자</span><span class="sxs-lookup"><span data-stu-id="bd365-134">NOTES</span></span>

## <span data-ttu-id="bd365-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd365-135">RELATED LINKS</span></span>
