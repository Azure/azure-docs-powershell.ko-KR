---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkpeering
schema: 2.0.0
ms.openlocfilehash: de39828183f06f8435078ceffc8c303c376e6186
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882845"
---
# <span data-ttu-id="c5385-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c5385-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="c5385-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5385-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5385-103">구문과</span><span class="sxs-lookup"><span data-stu-id="c5385-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5385-104">설명은</span><span class="sxs-lookup"><span data-stu-id="c5385-104">DESCRIPTION</span></span>

## <span data-ttu-id="c5385-105">예제의</span><span class="sxs-lookup"><span data-stu-id="c5385-105">EXAMPLES</span></span>

### <span data-ttu-id="c5385-106">예제 1: 가상 네트워크 피어 링 제거</span><span class="sxs-lookup"><span data-stu-id="c5385-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="c5385-107">변수</span><span class="sxs-lookup"><span data-stu-id="c5385-107">PARAMETERS</span></span>

### <span data-ttu-id="c5385-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5385-108">-AsJob</span></span>
<span data-ttu-id="c5385-109">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c5385-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5385-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5385-110">-DefaultProfile</span></span>
<span data-ttu-id="c5385-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5385-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5385-112">-Force</span><span class="sxs-lookup"><span data-stu-id="c5385-112">-Force</span></span>
<span data-ttu-id="c5385-113">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5385-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c5385-114">-이름</span><span class="sxs-lookup"><span data-stu-id="c5385-114">-Name</span></span>
<span data-ttu-id="c5385-115">가상 네트워크 피어 링 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5385-115">The virtual network peering name.</span></span>

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

### <span data-ttu-id="c5385-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5385-116">-PassThru</span></span>
<span data-ttu-id="c5385-117">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5385-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c5385-118">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5385-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c5385-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5385-119">-ResourceGroupName</span></span>
<span data-ttu-id="c5385-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c5385-120">The resource group name</span></span>

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

### <span data-ttu-id="c5385-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="c5385-121">-VirtualNetworkName</span></span>
<span data-ttu-id="c5385-122">가상 네트워크 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5385-122">The virtual network name.</span></span>

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

### <span data-ttu-id="c5385-123">-확인</span><span class="sxs-lookup"><span data-stu-id="c5385-123">-Confirm</span></span>
<span data-ttu-id="c5385-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5385-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5385-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5385-125">-WhatIf</span></span>
<span data-ttu-id="c5385-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c5385-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5385-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5385-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5385-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5385-128">CommonParameters</span></span>
<span data-ttu-id="c5385-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5385-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5385-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5385-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5385-131">입력</span><span class="sxs-lookup"><span data-stu-id="c5385-131">INPUTS</span></span>

## <span data-ttu-id="c5385-132">출력</span><span class="sxs-lookup"><span data-stu-id="c5385-132">OUTPUTS</span></span>

## <span data-ttu-id="c5385-133">상속자</span><span class="sxs-lookup"><span data-stu-id="c5385-133">NOTES</span></span>

## <span data-ttu-id="c5385-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5385-134">RELATED LINKS</span></span>

