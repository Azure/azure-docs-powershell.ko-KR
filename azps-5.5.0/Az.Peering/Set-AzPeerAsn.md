---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeerAsn.md
ms.openlocfilehash: ec7003b90d9489f2966d4fd1ebe3e3fb3fa74ce5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191452"
---
# <span data-ttu-id="ac29f-101">Set-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="ac29f-101">Set-AzPeerAsn</span></span>

## <span data-ttu-id="ac29f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac29f-102">SYNOPSIS</span></span>
<span data-ttu-id="ac29f-103">연락처 정보 업데이트</span><span class="sxs-lookup"><span data-stu-id="ac29f-103">Update Contact Information</span></span>

## <span data-ttu-id="ac29f-104">구문</span><span class="sxs-lookup"><span data-stu-id="ac29f-104">SYNTAX</span></span>

```
Set-AzPeerAsn [-InputObject] <PSPeerAsn> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac29f-105">설명</span><span class="sxs-lookup"><span data-stu-id="ac29f-105">DESCRIPTION</span></span>
<span data-ttu-id="ac29f-106">구독에서 PeerAsn에 대한 연락처 정보를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac29f-106">Allows you to update contact information for a PeerAsn on the subscription.</span></span>

## <span data-ttu-id="ac29f-107">예제</span><span class="sxs-lookup"><span data-stu-id="ac29f-107">EXAMPLES</span></span>

### <span data-ttu-id="ac29f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ac29f-108">Example 1</span></span>
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

<span data-ttu-id="ac29f-109">피어 Asn에 전자 메일 주소 추가</span><span class="sxs-lookup"><span data-stu-id="ac29f-109">Adds an email address to the Peer Asn</span></span>

## <span data-ttu-id="ac29f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac29f-110">PARAMETERS</span></span>

### <span data-ttu-id="ac29f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac29f-111">-AsJob</span></span>
<span data-ttu-id="ac29f-112">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ac29f-112">Run in the background.</span></span>

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

### <span data-ttu-id="ac29f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac29f-113">-DefaultProfile</span></span>
<span data-ttu-id="ac29f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac29f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac29f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac29f-115">-InputObject</span></span>
<span data-ttu-id="ac29f-116">{{ InputObject 설명 입력 }}</span><span class="sxs-lookup"><span data-stu-id="ac29f-116">{{ Fill InputObject Description }}</span></span>

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

### <span data-ttu-id="ac29f-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac29f-117">-Confirm</span></span>
<span data-ttu-id="ac29f-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac29f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac29f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac29f-119">-WhatIf</span></span>
<span data-ttu-id="ac29f-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ac29f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac29f-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac29f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac29f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac29f-122">CommonParameters</span></span>
<span data-ttu-id="ac29f-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ac29f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac29f-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ac29f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac29f-125">입력</span><span class="sxs-lookup"><span data-stu-id="ac29f-125">INPUTS</span></span>

### <span data-ttu-id="ac29f-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="ac29f-126">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="ac29f-127">출력</span><span class="sxs-lookup"><span data-stu-id="ac29f-127">OUTPUTS</span></span>

### <span data-ttu-id="ac29f-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="ac29f-128">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="ac29f-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ac29f-129">NOTES</span></span>

## <span data-ttu-id="ac29f-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac29f-130">RELATED LINKS</span></span>
