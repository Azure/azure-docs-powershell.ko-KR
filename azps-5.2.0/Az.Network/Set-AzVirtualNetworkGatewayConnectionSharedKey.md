---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a35d659de6019d9d9451289716a7acac7e33a8b7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331749"
---
# <span data-ttu-id="b539d-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b539d-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="b539d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b539d-102">SYNOPSIS</span></span>
<span data-ttu-id="b539d-103">가상 네트워크 게이트웨이 연결의 공유 키를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="b539d-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="b539d-104">구문</span><span class="sxs-lookup"><span data-stu-id="b539d-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b539d-105">설명</span><span class="sxs-lookup"><span data-stu-id="b539d-105">DESCRIPTION</span></span>
<span data-ttu-id="b539d-106">**Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet은 가상 네트워크 게이트웨이 연결의 공유 키를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="b539d-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="b539d-107">예제</span><span class="sxs-lookup"><span data-stu-id="b539d-107">EXAMPLES</span></span>

### <span data-ttu-id="b539d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b539d-108">Example 1</span></span>
```powershell
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="b539d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b539d-109">PARAMETERS</span></span>

### <span data-ttu-id="b539d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b539d-110">-DefaultProfile</span></span>
<span data-ttu-id="b539d-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b539d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b539d-112">-Force</span><span class="sxs-lookup"><span data-stu-id="b539d-112">-Force</span></span>
<span data-ttu-id="b539d-113">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b539d-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b539d-114">-Name</span><span class="sxs-lookup"><span data-stu-id="b539d-114">-Name</span></span>
<span data-ttu-id="b539d-115">가상 네트워크 게이트웨이 공유 키의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b539d-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="b539d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b539d-116">-ResourceGroupName</span></span>
<span data-ttu-id="b539d-117">가상 네트워크 게이트웨이가 속한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b539d-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="b539d-118">-Value</span><span class="sxs-lookup"><span data-stu-id="b539d-118">-Value</span></span>
<span data-ttu-id="b539d-119">공유 키의 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b539d-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="b539d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b539d-120">-Confirm</span></span>
<span data-ttu-id="b539d-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b539d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b539d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b539d-122">-WhatIf</span></span>
<span data-ttu-id="b539d-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b539d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b539d-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b539d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b539d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b539d-125">CommonParameters</span></span>
<span data-ttu-id="b539d-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b539d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b539d-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b539d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b539d-128">입력</span><span class="sxs-lookup"><span data-stu-id="b539d-128">INPUTS</span></span>

### <span data-ttu-id="b539d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b539d-129">System.String</span></span>

## <span data-ttu-id="b539d-130">출력</span><span class="sxs-lookup"><span data-stu-id="b539d-130">OUTPUTS</span></span>

### <span data-ttu-id="b539d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b539d-131">System.String</span></span>

## <span data-ttu-id="b539d-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b539d-132">NOTES</span></span>

## <span data-ttu-id="b539d-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b539d-133">RELATED LINKS</span></span>

[<span data-ttu-id="b539d-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b539d-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="b539d-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="b539d-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)
