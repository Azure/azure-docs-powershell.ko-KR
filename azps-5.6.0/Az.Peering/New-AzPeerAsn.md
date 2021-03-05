---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: 11f3a729c6818a7794a8b42a4b21a658530cc60d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989459"
---
# <span data-ttu-id="cf8bd-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="cf8bd-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="cf8bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf8bd-102">SYNOPSIS</span></span>
<span data-ttu-id="cf8bd-103">새 피어 ASN을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf8bd-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="cf8bd-104">구문</span><span class="sxs-lookup"><span data-stu-id="cf8bd-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf8bd-105">설명</span><span class="sxs-lookup"><span data-stu-id="cf8bd-105">DESCRIPTION</span></span>
<span data-ttu-id="cf8bd-106">구독에 대한 새 PeerAsn 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf8bd-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="cf8bd-107">예제</span><span class="sxs-lookup"><span data-stu-id="cf8bd-107">EXAMPLES</span></span>

### <span data-ttu-id="cf8bd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cf8bd-108">Example 1</span></span>
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

<span data-ttu-id="cf8bd-109">새 PeerAsn을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf8bd-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="cf8bd-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cf8bd-110">PARAMETERS</span></span>

### <span data-ttu-id="cf8bd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf8bd-111">-AsJob</span></span>
<span data-ttu-id="cf8bd-112">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="cf8bd-112">Run in the background.</span></span>

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

### <span data-ttu-id="cf8bd-113">-ContactDetail</span><span class="sxs-lookup"><span data-stu-id="cf8bd-113">-ContactDetail</span></span>
<span data-ttu-id="cf8bd-114">일반적으로 네트워크 작업 센터에서 문제가 해결되는 경우 연락하는 데 사용되는 전자 메일 주소</span><span class="sxs-lookup"><span data-stu-id="cf8bd-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="cf8bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf8bd-115">-DefaultProfile</span></span>
<span data-ttu-id="cf8bd-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf8bd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf8bd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cf8bd-117">-Name</span></span>
<span data-ttu-id="cf8bd-118">PSPeering의 고유한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf8bd-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="cf8bd-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="cf8bd-119">-PeerAsn</span></span>
<span data-ttu-id="cf8bd-120">피어 Asn 리소스 ID. Get-AzPeerAsn ID를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="cf8bd-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="cf8bd-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="cf8bd-121">-PeerName</span></span>
<span data-ttu-id="cf8bd-122">PSPeering의 고유한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf8bd-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="cf8bd-123">-확인</span><span class="sxs-lookup"><span data-stu-id="cf8bd-123">-Confirm</span></span>
<span data-ttu-id="cf8bd-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf8bd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf8bd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf8bd-125">-WhatIf</span></span>
<span data-ttu-id="cf8bd-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cf8bd-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf8bd-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf8bd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf8bd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf8bd-128">CommonParameters</span></span>
<span data-ttu-id="cf8bd-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cf8bd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf8bd-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cf8bd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf8bd-131">입력</span><span class="sxs-lookup"><span data-stu-id="cf8bd-131">INPUTS</span></span>

### <span data-ttu-id="cf8bd-132">없음</span><span class="sxs-lookup"><span data-stu-id="cf8bd-132">None</span></span>

## <span data-ttu-id="cf8bd-133">출력</span><span class="sxs-lookup"><span data-stu-id="cf8bd-133">OUTPUTS</span></span>

### <span data-ttu-id="cf8bd-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="cf8bd-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="cf8bd-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cf8bd-135">NOTES</span></span>

## <span data-ttu-id="cf8bd-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf8bd-136">RELATED LINKS</span></span>
