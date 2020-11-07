---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: 5ce29456e79755758989f208802e2850642fdcd7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872366"
---
# <span data-ttu-id="9e09e-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="9e09e-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="9e09e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e09e-102">SYNOPSIS</span></span>
<span data-ttu-id="9e09e-103">새 피어 ASN을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e09e-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="9e09e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e09e-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -Email <String[]> -Phone <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e09e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9e09e-105">DESCRIPTION</span></span>
<span data-ttu-id="9e09e-106">구독에 대 한 새 PeerAsn 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e09e-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="9e09e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9e09e-107">EXAMPLES</span></span>

### <span data-ttu-id="9e09e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9e09e-108">Example 1</span></span>
```powershell
PS C:> New-AzPeerAsn -Name Contoso65050 -PeerName Contoso -PeerAsn 65050 -Emails noc@contoso.com -Phone "888-888-8889"

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="9e09e-109">새 PeerAsn을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9e09e-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="9e09e-110">변수</span><span class="sxs-lookup"><span data-stu-id="9e09e-110">PARAMETERS</span></span>

### <span data-ttu-id="9e09e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e09e-111">-AsJob</span></span>
<span data-ttu-id="9e09e-112">백그라운드에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e09e-112">Run in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e09e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e09e-113">-DefaultProfile</span></span>
<span data-ttu-id="9e09e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e09e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e09e-115">-전자 메일</span><span class="sxs-lookup"><span data-stu-id="9e09e-115">-Email</span></span>
<span data-ttu-id="9e09e-116">메일 주소</span><span class="sxs-lookup"><span data-stu-id="9e09e-116">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e09e-117">-이름</span><span class="sxs-lookup"><span data-stu-id="9e09e-117">-Name</span></span>
<span data-ttu-id="9e09e-118">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e09e-118">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e09e-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="9e09e-119">-PeerAsn</span></span>
<span data-ttu-id="9e09e-120">피어 Asn 리소스 Id입니다. Get-AzPeerAsn를 사용 하 여 Id를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e09e-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e09e-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="9e09e-121">-PeerName</span></span>
<span data-ttu-id="9e09e-122">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9e09e-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e09e-123">-전화</span><span class="sxs-lookup"><span data-stu-id="9e09e-123">-Phone</span></span>
<span data-ttu-id="9e09e-124">전화</span><span class="sxs-lookup"><span data-stu-id="9e09e-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e09e-125">-확인</span><span class="sxs-lookup"><span data-stu-id="9e09e-125">-Confirm</span></span>
<span data-ttu-id="9e09e-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e09e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e09e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e09e-127">-WhatIf</span></span>
<span data-ttu-id="9e09e-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9e09e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e09e-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e09e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e09e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e09e-130">CommonParameters</span></span>
<span data-ttu-id="9e09e-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e09e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e09e-132">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9e09e-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e09e-133">입력</span><span class="sxs-lookup"><span data-stu-id="9e09e-133">INPUTS</span></span>

### <span data-ttu-id="9e09e-134">않아야</span><span class="sxs-lookup"><span data-stu-id="9e09e-134">None</span></span>

## <span data-ttu-id="9e09e-135">출력</span><span class="sxs-lookup"><span data-stu-id="9e09e-135">OUTPUTS</span></span>

### <span data-ttu-id="9e09e-136">PSPeerAsn (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9e09e-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="9e09e-137">상속자</span><span class="sxs-lookup"><span data-stu-id="9e09e-137">NOTES</span></span>

## <span data-ttu-id="9e09e-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e09e-138">RELATED LINKS</span></span>
