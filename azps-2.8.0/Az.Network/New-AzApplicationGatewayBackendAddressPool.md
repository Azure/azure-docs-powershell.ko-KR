---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 1165d7abccdbf21dc94e4f39b8b2dad953fdba07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870017"
---
# <span data-ttu-id="c5798-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c5798-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="c5798-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5798-102">SYNOPSIS</span></span>
<span data-ttu-id="c5798-103">응용 프로그램 게이트웨이에 사용할 백 엔드 주소 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c5798-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="c5798-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c5798-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String> [-BackendIPAddresses <String[]>]
 [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5798-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c5798-105">DESCRIPTION</span></span>
<span data-ttu-id="c5798-106">**AzApplicationGatewayBackendAddressPool** Cmdlet은 Azure application gateway에 대 한 백 엔드 주소 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c5798-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="c5798-107">백 엔드 주소는 IP 주소, FQDN (정규화 된 도메인 이름) 또는 IP 구성 ID로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5798-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="c5798-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c5798-108">EXAMPLES</span></span>

### <span data-ttu-id="c5798-109">예제 1: 백 엔드 서버의 FQDN을 사용 하 여 백 엔드 주소 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="c5798-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="c5798-110">이 명령은 백 엔드 서버의 Fqdn을 사용 하 여 Pool01 라는 백 엔드 주소 풀을 만들고이를 $Pool 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5798-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="c5798-111">예제 2: 백 엔드 서버의 IP 주소를 사용 하 여 백 엔드 주소 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="c5798-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="c5798-112">이 명령은 백 엔드 서버의 IP 주소를 사용 하 여 Pool02 라는 백 엔드 주소 풀을 만들고이를 $Pool 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5798-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="c5798-113">변수</span><span class="sxs-lookup"><span data-stu-id="c5798-113">PARAMETERS</span></span>

### <span data-ttu-id="c5798-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="c5798-114">-BackendFqdns</span></span>
<span data-ttu-id="c5798-115">이 cmdlet이 백 엔드 서버 풀과 연결 하는 백 엔드 Fqdn의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5798-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="c5798-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="c5798-116">-BackendIPAddresses</span></span>
<span data-ttu-id="c5798-117">이 cmdlet이 백 엔드 서버 풀과 연결 하는 백 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5798-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="c5798-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5798-118">-DefaultProfile</span></span>
<span data-ttu-id="c5798-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5798-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5798-120">-이름</span><span class="sxs-lookup"><span data-stu-id="c5798-120">-Name</span></span>
<span data-ttu-id="c5798-121">이 cmdlet이 만드는 백 엔드 서버 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5798-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c5798-122">-확인</span><span class="sxs-lookup"><span data-stu-id="c5798-122">-Confirm</span></span>
<span data-ttu-id="c5798-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5798-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5798-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5798-124">-WhatIf</span></span>
<span data-ttu-id="c5798-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c5798-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5798-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5798-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5798-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5798-127">CommonParameters</span></span>
<span data-ttu-id="c5798-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5798-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5798-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5798-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5798-130">입력</span><span class="sxs-lookup"><span data-stu-id="c5798-130">INPUTS</span></span>

### <span data-ttu-id="c5798-131">않아야</span><span class="sxs-lookup"><span data-stu-id="c5798-131">None</span></span>

## <span data-ttu-id="c5798-132">출력</span><span class="sxs-lookup"><span data-stu-id="c5798-132">OUTPUTS</span></span>

### <span data-ttu-id="c5798-133">PSApplicationGatewayBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c5798-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="c5798-134">상속자</span><span class="sxs-lookup"><span data-stu-id="c5798-134">NOTES</span></span>

## <span data-ttu-id="c5798-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5798-135">RELATED LINKS</span></span>

[<span data-ttu-id="c5798-136">추가-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c5798-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c5798-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c5798-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c5798-138">제거-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c5798-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c5798-139">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c5798-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


