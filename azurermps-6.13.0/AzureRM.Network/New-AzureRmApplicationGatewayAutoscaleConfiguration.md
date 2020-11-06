---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: f19a2e9f1531f6e009561a9d45ecae07d1bb0a3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534251"
---
# <span data-ttu-id="11485-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="11485-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="11485-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11485-102">SYNOPSIS</span></span>
<span data-ttu-id="11485-103">Application Gateway에 대 한 자동 크기 조정 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11485-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11485-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11485-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11485-105">설명은</span><span class="sxs-lookup"><span data-stu-id="11485-105">DESCRIPTION</span></span>
<span data-ttu-id="11485-106">**AzureRmApplicationGatewayAutoscaleConfiguration** Cmdlet은 Azure application gateway에 대 한 자동 크기 조정 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11485-106">The **New-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="11485-107">예제의</span><span class="sxs-lookup"><span data-stu-id="11485-107">EXAMPLES</span></span>

### <span data-ttu-id="11485-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="11485-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="11485-109">첫 번째 명령은 최소 용량 3으로 자동 크기 조정 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11485-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="11485-110">두 번째 명령은 자동 크기 조정 구성을 사용 하 여 응용 프로그램 게이트웨이를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11485-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="11485-111">변수</span><span class="sxs-lookup"><span data-stu-id="11485-111">PARAMETERS</span></span>

### <span data-ttu-id="11485-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11485-112">-DefaultProfile</span></span>
<span data-ttu-id="11485-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11485-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11485-114">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="11485-114">-MinCapacity</span></span>
<span data-ttu-id="11485-115">항상 응용 프로그램 게이트웨이에 대해 사용할 수 있는 최소 용량 단위 이며, 충전 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11485-115">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="11485-116">-확인</span><span class="sxs-lookup"><span data-stu-id="11485-116">-Confirm</span></span>
<span data-ttu-id="11485-117">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11485-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11485-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11485-118">-WhatIf</span></span>
<span data-ttu-id="11485-119">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="11485-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11485-120">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11485-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11485-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11485-121">CommonParameters</span></span>
<span data-ttu-id="11485-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11485-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11485-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11485-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11485-124">입력</span><span class="sxs-lookup"><span data-stu-id="11485-124">INPUTS</span></span>

### <span data-ttu-id="11485-125">않아야</span><span class="sxs-lookup"><span data-stu-id="11485-125">None</span></span>

## <span data-ttu-id="11485-126">출력</span><span class="sxs-lookup"><span data-stu-id="11485-126">OUTPUTS</span></span>

### <span data-ttu-id="11485-127">PSApplicationGatewayAutoscaleConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="11485-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="11485-128">상속자</span><span class="sxs-lookup"><span data-stu-id="11485-128">NOTES</span></span>

## <span data-ttu-id="11485-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11485-129">RELATED LINKS</span></span>
