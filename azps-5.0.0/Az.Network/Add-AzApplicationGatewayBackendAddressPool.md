---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: c415fb890240ea6f4fb03b71c3a249eece1ba02b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226739"
---
# <span data-ttu-id="e03df-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e03df-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="e03df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e03df-102">SYNOPSIS</span></span>
<span data-ttu-id="e03df-103">응용 프로그램 게이트웨이에 백 엔드 주소 풀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03df-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="e03df-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e03df-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e03df-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e03df-105">DESCRIPTION</span></span>
<span data-ttu-id="e03df-106">**Add-AzApplicationGatewayBackendAddressPool** cmdlet은 응용 프로그램 게이트웨이에 백 엔드 주소 풀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03df-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="e03df-107">백 엔드 주소는 IP 주소, FQDN (정규화 된 도메인 이름) 또는 IP 구성 Id를 사용 하 여 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e03df-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="e03df-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e03df-108">EXAMPLES</span></span>

### <span data-ttu-id="e03df-109">예제 1: 백 엔드 서버 FQDN을 사용 하 여 백 엔드 주소 풀 추가</span><span class="sxs-lookup"><span data-stu-id="e03df-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="e03df-110">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다. 두 번째 명령은 Fqdn을 사용 하 여 $AppGw에 저장 된 응용 프로그램 게이트웨이의 백 엔드 주소 풀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03df-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="e03df-111">예제 2: 백엔드 서버 IP 주소를 사용 하 여 백 엔드 주소 풀 추가</span><span class="sxs-lookup"><span data-stu-id="e03df-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="e03df-112">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다. 두 번째 명령은 IP 주소를 사용 하 여 $AppGw에 저장 된 응용 프로그램 게이트웨이의 백 엔드 주소 풀을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03df-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="e03df-113">변수</span><span class="sxs-lookup"><span data-stu-id="e03df-113">PARAMETERS</span></span>

### <span data-ttu-id="e03df-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e03df-114">-ApplicationGateway</span></span>
<span data-ttu-id="e03df-115">이 cmdlet이 백 엔드 주소 풀을 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03df-115">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="e03df-116">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="e03df-116">-BackendFqdns</span></span>
<span data-ttu-id="e03df-117">이 cmdlet이 백 엔드 서버 풀로 추가 하는 백엔드 Fqdn 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03df-117">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="e03df-118">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="e03df-118">-BackendIPAddresses</span></span>
<span data-ttu-id="e03df-119">이 cmdlet이 백 엔드 서버 풀로 추가 하는 백 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03df-119">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="e03df-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e03df-120">-DefaultProfile</span></span>
<span data-ttu-id="e03df-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e03df-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e03df-122">-이름</span><span class="sxs-lookup"><span data-stu-id="e03df-122">-Name</span></span>
<span data-ttu-id="e03df-123">이 cmdlet이 추가 하는 백 엔드 서버 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03df-123">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="e03df-124">-확인</span><span class="sxs-lookup"><span data-stu-id="e03df-124">-Confirm</span></span>
<span data-ttu-id="e03df-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03df-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e03df-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e03df-126">-WhatIf</span></span>
<span data-ttu-id="e03df-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e03df-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e03df-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e03df-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e03df-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e03df-129">CommonParameters</span></span>
<span data-ttu-id="e03df-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e03df-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e03df-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e03df-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e03df-132">입력</span><span class="sxs-lookup"><span data-stu-id="e03df-132">INPUTS</span></span>

### <span data-ttu-id="e03df-133">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e03df-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e03df-134">출력</span><span class="sxs-lookup"><span data-stu-id="e03df-134">OUTPUTS</span></span>

### <span data-ttu-id="e03df-135">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e03df-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e03df-136">상속자</span><span class="sxs-lookup"><span data-stu-id="e03df-136">NOTES</span></span>

## <span data-ttu-id="e03df-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e03df-137">RELATED LINKS</span></span>

[<span data-ttu-id="e03df-138">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e03df-138">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e03df-139">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e03df-139">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e03df-140">새로운 AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e03df-140">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e03df-141">제거-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e03df-141">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e03df-142">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e03df-142">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e03df-143">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e03df-143">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
