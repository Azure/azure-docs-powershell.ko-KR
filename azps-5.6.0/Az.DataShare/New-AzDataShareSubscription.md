---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: a7b3a60d97692d01eb8be374ab9670af4b331f95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996711"
---
# <span data-ttu-id="80c20-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="80c20-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="80c20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80c20-102">SYNOPSIS</span></span>
<span data-ttu-id="80c20-103">새 공유 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80c20-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="80c20-104">구문</span><span class="sxs-lookup"><span data-stu-id="80c20-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> -SourceShareLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80c20-105">설명</span><span class="sxs-lookup"><span data-stu-id="80c20-105">DESCRIPTION</span></span>
<span data-ttu-id="80c20-106">**New-AzDataShareSubscription** cmdlet은 지정된 데이터 공유 계정 및 초대 ID에서 공유 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80c20-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="80c20-107">예제</span><span class="sxs-lookup"><span data-stu-id="80c20-107">EXAMPLES</span></span>

### <span data-ttu-id="80c20-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="80c20-108">Example 1</span></span>
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

<span data-ttu-id="80c20-109">이 명령은 데이터 공유 계정 WikiAds에서 invitaionId에 대한 새 공유 구독 AdsShareSubscription을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80c20-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="80c20-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="80c20-110">PARAMETERS</span></span>

### <span data-ttu-id="80c20-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="80c20-111">-AccountName</span></span>
<span data-ttu-id="80c20-112">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="80c20-112">Azure data share account name</span></span>

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

### <span data-ttu-id="80c20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c20-113">-DefaultProfile</span></span>
<span data-ttu-id="80c20-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80c20-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80c20-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="80c20-115">-InvitationId</span></span>
<span data-ttu-id="80c20-116">Azure 데이터 공유 invitationId</span><span class="sxs-lookup"><span data-stu-id="80c20-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="80c20-117">-Name</span><span class="sxs-lookup"><span data-stu-id="80c20-117">-Name</span></span>
<span data-ttu-id="80c20-118">Azure 데이터 공유 구독 이름</span><span class="sxs-lookup"><span data-stu-id="80c20-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="80c20-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80c20-119">-ResourceGroupName</span></span>
<span data-ttu-id="80c20-120">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="80c20-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="80c20-121">-SourceShareLocation</span><span class="sxs-lookup"><span data-stu-id="80c20-121">-SourceShareLocation</span></span>
<span data-ttu-id="80c20-122">Azure 데이터 공유 위치</span><span class="sxs-lookup"><span data-stu-id="80c20-122">Azure data share location</span></span>

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

### <span data-ttu-id="80c20-123">-확인</span><span class="sxs-lookup"><span data-stu-id="80c20-123">-Confirm</span></span>
<span data-ttu-id="80c20-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="80c20-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80c20-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80c20-125">-WhatIf</span></span>
<span data-ttu-id="80c20-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="80c20-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80c20-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80c20-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80c20-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c20-128">CommonParameters</span></span>
<span data-ttu-id="80c20-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="80c20-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c20-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80c20-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c20-131">입력</span><span class="sxs-lookup"><span data-stu-id="80c20-131">INPUTS</span></span>

### <span data-ttu-id="80c20-132">없음</span><span class="sxs-lookup"><span data-stu-id="80c20-132">None</span></span>

## <span data-ttu-id="80c20-133">출력</span><span class="sxs-lookup"><span data-stu-id="80c20-133">OUTPUTS</span></span>

### <span data-ttu-id="80c20-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="80c20-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="80c20-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="80c20-135">NOTES</span></span>

## <span data-ttu-id="80c20-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80c20-136">RELATED LINKS</span></span>
