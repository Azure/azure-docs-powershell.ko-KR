---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: dbde273c1694f4622904ac00b261e902036c6e03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971456"
---
# <span data-ttu-id="67d16-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="67d16-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="67d16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67d16-102">SYNOPSIS</span></span>
<span data-ttu-id="67d16-103">트랜잭션 노드에 대한 API 키를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="67d16-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="67d16-104">구문</span><span class="sxs-lookup"><span data-stu-id="67d16-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="67d16-105">설명</span><span class="sxs-lookup"><span data-stu-id="67d16-105">DESCRIPTION</span></span>
<span data-ttu-id="67d16-106">트랜잭션 노드에 대한 API 키를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="67d16-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="67d16-107">예제</span><span class="sxs-lookup"><span data-stu-id="67d16-107">EXAMPLES</span></span>

### <span data-ttu-id="67d16-108">예제 1: 트랜잭션 노드에 대한 Api 키 나열</span><span class="sxs-lookup"><span data-stu-id="67d16-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="67d16-109">이 명령은 트랜잭션 노드에 대한 Api 키를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="67d16-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="67d16-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="67d16-110">PARAMETERS</span></span>

### <span data-ttu-id="67d16-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="67d16-111">-BlockchainMemberName</span></span>
<span data-ttu-id="67d16-112">블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67d16-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="67d16-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d16-113">-DefaultProfile</span></span>
<span data-ttu-id="67d16-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67d16-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67d16-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67d16-115">-ResourceGroupName</span></span>
<span data-ttu-id="67d16-116">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67d16-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="67d16-117">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="67d16-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="67d16-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67d16-118">-SubscriptionId</span></span>
<span data-ttu-id="67d16-119">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67d16-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="67d16-120">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="67d16-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="67d16-121">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="67d16-121">-TransactionNodeName</span></span>
<span data-ttu-id="67d16-122">트랜잭션 노드 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67d16-122">Transaction node name.</span></span>

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

### <span data-ttu-id="67d16-123">-확인</span><span class="sxs-lookup"><span data-stu-id="67d16-123">-Confirm</span></span>
<span data-ttu-id="67d16-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="67d16-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67d16-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67d16-125">-WhatIf</span></span>
<span data-ttu-id="67d16-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="67d16-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67d16-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67d16-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67d16-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d16-128">CommonParameters</span></span>
<span data-ttu-id="67d16-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="67d16-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d16-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67d16-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d16-131">입력</span><span class="sxs-lookup"><span data-stu-id="67d16-131">INPUTS</span></span>

## <span data-ttu-id="67d16-132">출력</span><span class="sxs-lookup"><span data-stu-id="67d16-132">OUTPUTS</span></span>

### <span data-ttu-id="67d16-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="67d16-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="67d16-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="67d16-134">NOTES</span></span>

<span data-ttu-id="67d16-135">별칭</span><span class="sxs-lookup"><span data-stu-id="67d16-135">ALIASES</span></span>

## <span data-ttu-id="67d16-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67d16-136">RELATED LINKS</span></span>

