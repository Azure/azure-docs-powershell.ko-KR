---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: b47db38e49bdc066fed9637e65d87693738a4776
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216367"
---
# <span data-ttu-id="04992-101">Remove-AzPeerAsn</span><span class="sxs-lookup"><span data-stu-id="04992-101">Remove-AzPeerAsn</span></span>

## <span data-ttu-id="04992-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04992-102">SYNOPSIS</span></span>
<span data-ttu-id="04992-103">피어 Asn 제거</span><span class="sxs-lookup"><span data-stu-id="04992-103">Remove Peer Asn</span></span>

## <span data-ttu-id="04992-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04992-104">SYNTAX</span></span>

### <span data-ttu-id="04992-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="04992-105">ByName (Default)</span></span>
```
Remove-AzPeerAsn -Name <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04992-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="04992-106">InputObject</span></span>
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04992-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="04992-107">ByResourceId</span></span>
```
Remove-AzPeerAsn -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04992-108">설명은</span><span class="sxs-lookup"><span data-stu-id="04992-108">DESCRIPTION</span></span>
<span data-ttu-id="04992-109">구독에서 PeerAsn을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="04992-109">Remove a PeerAsn from the subscription.</span></span>

## <span data-ttu-id="04992-110">예제의</span><span class="sxs-lookup"><span data-stu-id="04992-110">EXAMPLES</span></span>

### <span data-ttu-id="04992-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="04992-111">Example 1</span></span>
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

<span data-ttu-id="04992-112">피어 Asn을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="04992-112">Removes the Peer Asn</span></span>

## <span data-ttu-id="04992-113">변수</span><span class="sxs-lookup"><span data-stu-id="04992-113">PARAMETERS</span></span>

### <span data-ttu-id="04992-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04992-114">-AsJob</span></span>
<span data-ttu-id="04992-115">백그라운드에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="04992-115">Run in the background.</span></span>

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

### <span data-ttu-id="04992-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04992-116">-DefaultProfile</span></span>
<span data-ttu-id="04992-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04992-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04992-118">-Force</span><span class="sxs-lookup"><span data-stu-id="04992-118">-Force</span></span>
<span data-ttu-id="04992-119">{{Force 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="04992-119">{{ Fill Force Description }}</span></span>

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

### <span data-ttu-id="04992-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04992-120">-InputObject</span></span>
<span data-ttu-id="04992-121">PeerAsn 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="04992-121">The PeerAsn object.</span></span>

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

### <span data-ttu-id="04992-122">-이름</span><span class="sxs-lookup"><span data-stu-id="04992-122">-Name</span></span>
<span data-ttu-id="04992-123">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04992-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="04992-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04992-124">-PassThru</span></span>
<span data-ttu-id="04992-125">완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="04992-125">Return true if complete</span></span>

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

### <span data-ttu-id="04992-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04992-126">-ResourceId</span></span>
<span data-ttu-id="04992-127">리소스 id 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04992-127">The resource id string name.</span></span>

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

### <span data-ttu-id="04992-128">-확인</span><span class="sxs-lookup"><span data-stu-id="04992-128">-Confirm</span></span>
<span data-ttu-id="04992-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="04992-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04992-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04992-130">-WhatIf</span></span>
<span data-ttu-id="04992-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="04992-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04992-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04992-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04992-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04992-133">CommonParameters</span></span>
<span data-ttu-id="04992-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04992-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04992-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="04992-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04992-136">입력</span><span class="sxs-lookup"><span data-stu-id="04992-136">INPUTS</span></span>

### <span data-ttu-id="04992-137">PSPeerAsn (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="04992-137">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn</span></span>

### <span data-ttu-id="04992-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="04992-138">System.String</span></span>

## <span data-ttu-id="04992-139">출력</span><span class="sxs-lookup"><span data-stu-id="04992-139">OUTPUTS</span></span>

### <span data-ttu-id="04992-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="04992-140">System.Boolean</span></span>

## <span data-ttu-id="04992-141">상속자</span><span class="sxs-lookup"><span data-stu-id="04992-141">NOTES</span></span>

## <span data-ttu-id="04992-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04992-142">RELATED LINKS</span></span>
