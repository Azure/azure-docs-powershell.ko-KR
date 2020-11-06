---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 5655272afa9ddc9c0ff4c1873a0fac7a0e1f50dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527404"
---
# <span data-ttu-id="1e8c1-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1e8c1-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="1e8c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e8c1-102">SYNOPSIS</span></span>
<span data-ttu-id="1e8c1-103">응용 프로그램 게이트웨이에서 백 엔드 주소 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-103">Removes a back-end address pool from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e8c1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e8c1-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e8c1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1e8c1-105">DESCRIPTION</span></span>
<span data-ttu-id="1e8c1-106">**AzureRmApplicationGatewayBackendAddressPool** Cmdlet은 Azure application gateway에서 백 엔드 주소 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-106">The **Remove-AzureRmApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="1e8c1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1e8c1-107">EXAMPLES</span></span>

### <span data-ttu-id="1e8c1-108">예제 1: 응용 프로그램 게이트웨이에서 백 엔드 주소 풀 제거</span><span class="sxs-lookup"><span data-stu-id="1e8c1-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="1e8c1-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>

<span data-ttu-id="1e8c1-110">두 번째 명령은 응용 프로그램 게이트웨이에서 BackEndPool02 이라는 백 엔드 주소 풀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="1e8c1-111">변수</span><span class="sxs-lookup"><span data-stu-id="1e8c1-111">PARAMETERS</span></span>

### <span data-ttu-id="1e8c1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1e8c1-112">-ApplicationGateway</span></span>
<span data-ttu-id="1e8c1-113">이 cmdlet이 백 엔드 주소 풀을 제거 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="1e8c1-114">-이름</span><span class="sxs-lookup"><span data-stu-id="1e8c1-114">-Name</span></span>
<span data-ttu-id="1e8c1-115">이 cmdlet이 제거 하는 백 엔드 주소 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-115">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1e8c1-116">-확인</span><span class="sxs-lookup"><span data-stu-id="1e8c1-116">-Confirm</span></span>
<span data-ttu-id="1e8c1-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e8c1-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e8c1-118">-WhatIf</span></span>
<span data-ttu-id="1e8c1-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e8c1-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e8c1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e8c1-121">-DefaultProfile</span></span>
<span data-ttu-id="1e8c1-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e8c1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e8c1-123">CommonParameters</span></span>
<span data-ttu-id="1e8c1-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e8c1-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e8c1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e8c1-126">입력</span><span class="sxs-lookup"><span data-stu-id="1e8c1-126">INPUTS</span></span>

### <span data-ttu-id="1e8c1-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1e8c1-127">System.String</span></span>

## <span data-ttu-id="1e8c1-128">출력</span><span class="sxs-lookup"><span data-stu-id="1e8c1-128">OUTPUTS</span></span>

### <span data-ttu-id="1e8c1-129">PSApplicationGatewayBackendAddressPool에 대 한.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="1e8c1-130">상속자</span><span class="sxs-lookup"><span data-stu-id="1e8c1-130">NOTES</span></span>

## <span data-ttu-id="1e8c1-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e8c1-131">RELATED LINKS</span></span>

[<span data-ttu-id="1e8c1-132">추가-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1e8c1-132">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="1e8c1-133">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1e8c1-133">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="1e8c1-134">새로운 AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1e8c1-134">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="1e8c1-135">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1e8c1-135">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)

