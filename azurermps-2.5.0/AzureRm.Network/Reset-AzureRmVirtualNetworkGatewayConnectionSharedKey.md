---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: 160fb1b7455a2440773978ec80741922248a8af4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882834"
---
# <span data-ttu-id="aea18-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="aea18-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="aea18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aea18-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aea18-103">구문과</span><span class="sxs-lookup"><span data-stu-id="aea18-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aea18-104">설명은</span><span class="sxs-lookup"><span data-stu-id="aea18-104">DESCRIPTION</span></span>

## <span data-ttu-id="aea18-105">예제의</span><span class="sxs-lookup"><span data-stu-id="aea18-105">EXAMPLES</span></span>

### <span data-ttu-id="aea18-106">raid-1</span><span class="sxs-lookup"><span data-stu-id="aea18-106">1:</span></span>
```

```

## <span data-ttu-id="aea18-107">변수</span><span class="sxs-lookup"><span data-stu-id="aea18-107">PARAMETERS</span></span>

### <span data-ttu-id="aea18-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea18-108">-DefaultProfile</span></span>
<span data-ttu-id="aea18-109">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aea18-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aea18-110">-Force</span><span class="sxs-lookup"><span data-stu-id="aea18-110">-Force</span></span>
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

### <span data-ttu-id="aea18-111">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="aea18-111">-KeyLength</span></span>
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

### <span data-ttu-id="aea18-112">-이름</span><span class="sxs-lookup"><span data-stu-id="aea18-112">-Name</span></span>
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

### <span data-ttu-id="aea18-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aea18-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="aea18-114">-확인</span><span class="sxs-lookup"><span data-stu-id="aea18-114">-Confirm</span></span>
<span data-ttu-id="aea18-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea18-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aea18-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aea18-116">-WhatIf</span></span>
<span data-ttu-id="aea18-117">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aea18-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aea18-118">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aea18-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aea18-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea18-119">CommonParameters</span></span>
<span data-ttu-id="aea18-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aea18-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea18-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea18-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea18-122">입력</span><span class="sxs-lookup"><span data-stu-id="aea18-122">INPUTS</span></span>

## <span data-ttu-id="aea18-123">출력</span><span class="sxs-lookup"><span data-stu-id="aea18-123">OUTPUTS</span></span>

### <span data-ttu-id="aea18-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aea18-124">System.String</span></span>

## <span data-ttu-id="aea18-125">상속자</span><span class="sxs-lookup"><span data-stu-id="aea18-125">NOTES</span></span>

## <span data-ttu-id="aea18-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aea18-126">RELATED LINKS</span></span>

[<span data-ttu-id="aea18-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="aea18-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="aea18-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="aea18-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

