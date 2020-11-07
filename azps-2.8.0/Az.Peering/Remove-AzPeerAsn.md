---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: 82a112363a561e7566b0d748d00acc75dc026ebb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872358"
---
# <span data-ttu-id="e2964-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="e2964-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="e2964-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2964-102">SYNOPSIS</span></span>
<span data-ttu-id="e2964-103">피어 Asn 제거</span><span class="sxs-lookup"><span data-stu-id="e2964-103">Remove Peer Asn</span></span>

## <span data-ttu-id="e2964-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2964-104">SYNTAX</span></span>

### <span data-ttu-id="e2964-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e2964-105">Default (Default)</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2964-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e2964-106">ByName</span></span>
```
Remove-AzPeerAsn [-Name] <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2964-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e2964-107">DESCRIPTION</span></span>
<span data-ttu-id="e2964-108">구독에서 PeerAsn을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2964-108">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="e2964-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e2964-109">EXAMPLES</span></span>

### <span data-ttu-id="e2964-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e2964-110">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="e2964-111">피어 Asn을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2964-111">Removes the Peer Asn</span></span>

## <span data-ttu-id="e2964-112">변수</span><span class="sxs-lookup"><span data-stu-id="e2964-112">PARAMETERS</span></span>

### <span data-ttu-id="e2964-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2964-113">-AsJob</span></span>
<span data-ttu-id="e2964-114">백그라운드에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2964-114">Run in the background.</span></span>

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

### <span data-ttu-id="e2964-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2964-115">-DefaultProfile</span></span>
<span data-ttu-id="e2964-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2964-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2964-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e2964-117">-Force</span></span>
<span data-ttu-id="e2964-118">{{Force 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="e2964-118">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="e2964-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2964-119">-InputObject</span></span>
<span data-ttu-id="e2964-120">PeerAsn 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e2964-120">The PeerAsn object.</span></span>

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

### <span data-ttu-id="e2964-121">-이름</span><span class="sxs-lookup"><span data-stu-id="e2964-121">-Name</span></span>
<span data-ttu-id="e2964-122">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2964-122">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e2964-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2964-123">-PassThru</span></span>
<span data-ttu-id="e2964-124">완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2964-124">Return true if complete</span></span>

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

### <span data-ttu-id="e2964-125">-확인</span><span class="sxs-lookup"><span data-stu-id="e2964-125">-Confirm</span></span>
<span data-ttu-id="e2964-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2964-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2964-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2964-127">-WhatIf</span></span>
<span data-ttu-id="e2964-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2964-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2964-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2964-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2964-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2964-130">CommonParameters</span></span>
<span data-ttu-id="e2964-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2964-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2964-132">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e2964-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2964-133">입력</span><span class="sxs-lookup"><span data-stu-id="e2964-133">INPUTS</span></span>

### <span data-ttu-id="e2964-134">PSPeerAsn (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e2964-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

## <span data-ttu-id="e2964-135">출력</span><span class="sxs-lookup"><span data-stu-id="e2964-135">OUTPUTS</span></span>

### <span data-ttu-id="e2964-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e2964-136">System.Boolean</span></span>

## <span data-ttu-id="e2964-137">상속자</span><span class="sxs-lookup"><span data-stu-id="e2964-137">NOTES</span></span>

## <span data-ttu-id="e2964-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2964-138">RELATED LINKS</span></span>
