---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: dcce5b85fc9d3e8046ecc90330da5f3d40b88e33
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881394"
---
# <span data-ttu-id="30c97-101">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="30c97-101">New-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="30c97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30c97-102">SYNOPSIS</span></span>
<span data-ttu-id="30c97-103">응용 프로그램 게이트웨이에 사용할 백 엔드 주소 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30c97-103">Creates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30c97-104">구문과</span><span class="sxs-lookup"><span data-stu-id="30c97-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30c97-105">설명은</span><span class="sxs-lookup"><span data-stu-id="30c97-105">DESCRIPTION</span></span>
<span data-ttu-id="30c97-106">**AzureRmApplicationGatewayBackendAddressPool** Cmdlet은 Azure application gateway에 대 한 백 엔드 주소 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="30c97-106">The **New-AzureRmApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="30c97-107">백 엔드 주소는 IP 주소, FQDN (정규화 된 도메인 이름) 또는 IP 구성 ID로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="30c97-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="30c97-108">예제의</span><span class="sxs-lookup"><span data-stu-id="30c97-108">EXAMPLES</span></span>

### <span data-ttu-id="30c97-109">예제 1: 백 엔드 서버의 FQDN을 사용 하 여 백 엔드 주소 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="30c97-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="30c97-110">이 명령은 백 엔드 서버의 Fqdn을 사용 하 여 Pool01 라는 백 엔드 주소 풀을 만들고이를 $Pool 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="30c97-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="30c97-111">예제 2: 백 엔드 서버의 IP 주소를 사용 하 여 백 엔드 주소 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="30c97-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="30c97-112">이 명령은 백 엔드 서버의 IP 주소를 사용 하 여 Pool02 라는 백 엔드 주소 풀을 만들고이를 $Pool 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="30c97-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="30c97-113">변수</span><span class="sxs-lookup"><span data-stu-id="30c97-113">PARAMETERS</span></span>

### <span data-ttu-id="30c97-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="30c97-114">-BackendFqdns</span></span>
<span data-ttu-id="30c97-115">이 cmdlet이 백 엔드 서버 풀과 연결 하는 백 엔드 Fqdn의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30c97-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="30c97-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="30c97-116">-BackendIPAddresses</span></span>
<span data-ttu-id="30c97-117">이 cmdlet이 백 엔드 서버 풀과 연결 하는 백 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30c97-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="30c97-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c97-118">-DefaultProfile</span></span>
<span data-ttu-id="30c97-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30c97-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30c97-120">-이름</span><span class="sxs-lookup"><span data-stu-id="30c97-120">-Name</span></span>
<span data-ttu-id="30c97-121">이 cmdlet이 만드는 백 엔드 서버 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="30c97-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="30c97-122">-확인</span><span class="sxs-lookup"><span data-stu-id="30c97-122">-Confirm</span></span>
<span data-ttu-id="30c97-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="30c97-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30c97-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30c97-124">-WhatIf</span></span>
<span data-ttu-id="30c97-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="30c97-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30c97-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30c97-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30c97-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c97-127">CommonParameters</span></span>
<span data-ttu-id="30c97-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="30c97-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c97-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30c97-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c97-130">입력</span><span class="sxs-lookup"><span data-stu-id="30c97-130">INPUTS</span></span>

### <span data-ttu-id="30c97-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="30c97-131">System.String</span></span>

## <span data-ttu-id="30c97-132">출력</span><span class="sxs-lookup"><span data-stu-id="30c97-132">OUTPUTS</span></span>

### <span data-ttu-id="30c97-133">PSApplicationGatewayBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="30c97-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="30c97-134">상속자</span><span class="sxs-lookup"><span data-stu-id="30c97-134">NOTES</span></span>

## <span data-ttu-id="30c97-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30c97-135">RELATED LINKS</span></span>

[<span data-ttu-id="30c97-136">추가-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="30c97-136">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="30c97-137">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="30c97-137">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="30c97-138">제거-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="30c97-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="30c97-139">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="30c97-139">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


