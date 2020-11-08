---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: f3da23b4ae30860013dfd31d714177e09a9cbd89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226269"
---
# <span data-ttu-id="59ba0-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="59ba0-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="59ba0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="59ba0-103">리소스 종류의 Sku를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="59ba0-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="59ba0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59ba0-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="59ba0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="59ba0-105">DESCRIPTION</span></span>
<span data-ttu-id="59ba0-106">리소스 종류의 Sku를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="59ba0-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="59ba0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="59ba0-107">EXAMPLES</span></span>

### <span data-ttu-id="59ba0-108">예제 1: 구독에 대 한 SKU 목록</span><span class="sxs-lookup"><span data-stu-id="59ba0-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="59ba0-109">이 명령은 구독에 대 한 SKU 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="59ba0-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="59ba0-110">변수</span><span class="sxs-lookup"><span data-stu-id="59ba0-110">PARAMETERS</span></span>

### <span data-ttu-id="59ba0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59ba0-111">-DefaultProfile</span></span>
<span data-ttu-id="59ba0-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59ba0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59ba0-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59ba0-113">-SubscriptionId</span></span>
<span data-ttu-id="59ba0-114">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59ba0-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="59ba0-115">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="59ba0-115">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="59ba0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59ba0-116">CommonParameters</span></span>
<span data-ttu-id="59ba0-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59ba0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59ba0-118">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="59ba0-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59ba0-119">입력</span><span class="sxs-lookup"><span data-stu-id="59ba0-119">INPUTS</span></span>

## <span data-ttu-id="59ba0-120">출력</span><span class="sxs-lookup"><span data-stu-id="59ba0-120">OUTPUTS</span></span>

### <span data-ttu-id="59ba0-121">Api20180601Preview. IResourceTypeSku에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="59ba0-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="59ba0-122">상속자</span><span class="sxs-lookup"><span data-stu-id="59ba0-122">NOTES</span></span>

<span data-ttu-id="59ba0-123">별칭과</span><span class="sxs-lookup"><span data-stu-id="59ba0-123">ALIASES</span></span>

## <span data-ttu-id="59ba0-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59ba0-124">RELATED LINKS</span></span>

