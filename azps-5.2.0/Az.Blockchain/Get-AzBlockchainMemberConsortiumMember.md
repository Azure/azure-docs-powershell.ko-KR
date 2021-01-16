---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: f4dc342d72ce092a1f3cbd1695613fce2220661d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341913"
---
# <span data-ttu-id="c5d28-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="c5d28-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="c5d28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5d28-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d28-103">블록체인 멤버에 대한 컨소시엄 멤버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c5d28-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="c5d28-104">구문</span><span class="sxs-lookup"><span data-stu-id="c5d28-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c5d28-105">설명</span><span class="sxs-lookup"><span data-stu-id="c5d28-105">DESCRIPTION</span></span>
<span data-ttu-id="c5d28-106">블록체인 멤버에 대한 컨소시엄 멤버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c5d28-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="c5d28-107">예제</span><span class="sxs-lookup"><span data-stu-id="c5d28-107">EXAMPLES</span></span>

### <span data-ttu-id="c5d28-108">예제 1: 블록체인 멤버에 대한 컨소시엄 멤버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c5d28-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="c5d28-109">이 명령은 블록체인 멤버에 대한 컨소시엄 멤버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c5d28-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="c5d28-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5d28-110">PARAMETERS</span></span>

### <span data-ttu-id="c5d28-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="c5d28-111">-BlockchainMemberName</span></span>
<span data-ttu-id="c5d28-112">블록체인 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5d28-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="c5d28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5d28-113">-DefaultProfile</span></span>
<span data-ttu-id="c5d28-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5d28-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5d28-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5d28-115">-ResourceGroupName</span></span>
<span data-ttu-id="c5d28-116">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5d28-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c5d28-117">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5d28-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c5d28-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c5d28-118">-SubscriptionId</span></span>
<span data-ttu-id="c5d28-119">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5d28-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c5d28-120">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="c5d28-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c5d28-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d28-121">CommonParameters</span></span>
<span data-ttu-id="c5d28-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c5d28-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d28-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c5d28-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d28-124">입력</span><span class="sxs-lookup"><span data-stu-id="c5d28-124">INPUTS</span></span>

## <span data-ttu-id="c5d28-125">출력</span><span class="sxs-lookup"><span data-stu-id="c5d28-125">OUTPUTS</span></span>

### <span data-ttu-id="c5d28-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="c5d28-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="c5d28-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c5d28-127">NOTES</span></span>

<span data-ttu-id="c5d28-128">별칭</span><span class="sxs-lookup"><span data-stu-id="c5d28-128">ALIASES</span></span>

## <span data-ttu-id="c5d28-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5d28-129">RELATED LINKS</span></span>

