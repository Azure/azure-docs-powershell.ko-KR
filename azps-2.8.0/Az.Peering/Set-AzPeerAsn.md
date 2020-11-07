---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: 81398d4ab62db1b8dca573dfd6beccde3be63700
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872350"
---
# <span data-ttu-id="03c3b-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="03c3b-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="03c3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="03c3b-103">연락처 정보 업데이트</span><span class="sxs-lookup"><span data-stu-id="03c3b-103">Update Contact Information</span></span>

## <span data-ttu-id="03c3b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03c3b-104">SYNTAX</span></span>

### <span data-ttu-id="03c3b-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="03c3b-105">ByName (Default)</span></span>
```
Set-AzPeerAsn [-Name] <String> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c3b-106">기본값</span><span class="sxs-lookup"><span data-stu-id="03c3b-106">Default</span></span>
```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-Email <String[]>] [-Phone <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03c3b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="03c3b-107">DESCRIPTION</span></span>
<span data-ttu-id="03c3b-108">구독에서 PeerAsn에 대 한 연락처 정보를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03c3b-108">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="03c3b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="03c3b-109">EXAMPLES</span></span>

### <span data-ttu-id="03c3b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="03c3b-110">Example 1</span></span>
```powershell
#Get the Peer ASN object
PS C:> Get-AzPeerAsn -PeerName Contoso | Set-AzPeerAsn -Email noc1@contoso.com

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactInfo
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="03c3b-111">피어 Asn에 전자 메일 주소를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="03c3b-111">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="03c3b-112">변수</span><span class="sxs-lookup"><span data-stu-id="03c3b-112">PARAMETERS</span></span>

### <span data-ttu-id="03c3b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03c3b-113">-AsJob</span></span>
<span data-ttu-id="03c3b-114">백그라운드에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="03c3b-114">Run in the background.</span></span>

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

### <span data-ttu-id="03c3b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c3b-115">-DefaultProfile</span></span>
<span data-ttu-id="03c3b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03c3b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03c3b-117">-전자 메일</span><span class="sxs-lookup"><span data-stu-id="03c3b-117">-Email</span></span>
<span data-ttu-id="03c3b-118">메일 주소</span><span class="sxs-lookup"><span data-stu-id="03c3b-118">Email</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c3b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03c3b-119">-InputObject</span></span>
<span data-ttu-id="03c3b-120">{{Fill InputObject 설명}}</span><span class="sxs-lookup"><span data-stu-id="03c3b-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03c3b-121">-이름</span><span class="sxs-lookup"><span data-stu-id="03c3b-121">-Name</span></span>
<span data-ttu-id="03c3b-122">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="03c3b-122">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c3b-123">-전화</span><span class="sxs-lookup"><span data-stu-id="03c3b-123">-Phone</span></span>
<span data-ttu-id="03c3b-124">전화</span><span class="sxs-lookup"><span data-stu-id="03c3b-124">Phone</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03c3b-125">-확인</span><span class="sxs-lookup"><span data-stu-id="03c3b-125">-Confirm</span></span>
<span data-ttu-id="03c3b-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="03c3b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03c3b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c3b-127">-WhatIf</span></span>
<span data-ttu-id="03c3b-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="03c3b-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03c3b-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03c3b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03c3b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c3b-130">CommonParameters</span></span>
<span data-ttu-id="03c3b-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03c3b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c3b-132">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="03c3b-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c3b-133">입력</span><span class="sxs-lookup"><span data-stu-id="03c3b-133">INPUTS</span></span>

### <span data-ttu-id="03c3b-134">PSPeerAsn (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="03c3b-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="03c3b-135">출력</span><span class="sxs-lookup"><span data-stu-id="03c3b-135">OUTPUTS</span></span>

### <span data-ttu-id="03c3b-136">PSPeerAsn (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="03c3b-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="03c3b-137">상속자</span><span class="sxs-lookup"><span data-stu-id="03c3b-137">NOTES</span></span>

## <span data-ttu-id="03c3b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03c3b-138">RELATED LINKS</span></span>
