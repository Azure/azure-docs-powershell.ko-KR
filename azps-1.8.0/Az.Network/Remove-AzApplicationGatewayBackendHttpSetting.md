---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 6c5729ec4d450ad122e359b9bd009000212e3b0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700230"
---
# <span data-ttu-id="00b72-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="00b72-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="00b72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00b72-102">SYNOPSIS</span></span>
<span data-ttu-id="00b72-103">응용 프로그램 게이트웨이에서 백 엔드 HTTP 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b72-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="00b72-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00b72-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00b72-105">설명은</span><span class="sxs-lookup"><span data-stu-id="00b72-105">DESCRIPTION</span></span>
<span data-ttu-id="00b72-106">Remove-AzApplicationGatewayBackendHttpSetting cmdlet은 Azure application gateway에서 백 엔드 HTTP (하이퍼텍스트 전송 프로토콜) 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b72-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="00b72-107">예제의</span><span class="sxs-lookup"><span data-stu-id="00b72-107">EXAMPLES</span></span>

### <span data-ttu-id="00b72-108">예제 1: 응용 프로그램 게이트웨이에서 백 엔드 HTTP 설정 제거</span><span class="sxs-lookup"><span data-stu-id="00b72-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="00b72-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하고이를 $AppGw 변수에 저장 하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="00b72-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="00b72-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에서 BackEndSetting02 이라는 백 엔드 HTTP 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b72-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="00b72-111">변수</span><span class="sxs-lookup"><span data-stu-id="00b72-111">PARAMETERS</span></span>

### <span data-ttu-id="00b72-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00b72-112">-ApplicationGateway</span></span>
<span data-ttu-id="00b72-113">이 cmdlet이 백 엔드 HTTP 설정을 제거 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b72-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="00b72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00b72-114">-DefaultProfile</span></span>
<span data-ttu-id="00b72-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00b72-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00b72-116">-이름</span><span class="sxs-lookup"><span data-stu-id="00b72-116">-Name</span></span>
<span data-ttu-id="00b72-117">이 cmdlet이 제거 하는 백 엔드 HTTP 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b72-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="00b72-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00b72-118">CommonParameters</span></span>
<span data-ttu-id="00b72-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00b72-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00b72-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00b72-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00b72-121">입력</span><span class="sxs-lookup"><span data-stu-id="00b72-121">INPUTS</span></span>

### <span data-ttu-id="00b72-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00b72-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="00b72-123">출력</span><span class="sxs-lookup"><span data-stu-id="00b72-123">OUTPUTS</span></span>

### <span data-ttu-id="00b72-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00b72-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="00b72-125">상속자</span><span class="sxs-lookup"><span data-stu-id="00b72-125">NOTES</span></span>

## <span data-ttu-id="00b72-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00b72-126">RELATED LINKS</span></span>

[<span data-ttu-id="00b72-127">추가-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="00b72-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="00b72-128">새로운 AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="00b72-128">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="00b72-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="00b72-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="00b72-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="00b72-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

