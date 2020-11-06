---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 036fef4e43d8d754bd0798e72159cba367a3e2f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528499"
---
# <span data-ttu-id="4869a-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4869a-101">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="4869a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4869a-102">SYNOPSIS</span></span>
<span data-ttu-id="4869a-103">응용 프로그램 게이트웨이에서 백 엔드 HTTP 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4869a-103">Removes back-end HTTP settings from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4869a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4869a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4869a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4869a-105">DESCRIPTION</span></span>
<span data-ttu-id="4869a-106">Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet은 Azure application gateway에서 백 엔드 HTTP (하이퍼텍스트 전송 프로토콜) 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4869a-106">The Remove-AzureRmApplicationGatewayBackendHttpSettings cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="4869a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4869a-107">EXAMPLES</span></span>

### <span data-ttu-id="4869a-108">예제 1: 응용 프로그램 게이트웨이에서 백 엔드 HTTP 설정 제거</span><span class="sxs-lookup"><span data-stu-id="4869a-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="4869a-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하고이를 $AppGw 변수에 저장 하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4869a-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4869a-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에서 BackEndSetting02 이라는 백 엔드 HTTP 설정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4869a-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="4869a-111">변수</span><span class="sxs-lookup"><span data-stu-id="4869a-111">PARAMETERS</span></span>

### <span data-ttu-id="4869a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4869a-112">-ApplicationGateway</span></span>
<span data-ttu-id="4869a-113">이 cmdlet이 백 엔드 HTTP 설정을 제거 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4869a-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="4869a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4869a-114">-DefaultProfile</span></span>
<span data-ttu-id="4869a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4869a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4869a-116">-이름</span><span class="sxs-lookup"><span data-stu-id="4869a-116">-Name</span></span>
<span data-ttu-id="4869a-117">이 cmdlet이 제거 하는 백 엔드 HTTP 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4869a-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4869a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4869a-118">CommonParameters</span></span>
<span data-ttu-id="4869a-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4869a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4869a-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4869a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4869a-121">입력</span><span class="sxs-lookup"><span data-stu-id="4869a-121">INPUTS</span></span>

### <span data-ttu-id="4869a-122">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4869a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="4869a-123">매개 변수: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4869a-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="4869a-124">출력</span><span class="sxs-lookup"><span data-stu-id="4869a-124">OUTPUTS</span></span>

### <span data-ttu-id="4869a-125">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4869a-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4869a-126">상속자</span><span class="sxs-lookup"><span data-stu-id="4869a-126">NOTES</span></span>

## <span data-ttu-id="4869a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4869a-127">RELATED LINKS</span></span>

[<span data-ttu-id="4869a-128">추가-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4869a-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="4869a-129">새로운 AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4869a-129">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="4869a-130">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4869a-130">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="4869a-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4869a-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

