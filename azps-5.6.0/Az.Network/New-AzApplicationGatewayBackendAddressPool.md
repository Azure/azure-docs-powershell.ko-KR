---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 3ce9cb761bb945c777a39e728ac8ebea2c40b885
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010352"
---
# <span data-ttu-id="79303-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="79303-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="79303-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79303-102">SYNOPSIS</span></span>
<span data-ttu-id="79303-103">애플리케이션 게이트웨이에 대한 백 엔드 주소 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79303-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="79303-104">구문</span><span class="sxs-lookup"><span data-stu-id="79303-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String> [-BackendIPAddresses <String[]>]
 [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79303-105">설명</span><span class="sxs-lookup"><span data-stu-id="79303-105">DESCRIPTION</span></span>
<span data-ttu-id="79303-106">**New-AzApplicationGatewayBackendAddressPool** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 백 엔드 주소 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79303-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="79303-107">백 엔드 주소를 IP 주소, FQDN(정식 도메인 이름) 또는 IP 구성 ID로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79303-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="79303-108">예제</span><span class="sxs-lookup"><span data-stu-id="79303-108">EXAMPLES</span></span>

### <span data-ttu-id="79303-109">예제 1: 백 엔드 서버의 FQDN을 사용하여 백 엔드 주소 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="79303-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="79303-110">이 명령은 백 엔드 서버의 FQDNS를 사용하여 Pool01이라는 백 엔드 주소 풀을 만들고, 해당 주소를 $Pool 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="79303-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="79303-111">예제 2: 백 엔드 서버의 IP 주소를 사용하여 백 엔드 주소 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="79303-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="79303-112">이 명령은 백 엔드 서버의 IP 주소를 사용하여 Pool02라는 백 엔드 주소 풀을 만들고, 해당 주소를 $Pool 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="79303-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="79303-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="79303-113">PARAMETERS</span></span>

### <span data-ttu-id="79303-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="79303-114">-BackendFqdns</span></span>
<span data-ttu-id="79303-115">이 cmdlet이 백 엔드 서버 풀과 연결되는 백 엔드 FQDNS 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="79303-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="79303-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="79303-116">-BackendIPAddresses</span></span>
<span data-ttu-id="79303-117">이 cmdlet이 백 엔드 서버 풀과 연결되는 백 엔드 IP 주소 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="79303-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="79303-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79303-118">-DefaultProfile</span></span>
<span data-ttu-id="79303-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79303-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79303-120">-Name</span><span class="sxs-lookup"><span data-stu-id="79303-120">-Name</span></span>
<span data-ttu-id="79303-121">이 cmdlet이 만드는 백 엔드 서버 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="79303-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="79303-122">-확인</span><span class="sxs-lookup"><span data-stu-id="79303-122">-Confirm</span></span>
<span data-ttu-id="79303-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="79303-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79303-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79303-124">-WhatIf</span></span>
<span data-ttu-id="79303-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="79303-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79303-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79303-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79303-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79303-127">CommonParameters</span></span>
<span data-ttu-id="79303-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="79303-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79303-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="79303-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79303-130">입력</span><span class="sxs-lookup"><span data-stu-id="79303-130">INPUTS</span></span>

### <span data-ttu-id="79303-131">없음</span><span class="sxs-lookup"><span data-stu-id="79303-131">None</span></span>

## <span data-ttu-id="79303-132">출력</span><span class="sxs-lookup"><span data-stu-id="79303-132">OUTPUTS</span></span>

### <span data-ttu-id="79303-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="79303-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="79303-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="79303-134">NOTES</span></span>

## <span data-ttu-id="79303-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79303-135">RELATED LINKS</span></span>

[<span data-ttu-id="79303-136">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="79303-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="79303-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="79303-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="79303-138">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="79303-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="79303-139">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="79303-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


