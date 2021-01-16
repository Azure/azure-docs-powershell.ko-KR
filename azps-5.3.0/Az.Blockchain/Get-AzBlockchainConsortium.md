---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494032"
---
# <span data-ttu-id="1daca-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="1daca-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="1daca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1daca-102">SYNOPSIS</span></span>
<span data-ttu-id="1daca-103">구독에 사용 가능한 컨소시엄을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1daca-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="1daca-104">구문</span><span class="sxs-lookup"><span data-stu-id="1daca-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1daca-105">설명</span><span class="sxs-lookup"><span data-stu-id="1daca-105">DESCRIPTION</span></span>
<span data-ttu-id="1daca-106">구독에 사용 가능한 컨소시엄을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1daca-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="1daca-107">예제</span><span class="sxs-lookup"><span data-stu-id="1daca-107">EXAMPLES</span></span>

### <span data-ttu-id="1daca-108">예제 1: 블록체인 컨소시엄을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1daca-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="1daca-109">이 명령은 특정 위치에 대한 구독의 컨소시엄을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1daca-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="1daca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1daca-110">PARAMETERS</span></span>

### <span data-ttu-id="1daca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1daca-111">-DefaultProfile</span></span>
<span data-ttu-id="1daca-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1daca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1daca-113">-Location</span><span class="sxs-lookup"><span data-stu-id="1daca-113">-Location</span></span>
<span data-ttu-id="1daca-114">위치 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1daca-114">Location Name.</span></span>

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

### <span data-ttu-id="1daca-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1daca-115">-SubscriptionId</span></span>
<span data-ttu-id="1daca-116">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1daca-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1daca-117">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="1daca-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1daca-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1daca-118">-Confirm</span></span>
<span data-ttu-id="1daca-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1daca-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1daca-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1daca-120">-WhatIf</span></span>
<span data-ttu-id="1daca-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1daca-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1daca-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1daca-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1daca-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1daca-123">CommonParameters</span></span>
<span data-ttu-id="1daca-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1daca-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1daca-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1daca-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1daca-126">입력</span><span class="sxs-lookup"><span data-stu-id="1daca-126">INPUTS</span></span>

## <span data-ttu-id="1daca-127">출력</span><span class="sxs-lookup"><span data-stu-id="1daca-127">OUTPUTS</span></span>

### <span data-ttu-id="1daca-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span><span class="sxs-lookup"><span data-stu-id="1daca-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="1daca-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1daca-129">NOTES</span></span>

<span data-ttu-id="1daca-130">별칭</span><span class="sxs-lookup"><span data-stu-id="1daca-130">ALIASES</span></span>

## <span data-ttu-id="1daca-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1daca-131">RELATED LINKS</span></span>

