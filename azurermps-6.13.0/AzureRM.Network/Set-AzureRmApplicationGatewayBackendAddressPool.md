---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: d62afff67d1b5e7722b107b70810ac82e5b151d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703143"
---
# <span data-ttu-id="93c44-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="93c44-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="93c44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93c44-102">SYNOPSIS</span></span>
<span data-ttu-id="93c44-103">응용 프로그램 게이트웨이의 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="93c44-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93c44-104">구문과</span><span class="sxs-lookup"><span data-stu-id="93c44-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93c44-105">설명은</span><span class="sxs-lookup"><span data-stu-id="93c44-105">DESCRIPTION</span></span>
<span data-ttu-id="93c44-106">**AzureRmApplicationGatewayBackendAddressPool** Cmdlet은 Azure application gateway에 대 한 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="93c44-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="93c44-107">백 엔드 주소는 IP 주소, FQDN (정규화 된 도메인 이름) 또는 IP 구성 Id로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93c44-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="93c44-108">예제의</span><span class="sxs-lookup"><span data-stu-id="93c44-108">EXAMPLES</span></span>

### <span data-ttu-id="93c44-109">예제 1: Fqdn을 사용 하 여 백 엔드 주소 풀 설정</span><span class="sxs-lookup"><span data-stu-id="93c44-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="93c44-110">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="93c44-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="93c44-111">두 번째 명령은 Fqdn을 사용 하 여 $AppGw에서 응용 프로그램 게이트웨이의 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="93c44-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="93c44-112">예제 2: 백엔드 서버 IP 주소를 사용 하 여 백 엔드 주소 풀 설정</span><span class="sxs-lookup"><span data-stu-id="93c44-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="93c44-113">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="93c44-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="93c44-114">두 번째 명령은 IP 주소를 사용 하 여 $AppGw에서 응용 프로그램 게이트웨이의 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="93c44-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="93c44-115">변수</span><span class="sxs-lookup"><span data-stu-id="93c44-115">PARAMETERS</span></span>

### <span data-ttu-id="93c44-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93c44-116">-ApplicationGateway</span></span>
<span data-ttu-id="93c44-117">이 cmdlet이 백 엔드 주소 풀을 연결 하는 데 사용할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93c44-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="93c44-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="93c44-118">-BackendFqdns</span></span>
<span data-ttu-id="93c44-119">백 엔드 서버 풀로 사용할 백 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93c44-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c44-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="93c44-120">-BackendIPAddresses</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93c44-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c44-121">-DefaultProfile</span></span>
<span data-ttu-id="93c44-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93c44-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93c44-123">-이름</span><span class="sxs-lookup"><span data-stu-id="93c44-123">-Name</span></span>
<span data-ttu-id="93c44-124">백 엔드 주소 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="93c44-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="93c44-125">이 백 엔드 주소 풀은 응용 프로그램 게이트웨이에서 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="93c44-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="93c44-126">-확인</span><span class="sxs-lookup"><span data-stu-id="93c44-126">-Confirm</span></span>
<span data-ttu-id="93c44-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="93c44-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93c44-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93c44-128">-WhatIf</span></span>
<span data-ttu-id="93c44-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="93c44-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93c44-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93c44-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93c44-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c44-131">CommonParameters</span></span>
<span data-ttu-id="93c44-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="93c44-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c44-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93c44-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c44-134">입력</span><span class="sxs-lookup"><span data-stu-id="93c44-134">INPUTS</span></span>

### <span data-ttu-id="93c44-135">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93c44-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="93c44-136">매개 변수: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="93c44-136">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="93c44-137">출력</span><span class="sxs-lookup"><span data-stu-id="93c44-137">OUTPUTS</span></span>

### <span data-ttu-id="93c44-138">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93c44-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="93c44-139">상속자</span><span class="sxs-lookup"><span data-stu-id="93c44-139">NOTES</span></span>

## <span data-ttu-id="93c44-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93c44-140">RELATED LINKS</span></span>

[<span data-ttu-id="93c44-141">추가-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="93c44-141">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="93c44-142">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="93c44-142">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="93c44-143">새로운 AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="93c44-143">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="93c44-144">제거-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="93c44-144">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)


