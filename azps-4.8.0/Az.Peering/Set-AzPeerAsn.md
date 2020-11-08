---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: ec7003b90d9489f2966d4fd1ebe3e3fb3fa74ce5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214027"
---
# <span data-ttu-id="ee03b-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="ee03b-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="ee03b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee03b-102">SYNOPSIS</span></span>
<span data-ttu-id="ee03b-103">연락처 정보 업데이트</span><span class="sxs-lookup"><span data-stu-id="ee03b-103">Update Contact Information</span></span>

## <span data-ttu-id="ee03b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee03b-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee03b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ee03b-105">DESCRIPTION</span></span>
<span data-ttu-id="ee03b-106">구독에서 PeerAsn에 대 한 연락처 정보를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee03b-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="ee03b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ee03b-107">EXAMPLES</span></span>

### <span data-ttu-id="ee03b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ee03b-108">Example 1</span></span>
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

<span data-ttu-id="ee03b-109">피어 Asn에 전자 메일 주소를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee03b-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="ee03b-110">변수</span><span class="sxs-lookup"><span data-stu-id="ee03b-110">PARAMETERS</span></span>

### <span data-ttu-id="ee03b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee03b-111">-AsJob</span></span>
<span data-ttu-id="ee03b-112">백그라운드에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee03b-112">Run in the background.</span></span>

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

### <span data-ttu-id="ee03b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee03b-113">-DefaultProfile</span></span>
<span data-ttu-id="ee03b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee03b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee03b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee03b-115">-InputObject</span></span>
<span data-ttu-id="ee03b-116">{{Fill InputObject 설명}}</span><span class="sxs-lookup"><span data-stu-id="ee03b-116">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee03b-117">-확인</span><span class="sxs-lookup"><span data-stu-id="ee03b-117">-Confirm</span></span>
<span data-ttu-id="ee03b-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee03b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee03b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee03b-119">-WhatIf</span></span>
<span data-ttu-id="ee03b-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ee03b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee03b-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee03b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee03b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee03b-122">CommonParameters</span></span>
<span data-ttu-id="ee03b-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee03b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee03b-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ee03b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee03b-125">입력</span><span class="sxs-lookup"><span data-stu-id="ee03b-125">INPUTS</span></span>

### <span data-ttu-id="ee03b-126">PSPeerAsn (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ee03b-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="ee03b-127">출력</span><span class="sxs-lookup"><span data-stu-id="ee03b-127">OUTPUTS</span></span>

### <span data-ttu-id="ee03b-128">PSPeerAsn (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ee03b-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="ee03b-129">상속자</span><span class="sxs-lookup"><span data-stu-id="ee03b-129">NOTES</span></span>

## <span data-ttu-id="ee03b-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee03b-130">RELATED LINKS</span></span>
