---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: c7fdf250ad7c322e47c26e023f04689a12a8eee5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976672"
---
# <span data-ttu-id="1711e-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1711e-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="1711e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1711e-102">SYNOPSIS</span></span>
<span data-ttu-id="1711e-103">애플리케이션 게이트웨이에서 신뢰할 수 있는 클라이언트 CA 인증서 체인 개체를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1711e-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="1711e-104">구문</span><span class="sxs-lookup"><span data-stu-id="1711e-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1711e-105">설명</span><span class="sxs-lookup"><span data-stu-id="1711e-105">DESCRIPTION</span></span>
<span data-ttu-id="1711e-106">**Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet은 애플리케이션 게이트웨이에서 신뢰할 수 있는 클라이언트 CA 인증서 체인 개체를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1711e-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="1711e-107">예제</span><span class="sxs-lookup"><span data-stu-id="1711e-107">EXAMPLES</span></span>

### <span data-ttu-id="1711e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1711e-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="1711e-109">첫 번째 명령은 애플리케이션 게이트웨이를 얻게 하여 $gw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1711e-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="1711e-110">두 번째 명령은 에 저장된 애플리케이션 게이트웨이에서 "TrustedClientCertificate01"이라는 신뢰할 수 있는 클라이언트 CA 인증서 체인을 $gw.</span><span class="sxs-lookup"><span data-stu-id="1711e-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="1711e-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1711e-111">PARAMETERS</span></span>

### <span data-ttu-id="1711e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1711e-112">-ApplicationGateway</span></span>
<span data-ttu-id="1711e-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1711e-113">The applicationGateway</span></span>

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

### <span data-ttu-id="1711e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1711e-114">-DefaultProfile</span></span>
<span data-ttu-id="1711e-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1711e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1711e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1711e-116">-Name</span></span>
<span data-ttu-id="1711e-117">신뢰할 수 있는 클라이언트 CA 인증서 체인의 이름</span><span class="sxs-lookup"><span data-stu-id="1711e-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="1711e-118">-확인</span><span class="sxs-lookup"><span data-stu-id="1711e-118">-Confirm</span></span>
<span data-ttu-id="1711e-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1711e-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1711e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1711e-120">-WhatIf</span></span>
<span data-ttu-id="1711e-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1711e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1711e-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1711e-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1711e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1711e-123">CommonParameters</span></span>
<span data-ttu-id="1711e-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1711e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1711e-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1711e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1711e-126">입력</span><span class="sxs-lookup"><span data-stu-id="1711e-126">INPUTS</span></span>

### <span data-ttu-id="1711e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1711e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1711e-128">출력</span><span class="sxs-lookup"><span data-stu-id="1711e-128">OUTPUTS</span></span>

### <span data-ttu-id="1711e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1711e-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1711e-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1711e-130">NOTES</span></span>

## <span data-ttu-id="1711e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1711e-131">RELATED LINKS</span></span>

[<span data-ttu-id="1711e-132">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1711e-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1711e-133">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1711e-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1711e-134">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1711e-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1711e-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1711e-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)