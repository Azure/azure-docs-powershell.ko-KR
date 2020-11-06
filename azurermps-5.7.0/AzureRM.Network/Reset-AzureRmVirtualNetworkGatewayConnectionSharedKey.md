---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a805145445f8bd17ac60497e2c7d7e89ea56a3c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536751"
---
# <span data-ttu-id="e5538-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="e5538-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="e5538-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5538-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5538-103">구문과</span><span class="sxs-lookup"><span data-stu-id="e5538-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5538-104">설명은</span><span class="sxs-lookup"><span data-stu-id="e5538-104">DESCRIPTION</span></span>

## <span data-ttu-id="e5538-105">예제의</span><span class="sxs-lookup"><span data-stu-id="e5538-105">EXAMPLES</span></span>

## <span data-ttu-id="e5538-106">변수</span><span class="sxs-lookup"><span data-stu-id="e5538-106">PARAMETERS</span></span>

### <span data-ttu-id="e5538-107">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5538-107">-DefaultProfile</span></span>
<span data-ttu-id="e5538-108">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5538-108">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5538-109">-Force</span><span class="sxs-lookup"><span data-stu-id="e5538-109">-Force</span></span>
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

### <span data-ttu-id="e5538-110">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="e5538-110">-KeyLength</span></span>
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

### <span data-ttu-id="e5538-111">-이름</span><span class="sxs-lookup"><span data-stu-id="e5538-111">-Name</span></span>
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

### <span data-ttu-id="e5538-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5538-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="e5538-113">-확인</span><span class="sxs-lookup"><span data-stu-id="e5538-113">-Confirm</span></span>
<span data-ttu-id="e5538-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5538-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5538-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5538-115">-WhatIf</span></span>
<span data-ttu-id="e5538-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e5538-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5538-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5538-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5538-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5538-118">CommonParameters</span></span>
<span data-ttu-id="e5538-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5538-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5538-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5538-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5538-121">입력</span><span class="sxs-lookup"><span data-stu-id="e5538-121">INPUTS</span></span>

### <span data-ttu-id="e5538-122">않아야</span><span class="sxs-lookup"><span data-stu-id="e5538-122">None</span></span>
<span data-ttu-id="e5538-123">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5538-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e5538-124">출력</span><span class="sxs-lookup"><span data-stu-id="e5538-124">OUTPUTS</span></span>

### <span data-ttu-id="e5538-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e5538-125">System.String</span></span>

## <span data-ttu-id="e5538-126">상속자</span><span class="sxs-lookup"><span data-stu-id="e5538-126">NOTES</span></span>

## <span data-ttu-id="e5538-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5538-127">RELATED LINKS</span></span>

[<span data-ttu-id="e5538-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="e5538-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="e5538-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="e5538-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


