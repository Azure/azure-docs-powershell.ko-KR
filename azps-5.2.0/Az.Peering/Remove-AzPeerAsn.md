---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: b47db38e49bdc066fed9637e65d87693738a4776
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360949"
---
# <span data-ttu-id="5cab1-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="5cab1-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="5cab1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cab1-102">SYNOPSIS</span></span>
<span data-ttu-id="5cab1-103">피어 Asn 제거</span><span class="sxs-lookup"><span data-stu-id="5cab1-103">Remove Peer Asn</span></span>

## <span data-ttu-id="5cab1-104">구문</span><span class="sxs-lookup"><span data-stu-id="5cab1-104">SYNTAX</span></span>

### <span data-ttu-id="5cab1-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="5cab1-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cab1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5cab1-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cab1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5cab1-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cab1-108">설명</span><span class="sxs-lookup"><span data-stu-id="5cab1-108">DESCRIPTION</span></span>
<span data-ttu-id="5cab1-109">구독에서 PeerAsn을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5cab1-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="5cab1-110">예제</span><span class="sxs-lookup"><span data-stu-id="5cab1-110">EXAMPLES</span></span>

### <span data-ttu-id="5cab1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5cab1-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="5cab1-112">피어 Asn을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5cab1-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="5cab1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cab1-113">PARAMETERS</span></span>

### <span data-ttu-id="5cab1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5cab1-114">-AsJob</span></span>
<span data-ttu-id="5cab1-115">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5cab1-115">Run in the background.</span></span>

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

### <span data-ttu-id="5cab1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cab1-116">-DefaultProfile</span></span>
<span data-ttu-id="5cab1-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5cab1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cab1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5cab1-118">-Force</span></span>
<span data-ttu-id="5cab1-119">{{ 채우기 힘 설명 }}</span><span class="sxs-lookup"><span data-stu-id="5cab1-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="5cab1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cab1-120">-InputObject</span></span>
<span data-ttu-id="5cab1-121">PeerAsn 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5cab1-121">The PeerAsn object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cab1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5cab1-122">-Name</span></span>
<span data-ttu-id="5cab1-123">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cab1-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cab1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cab1-124">-PassThru</span></span>
<span data-ttu-id="5cab1-125">완료된 경우 true 반환</span><span class="sxs-lookup"><span data-stu-id="5cab1-125">Return true if complete</span></span>

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

### <span data-ttu-id="5cab1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cab1-126">-ResourceId</span></span>
<span data-ttu-id="5cab1-127">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cab1-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cab1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cab1-128">-Confirm</span></span>
<span data-ttu-id="5cab1-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5cab1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cab1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cab1-130">-WhatIf</span></span>
<span data-ttu-id="5cab1-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5cab1-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5cab1-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5cab1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cab1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cab1-133">CommonParameters</span></span>
<span data-ttu-id="5cab1-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5cab1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cab1-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5cab1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cab1-136">입력</span><span class="sxs-lookup"><span data-stu-id="5cab1-136">INPUTS</span></span>

### <span data-ttu-id="5cab1-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="5cab1-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="5cab1-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5cab1-138">System.String</span></span>

## <span data-ttu-id="5cab1-139">출력</span><span class="sxs-lookup"><span data-stu-id="5cab1-139">OUTPUTS</span></span>

### <span data-ttu-id="5cab1-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5cab1-140">System.Boolean</span></span>

## <span data-ttu-id="5cab1-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5cab1-141">NOTES</span></span>

## <span data-ttu-id="5cab1-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5cab1-142">RELATED LINKS</span></span>
