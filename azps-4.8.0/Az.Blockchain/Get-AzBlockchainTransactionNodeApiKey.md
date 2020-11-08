---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 401073a8d97affaec866486b19113373c001ae58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056766"
---
# <span data-ttu-id="f688e-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="f688e-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="f688e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f688e-102">SYNOPSIS</span></span>
<span data-ttu-id="f688e-103">트랜잭션 노드에 대 한 API 키를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f688e-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="f688e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f688e-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f688e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f688e-105">DESCRIPTION</span></span>
<span data-ttu-id="f688e-106">트랜잭션 노드에 대 한 API 키를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f688e-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="f688e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f688e-107">EXAMPLES</span></span>

### <span data-ttu-id="f688e-108">예제 1: 트랜잭션 노드에 대 한 Api 키 목록</span><span class="sxs-lookup"><span data-stu-id="f688e-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="f688e-109">이 명령은 트랜잭션 노드에 대 한 Api 키를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f688e-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="f688e-110">변수</span><span class="sxs-lookup"><span data-stu-id="f688e-110">PARAMETERS</span></span>

### <span data-ttu-id="f688e-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="f688e-111">-BlockchainMemberName</span></span>
<span data-ttu-id="f688e-112">Blockchain 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f688e-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="f688e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f688e-113">-DefaultProfile</span></span>
<span data-ttu-id="f688e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f688e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f688e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f688e-115">-ResourceGroupName</span></span>
<span data-ttu-id="f688e-116">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f688e-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f688e-117">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f688e-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f688e-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f688e-118">-SubscriptionId</span></span>
<span data-ttu-id="f688e-119">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f688e-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f688e-120">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="f688e-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f688e-121">TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="f688e-121">-TransactionNodeName</span></span>
<span data-ttu-id="f688e-122">트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f688e-122">Transaction node name.</span></span>

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

### <span data-ttu-id="f688e-123">-확인</span><span class="sxs-lookup"><span data-stu-id="f688e-123">-Confirm</span></span>
<span data-ttu-id="f688e-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f688e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f688e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f688e-125">-WhatIf</span></span>
<span data-ttu-id="f688e-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f688e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f688e-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f688e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f688e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f688e-128">CommonParameters</span></span>
<span data-ttu-id="f688e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f688e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f688e-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f688e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f688e-131">입력</span><span class="sxs-lookup"><span data-stu-id="f688e-131">INPUTS</span></span>

## <span data-ttu-id="f688e-132">출력</span><span class="sxs-lookup"><span data-stu-id="f688e-132">OUTPUTS</span></span>

### <span data-ttu-id="f688e-133">Api20180601Preview. i a PowerShell. i a i. IApiKey</span><span class="sxs-lookup"><span data-stu-id="f688e-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="f688e-134">상속자</span><span class="sxs-lookup"><span data-stu-id="f688e-134">NOTES</span></span>

<span data-ttu-id="f688e-135">별칭과</span><span class="sxs-lookup"><span data-stu-id="f688e-135">ALIASES</span></span>

## <span data-ttu-id="f688e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f688e-136">RELATED LINKS</span></span>

