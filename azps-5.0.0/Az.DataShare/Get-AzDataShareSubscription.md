---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: 910afff2a9c5524d452c5a5f4bec48a3f18359a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305273"
---
# <span data-ttu-id="1602d-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="1602d-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="1602d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1602d-102">SYNOPSIS</span></span>
<span data-ttu-id="1602d-103">데이터 공유 계정의 공유 구독에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1602d-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="1602d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1602d-104">SYNTAX</span></span>

### <span data-ttu-id="1602d-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="1602d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1602d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1602d-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1602d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1602d-107">DESCRIPTION</span></span>
<span data-ttu-id="1602d-108">**AzDataShareSubscription** cmdlet은 데이터 공유 계정의 공유 구독에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1602d-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="1602d-109">공유 구독 이름을 제공 하는 경우 cmdlet은 특정 공유 구독에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1602d-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="1602d-110">그렇지 않으면 cmdlet이 데이터 공유 계정에서 공유 구독 목록을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1602d-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="1602d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1602d-111">EXAMPLES</span></span>

### <span data-ttu-id="1602d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="1602d-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"

CreatedAt               : 7/9/2019 12:32:53 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 0c14f5b6-0e22-49ab-8043-d6edad51db13
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Test
ShareDescription        : Ads description
ShareTerms              : Ads terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="1602d-113">이 명령은 데이터 공유 계정 WikiAds의 구독 AdsShareSubscription 공유에 대 한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="1602d-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="1602d-114">변수</span><span class="sxs-lookup"><span data-stu-id="1602d-114">PARAMETERS</span></span>

### <span data-ttu-id="1602d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1602d-115">-AccountName</span></span>
<span data-ttu-id="1602d-116">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="1602d-116">Azure data share account name</span></span>

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

### <span data-ttu-id="1602d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1602d-117">-DefaultProfile</span></span>
<span data-ttu-id="1602d-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1602d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1602d-119">-이름</span><span class="sxs-lookup"><span data-stu-id="1602d-119">-Name</span></span>
<span data-ttu-id="1602d-120">Azure data share 구독 이름</span><span class="sxs-lookup"><span data-stu-id="1602d-120">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1602d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1602d-121">-ResourceGroupName</span></span>
<span data-ttu-id="1602d-122">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1602d-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="1602d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1602d-123">-ResourceId</span></span>
<span data-ttu-id="1602d-124">Azure data share 구독의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="1602d-124">The resource id of the azure data share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1602d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1602d-125">CommonParameters</span></span>
<span data-ttu-id="1602d-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1602d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1602d-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1602d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1602d-128">입력</span><span class="sxs-lookup"><span data-stu-id="1602d-128">INPUTS</span></span>

### <span data-ttu-id="1602d-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1602d-129">System.String</span></span>

## <span data-ttu-id="1602d-130">출력</span><span class="sxs-lookup"><span data-stu-id="1602d-130">OUTPUTS</span></span>

### <span data-ttu-id="1602d-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="1602d-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="1602d-132">상속자</span><span class="sxs-lookup"><span data-stu-id="1602d-132">NOTES</span></span>

## <span data-ttu-id="1602d-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1602d-133">RELATED LINKS</span></span>
