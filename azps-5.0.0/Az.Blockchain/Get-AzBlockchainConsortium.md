---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226279"
---
# <span data-ttu-id="08b09-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="08b09-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="08b09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08b09-102">SYNOPSIS</span></span>
<span data-ttu-id="08b09-103">구독에 사용할 수 있는 consorums 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="08b09-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="08b09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="08b09-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="08b09-105">설명은</span><span class="sxs-lookup"><span data-stu-id="08b09-105">DESCRIPTION</span></span>
<span data-ttu-id="08b09-106">구독에 사용할 수 있는 consorums 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="08b09-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="08b09-107">예제의</span><span class="sxs-lookup"><span data-stu-id="08b09-107">EXAMPLES</span></span>

### <span data-ttu-id="08b09-108">예제 1: Blockchain consortiums를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08b09-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="08b09-109">이 명령은 특정 위치에 대 한 구독 아래에 있는 consortiums를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="08b09-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="08b09-110">변수</span><span class="sxs-lookup"><span data-stu-id="08b09-110">PARAMETERS</span></span>

### <span data-ttu-id="08b09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08b09-111">-DefaultProfile</span></span>
<span data-ttu-id="08b09-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="08b09-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08b09-113">-위치</span><span class="sxs-lookup"><span data-stu-id="08b09-113">-Location</span></span>
<span data-ttu-id="08b09-114">위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08b09-114">Location Name.</span></span>

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

### <span data-ttu-id="08b09-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="08b09-115">-SubscriptionId</span></span>
<span data-ttu-id="08b09-116">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08b09-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="08b09-117">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="08b09-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="08b09-118">-확인</span><span class="sxs-lookup"><span data-stu-id="08b09-118">-Confirm</span></span>
<span data-ttu-id="08b09-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="08b09-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08b09-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08b09-120">-WhatIf</span></span>
<span data-ttu-id="08b09-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="08b09-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08b09-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08b09-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08b09-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08b09-123">CommonParameters</span></span>
<span data-ttu-id="08b09-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="08b09-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08b09-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="08b09-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08b09-126">입력</span><span class="sxs-lookup"><span data-stu-id="08b09-126">INPUTS</span></span>

## <span data-ttu-id="08b09-127">출력</span><span class="sxs-lookup"><span data-stu-id="08b09-127">OUTPUTS</span></span>

### <span data-ttu-id="08b09-128">Api20180601Preview. IConsortium에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="08b09-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="08b09-129">상속자</span><span class="sxs-lookup"><span data-stu-id="08b09-129">NOTES</span></span>

<span data-ttu-id="08b09-130">별칭과</span><span class="sxs-lookup"><span data-stu-id="08b09-130">ALIASES</span></span>

## <span data-ttu-id="08b09-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08b09-131">RELATED LINKS</span></span>

