---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 3facee36f6862c02975566dee20d9e7fb8c8824f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527403"
---
# <span data-ttu-id="ea610-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ea610-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="ea610-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea610-102">SYNOPSIS</span></span>
<span data-ttu-id="ea610-103">응용 프로그램 게이트웨이에서 인증 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea610-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea610-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea610-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea610-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ea610-105">DESCRIPTION</span></span>
<span data-ttu-id="ea610-106">**AzureRmApplicationGatewayAuthenticationCertificate** Cmdlet은 Azure application gateway에서 인증 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea610-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="ea610-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ea610-107">EXAMPLES</span></span>

## <span data-ttu-id="ea610-108">변수</span><span class="sxs-lookup"><span data-stu-id="ea610-108">PARAMETERS</span></span>

### <span data-ttu-id="ea610-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ea610-109">-ApplicationGateway</span></span>
<span data-ttu-id="ea610-110">이 cmdlet에서 인증 인증서를 제거 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea610-110">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="ea610-111">-이름</span><span class="sxs-lookup"><span data-stu-id="ea610-111">-Name</span></span>
<span data-ttu-id="ea610-112">이 cmdlet이 제거 하는 인증 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea610-112">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ea610-113">-확인</span><span class="sxs-lookup"><span data-stu-id="ea610-113">-Confirm</span></span>
<span data-ttu-id="ea610-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea610-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea610-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea610-115">-WhatIf</span></span>
<span data-ttu-id="ea610-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea610-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea610-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea610-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea610-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea610-118">-DefaultProfile</span></span>
<span data-ttu-id="ea610-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea610-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea610-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea610-120">CommonParameters</span></span>
<span data-ttu-id="ea610-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea610-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea610-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea610-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea610-123">입력</span><span class="sxs-lookup"><span data-stu-id="ea610-123">INPUTS</span></span>

### <span data-ttu-id="ea610-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ea610-124">System.String</span></span>

## <span data-ttu-id="ea610-125">출력</span><span class="sxs-lookup"><span data-stu-id="ea610-125">OUTPUTS</span></span>

### <span data-ttu-id="ea610-126">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ea610-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ea610-127">상속자</span><span class="sxs-lookup"><span data-stu-id="ea610-127">NOTES</span></span>
* <span data-ttu-id="ea610-128">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="ea610-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ea610-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea610-129">RELATED LINKS</span></span>

[<span data-ttu-id="ea610-130">추가-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ea610-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ea610-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ea610-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ea610-132">새로운 AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ea610-132">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="ea610-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="ea610-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


