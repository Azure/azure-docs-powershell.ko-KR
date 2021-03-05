---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: b94a7158830530be9df31531101c9c9c5be90df1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991704"
---
# <span data-ttu-id="7904a-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="7904a-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="7904a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7904a-102">SYNOPSIS</span></span>
<span data-ttu-id="7904a-103">블록체인 멤버에 대한 API 키를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7904a-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="7904a-104">구문</span><span class="sxs-lookup"><span data-stu-id="7904a-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7904a-105">설명</span><span class="sxs-lookup"><span data-stu-id="7904a-105">DESCRIPTION</span></span>
<span data-ttu-id="7904a-106">블록체인 멤버에 대한 API 키를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7904a-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="7904a-107">예제</span><span class="sxs-lookup"><span data-stu-id="7904a-107">EXAMPLES</span></span>

### <span data-ttu-id="7904a-108">예제 1: blockchain Api 키 나열</span><span class="sxs-lookup"><span data-stu-id="7904a-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="7904a-109">이 명령은 블록체인 멤버에 대한 Api 키를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7904a-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="7904a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7904a-110">PARAMETERS</span></span>

### <span data-ttu-id="7904a-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="7904a-111">-BlockchainMemberName</span></span>
<span data-ttu-id="7904a-112">블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7904a-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="7904a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7904a-113">-DefaultProfile</span></span>
<span data-ttu-id="7904a-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7904a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7904a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7904a-115">-ResourceGroupName</span></span>
<span data-ttu-id="7904a-116">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7904a-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7904a-117">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7904a-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7904a-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7904a-118">-SubscriptionId</span></span>
<span data-ttu-id="7904a-119">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7904a-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7904a-120">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="7904a-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7904a-121">-확인</span><span class="sxs-lookup"><span data-stu-id="7904a-121">-Confirm</span></span>
<span data-ttu-id="7904a-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7904a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7904a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7904a-123">-WhatIf</span></span>
<span data-ttu-id="7904a-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7904a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7904a-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7904a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7904a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7904a-126">CommonParameters</span></span>
<span data-ttu-id="7904a-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7904a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7904a-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7904a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7904a-129">입력</span><span class="sxs-lookup"><span data-stu-id="7904a-129">INPUTS</span></span>

## <span data-ttu-id="7904a-130">출력</span><span class="sxs-lookup"><span data-stu-id="7904a-130">OUTPUTS</span></span>

### <span data-ttu-id="7904a-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="7904a-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="7904a-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7904a-132">NOTES</span></span>

<span data-ttu-id="7904a-133">별칭</span><span class="sxs-lookup"><span data-stu-id="7904a-133">ALIASES</span></span>

## <span data-ttu-id="7904a-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7904a-134">RELATED LINKS</span></span>

