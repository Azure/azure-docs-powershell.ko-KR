---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: e051bd56aa8c5b5da27e2179b8f4d58ec4e4196d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711044"
---
# <span data-ttu-id="2c8d2-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="2c8d2-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="2c8d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c8d2-102">SYNOPSIS</span></span>
<span data-ttu-id="2c8d2-103">가상 네트워크 게이트웨이 연결의 공유 키를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c8d2-103">Resets the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c8d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c8d2-104">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c8d2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2c8d2-105">DESCRIPTION</span></span>
<span data-ttu-id="2c8d2-106">가상 네트워크 게이트웨이 연결의 공유 키를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c8d2-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="2c8d2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2c8d2-107">EXAMPLES</span></span>

### <span data-ttu-id="2c8d2-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="2c8d2-108">Example 1:</span></span>
```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="2c8d2-109">변수</span><span class="sxs-lookup"><span data-stu-id="2c8d2-109">PARAMETERS</span></span>

### <span data-ttu-id="2c8d2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c8d2-110">-DefaultProfile</span></span>
<span data-ttu-id="2c8d2-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c8d2-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c8d2-112">-Force</span><span class="sxs-lookup"><span data-stu-id="2c8d2-112">-Force</span></span>
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

### <span data-ttu-id="2c8d2-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="2c8d2-113">-KeyLength</span></span>
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

### <span data-ttu-id="2c8d2-114">-이름</span><span class="sxs-lookup"><span data-stu-id="2c8d2-114">-Name</span></span>
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

### <span data-ttu-id="2c8d2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c8d2-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="2c8d2-116">-확인</span><span class="sxs-lookup"><span data-stu-id="2c8d2-116">-Confirm</span></span>
<span data-ttu-id="2c8d2-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c8d2-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c8d2-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c8d2-118">-WhatIf</span></span>
<span data-ttu-id="2c8d2-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2c8d2-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c8d2-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c8d2-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c8d2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c8d2-121">CommonParameters</span></span>
<span data-ttu-id="2c8d2-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c8d2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c8d2-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c8d2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c8d2-124">입력</span><span class="sxs-lookup"><span data-stu-id="2c8d2-124">INPUTS</span></span>

### <span data-ttu-id="2c8d2-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2c8d2-125">System.String</span></span>

### <span data-ttu-id="2c8d2-126">시스템. UInt32</span><span class="sxs-lookup"><span data-stu-id="2c8d2-126">System.UInt32</span></span>

## <span data-ttu-id="2c8d2-127">출력</span><span class="sxs-lookup"><span data-stu-id="2c8d2-127">OUTPUTS</span></span>

### <span data-ttu-id="2c8d2-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2c8d2-128">System.String</span></span>

## <span data-ttu-id="2c8d2-129">상속자</span><span class="sxs-lookup"><span data-stu-id="2c8d2-129">NOTES</span></span>

## <span data-ttu-id="2c8d2-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c8d2-130">RELATED LINKS</span></span>

[<span data-ttu-id="2c8d2-131">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="2c8d2-131">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="2c8d2-132">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="2c8d2-132">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


