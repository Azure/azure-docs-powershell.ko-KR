---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: 077b1f18e18fbf47d8c89d02c44722c0a1561dac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954891"
---
# <span data-ttu-id="07295-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="07295-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="07295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07295-102">SYNOPSIS</span></span>
<span data-ttu-id="07295-103">구독에 사용할 수 있는 컨소시엄을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="07295-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="07295-104">구문</span><span class="sxs-lookup"><span data-stu-id="07295-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="07295-105">설명</span><span class="sxs-lookup"><span data-stu-id="07295-105">DESCRIPTION</span></span>
<span data-ttu-id="07295-106">구독에 사용할 수 있는 컨소시엄을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="07295-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="07295-107">예제</span><span class="sxs-lookup"><span data-stu-id="07295-107">EXAMPLES</span></span>

### <span data-ttu-id="07295-108">예제 1: 블록체인 컨소시엄을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="07295-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="07295-109">이 명령은 특정 위치에 대한 구독 아래에 컨소시엄을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="07295-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="07295-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="07295-110">PARAMETERS</span></span>

### <span data-ttu-id="07295-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07295-111">-DefaultProfile</span></span>
<span data-ttu-id="07295-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07295-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07295-113">-Location</span><span class="sxs-lookup"><span data-stu-id="07295-113">-Location</span></span>
<span data-ttu-id="07295-114">위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07295-114">Location Name.</span></span>

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

### <span data-ttu-id="07295-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="07295-115">-SubscriptionId</span></span>
<span data-ttu-id="07295-116">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="07295-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="07295-117">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="07295-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="07295-118">-확인</span><span class="sxs-lookup"><span data-stu-id="07295-118">-Confirm</span></span>
<span data-ttu-id="07295-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="07295-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07295-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07295-120">-WhatIf</span></span>
<span data-ttu-id="07295-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="07295-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07295-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07295-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07295-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07295-123">CommonParameters</span></span>
<span data-ttu-id="07295-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="07295-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07295-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07295-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07295-126">입력</span><span class="sxs-lookup"><span data-stu-id="07295-126">INPUTS</span></span>

## <span data-ttu-id="07295-127">출력</span><span class="sxs-lookup"><span data-stu-id="07295-127">OUTPUTS</span></span>

### <span data-ttu-id="07295-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span><span class="sxs-lookup"><span data-stu-id="07295-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="07295-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="07295-129">NOTES</span></span>

<span data-ttu-id="07295-130">별칭</span><span class="sxs-lookup"><span data-stu-id="07295-130">ALIASES</span></span>

## <span data-ttu-id="07295-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07295-131">RELATED LINKS</span></span>

