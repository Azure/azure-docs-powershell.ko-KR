---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 9db92f11a7401eec1643156490079da8ff2b00d6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378820"
---
# <span data-ttu-id="4a27e-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4a27e-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="4a27e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a27e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a27e-103">애플리케이션 게이트웨이에서 백 엔드 HTTP 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4a27e-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="4a27e-104">구문</span><span class="sxs-lookup"><span data-stu-id="4a27e-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a27e-105">설명</span><span class="sxs-lookup"><span data-stu-id="4a27e-105">DESCRIPTION</span></span>
<span data-ttu-id="4a27e-106">이 Remove-AzApplicationGatewayBackendHttpSetting cmdlet은 Azure 애플리케이션 게이트웨이에서 백 엔드 HTTP(Hypertext Transfer Protocol) 설정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4a27e-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="4a27e-107">예제</span><span class="sxs-lookup"><span data-stu-id="4a27e-107">EXAMPLES</span></span>

### <span data-ttu-id="4a27e-108">예제 1: 애플리케이션 게이트웨이에서 백 엔드 HTTP 설정 제거</span><span class="sxs-lookup"><span data-stu-id="4a27e-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="4a27e-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="4a27e-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4a27e-110">두 번째 명령은 백 엔드에 저장된 애플리케이션 게이트웨이에서 BackEndSetting02라는 백 엔드 HTTP 설정을 $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4a27e-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="4a27e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a27e-111">PARAMETERS</span></span>

### <span data-ttu-id="4a27e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a27e-112">-ApplicationGateway</span></span>
<span data-ttu-id="4a27e-113">이 cmdlet이 백 엔드 HTTP 설정을 제거하는 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a27e-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="4a27e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a27e-114">-DefaultProfile</span></span>
<span data-ttu-id="4a27e-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4a27e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a27e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="4a27e-116">-Name</span></span>
<span data-ttu-id="4a27e-117">이 cmdlet에서 제거하는 백 엔드 HTTP 설정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4a27e-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4a27e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a27e-118">CommonParameters</span></span>
<span data-ttu-id="4a27e-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4a27e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a27e-120">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4a27e-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a27e-121">입력</span><span class="sxs-lookup"><span data-stu-id="4a27e-121">INPUTS</span></span>

### <span data-ttu-id="4a27e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a27e-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4a27e-123">출력</span><span class="sxs-lookup"><span data-stu-id="4a27e-123">OUTPUTS</span></span>

### <span data-ttu-id="4a27e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4a27e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4a27e-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4a27e-125">NOTES</span></span>

## <span data-ttu-id="4a27e-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4a27e-126">RELATED LINKS</span></span>

[<span data-ttu-id="4a27e-127">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4a27e-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="4a27e-128">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4a27e-128">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="4a27e-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4a27e-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="4a27e-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4a27e-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

