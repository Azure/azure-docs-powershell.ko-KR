---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: f4dc342d72ce092a1f3cbd1695613fce2220661d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048485"
---
# <span data-ttu-id="2ceca-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="2ceca-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="2ceca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ceca-102">SYNOPSIS</span></span>
<span data-ttu-id="2ceca-103">Blockchain 구성원에 대 한 컨소시엄 회원을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ceca-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="2ceca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2ceca-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2ceca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2ceca-105">DESCRIPTION</span></span>
<span data-ttu-id="2ceca-106">Blockchain 구성원에 대 한 컨소시엄 회원을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ceca-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="2ceca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2ceca-107">EXAMPLES</span></span>

### <span data-ttu-id="2ceca-108">예제 1: blockchain 구성원에 대 한 컨소시엄 구성원을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ceca-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="2ceca-109">이 명령은 blockchain 구성원에 대 한 컨소시엄 구성원을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ceca-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="2ceca-110">변수</span><span class="sxs-lookup"><span data-stu-id="2ceca-110">PARAMETERS</span></span>

### <span data-ttu-id="2ceca-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="2ceca-111">-BlockchainMemberName</span></span>
<span data-ttu-id="2ceca-112">Blockchain 구성원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ceca-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="2ceca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ceca-113">-DefaultProfile</span></span>
<span data-ttu-id="2ceca-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ceca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ceca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ceca-115">-ResourceGroupName</span></span>
<span data-ttu-id="2ceca-116">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ceca-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2ceca-117">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ceca-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2ceca-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ceca-118">-SubscriptionId</span></span>
<span data-ttu-id="2ceca-119">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2ceca-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2ceca-120">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="2ceca-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2ceca-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ceca-121">CommonParameters</span></span>
<span data-ttu-id="2ceca-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ceca-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ceca-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2ceca-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ceca-124">입력</span><span class="sxs-lookup"><span data-stu-id="2ceca-124">INPUTS</span></span>

## <span data-ttu-id="2ceca-125">출력</span><span class="sxs-lookup"><span data-stu-id="2ceca-125">OUTPUTS</span></span>

### <span data-ttu-id="2ceca-126">Api20180601Preview. t t t. IConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="2ceca-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="2ceca-127">상속자</span><span class="sxs-lookup"><span data-stu-id="2ceca-127">NOTES</span></span>

<span data-ttu-id="2ceca-128">별칭과</span><span class="sxs-lookup"><span data-stu-id="2ceca-128">ALIASES</span></span>

## <span data-ttu-id="2ceca-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ceca-129">RELATED LINKS</span></span>

