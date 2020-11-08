---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 646d07646ff7530dc805d4c516a1cf981aafe915
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047901"
---
# <span data-ttu-id="6cbce-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="6cbce-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="6cbce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cbce-102">SYNOPSIS</span></span>
<span data-ttu-id="6cbce-103">Blockchain 구성원에 대 한 API 키를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cbce-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="6cbce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6cbce-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6cbce-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6cbce-105">DESCRIPTION</span></span>
<span data-ttu-id="6cbce-106">Blockchain 구성원에 대 한 API 키를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cbce-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="6cbce-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6cbce-107">EXAMPLES</span></span>

### <span data-ttu-id="6cbce-108">예제 1: List blockchain Api 키</span><span class="sxs-lookup"><span data-stu-id="6cbce-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="6cbce-109">이 명령은 blockchain 구성원에 대 한 Api 키를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cbce-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="6cbce-110">변수</span><span class="sxs-lookup"><span data-stu-id="6cbce-110">PARAMETERS</span></span>

### <span data-ttu-id="6cbce-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="6cbce-111">-BlockchainMemberName</span></span>
<span data-ttu-id="6cbce-112">Blockchain 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6cbce-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="6cbce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cbce-113">-DefaultProfile</span></span>
<span data-ttu-id="6cbce-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6cbce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cbce-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cbce-115">-ResourceGroupName</span></span>
<span data-ttu-id="6cbce-116">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6cbce-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6cbce-117">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6cbce-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6cbce-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cbce-118">-SubscriptionId</span></span>
<span data-ttu-id="6cbce-119">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6cbce-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6cbce-120">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="6cbce-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6cbce-121">-확인</span><span class="sxs-lookup"><span data-stu-id="6cbce-121">-Confirm</span></span>
<span data-ttu-id="6cbce-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cbce-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cbce-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cbce-123">-WhatIf</span></span>
<span data-ttu-id="6cbce-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6cbce-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cbce-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6cbce-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cbce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cbce-126">CommonParameters</span></span>
<span data-ttu-id="6cbce-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6cbce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cbce-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6cbce-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cbce-129">입력</span><span class="sxs-lookup"><span data-stu-id="6cbce-129">INPUTS</span></span>

## <span data-ttu-id="6cbce-130">출력</span><span class="sxs-lookup"><span data-stu-id="6cbce-130">OUTPUTS</span></span>

### <span data-ttu-id="6cbce-131">Api20180601Preview. i a PowerShell. i a i. IApiKey</span><span class="sxs-lookup"><span data-stu-id="6cbce-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="6cbce-132">상속자</span><span class="sxs-lookup"><span data-stu-id="6cbce-132">NOTES</span></span>

<span data-ttu-id="6cbce-133">별칭과</span><span class="sxs-lookup"><span data-stu-id="6cbce-133">ALIASES</span></span>

## <span data-ttu-id="6cbce-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6cbce-134">RELATED LINKS</span></span>

