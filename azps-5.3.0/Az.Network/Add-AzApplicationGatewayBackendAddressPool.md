---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: c415fb890240ea6f4fb03b71c3a249eece1ba02b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380374"
---
# <span data-ttu-id="cb022-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cb022-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="cb022-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb022-102">SYNOPSIS</span></span>
<span data-ttu-id="cb022-103">애플리케이션 게이트웨이에 백 엔드 주소 풀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cb022-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="cb022-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb022-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb022-105">설명</span><span class="sxs-lookup"><span data-stu-id="cb022-105">DESCRIPTION</span></span>
<span data-ttu-id="cb022-106">**Add-AzApplicationGatewayBackendAddressPool** cmdlet은 애플리케이션 게이트웨이에 백 엔드 주소 풀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cb022-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="cb022-107">백 엔드 주소는 IP 주소, FQDN(정식 도메인 이름) 또는 IP 구성 ID를 사용하여 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cb022-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="cb022-108">예제</span><span class="sxs-lookup"><span data-stu-id="cb022-108">EXAMPLES</span></span>

### <span data-ttu-id="cb022-109">예제 1: 백 엔드 서버 FQDN을 사용하여 백 엔드 주소 풀 추가</span><span class="sxs-lookup"><span data-stu-id="cb022-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="cb022-110">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다. 두 번째 명령은 FQDNS를 사용하여 애플리케이션 게이트웨이에 저장된 애플리케이션 $AppGw 풀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cb022-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="cb022-111">예제 2: 백 엔드 서버 IP 주소를 사용하여 백 엔드 주소 풀 추가</span><span class="sxs-lookup"><span data-stu-id="cb022-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="cb022-112">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다. 두 번째 명령은 IP 주소를 사용하여 $AppGw 애플리케이션 게이트웨이의 백 엔드 주소 풀을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="cb022-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="cb022-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb022-113">PARAMETERS</span></span>

### <span data-ttu-id="cb022-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb022-114">-ApplicationGateway</span></span>
<span data-ttu-id="cb022-115">이 cmdlet이 백 엔드 주소 풀을 추가할 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb022-115">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb022-116">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="cb022-116">-BackendFqdns</span></span>
<span data-ttu-id="cb022-117">이 cmdlet이 백 엔드 서버 풀로 추가하는 백 엔드 FQDNS 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb022-117">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb022-118">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="cb022-118">-BackendIPAddresses</span></span>
<span data-ttu-id="cb022-119">이 cmdlet이 백 엔드 서버 풀로 추가하는 백 엔드 IP 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb022-119">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb022-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb022-120">-DefaultProfile</span></span>
<span data-ttu-id="cb022-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb022-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb022-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cb022-122">-Name</span></span>
<span data-ttu-id="cb022-123">이 cmdlet이 추가하는 백 엔드 서버 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cb022-123">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb022-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb022-124">-Confirm</span></span>
<span data-ttu-id="cb022-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb022-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb022-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb022-126">-WhatIf</span></span>
<span data-ttu-id="cb022-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cb022-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb022-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb022-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb022-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb022-129">CommonParameters</span></span>
<span data-ttu-id="cb022-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb022-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb022-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cb022-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb022-132">입력</span><span class="sxs-lookup"><span data-stu-id="cb022-132">INPUTS</span></span>

### <span data-ttu-id="cb022-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb022-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cb022-134">출력</span><span class="sxs-lookup"><span data-stu-id="cb022-134">OUTPUTS</span></span>

### <span data-ttu-id="cb022-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb022-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cb022-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb022-136">NOTES</span></span>

## <span data-ttu-id="cb022-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb022-137">RELATED LINKS</span></span>

[<span data-ttu-id="cb022-138">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cb022-138">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="cb022-139">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cb022-139">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="cb022-140">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cb022-140">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="cb022-141">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cb022-141">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="cb022-142">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cb022-142">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="cb022-143">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cb022-143">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
