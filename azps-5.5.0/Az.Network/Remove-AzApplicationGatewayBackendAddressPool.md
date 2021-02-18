---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 1ce5989516286d366e6363cbeeee8ebddc93edfc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206653"
---
# <span data-ttu-id="12c05-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="12c05-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="12c05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12c05-102">SYNOPSIS</span></span>
<span data-ttu-id="12c05-103">애플리케이션 게이트웨이에서 백 엔드 주소 풀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="12c05-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="12c05-104">구문</span><span class="sxs-lookup"><span data-stu-id="12c05-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12c05-105">설명</span><span class="sxs-lookup"><span data-stu-id="12c05-105">DESCRIPTION</span></span>
<span data-ttu-id="12c05-106">**Remove-AzApplicationGatewayBackendAddressPool** cmdlet은 Azure 애플리케이션 게이트웨이에서 백 엔드 주소 풀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="12c05-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="12c05-107">예제</span><span class="sxs-lookup"><span data-stu-id="12c05-107">EXAMPLES</span></span>

### <span data-ttu-id="12c05-108">예제 1: 애플리케이션 게이트웨이에서 백 엔드 주소 풀 제거</span><span class="sxs-lookup"><span data-stu-id="12c05-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="12c05-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="12c05-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="12c05-110">두 번째 명령은 애플리케이션 게이트웨이에서 BackEndPool02라는 백 엔드 주소 풀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="12c05-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="12c05-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12c05-111">PARAMETERS</span></span>

### <span data-ttu-id="12c05-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12c05-112">-ApplicationGateway</span></span>
<span data-ttu-id="12c05-113">이 cmdlet이 백 엔드 주소 풀을 제거하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="12c05-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="12c05-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12c05-114">-DefaultProfile</span></span>
<span data-ttu-id="12c05-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="12c05-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12c05-116">-Name</span><span class="sxs-lookup"><span data-stu-id="12c05-116">-Name</span></span>
<span data-ttu-id="12c05-117">이 cmdlet에서 제거하는 백 엔드 주소 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="12c05-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="12c05-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12c05-118">-Confirm</span></span>
<span data-ttu-id="12c05-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="12c05-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12c05-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12c05-120">-WhatIf</span></span>
<span data-ttu-id="12c05-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="12c05-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12c05-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="12c05-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12c05-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c05-123">CommonParameters</span></span>
<span data-ttu-id="12c05-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="12c05-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12c05-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="12c05-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c05-126">입력</span><span class="sxs-lookup"><span data-stu-id="12c05-126">INPUTS</span></span>

### <span data-ttu-id="12c05-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12c05-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="12c05-128">출력</span><span class="sxs-lookup"><span data-stu-id="12c05-128">OUTPUTS</span></span>

### <span data-ttu-id="12c05-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="12c05-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="12c05-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="12c05-130">NOTES</span></span>

## <span data-ttu-id="12c05-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12c05-131">RELATED LINKS</span></span>

[<span data-ttu-id="12c05-132">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="12c05-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="12c05-133">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="12c05-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="12c05-134">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="12c05-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="12c05-135">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="12c05-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


