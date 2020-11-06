---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 2d7fa9dd9030f1e5878293276a248c2f6718efe5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531979"
---
# <span data-ttu-id="fb3c0-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb3c0-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="fb3c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb3c0-102">SYNOPSIS</span></span>
<span data-ttu-id="fb3c0-103">Application gateway의 자동 크기 조정 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb3c0-103">Updates Autoscale Configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb3c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb3c0-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 -MinCapacity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb3c0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fb3c0-105">DESCRIPTION</span></span>
<span data-ttu-id="fb3c0-106">**AzureRmApplicationGatewayAutoscaleConfiguration** Cmdlet은 응용 프로그램 게이트웨이의 기존 자동 크기 조정 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb3c0-106">The **Set-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="fb3c0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fb3c0-107">EXAMPLES</span></span>

### <span data-ttu-id="fb3c0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fb3c0-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="fb3c0-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $gw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb3c0-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="fb3c0-110">두 번째 명령은 applicationg 게이트웨이에서 자동 크기 조정 구성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb3c0-110">The second command updates the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="fb3c0-111">세 번째 명령은 Azure의 응용 프로그램 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb3c0-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="fb3c0-112">변수</span><span class="sxs-lookup"><span data-stu-id="fb3c0-112">PARAMETERS</span></span>

### <span data-ttu-id="fb3c0-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb3c0-113">-ApplicationGateway</span></span>
<span data-ttu-id="fb3c0-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb3c0-114">The applicationGateway</span></span>

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

### <span data-ttu-id="fb3c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb3c0-115">-DefaultProfile</span></span>
<span data-ttu-id="fb3c0-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb3c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb3c0-117">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="fb3c0-117">-MinCapacity</span></span>
<span data-ttu-id="fb3c0-118">Application gateway에 대 한 최소 capcity.</span><span class="sxs-lookup"><span data-stu-id="fb3c0-118">Minimum capcity for application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb3c0-119">-확인</span><span class="sxs-lookup"><span data-stu-id="fb3c0-119">-Confirm</span></span>
<span data-ttu-id="fb3c0-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb3c0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb3c0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb3c0-121">-WhatIf</span></span>
<span data-ttu-id="fb3c0-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fb3c0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb3c0-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb3c0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb3c0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb3c0-124">CommonParameters</span></span>
<span data-ttu-id="fb3c0-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb3c0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb3c0-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb3c0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb3c0-127">입력</span><span class="sxs-lookup"><span data-stu-id="fb3c0-127">INPUTS</span></span>

### <span data-ttu-id="fb3c0-128">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb3c0-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fb3c0-129">출력</span><span class="sxs-lookup"><span data-stu-id="fb3c0-129">OUTPUTS</span></span>

### <span data-ttu-id="fb3c0-130">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb3c0-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fb3c0-131">상속자</span><span class="sxs-lookup"><span data-stu-id="fb3c0-131">NOTES</span></span>

## <span data-ttu-id="fb3c0-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb3c0-132">RELATED LINKS</span></span>
