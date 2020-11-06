---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 1ca390eb8c99ad991f5a15c6a3959d366ae5f983
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528501"
---
# <span data-ttu-id="01e1c-101">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="01e1c-101">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="01e1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="01e1c-103">응용 프로그램 게이트웨이에서 자동 크기 조정 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1c-103">Removes Autoscale Configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01e1c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01e1c-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01e1c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="01e1c-105">DESCRIPTION</span></span>
<span data-ttu-id="01e1c-106">**AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet은 기존 응용 프로그램 게이트웨이에서 자동 크기 조정 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1c-106">The **Remove-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="01e1c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="01e1c-107">EXAMPLES</span></span>

### <span data-ttu-id="01e1c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="01e1c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="01e1c-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $gw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1c-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="01e1c-110">두 번째 명령은 applicationg 게이트웨이에서 자동 크기 조정 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1c-110">The second command removes the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="01e1c-111">세 번째 명령은 Azure의 응용 프로그램 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1c-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="01e1c-112">변수</span><span class="sxs-lookup"><span data-stu-id="01e1c-112">PARAMETERS</span></span>

### <span data-ttu-id="01e1c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01e1c-113">-ApplicationGateway</span></span>
<span data-ttu-id="01e1c-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01e1c-114">The applicationGateway</span></span>

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

### <span data-ttu-id="01e1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e1c-115">-DefaultProfile</span></span>
<span data-ttu-id="01e1c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01e1c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01e1c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="01e1c-117">-Force</span></span>
<span data-ttu-id="01e1c-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01e1c-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="01e1c-119">-확인</span><span class="sxs-lookup"><span data-stu-id="01e1c-119">-Confirm</span></span>
<span data-ttu-id="01e1c-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01e1c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01e1c-121">-WhatIf</span></span>
<span data-ttu-id="01e1c-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="01e1c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01e1c-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01e1c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01e1c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e1c-124">CommonParameters</span></span>
<span data-ttu-id="01e1c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01e1c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e1c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01e1c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e1c-127">입력</span><span class="sxs-lookup"><span data-stu-id="01e1c-127">INPUTS</span></span>

### <span data-ttu-id="01e1c-128">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01e1c-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="01e1c-129">출력</span><span class="sxs-lookup"><span data-stu-id="01e1c-129">OUTPUTS</span></span>

### <span data-ttu-id="01e1c-130">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01e1c-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="01e1c-131">상속자</span><span class="sxs-lookup"><span data-stu-id="01e1c-131">NOTES</span></span>

## <span data-ttu-id="01e1c-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01e1c-132">RELATED LINKS</span></span>
