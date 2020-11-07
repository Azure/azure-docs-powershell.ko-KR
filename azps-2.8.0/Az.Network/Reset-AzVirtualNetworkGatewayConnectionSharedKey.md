---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 1fa793396fba139d1aa08e760c9aa780f8e0f166
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871137"
---
# <span data-ttu-id="b0437-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b0437-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="b0437-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0437-102">SYNOPSIS</span></span>
<span data-ttu-id="b0437-103">가상 네트워크 게이트웨이 연결의 공유 키를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0437-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="b0437-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0437-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0437-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b0437-105">DESCRIPTION</span></span>
<span data-ttu-id="b0437-106">가상 네트워크 게이트웨이 연결의 공유 키를 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0437-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="b0437-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b0437-107">EXAMPLES</span></span>

### <span data-ttu-id="b0437-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="b0437-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="b0437-109">변수</span><span class="sxs-lookup"><span data-stu-id="b0437-109">PARAMETERS</span></span>

### <span data-ttu-id="b0437-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0437-110">-DefaultProfile</span></span>
<span data-ttu-id="b0437-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0437-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0437-112">-Force</span><span class="sxs-lookup"><span data-stu-id="b0437-112">-Force</span></span>
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

### <span data-ttu-id="b0437-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="b0437-113">-KeyLength</span></span>
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

### <span data-ttu-id="b0437-114">-이름</span><span class="sxs-lookup"><span data-stu-id="b0437-114">-Name</span></span>
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

### <span data-ttu-id="b0437-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0437-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="b0437-116">-확인</span><span class="sxs-lookup"><span data-stu-id="b0437-116">-Confirm</span></span>
<span data-ttu-id="b0437-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0437-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0437-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0437-118">-WhatIf</span></span>
<span data-ttu-id="b0437-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0437-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0437-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0437-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0437-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0437-121">CommonParameters</span></span>
<span data-ttu-id="b0437-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0437-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0437-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0437-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0437-124">입력</span><span class="sxs-lookup"><span data-stu-id="b0437-124">INPUTS</span></span>

### <span data-ttu-id="b0437-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b0437-125">System.String</span></span>

### <span data-ttu-id="b0437-126">시스템. UInt32</span><span class="sxs-lookup"><span data-stu-id="b0437-126">System.UInt32</span></span>

## <span data-ttu-id="b0437-127">출력</span><span class="sxs-lookup"><span data-stu-id="b0437-127">OUTPUTS</span></span>

### <span data-ttu-id="b0437-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b0437-128">System.String</span></span>

## <span data-ttu-id="b0437-129">상속자</span><span class="sxs-lookup"><span data-stu-id="b0437-129">NOTES</span></span>

## <span data-ttu-id="b0437-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0437-130">RELATED LINKS</span></span>

[<span data-ttu-id="b0437-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b0437-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="b0437-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b0437-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
