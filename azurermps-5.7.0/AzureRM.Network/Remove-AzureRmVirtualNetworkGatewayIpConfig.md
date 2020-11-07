---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 6be6c0d7993b44d807cad5bf8c06a203fe8ff7a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704165"
---
# <span data-ttu-id="f99b5-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="f99b5-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="f99b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f99b5-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f99b5-103">구문과</span><span class="sxs-lookup"><span data-stu-id="f99b5-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f99b5-104">설명은</span><span class="sxs-lookup"><span data-stu-id="f99b5-104">DESCRIPTION</span></span>

## <span data-ttu-id="f99b5-105">예제의</span><span class="sxs-lookup"><span data-stu-id="f99b5-105">EXAMPLES</span></span>

### <span data-ttu-id="f99b5-106">raid-1</span><span class="sxs-lookup"><span data-stu-id="f99b5-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="f99b5-107">변수</span><span class="sxs-lookup"><span data-stu-id="f99b5-107">PARAMETERS</span></span>

### <span data-ttu-id="f99b5-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f99b5-108">-DefaultProfile</span></span>
<span data-ttu-id="f99b5-109">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f99b5-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f99b5-110">-이름</span><span class="sxs-lookup"><span data-stu-id="f99b5-110">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f99b5-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f99b5-111">-VirtualNetworkGateway</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f99b5-112">-확인</span><span class="sxs-lookup"><span data-stu-id="f99b5-112">-Confirm</span></span>
<span data-ttu-id="f99b5-113">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f99b5-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f99b5-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f99b5-114">-WhatIf</span></span>
<span data-ttu-id="f99b5-115">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f99b5-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f99b5-116">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f99b5-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f99b5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f99b5-117">CommonParameters</span></span>
<span data-ttu-id="f99b5-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f99b5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f99b5-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f99b5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f99b5-120">입력</span><span class="sxs-lookup"><span data-stu-id="f99b5-120">INPUTS</span></span>

### <span data-ttu-id="f99b5-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f99b5-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="f99b5-122">' VirtualNetworkGateway ' 매개 변수는 파이프라인에서 ' PSVirtualNetworkGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f99b5-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="f99b5-123">출력</span><span class="sxs-lookup"><span data-stu-id="f99b5-123">OUTPUTS</span></span>

### <span data-ttu-id="f99b5-124">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f99b5-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f99b5-125">상속자</span><span class="sxs-lookup"><span data-stu-id="f99b5-125">NOTES</span></span>

## <span data-ttu-id="f99b5-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f99b5-126">RELATED LINKS</span></span>

