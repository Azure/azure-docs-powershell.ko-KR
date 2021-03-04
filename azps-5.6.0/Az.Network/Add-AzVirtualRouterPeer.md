---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 87647d504d47bf3f53b775d68b42ab617485f73d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979723"
---
# <span data-ttu-id="02e5e-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="02e5e-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="02e5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="02e5e-103">Azure VirtualRouter에 피어 추가</span><span class="sxs-lookup"><span data-stu-id="02e5e-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="02e5e-104">구문</span><span class="sxs-lookup"><span data-stu-id="02e5e-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02e5e-105">설명</span><span class="sxs-lookup"><span data-stu-id="02e5e-105">DESCRIPTION</span></span>
<span data-ttu-id="02e5e-106">**Add-AzVirtualRouterPeer** cmdlet은 Azure VirtualRouter에 VirtualRouter 피어를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="02e5e-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="02e5e-107">예제</span><span class="sxs-lookup"><span data-stu-id="02e5e-107">EXAMPLES</span></span>

### <span data-ttu-id="02e5e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="02e5e-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="02e5e-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="02e5e-109">PARAMETERS</span></span>

### <span data-ttu-id="02e5e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02e5e-110">-AsJob</span></span>
<span data-ttu-id="02e5e-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="02e5e-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02e5e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02e5e-112">-DefaultProfile</span></span>
<span data-ttu-id="02e5e-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02e5e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02e5e-114">-Force</span><span class="sxs-lookup"><span data-stu-id="02e5e-114">-Force</span></span>
<span data-ttu-id="02e5e-115">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02e5e-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="02e5e-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="02e5e-116">-PeerAsn</span></span>
<span data-ttu-id="02e5e-117">피어 ASN.</span><span class="sxs-lookup"><span data-stu-id="02e5e-117">Peer ASN.</span></span>

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

### <span data-ttu-id="02e5e-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="02e5e-118">-PeerIp</span></span>
<span data-ttu-id="02e5e-119">피어 IP입니다.</span><span class="sxs-lookup"><span data-stu-id="02e5e-119">Peer Ip.</span></span>

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

### <span data-ttu-id="02e5e-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="02e5e-120">-PeerName</span></span>
<span data-ttu-id="02e5e-121">가상 라우터 피어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02e5e-121">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="02e5e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02e5e-122">-ResourceGroupName</span></span>
<span data-ttu-id="02e5e-123">가상 라우터/피어의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02e5e-123">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="02e5e-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="02e5e-124">-VirtualRouterName</span></span>
<span data-ttu-id="02e5e-125">피어가 있는 가상 라우터입니다.</span><span class="sxs-lookup"><span data-stu-id="02e5e-125">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="02e5e-126">-확인</span><span class="sxs-lookup"><span data-stu-id="02e5e-126">-Confirm</span></span>
<span data-ttu-id="02e5e-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="02e5e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02e5e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02e5e-128">-WhatIf</span></span>
<span data-ttu-id="02e5e-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="02e5e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02e5e-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02e5e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02e5e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02e5e-131">CommonParameters</span></span>
<span data-ttu-id="02e5e-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="02e5e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02e5e-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02e5e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02e5e-134">입력</span><span class="sxs-lookup"><span data-stu-id="02e5e-134">INPUTS</span></span>

### <span data-ttu-id="02e5e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="02e5e-135">System.String</span></span>

### <span data-ttu-id="02e5e-136">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="02e5e-136">System.UInt32</span></span>

## <span data-ttu-id="02e5e-137">출력</span><span class="sxs-lookup"><span data-stu-id="02e5e-137">OUTPUTS</span></span>

### <span data-ttu-id="02e5e-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="02e5e-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="02e5e-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="02e5e-139">NOTES</span></span>

## <span data-ttu-id="02e5e-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02e5e-140">RELATED LINKS</span></span>
