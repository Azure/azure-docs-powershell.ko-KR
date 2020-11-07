---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 9315b279fd7ac6842a65c78898f1d5da23a8e1c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869621"
---
# <span data-ttu-id="689f5-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="689f5-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="689f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="689f5-102">SYNOPSIS</span></span>
<span data-ttu-id="689f5-103">응용 프로그램 게이트웨이의 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="689f5-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="689f5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="689f5-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="689f5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="689f5-105">DESCRIPTION</span></span>
<span data-ttu-id="689f5-106">**AzApplicationGatewayBackendAddressPool** Cmdlet은 Azure application gateway에 대 한 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="689f5-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="689f5-107">백 엔드 주소는 IP 주소, FQDN (정규화 된 도메인 이름) 또는 IP 구성 Id로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="689f5-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="689f5-108">예제의</span><span class="sxs-lookup"><span data-stu-id="689f5-108">EXAMPLES</span></span>

### <span data-ttu-id="689f5-109">예제 1: Fqdn을 사용 하 여 백 엔드 주소 풀 설정</span><span class="sxs-lookup"><span data-stu-id="689f5-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="689f5-110">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="689f5-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="689f5-111">두 번째 명령은 Fqdn을 사용 하 여 $AppGw에서 응용 프로그램 게이트웨이의 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="689f5-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="689f5-112">예제 2: 백엔드 서버 IP 주소를 사용 하 여 백 엔드 주소 풀 설정</span><span class="sxs-lookup"><span data-stu-id="689f5-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="689f5-113">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="689f5-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="689f5-114">두 번째 명령은 IP 주소를 사용 하 여 $AppGw에서 응용 프로그램 게이트웨이의 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="689f5-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="689f5-115">변수</span><span class="sxs-lookup"><span data-stu-id="689f5-115">PARAMETERS</span></span>

### <span data-ttu-id="689f5-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="689f5-116">-ApplicationGateway</span></span>
<span data-ttu-id="689f5-117">이 cmdlet이 백 엔드 주소 풀을 연결 하는 데 사용할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="689f5-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="689f5-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="689f5-118">-BackendFqdns</span></span>
<span data-ttu-id="689f5-119">백 엔드 서버 풀로 사용할 백 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="689f5-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="689f5-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="689f5-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="689f5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="689f5-121">-DefaultProfile</span></span>
<span data-ttu-id="689f5-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="689f5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="689f5-123">-이름</span><span class="sxs-lookup"><span data-stu-id="689f5-123">-Name</span></span>
<span data-ttu-id="689f5-124">백 엔드 주소 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="689f5-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="689f5-125">이 백 엔드 주소 풀은 응용 프로그램 게이트웨이에서 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="689f5-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="689f5-126">-확인</span><span class="sxs-lookup"><span data-stu-id="689f5-126">-Confirm</span></span>
<span data-ttu-id="689f5-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="689f5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="689f5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="689f5-128">-WhatIf</span></span>
<span data-ttu-id="689f5-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="689f5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="689f5-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="689f5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="689f5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="689f5-131">CommonParameters</span></span>
<span data-ttu-id="689f5-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="689f5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="689f5-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="689f5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="689f5-134">입력</span><span class="sxs-lookup"><span data-stu-id="689f5-134">INPUTS</span></span>

### <span data-ttu-id="689f5-135">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="689f5-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="689f5-136">출력</span><span class="sxs-lookup"><span data-stu-id="689f5-136">OUTPUTS</span></span>

### <span data-ttu-id="689f5-137">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="689f5-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="689f5-138">상속자</span><span class="sxs-lookup"><span data-stu-id="689f5-138">NOTES</span></span>

## <span data-ttu-id="689f5-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="689f5-139">RELATED LINKS</span></span>

[<span data-ttu-id="689f5-140">추가-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="689f5-140">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="689f5-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="689f5-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="689f5-142">새로운 AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="689f5-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="689f5-143">제거-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="689f5-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


