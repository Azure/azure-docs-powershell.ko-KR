---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: a5b0fa1054136354725ec404960bcf680a104d06
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496547"
---
# <span data-ttu-id="d1f88-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d1f88-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="d1f88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1f88-102">SYNOPSIS</span></span>
<span data-ttu-id="d1f88-103">애플리케이션 게이트웨이에 대한 백 엔드 주소 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f88-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="d1f88-104">구문</span><span class="sxs-lookup"><span data-stu-id="d1f88-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1f88-105">설명</span><span class="sxs-lookup"><span data-stu-id="d1f88-105">DESCRIPTION</span></span>
<span data-ttu-id="d1f88-106">**Set-AzApplicationGatewayBackendAddressPool** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 백 엔드 주소 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f88-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="d1f88-107">백 엔드 주소는 IP 주소, FQDN(정식 도메인 이름) 또는 IP 구성 ID로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f88-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="d1f88-108">예제</span><span class="sxs-lookup"><span data-stu-id="d1f88-108">EXAMPLES</span></span>

### <span data-ttu-id="d1f88-109">예제 1: FQDNs를 사용하여 백 엔드 주소 풀 설정</span><span class="sxs-lookup"><span data-stu-id="d1f88-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="d1f88-110">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f88-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d1f88-111">두 번째 명령은 FQDNS를 사용하여 애플리케이션 게이트웨이의 $AppGw 풀을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f88-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="d1f88-112">예제 2: 백 엔드 서버 IP 주소를 사용하여 백 엔드 주소 풀 설정</span><span class="sxs-lookup"><span data-stu-id="d1f88-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="d1f88-113">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f88-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d1f88-114">두 번째 명령은 IP 주소를 사용하여 애플리케이션 게이트웨이의 $AppGw 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f88-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="d1f88-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1f88-115">PARAMETERS</span></span>

### <span data-ttu-id="d1f88-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1f88-116">-ApplicationGateway</span></span>
<span data-ttu-id="d1f88-117">이 cmdlet이 백 엔드 주소 풀을 연결한 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f88-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="d1f88-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="d1f88-118">-BackendFqdns</span></span>
<span data-ttu-id="d1f88-119">백 엔드 서버 풀로 사용할 백 엔드 IP 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f88-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="d1f88-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="d1f88-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="d1f88-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1f88-121">-DefaultProfile</span></span>
<span data-ttu-id="d1f88-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1f88-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1f88-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d1f88-123">-Name</span></span>
<span data-ttu-id="d1f88-124">백 엔드 주소 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f88-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="d1f88-125">이 백 엔드 주소 풀은 애플리케이션 게이트웨이에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f88-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="d1f88-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1f88-126">-Confirm</span></span>
<span data-ttu-id="d1f88-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1f88-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1f88-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1f88-128">-WhatIf</span></span>
<span data-ttu-id="d1f88-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d1f88-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1f88-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1f88-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1f88-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f88-131">CommonParameters</span></span>
<span data-ttu-id="d1f88-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1f88-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1f88-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d1f88-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f88-134">입력</span><span class="sxs-lookup"><span data-stu-id="d1f88-134">INPUTS</span></span>

### <span data-ttu-id="d1f88-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1f88-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d1f88-136">출력</span><span class="sxs-lookup"><span data-stu-id="d1f88-136">OUTPUTS</span></span>

### <span data-ttu-id="d1f88-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d1f88-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d1f88-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d1f88-138">NOTES</span></span>

## <span data-ttu-id="d1f88-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1f88-139">RELATED LINKS</span></span>

[<span data-ttu-id="d1f88-140">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d1f88-140">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d1f88-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d1f88-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d1f88-142">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d1f88-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="d1f88-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d1f88-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


