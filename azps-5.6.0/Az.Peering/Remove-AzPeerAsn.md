---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: a5b50fd4d57fc7036196decdb7b967e2867b21f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989324"
---
# <span data-ttu-id="d8c2b-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="d8c2b-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="d8c2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c2b-103">피어 Asn 제거</span><span class="sxs-lookup"><span data-stu-id="d8c2b-103">Remove Peer Asn</span></span>

## <span data-ttu-id="d8c2b-104">구문</span><span class="sxs-lookup"><span data-stu-id="d8c2b-104">SYNTAX</span></span>

### <span data-ttu-id="d8c2b-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="d8c2b-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8c2b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d8c2b-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8c2b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d8c2b-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8c2b-108">설명</span><span class="sxs-lookup"><span data-stu-id="d8c2b-108">DESCRIPTION</span></span>
<span data-ttu-id="d8c2b-109">구독에서 PeerAsn을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c2b-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="d8c2b-110">예제</span><span class="sxs-lookup"><span data-stu-id="d8c2b-110">EXAMPLES</span></span>

### <span data-ttu-id="d8c2b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d8c2b-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="d8c2b-112">피어 Asn을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c2b-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="d8c2b-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d8c2b-113">PARAMETERS</span></span>

### <span data-ttu-id="d8c2b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8c2b-114">-AsJob</span></span>
<span data-ttu-id="d8c2b-115">백그라운드에서 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c2b-115">Run in the background.</span></span>

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

### <span data-ttu-id="d8c2b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c2b-116">-DefaultProfile</span></span>
<span data-ttu-id="d8c2b-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c2b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8c2b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d8c2b-118">-Force</span></span>
<span data-ttu-id="d8c2b-119">{{ 채우기 힘 설명 }}</span><span class="sxs-lookup"><span data-stu-id="d8c2b-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="d8c2b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8c2b-120">-InputObject</span></span>
<span data-ttu-id="d8c2b-121">PeerAsn 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c2b-121">The PeerAsn object.</span></span>

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

### <span data-ttu-id="d8c2b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d8c2b-122">-Name</span></span>
<span data-ttu-id="d8c2b-123">PSPeering의 고유한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c2b-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="d8c2b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8c2b-124">-PassThru</span></span>
<span data-ttu-id="d8c2b-125">완료된 경우 true 반환</span><span class="sxs-lookup"><span data-stu-id="d8c2b-125">Return true if complete</span></span>

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

### <span data-ttu-id="d8c2b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8c2b-126">-ResourceId</span></span>
<span data-ttu-id="d8c2b-127">리소스 ID 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8c2b-127">The resource id string name.</span></span>

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

### <span data-ttu-id="d8c2b-128">-확인</span><span class="sxs-lookup"><span data-stu-id="d8c2b-128">-Confirm</span></span>
<span data-ttu-id="d8c2b-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8c2b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8c2b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8c2b-130">-WhatIf</span></span>
<span data-ttu-id="d8c2b-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d8c2b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8c2b-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8c2b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8c2b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c2b-133">CommonParameters</span></span>
<span data-ttu-id="d8c2b-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d8c2b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c2b-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8c2b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c2b-136">입력</span><span class="sxs-lookup"><span data-stu-id="d8c2b-136">INPUTS</span></span>

### <span data-ttu-id="d8c2b-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span><span class="sxs-lookup"><span data-stu-id="d8c2b-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="d8c2b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d8c2b-138">System.String</span></span>

## <span data-ttu-id="d8c2b-139">출력</span><span class="sxs-lookup"><span data-stu-id="d8c2b-139">OUTPUTS</span></span>

### <span data-ttu-id="d8c2b-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8c2b-140">System.Boolean</span></span>

## <span data-ttu-id="d8c2b-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d8c2b-141">NOTES</span></span>

## <span data-ttu-id="d8c2b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8c2b-142">RELATED LINKS</span></span>
