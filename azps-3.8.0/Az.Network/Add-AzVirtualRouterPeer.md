---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: ce0d27bb091192db8f1cbc157daf1bb847f869d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042520"
---
# <span data-ttu-id="54fdd-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="54fdd-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="54fdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="54fdd-103">Azure VirtualRouter에 피어 추가</span><span class="sxs-lookup"><span data-stu-id="54fdd-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="54fdd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54fdd-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54fdd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="54fdd-105">DESCRIPTION</span></span>
<span data-ttu-id="54fdd-106">**Add-AzVirtualRouterPeer** Cmdlet은 Virtualrouter 피어를 Azure virtualrouter에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="54fdd-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>


## <span data-ttu-id="54fdd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="54fdd-107">EXAMPLES</span></span>

### <span data-ttu-id="54fdd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="54fdd-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="54fdd-109">변수</span><span class="sxs-lookup"><span data-stu-id="54fdd-109">PARAMETERS</span></span>

### <span data-ttu-id="54fdd-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54fdd-110">-AsJob</span></span>
<span data-ttu-id="54fdd-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="54fdd-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54fdd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54fdd-112">-DefaultProfile</span></span>
<span data-ttu-id="54fdd-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54fdd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54fdd-114">-Force</span><span class="sxs-lookup"><span data-stu-id="54fdd-114">-Force</span></span>
<span data-ttu-id="54fdd-115">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="54fdd-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54fdd-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="54fdd-116">-PeerAsn</span></span>
<span data-ttu-id="54fdd-117">피어 ASN.</span><span class="sxs-lookup"><span data-stu-id="54fdd-117">Peer ASN.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fdd-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="54fdd-118">-PeerIp</span></span>
<span data-ttu-id="54fdd-119">피어 Ip.</span><span class="sxs-lookup"><span data-stu-id="54fdd-119">Peer Ip.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fdd-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="54fdd-120">-PeerName</span></span>
<span data-ttu-id="54fdd-121">가상 라우터 피어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54fdd-121">The name of the virtual router Peer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fdd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54fdd-122">-ResourceGroupName</span></span>
<span data-ttu-id="54fdd-123">가상 라우터/피어의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="54fdd-123">The resource group name of the virtual router/peer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fdd-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="54fdd-124">-VirtualRouterName</span></span>
<span data-ttu-id="54fdd-125">피어가 있는 가상 라우터입니다.</span><span class="sxs-lookup"><span data-stu-id="54fdd-125">The virtual router where peer exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fdd-126">-확인</span><span class="sxs-lookup"><span data-stu-id="54fdd-126">-Confirm</span></span>
<span data-ttu-id="54fdd-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="54fdd-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54fdd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54fdd-128">-WhatIf</span></span>
<span data-ttu-id="54fdd-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="54fdd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54fdd-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54fdd-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54fdd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fdd-131">CommonParameters</span></span>
<span data-ttu-id="54fdd-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54fdd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fdd-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54fdd-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fdd-134">입력</span><span class="sxs-lookup"><span data-stu-id="54fdd-134">INPUTS</span></span>

### <span data-ttu-id="54fdd-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="54fdd-135">System.String</span></span>

### <span data-ttu-id="54fdd-136">시스템. UInt32</span><span class="sxs-lookup"><span data-stu-id="54fdd-136">System.UInt32</span></span>

## <span data-ttu-id="54fdd-137">출력</span><span class="sxs-lookup"><span data-stu-id="54fdd-137">OUTPUTS</span></span>

### <span data-ttu-id="54fdd-138">Microsoft. 네트워크 모델. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="54fdd-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="54fdd-139">상속자</span><span class="sxs-lookup"><span data-stu-id="54fdd-139">NOTES</span></span>

## <span data-ttu-id="54fdd-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54fdd-140">RELATED LINKS</span></span>
