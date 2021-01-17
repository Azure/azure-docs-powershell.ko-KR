---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 496e5aca71d1a947b97c8fd27cab348cee9ba49b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323266"
---
# <span data-ttu-id="4e3d7-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="4e3d7-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="4e3d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e3d7-102">SYNOPSIS</span></span>
<span data-ttu-id="4e3d7-103">가상 네트워크 게이트웨이 연결의 공유 키를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="4e3d7-104">구문</span><span class="sxs-lookup"><span data-stu-id="4e3d7-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e3d7-105">설명</span><span class="sxs-lookup"><span data-stu-id="4e3d7-105">DESCRIPTION</span></span>
<span data-ttu-id="4e3d7-106">가상 네트워크 게이트웨이 연결의 공유 키를 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="4e3d7-107">예제</span><span class="sxs-lookup"><span data-stu-id="4e3d7-107">EXAMPLES</span></span>

### <span data-ttu-id="4e3d7-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="4e3d7-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="4e3d7-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e3d7-109">PARAMETERS</span></span>

### <span data-ttu-id="4e3d7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e3d7-110">-DefaultProfile</span></span>
<span data-ttu-id="4e3d7-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e3d7-112">-Force</span><span class="sxs-lookup"><span data-stu-id="4e3d7-112">-Force</span></span>
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

### <span data-ttu-id="4e3d7-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="4e3d7-113">-KeyLength</span></span>
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

### <span data-ttu-id="4e3d7-114">-Name</span><span class="sxs-lookup"><span data-stu-id="4e3d7-114">-Name</span></span>
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

### <span data-ttu-id="4e3d7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e3d7-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="4e3d7-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e3d7-116">-Confirm</span></span>
<span data-ttu-id="4e3d7-117">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e3d7-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e3d7-118">-WhatIf</span></span>
<span data-ttu-id="4e3d7-119">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4e3d7-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e3d7-120">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e3d7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e3d7-121">CommonParameters</span></span>
<span data-ttu-id="4e3d7-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e3d7-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4e3d7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e3d7-124">입력</span><span class="sxs-lookup"><span data-stu-id="4e3d7-124">INPUTS</span></span>

### <span data-ttu-id="4e3d7-125">System.String</span><span class="sxs-lookup"><span data-stu-id="4e3d7-125">System.String</span></span>

### <span data-ttu-id="4e3d7-126">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="4e3d7-126">System.UInt32</span></span>

## <span data-ttu-id="4e3d7-127">출력</span><span class="sxs-lookup"><span data-stu-id="4e3d7-127">OUTPUTS</span></span>

### <span data-ttu-id="4e3d7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4e3d7-128">System.String</span></span>

## <span data-ttu-id="4e3d7-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4e3d7-129">NOTES</span></span>

## <span data-ttu-id="4e3d7-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4e3d7-130">RELATED LINKS</span></span>

[<span data-ttu-id="4e3d7-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="4e3d7-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="4e3d7-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="4e3d7-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
