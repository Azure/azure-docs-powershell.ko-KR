---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 5aeae0fe7a3efe4513869991d1e53ac429f52401
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043570"
---
# <span data-ttu-id="6065b-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="6065b-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="6065b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6065b-102">SYNOPSIS</span></span>
<span data-ttu-id="6065b-103">응용 프로그램 게이트웨이의 백 엔드 HTTP 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6065b-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="6065b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6065b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6065b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6065b-105">DESCRIPTION</span></span>
<span data-ttu-id="6065b-106">Get-AzApplicationGatewayBackendHttpSetting cmdlet은 응용 프로그램 게이트웨이의 백 엔드 HTTP 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6065b-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="6065b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6065b-107">EXAMPLES</span></span>

### <span data-ttu-id="6065b-108">예제 1: 이름으로 백 엔드 HTTP 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="6065b-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="6065b-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다. 두 번째 명령은 $AppGw에 대 한 Settings01 이라는 HTTP 설정을 가져오고 $Settings 변수에 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6065b-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="6065b-110">예제 2: 백 엔드 HTTP 설정 컬렉션 가져오기</span><span class="sxs-lookup"><span data-stu-id="6065b-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="6065b-111">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다. 두 번째 명령은 $AppGw에 대 한 HTTP 설정 컬렉션을 가져와 $SettingsList 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6065b-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="6065b-112">변수</span><span class="sxs-lookup"><span data-stu-id="6065b-112">PARAMETERS</span></span>

### <span data-ttu-id="6065b-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6065b-113">-ApplicationGateway</span></span>
<span data-ttu-id="6065b-114">백 엔드 HTTP 설정을 포함 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6065b-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="6065b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6065b-115">-DefaultProfile</span></span>
<span data-ttu-id="6065b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6065b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6065b-117">-이름</span><span class="sxs-lookup"><span data-stu-id="6065b-117">-Name</span></span>
<span data-ttu-id="6065b-118">이 cmdlet이 가져오는 백 엔드 HTTP 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6065b-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6065b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6065b-119">CommonParameters</span></span>
<span data-ttu-id="6065b-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6065b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6065b-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6065b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6065b-122">입력</span><span class="sxs-lookup"><span data-stu-id="6065b-122">INPUTS</span></span>

### <span data-ttu-id="6065b-123">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6065b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6065b-124">출력</span><span class="sxs-lookup"><span data-stu-id="6065b-124">OUTPUTS</span></span>

### <span data-ttu-id="6065b-125">PSApplicationGatewayBackendHttpSettings에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6065b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="6065b-126">상속자</span><span class="sxs-lookup"><span data-stu-id="6065b-126">NOTES</span></span>

## <span data-ttu-id="6065b-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6065b-127">RELATED LINKS</span></span>

[<span data-ttu-id="6065b-128">추가-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="6065b-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="6065b-129">새로운 AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="6065b-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="6065b-130">제거-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="6065b-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="6065b-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="6065b-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

