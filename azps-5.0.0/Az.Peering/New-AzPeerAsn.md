---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsn.md
ms.openlocfilehash: cf27cf7f82e44ec52978b3d04af973ba47cd1632
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217227"
---
# <span data-ttu-id="c1873-101">New-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="c1873-101">New-AzPeerAsn</span></span>

## <span data-ttu-id="c1873-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1873-102">SYNOPSIS</span></span>
<span data-ttu-id="c1873-103">새 피어 ASN을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-103">Creates a new Peer ASN</span></span> 

## <span data-ttu-id="c1873-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c1873-104">SYNTAX</span></span>

```
New-AzPeerAsn [-Name] <String> [-PeerName] <String> [-PeerAsn] <Int32> -ContactDetail <PSContactDetail[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1873-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c1873-105">DESCRIPTION</span></span>
<span data-ttu-id="c1873-106">구독에 대 한 새 PeerAsn 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-106">Creates a new PeerAsn object for the subscription.</span></span>

## <span data-ttu-id="c1873-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c1873-107">EXAMPLES</span></span>

### <span data-ttu-id="c1873-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c1873-108">Example 1</span></span>
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

<span data-ttu-id="c1873-109">새 PeerAsn을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-109">Creates a new PeerAsn</span></span>

## <span data-ttu-id="c1873-110">변수</span><span class="sxs-lookup"><span data-stu-id="c1873-110">PARAMETERS</span></span>

### <span data-ttu-id="c1873-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1873-111">-AsJob</span></span>
<span data-ttu-id="c1873-112">백그라운드에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-112">Run in the background.</span></span>

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

### <span data-ttu-id="c1873-113">-연락처 정보</span><span class="sxs-lookup"><span data-stu-id="c1873-113">-ContactDetail</span></span>
<span data-ttu-id="c1873-114">일반적으로 네트워크 작업 센터에 문제가 arrise 때 연락 하는 데 사용 되는 전자 메일 주소</span><span class="sxs-lookup"><span data-stu-id="c1873-114">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="c1873-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1873-115">-DefaultProfile</span></span>
<span data-ttu-id="c1873-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1873-117">-이름</span><span class="sxs-lookup"><span data-stu-id="c1873-117">-Name</span></span>
<span data-ttu-id="c1873-118">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-118">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="c1873-119">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="c1873-119">-PeerAsn</span></span>
<span data-ttu-id="c1873-120">피어 Asn 리소스 Id입니다. Get-AzPeerAsn를 사용 하 여 Id를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-120">The Peer Asn Resource Id. Use Get-AzPeerAsn to retrieve the Id.</span></span>

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

### <span data-ttu-id="c1873-121">-PeerName</span><span class="sxs-lookup"><span data-stu-id="c1873-121">-PeerName</span></span>
<span data-ttu-id="c1873-122">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="c1873-123">-확인</span><span class="sxs-lookup"><span data-stu-id="c1873-123">-Confirm</span></span>
<span data-ttu-id="c1873-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1873-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1873-125">-WhatIf</span></span>
<span data-ttu-id="c1873-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1873-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1873-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1873-128">CommonParameters</span></span>
<span data-ttu-id="c1873-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1873-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1873-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c1873-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1873-131">입력</span><span class="sxs-lookup"><span data-stu-id="c1873-131">INPUTS</span></span>

### <span data-ttu-id="c1873-132">않아야</span><span class="sxs-lookup"><span data-stu-id="c1873-132">None</span></span>

## <span data-ttu-id="c1873-133">출력</span><span class="sxs-lookup"><span data-stu-id="c1873-133">OUTPUTS</span></span>

### <span data-ttu-id="c1873-134">PSPeerAsn (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c1873-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="c1873-135">상속자</span><span class="sxs-lookup"><span data-stu-id="c1873-135">NOTES</span></span>

## <span data-ttu-id="c1873-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1873-136">RELATED LINKS</span></span>
