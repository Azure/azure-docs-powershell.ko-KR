---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: f3da23b4ae30860013dfd31d714177e09a9cbd89
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341901"
---
# <span data-ttu-id="015ac-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="015ac-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="015ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="015ac-102">SYNOPSIS</span></span>
<span data-ttu-id="015ac-103">리소스 유형의 SKU를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="015ac-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="015ac-104">구문</span><span class="sxs-lookup"><span data-stu-id="015ac-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="015ac-105">설명</span><span class="sxs-lookup"><span data-stu-id="015ac-105">DESCRIPTION</span></span>
<span data-ttu-id="015ac-106">리소스 유형의 SKU를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="015ac-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="015ac-107">예제</span><span class="sxs-lookup"><span data-stu-id="015ac-107">EXAMPLES</span></span>

### <span data-ttu-id="015ac-108">예제 1: 구독에 대한 SKU 나열</span><span class="sxs-lookup"><span data-stu-id="015ac-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="015ac-109">이 명령은 구독에 대한 SKU를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="015ac-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="015ac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="015ac-110">PARAMETERS</span></span>

### <span data-ttu-id="015ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="015ac-111">-DefaultProfile</span></span>
<span data-ttu-id="015ac-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="015ac-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="015ac-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="015ac-113">-SubscriptionId</span></span>
<span data-ttu-id="015ac-114">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="015ac-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="015ac-115">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="015ac-115">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="015ac-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="015ac-116">CommonParameters</span></span>
<span data-ttu-id="015ac-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="015ac-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="015ac-118">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="015ac-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="015ac-119">입력</span><span class="sxs-lookup"><span data-stu-id="015ac-119">INPUTS</span></span>

## <span data-ttu-id="015ac-120">출력</span><span class="sxs-lookup"><span data-stu-id="015ac-120">OUTPUTS</span></span>

### <span data-ttu-id="015ac-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="015ac-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="015ac-122">참고 사항</span><span class="sxs-lookup"><span data-stu-id="015ac-122">NOTES</span></span>

<span data-ttu-id="015ac-123">별칭</span><span class="sxs-lookup"><span data-stu-id="015ac-123">ALIASES</span></span>

## <span data-ttu-id="015ac-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="015ac-124">RELATED LINKS</span></span>

