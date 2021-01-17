---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: 910afff2a9c5524d452c5a5f4bec48a3f18359a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365989"
---
# <span data-ttu-id="1bf31-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="1bf31-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="1bf31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bf31-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf31-103">데이터 공유 계정의 공유 구독에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1bf31-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="1bf31-104">구문</span><span class="sxs-lookup"><span data-stu-id="1bf31-104">SYNTAX</span></span>

### <span data-ttu-id="1bf31-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1bf31-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bf31-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bf31-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1bf31-107">설명</span><span class="sxs-lookup"><span data-stu-id="1bf31-107">DESCRIPTION</span></span>
<span data-ttu-id="1bf31-108">**Get-AzDataShareSubscription** cmdlet은 데이터 공유 계정의 공유 구독에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="1bf31-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="1bf31-109">공유 구독 이름이 제공된 경우 cmdlet은 특정 공유 구독에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="1bf31-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="1bf31-110">그렇지 않은 경우 cmdlet은 데이터 공유 계정의 공유 구독 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="1bf31-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="1bf31-111">예제</span><span class="sxs-lookup"><span data-stu-id="1bf31-111">EXAMPLES</span></span>

### <span data-ttu-id="1bf31-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="1bf31-112">Example 1</span></span>
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

<span data-ttu-id="1bf31-113">이 명령은 데이터 공유 계정 WikiAds의 공유 구독 AdsShareSubscription에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="1bf31-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="1bf31-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bf31-114">PARAMETERS</span></span>

### <span data-ttu-id="1bf31-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1bf31-115">-AccountName</span></span>
<span data-ttu-id="1bf31-116">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="1bf31-116">Azure data share account name</span></span>

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

### <span data-ttu-id="1bf31-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf31-117">-DefaultProfile</span></span>
<span data-ttu-id="1bf31-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1bf31-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bf31-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1bf31-119">-Name</span></span>
<span data-ttu-id="1bf31-120">Azure 데이터 공유 구독 이름</span><span class="sxs-lookup"><span data-stu-id="1bf31-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="1bf31-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bf31-121">-ResourceGroupName</span></span>
<span data-ttu-id="1bf31-122">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1bf31-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="1bf31-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bf31-123">-ResourceId</span></span>
<span data-ttu-id="1bf31-124">Azure 데이터 공유 구독의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="1bf31-124">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="1bf31-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf31-125">CommonParameters</span></span>
<span data-ttu-id="1bf31-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1bf31-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf31-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1bf31-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf31-128">입력</span><span class="sxs-lookup"><span data-stu-id="1bf31-128">INPUTS</span></span>

### <span data-ttu-id="1bf31-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1bf31-129">System.String</span></span>

## <span data-ttu-id="1bf31-130">출력</span><span class="sxs-lookup"><span data-stu-id="1bf31-130">OUTPUTS</span></span>

### <span data-ttu-id="1bf31-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="1bf31-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="1bf31-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1bf31-132">NOTES</span></span>

## <span data-ttu-id="1bf31-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1bf31-133">RELATED LINKS</span></span>
