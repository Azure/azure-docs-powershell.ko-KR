---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: cf27cf7f82e44ec52978b3d04af973ba47cd1632
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336093"
---
# <span data-ttu-id="90c18-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="90c18-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="90c18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90c18-102">SYNOPSIS</span></span>
<span data-ttu-id="90c18-103">새 피어 ASN을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90c18-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="90c18-104">구문</span><span class="sxs-lookup"><span data-stu-id="90c18-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90c18-105">설명</span><span class="sxs-lookup"><span data-stu-id="90c18-105">DESCRIPTION</span></span>
<span data-ttu-id="90c18-106">구독에 대한 새 PeerAsn 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90c18-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="90c18-107">예제</span><span class="sxs-lookup"><span data-stu-id="90c18-107">EXAMPLES</span></span>

### <span data-ttu-id="90c18-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="90c18-108">Example 1</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact

PeerContactInfo : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail
PeerName        : Contoso
ValidationState : None
PeerAsnProperty : 65050
Name            : Contoso65050
Id              : /subscriptions//providers/Microsoft.Peering/peerAsns/Contoso65050
Type            : Microsoft.Peering/peerAsns
```

<span data-ttu-id="90c18-109">새 PeerAsn을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90c18-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="90c18-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90c18-110">PARAMETERS</span></span>

### <span data-ttu-id="90c18-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90c18-111">-AsJob</span></span>
<span data-ttu-id="90c18-112">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="90c18-112">Run in the background.</span></span>

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

### <span data-ttu-id="90c18-113">-ContactDetail</span><span class="sxs-lookup"><span data-stu-id="90c18-113">-ContactDetail</span></span>
<span data-ttu-id="90c18-114">일반적으로 네트워크 운영 센터에서 문제가 해결되는 경우 연락하는 데 사용되는 전자 메일 주소</span><span class="sxs-lookup"><span data-stu-id="90c18-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c18-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c18-115">-DefaultProfile</span></span>
<span data-ttu-id="90c18-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90c18-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90c18-117">-Name</span><span class="sxs-lookup"><span data-stu-id="90c18-117">-Name</span></span>
<span data-ttu-id="90c18-118">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90c18-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="90c18-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="90c18-119">-PeerAsn</span></span>
<span data-ttu-id="90c18-120">피어 Asn 리소스 ID입니다. Get-AzPeerAsn 사용하여 ID를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="90c18-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="90c18-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="90c18-121">-PeerName</span></span>
<span data-ttu-id="90c18-122">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90c18-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="90c18-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90c18-123">-Confirm</span></span>
<span data-ttu-id="90c18-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="90c18-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90c18-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90c18-125">-WhatIf</span></span>
<span data-ttu-id="90c18-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="90c18-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90c18-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90c18-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90c18-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c18-128">CommonParameters</span></span>
<span data-ttu-id="90c18-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90c18-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c18-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="90c18-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c18-131">입력</span><span class="sxs-lookup"><span data-stu-id="90c18-131">INPUTS</span></span>

### <span data-ttu-id="90c18-132">없음</span><span class="sxs-lookup"><span data-stu-id="90c18-132">None</span></span>

## <span data-ttu-id="90c18-133">출력</span><span class="sxs-lookup"><span data-stu-id="90c18-133">OUTPUTS</span></span>

### <span data-ttu-id="90c18-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="90c18-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="90c18-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90c18-135">NOTES</span></span>

## <span data-ttu-id="90c18-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90c18-136">RELATED LINKS</span></span>
