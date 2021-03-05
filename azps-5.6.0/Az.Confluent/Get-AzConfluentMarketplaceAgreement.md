---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/get-azconfluentmarketplaceagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentMarketplaceAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentMarketplaceAgreement.md
ms.openlocfilehash: 72b60933ee2771278f1e225e4a022def55c3c03a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012603"
---
# <span data-ttu-id="c53ff-101">Get-AzConfluentMarketplaceAgreement</span><span class="sxs-lookup"><span data-stu-id="c53ff-101">Get-AzConfluentMarketplaceAgreement</span></span>

## <span data-ttu-id="c53ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c53ff-102">SYNOPSIS</span></span>
<span data-ttu-id="c53ff-103">구독에 Confluent Marketplace 계약을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c53ff-103">List Confluent marketplace agreements in the subscription.</span></span>

## <span data-ttu-id="c53ff-104">구문</span><span class="sxs-lookup"><span data-stu-id="c53ff-104">SYNTAX</span></span>

```
Get-AzConfluentMarketplaceAgreement [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c53ff-105">설명</span><span class="sxs-lookup"><span data-stu-id="c53ff-105">DESCRIPTION</span></span>
<span data-ttu-id="c53ff-106">구독에 Confluent Marketplace 계약을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c53ff-106">List Confluent marketplace agreements in the subscription.</span></span>

## <span data-ttu-id="c53ff-107">예제</span><span class="sxs-lookup"><span data-stu-id="c53ff-107">EXAMPLES</span></span>

### <span data-ttu-id="c53ff-108">예제 1: 구독 아래에 모든 confluent Marketplace 계약 나열</span><span class="sxs-lookup"><span data-stu-id="c53ff-108">Example 1: List all confluent marketplace agreement under a subscription</span></span>
```powershell
PS C:\> Get-AzConfluentMarketplaceAgreement

Name        Type
----        ----
marketplace Microsoft.Confluent/agreements
confluent   Microsoft.Confluent/offertypes
```

<span data-ttu-id="c53ff-109">이 명령은 구독 아래에 있는 모든 confluent Marketplace 계약을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c53ff-109">This command lists all confluent marketplace agreement under a subscription.</span></span>

## <span data-ttu-id="c53ff-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c53ff-110">PARAMETERS</span></span>

### <span data-ttu-id="c53ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c53ff-111">-DefaultProfile</span></span>
<span data-ttu-id="c53ff-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c53ff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c53ff-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c53ff-113">-SubscriptionId</span></span>
<span data-ttu-id="c53ff-114">Microsoft Azure 구독 ID</span><span class="sxs-lookup"><span data-stu-id="c53ff-114">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c53ff-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c53ff-115">CommonParameters</span></span>
<span data-ttu-id="c53ff-116">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c53ff-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c53ff-117">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c53ff-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c53ff-118">입력</span><span class="sxs-lookup"><span data-stu-id="c53ff-118">INPUTS</span></span>

## <span data-ttu-id="c53ff-119">출력</span><span class="sxs-lookup"><span data-stu-id="c53ff-119">OUTPUTS</span></span>

### <span data-ttu-id="c53ff-120">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span><span class="sxs-lookup"><span data-stu-id="c53ff-120">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span></span>

## <span data-ttu-id="c53ff-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c53ff-121">NOTES</span></span>

<span data-ttu-id="c53ff-122">별칭</span><span class="sxs-lookup"><span data-stu-id="c53ff-122">ALIASES</span></span>

## <span data-ttu-id="c53ff-123">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c53ff-123">RELATED LINKS</span></span>

