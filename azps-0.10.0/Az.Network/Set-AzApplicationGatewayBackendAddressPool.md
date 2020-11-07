---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: fd9d9c1b7956c16ab981b5426e9453de4d730dd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876616"
---
# <span data-ttu-id="1e571-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1e571-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="1e571-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e571-102">SYNOPSIS</span></span>
<span data-ttu-id="1e571-103">응용 프로그램 게이트웨이의 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="1e571-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e571-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e571-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1e571-105">DESCRIPTION</span></span>
<span data-ttu-id="1e571-106">**AzApplicationGatewayBackendAddressPool** Cmdlet은 Azure application gateway에 대 한 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="1e571-107">백 엔드 주소는 IP 주소, FQDN (정규화 된 도메인 이름) 또는 IP 구성 Id로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="1e571-108">예제의</span><span class="sxs-lookup"><span data-stu-id="1e571-108">EXAMPLES</span></span>

### <span data-ttu-id="1e571-109">예제 1: Fqdn을 사용 하 여 백 엔드 주소 풀 설정</span><span class="sxs-lookup"><span data-stu-id="1e571-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="1e571-110">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1e571-111">두 번째 명령은 Fqdn을 사용 하 여 $AppGw에서 응용 프로그램 게이트웨이의 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="1e571-112">예제 2: 백엔드 서버 IP 주소를 사용 하 여 백 엔드 주소 풀 설정</span><span class="sxs-lookup"><span data-stu-id="1e571-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="1e571-113">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1e571-114">두 번째 명령은 IP 주소를 사용 하 여 $AppGw에서 응용 프로그램 게이트웨이의 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="1e571-115">예제 3: 백엔드 서버의 ID를 사용 하 여 백 엔드 주소 풀 설정 IP 주소</span><span class="sxs-lookup"><span data-stu-id="1e571-115">Example 3: Setting a back-end address pool by using the ID of the backend server?s IP address</span></span>
```
PS C:\> $Nic01 = Get-AzNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="1e571-116">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 Nic01 라는 네트워크 인터페이스 개체를 가져와 $Nic 01 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-116">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.</span></span>

<span data-ttu-id="1e571-117">두 번째 명령은 ResourceGroup02 이라는 리소스 그룹에 속하는 Nic02 라는 네트워크 인터페이스 개체를 가져와 $Nic 02 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-117">The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.</span></span>

<span data-ttu-id="1e571-118">세 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-118">The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1e571-119">위의 명령은 $Nic 01 및 $Nic 02의 백 엔드 IP 구성 Id를 사용 하 여 $AppGw에서 응용 프로그램 게이트웨이의 백 엔드 주소 풀을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-119">The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to update the back-end address pool of the application gateway in $AppGw.</span></span>

## <span data-ttu-id="1e571-120">변수</span><span class="sxs-lookup"><span data-stu-id="1e571-120">PARAMETERS</span></span>

### <span data-ttu-id="1e571-121">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e571-121">-ApplicationGateway</span></span>
<span data-ttu-id="1e571-122">이 cmdlet이 백 엔드 주소 풀을 연결 하는 데 사용할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-122">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="1e571-123">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="1e571-123">-BackendFqdns</span></span>
<span data-ttu-id="1e571-124">백 엔드 서버 풀로 사용할 백 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-124">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="1e571-125">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="1e571-125">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="1e571-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e571-126">-DefaultProfile</span></span>
<span data-ttu-id="1e571-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e571-128">-이름</span><span class="sxs-lookup"><span data-stu-id="1e571-128">-Name</span></span>
<span data-ttu-id="1e571-129">백 엔드 주소 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-129">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="1e571-130">이 백 엔드 주소 풀은 응용 프로그램 게이트웨이에서 존재 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-130">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="1e571-131">-확인</span><span class="sxs-lookup"><span data-stu-id="1e571-131">-Confirm</span></span>
<span data-ttu-id="1e571-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e571-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e571-133">-WhatIf</span></span>
<span data-ttu-id="1e571-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e571-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e571-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e571-136">CommonParameters</span></span>
<span data-ttu-id="1e571-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e571-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e571-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e571-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e571-139">입력</span><span class="sxs-lookup"><span data-stu-id="1e571-139">INPUTS</span></span>

### <span data-ttu-id="1e571-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1e571-140">System.String</span></span>

## <span data-ttu-id="1e571-141">출력</span><span class="sxs-lookup"><span data-stu-id="1e571-141">OUTPUTS</span></span>

### <span data-ttu-id="1e571-142">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e571-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1e571-143">상속자</span><span class="sxs-lookup"><span data-stu-id="1e571-143">NOTES</span></span>

## <span data-ttu-id="1e571-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e571-144">RELATED LINKS</span></span>

[<span data-ttu-id="1e571-145">추가-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1e571-145">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="1e571-146">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1e571-146">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="1e571-147">새로운 AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1e571-147">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="1e571-148">제거-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1e571-148">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


