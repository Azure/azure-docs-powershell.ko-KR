---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: e6b911831a84ce708af93ef6cc7b9f9be919758b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213646"
---
# <span data-ttu-id="ccedc-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="ccedc-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="ccedc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccedc-102">SYNOPSIS</span></span>
<span data-ttu-id="ccedc-103">새 공유 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ccedc-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="ccedc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ccedc-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> -SourceShareLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccedc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ccedc-105">DESCRIPTION</span></span>
<span data-ttu-id="ccedc-106">**AzDataShareSubscription** cmdlet은 지정 된 데이터 공유 계정 및 초대 id에서 공유 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ccedc-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="ccedc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ccedc-107">EXAMPLES</span></span>

### <span data-ttu-id="ccedc-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ccedc-108">Example 1</span></span>
```
PS C:\> New-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription" -InvitationId "167e06ff-567f-4bc7-be0c-645a6de710f3"
CreatedAt               : 6/30/2019 12:42:12 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 167e06ff-567f-4bc7-be0c-645a6de710f3
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Company
ShareDescription        : Test description  
ShareTerms              : Test terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="ccedc-109">이 명령은 data 공유 계정 WikiAds에서 invitaionId에 대 한 새 공유 구독 AdsShareSubscription를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ccedc-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="ccedc-110">변수</span><span class="sxs-lookup"><span data-stu-id="ccedc-110">PARAMETERS</span></span>

### <span data-ttu-id="ccedc-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ccedc-111">-AccountName</span></span>
<span data-ttu-id="ccedc-112">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="ccedc-112">Azure data share account name</span></span>

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

### <span data-ttu-id="ccedc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccedc-113">-DefaultProfile</span></span>
<span data-ttu-id="ccedc-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ccedc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccedc-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="ccedc-115">-InvitationId</span></span>
<span data-ttu-id="ccedc-116">Azure data share invitationId</span><span class="sxs-lookup"><span data-stu-id="ccedc-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="ccedc-117">-이름</span><span class="sxs-lookup"><span data-stu-id="ccedc-117">-Name</span></span>
<span data-ttu-id="ccedc-118">Azure data share 구독 이름</span><span class="sxs-lookup"><span data-stu-id="ccedc-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="ccedc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccedc-119">-ResourceGroupName</span></span>
<span data-ttu-id="ccedc-120">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ccedc-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="ccedc-121">-SourceShareLocation</span><span class="sxs-lookup"><span data-stu-id="ccedc-121">-SourceShareLocation</span></span>
<span data-ttu-id="ccedc-122">Azure data share 위치</span><span class="sxs-lookup"><span data-stu-id="ccedc-122">Azure data share location</span></span>

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

### <span data-ttu-id="ccedc-123">-확인</span><span class="sxs-lookup"><span data-stu-id="ccedc-123">-Confirm</span></span>
<span data-ttu-id="ccedc-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccedc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccedc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccedc-125">-WhatIf</span></span>
<span data-ttu-id="ccedc-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ccedc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccedc-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ccedc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccedc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccedc-128">CommonParameters</span></span>
<span data-ttu-id="ccedc-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccedc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccedc-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ccedc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccedc-131">입력</span><span class="sxs-lookup"><span data-stu-id="ccedc-131">INPUTS</span></span>

### <span data-ttu-id="ccedc-132">않아야</span><span class="sxs-lookup"><span data-stu-id="ccedc-132">None</span></span>

## <span data-ttu-id="ccedc-133">출력</span><span class="sxs-lookup"><span data-stu-id="ccedc-133">OUTPUTS</span></span>

### <span data-ttu-id="ccedc-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="ccedc-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="ccedc-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ccedc-135">NOTES</span></span>

## <span data-ttu-id="ccedc-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccedc-136">RELATED LINKS</span></span>
