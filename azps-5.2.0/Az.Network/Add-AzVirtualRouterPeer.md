---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 2cb7bc759847af456286bfc611904922a26dc443
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359647"
---
# <span data-ttu-id="185a5-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="185a5-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="185a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="185a5-102">SYNOPSIS</span></span>
<span data-ttu-id="185a5-103">Azure VirtualRouter에 피어 추가</span><span class="sxs-lookup"><span data-stu-id="185a5-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="185a5-104">구문</span><span class="sxs-lookup"><span data-stu-id="185a5-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="185a5-105">설명</span><span class="sxs-lookup"><span data-stu-id="185a5-105">DESCRIPTION</span></span>
<span data-ttu-id="185a5-106">**Add-AzVirtualRouterPeer** cmdlet은 VirtualRouter 피어를 Azure VirtualRouter에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="185a5-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="185a5-107">예제</span><span class="sxs-lookup"><span data-stu-id="185a5-107">EXAMPLES</span></span>

### <span data-ttu-id="185a5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="185a5-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="185a5-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="185a5-109">PARAMETERS</span></span>

### <span data-ttu-id="185a5-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="185a5-110">-AsJob</span></span>
<span data-ttu-id="185a5-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="185a5-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="185a5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="185a5-112">-DefaultProfile</span></span>
<span data-ttu-id="185a5-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="185a5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="185a5-114">-Force</span><span class="sxs-lookup"><span data-stu-id="185a5-114">-Force</span></span>
<span data-ttu-id="185a5-115">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="185a5-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="185a5-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="185a5-116">-PeerAsn</span></span>
<span data-ttu-id="185a5-117">피어 ASN.</span><span class="sxs-lookup"><span data-stu-id="185a5-117">Peer ASN.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="185a5-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="185a5-118">-PeerIp</span></span>
<span data-ttu-id="185a5-119">피어 IP.</span><span class="sxs-lookup"><span data-stu-id="185a5-119">Peer Ip.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="185a5-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="185a5-120">-PeerName</span></span>
<span data-ttu-id="185a5-121">가상 라우터 피어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="185a5-121">The name of the virtual router Peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="185a5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="185a5-122">-ResourceGroupName</span></span>
<span data-ttu-id="185a5-123">가상 라우터/피어의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="185a5-123">The resource group name of the virtual router/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="185a5-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="185a5-124">-VirtualRouterName</span></span>
<span data-ttu-id="185a5-125">피어가 있는 가상 라우터입니다.</span><span class="sxs-lookup"><span data-stu-id="185a5-125">The virtual router where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="185a5-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="185a5-126">-Confirm</span></span>
<span data-ttu-id="185a5-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="185a5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="185a5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="185a5-128">-WhatIf</span></span>
<span data-ttu-id="185a5-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="185a5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="185a5-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="185a5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="185a5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="185a5-131">CommonParameters</span></span>
<span data-ttu-id="185a5-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="185a5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="185a5-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="185a5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="185a5-134">입력</span><span class="sxs-lookup"><span data-stu-id="185a5-134">INPUTS</span></span>

### <span data-ttu-id="185a5-135">System.String</span><span class="sxs-lookup"><span data-stu-id="185a5-135">System.String</span></span>

### <span data-ttu-id="185a5-136">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="185a5-136">System.UInt32</span></span>

## <span data-ttu-id="185a5-137">출력</span><span class="sxs-lookup"><span data-stu-id="185a5-137">OUTPUTS</span></span>

### <span data-ttu-id="185a5-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="185a5-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="185a5-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="185a5-139">NOTES</span></span>

## <span data-ttu-id="185a5-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="185a5-140">RELATED LINKS</span></span>
