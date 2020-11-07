---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 66ca482f2b284118ccf5095ec833a5278a5ea73d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882810"
---
# <span data-ttu-id="e2dc9-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2dc9-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="e2dc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="e2dc9-103">응용 프로그램 게이트웨이의 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2dc9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2dc9-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2dc9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e2dc9-105">DESCRIPTION</span></span>
<span data-ttu-id="e2dc9-106">**AzureRmApplicationGatewayBackendAddressPool** Cmdlet은 Azure application gateway에 대 한 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="e2dc9-107">백 엔드 주소는 IP 주소, FQDN (정규화 된 도메인 이름) 또는 IP 구성 Id로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="e2dc9-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e2dc9-108">EXAMPLES</span></span>

### <span data-ttu-id="e2dc9-109">예제 1: Fqdn을 사용 하 여 백 엔드 주소 풀 설정</span><span class="sxs-lookup"><span data-stu-id="e2dc9-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="e2dc9-110">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="e2dc9-111">두 번째 명령은 Fqdn을 사용 하 여 $AppGw에서 응용 프로그램 게이트웨이의 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="e2dc9-112">예제 2: 백엔드 서버 IP 주소를 사용 하 여 백 엔드 주소 풀 설정</span><span class="sxs-lookup"><span data-stu-id="e2dc9-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="e2dc9-113">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="e2dc9-114">두 번째 명령은 IP 주소를 사용 하 여 $AppGw에서 응용 프로그램 게이트웨이의 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="e2dc9-115">예제 3: 백엔드 서버의 ID를 사용 하 여 백 엔드 주소 풀 설정 IP 주소</span><span class="sxs-lookup"><span data-stu-id="e2dc9-115">Example 3: Setting a back-end address pool by using the ID of the backend server?s IP address</span></span>
```
PS C:\> $Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="e2dc9-116">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 Nic01 라는 네트워크 인터페이스 개체를 가져와 $Nic 01 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-116">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.</span></span>

<span data-ttu-id="e2dc9-117">두 번째 명령은 ResourceGroup02 이라는 리소스 그룹에 속하는 Nic02 라는 네트워크 인터페이스 개체를 가져와 $Nic 02 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-117">The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.</span></span>

<span data-ttu-id="e2dc9-118">세 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-118">The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="e2dc9-119">위의 명령은 $Nic 01 및 $Nic 02의 백 엔드 IP 구성 Id를 사용 하 여 $AppGw에서 응용 프로그램 게이트웨이의 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-119">The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to update the back-end address pool of the application gateway in $AppGw.</span></span>

## <span data-ttu-id="e2dc9-120">변수</span><span class="sxs-lookup"><span data-stu-id="e2dc9-120">PARAMETERS</span></span>

### <span data-ttu-id="e2dc9-121">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2dc9-121">-ApplicationGateway</span></span>
<span data-ttu-id="e2dc9-122">이 cmdlet이 백 엔드 주소 풀을 연결 하는 데 사용할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-122">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2dc9-123">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="e2dc9-123">-BackendFqdns</span></span>
<span data-ttu-id="e2dc9-124">백 엔드 서버 풀로 사용할 백 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-124">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="e2dc9-125">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="e2dc9-125">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="e2dc9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2dc9-126">-DefaultProfile</span></span>
<span data-ttu-id="e2dc9-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2dc9-128">-이름</span><span class="sxs-lookup"><span data-stu-id="e2dc9-128">-Name</span></span>
<span data-ttu-id="e2dc9-129">백 엔드 주소 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-129">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="e2dc9-130">이 백 엔드 주소 풀은 응용 프로그램 게이트웨이에서 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-130">This back-end address pool must exist in the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2dc9-131">-확인</span><span class="sxs-lookup"><span data-stu-id="e2dc9-131">-Confirm</span></span>
<span data-ttu-id="e2dc9-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2dc9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2dc9-133">-WhatIf</span></span>
<span data-ttu-id="e2dc9-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2dc9-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2dc9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2dc9-136">CommonParameters</span></span>
<span data-ttu-id="e2dc9-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2dc9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2dc9-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2dc9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2dc9-139">입력</span><span class="sxs-lookup"><span data-stu-id="e2dc9-139">INPUTS</span></span>

### <span data-ttu-id="e2dc9-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e2dc9-140">System.String</span></span>

## <span data-ttu-id="e2dc9-141">출력</span><span class="sxs-lookup"><span data-stu-id="e2dc9-141">OUTPUTS</span></span>

### <span data-ttu-id="e2dc9-142">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e2dc9-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e2dc9-143">상속자</span><span class="sxs-lookup"><span data-stu-id="e2dc9-143">NOTES</span></span>

## <span data-ttu-id="e2dc9-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2dc9-144">RELATED LINKS</span></span>

[<span data-ttu-id="e2dc9-145">추가-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2dc9-145">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e2dc9-146">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2dc9-146">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e2dc9-147">새로운 AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2dc9-147">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="e2dc9-148">제거-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e2dc9-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)


