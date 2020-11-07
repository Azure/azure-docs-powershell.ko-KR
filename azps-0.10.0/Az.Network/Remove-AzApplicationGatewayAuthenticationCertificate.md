---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: bf11b2b3010a7f7683d670c3c5e95d4248b83cd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875379"
---
# <span data-ttu-id="9b556-101">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9b556-101">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="9b556-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b556-102">SYNOPSIS</span></span>
<span data-ttu-id="9b556-103">응용 프로그램 게이트웨이에서 인증 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b556-103">Removes an authentication certificate from an application gateway.</span></span>

## <span data-ttu-id="9b556-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b556-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b556-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9b556-105">DESCRIPTION</span></span>
<span data-ttu-id="9b556-106">**AzApplicationGatewayAuthenticationCertificate** Cmdlet은 Azure application gateway에서 인증 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b556-106">The **Remove-AzApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="9b556-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9b556-107">EXAMPLES</span></span>

### <span data-ttu-id="9b556-108">raid-1</span><span class="sxs-lookup"><span data-stu-id="9b556-108">1:</span></span>
```

```

## <span data-ttu-id="9b556-109">변수</span><span class="sxs-lookup"><span data-stu-id="9b556-109">PARAMETERS</span></span>

### <span data-ttu-id="9b556-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b556-110">-ApplicationGateway</span></span>
<span data-ttu-id="9b556-111">이 cmdlet에서 인증 인증서를 제거 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b556-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="9b556-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b556-112">-DefaultProfile</span></span>
<span data-ttu-id="9b556-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b556-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b556-114">-이름</span><span class="sxs-lookup"><span data-stu-id="9b556-114">-Name</span></span>
<span data-ttu-id="9b556-115">이 cmdlet이 제거 하는 인증 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b556-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9b556-116">-확인</span><span class="sxs-lookup"><span data-stu-id="9b556-116">-Confirm</span></span>
<span data-ttu-id="9b556-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b556-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b556-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b556-118">-WhatIf</span></span>
<span data-ttu-id="9b556-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9b556-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b556-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b556-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b556-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b556-121">CommonParameters</span></span>
<span data-ttu-id="9b556-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b556-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b556-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b556-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b556-124">입력</span><span class="sxs-lookup"><span data-stu-id="9b556-124">INPUTS</span></span>

### <span data-ttu-id="9b556-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9b556-125">System.String</span></span>

## <span data-ttu-id="9b556-126">출력</span><span class="sxs-lookup"><span data-stu-id="9b556-126">OUTPUTS</span></span>

### <span data-ttu-id="9b556-127">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b556-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9b556-128">상속자</span><span class="sxs-lookup"><span data-stu-id="9b556-128">NOTES</span></span>
* <span data-ttu-id="9b556-129">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="9b556-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="9b556-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b556-130">RELATED LINKS</span></span>

[<span data-ttu-id="9b556-131">추가-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9b556-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9b556-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9b556-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9b556-133">새로운 AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9b556-133">New-AzApplicationGatewayAuthenticationCertificate</span></span>](./New-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="9b556-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="9b556-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


