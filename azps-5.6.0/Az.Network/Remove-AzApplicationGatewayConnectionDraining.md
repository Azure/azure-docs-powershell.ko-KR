---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: ddcec36e8561196b31dd94eb15d99a7e2a92a378
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964080"
---
# <span data-ttu-id="ec700-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ec700-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="ec700-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec700-102">SYNOPSIS</span></span>
<span data-ttu-id="ec700-103">백 엔드 HTTP 설정 개체의 연결 드레인 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ec700-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="ec700-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec700-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec700-105">설명</span><span class="sxs-lookup"><span data-stu-id="ec700-105">DESCRIPTION</span></span>
<span data-ttu-id="ec700-106">**Remove-AzApplicationGatewayConnectionDraining** cmdlet은 백 엔드 HTTP 설정 개체의 연결 드레인 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ec700-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="ec700-107">예제</span><span class="sxs-lookup"><span data-stu-id="ec700-107">EXAMPLES</span></span>

### <span data-ttu-id="ec700-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec700-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="ec700-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ec700-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ec700-110">두 번째 명령은 $AppGw 설정이라는 백 엔드 HTTP 설정을 $Settings 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ec700-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="ec700-111">마지막 명령은 에 저장된 백 엔드 HTTP 설정의 연결 드레인 구성을 $Settings.</span><span class="sxs-lookup"><span data-stu-id="ec700-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="ec700-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ec700-112">PARAMETERS</span></span>

### <span data-ttu-id="ec700-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ec700-113">-BackendHttpSettings</span></span>
<span data-ttu-id="ec700-114">백end http 설정</span><span class="sxs-lookup"><span data-stu-id="ec700-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec700-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec700-115">-DefaultProfile</span></span>
<span data-ttu-id="ec700-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec700-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec700-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec700-117">CommonParameters</span></span>
<span data-ttu-id="ec700-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec700-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec700-119">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ec700-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec700-120">입력</span><span class="sxs-lookup"><span data-stu-id="ec700-120">INPUTS</span></span>

### <span data-ttu-id="ec700-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ec700-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="ec700-122">출력</span><span class="sxs-lookup"><span data-stu-id="ec700-122">OUTPUTS</span></span>

### <span data-ttu-id="ec700-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ec700-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="ec700-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec700-124">NOTES</span></span>

## <span data-ttu-id="ec700-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec700-125">RELATED LINKS</span></span>

[<span data-ttu-id="ec700-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec700-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="ec700-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ec700-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="ec700-128">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ec700-128">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="ec700-129">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ec700-129">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="ec700-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="ec700-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

