---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 81928913565c6e95f3768ccd5c05e8baa2c14b74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537839"
---
# <span data-ttu-id="95c93-101">Remove-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="95c93-101">Remove-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="95c93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95c93-102">SYNOPSIS</span></span>
<span data-ttu-id="95c93-103">Azure application gateway에서 SSL 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="95c93-103">Removes an SSL policy from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95c93-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95c93-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95c93-105">설명은</span><span class="sxs-lookup"><span data-stu-id="95c93-105">DESCRIPTION</span></span>
<span data-ttu-id="95c93-106">Remove-AzureRmApplicationGatewaySslPolicy cmdlet은 Azure 응용 프로그램 게이트웨이에서 SSL 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="95c93-106">The Remove-AzureRmApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="95c93-107">예제의</span><span class="sxs-lookup"><span data-stu-id="95c93-107">EXAMPLES</span></span>

### <span data-ttu-id="95c93-108">예제 1: 응용 프로그램 게이트웨이에서 SSL 정책 제거</span><span class="sxs-lookup"><span data-stu-id="95c93-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="95c93-109">이 명령은 ApplicationGateway01 이라는 응용 프로그램 게이트웨이에서 SSL 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="95c93-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="95c93-110">변수</span><span class="sxs-lookup"><span data-stu-id="95c93-110">PARAMETERS</span></span>

### <span data-ttu-id="95c93-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95c93-111">-ApplicationGateway</span></span>
<span data-ttu-id="95c93-112">이 cmdlet이 SSL 정책을 제거 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95c93-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="95c93-113">-Force</span><span class="sxs-lookup"><span data-stu-id="95c93-113">-Force</span></span>
<span data-ttu-id="95c93-114">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95c93-114">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95c93-115">-확인</span><span class="sxs-lookup"><span data-stu-id="95c93-115">-Confirm</span></span>
<span data-ttu-id="95c93-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95c93-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95c93-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95c93-117">-WhatIf</span></span>
<span data-ttu-id="95c93-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="95c93-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95c93-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95c93-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95c93-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95c93-120">-DefaultProfile</span></span>
<span data-ttu-id="95c93-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95c93-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95c93-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95c93-122">CommonParameters</span></span>
<span data-ttu-id="95c93-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95c93-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95c93-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95c93-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95c93-125">입력</span><span class="sxs-lookup"><span data-stu-id="95c93-125">INPUTS</span></span>

### <span data-ttu-id="95c93-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="95c93-126">System.String</span></span>

## <span data-ttu-id="95c93-127">출력</span><span class="sxs-lookup"><span data-stu-id="95c93-127">OUTPUTS</span></span>

### <span data-ttu-id="95c93-128">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="95c93-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="95c93-129">상속자</span><span class="sxs-lookup"><span data-stu-id="95c93-129">NOTES</span></span>
<span data-ttu-id="95c93-130">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="95c93-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="95c93-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95c93-131">RELATED LINKS</span></span>

[<span data-ttu-id="95c93-132">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="95c93-132">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="95c93-133">새로운 AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="95c93-133">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="95c93-134">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="95c93-134">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

