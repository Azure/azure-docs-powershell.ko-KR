---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: 366b3545e54c1465bf2eaf050a9e9199288fce5b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881478"
---
# <span data-ttu-id="44cb4-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="44cb4-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="44cb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44cb4-102">SYNOPSIS</span></span>
<span data-ttu-id="44cb4-103">응용 프로그램 게이트웨이의 백 엔드 HTTP 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="44cb4-103">Gets the back-end HTTP settings of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44cb4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="44cb4-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHttpSettings [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44cb4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="44cb4-105">DESCRIPTION</span></span>
<span data-ttu-id="44cb4-106">Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet은 응용 프로그램 게이트웨이의 백 엔드 HTTP 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="44cb4-106">The Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="44cb4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="44cb4-107">EXAMPLES</span></span>

### <span data-ttu-id="44cb4-108">예제 1: 이름으로 백 엔드 HTTP 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="44cb4-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="44cb4-109">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다. 두 번째 명령은 $AppGw에 대 한 Settings01 이라는 HTTP 설정을 가져오고 $Settings 변수에 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="44cb4-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="44cb4-110">예제 2: 백 엔드 HTTP 설정 컬렉션 가져오기</span><span class="sxs-lookup"><span data-stu-id="44cb4-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw
```

<span data-ttu-id="44cb4-111">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져와이를 $AppGw 변수에 저장 합니다. 두 번째 명령은 $AppGw에 대 한 HTTP 설정 컬렉션을 가져와 $SettingsList 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="44cb4-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="44cb4-112">변수</span><span class="sxs-lookup"><span data-stu-id="44cb4-112">PARAMETERS</span></span>

### <span data-ttu-id="44cb4-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="44cb4-113">-ApplicationGateway</span></span>
<span data-ttu-id="44cb4-114">백 엔드 HTTP 설정을 포함 하는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44cb4-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44cb4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44cb4-115">-DefaultProfile</span></span>
<span data-ttu-id="44cb4-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44cb4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44cb4-117">-이름</span><span class="sxs-lookup"><span data-stu-id="44cb4-117">-Name</span></span>
<span data-ttu-id="44cb4-118">이 cmdlet이 가져오는 백 엔드 HTTP 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="44cb4-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44cb4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44cb4-119">CommonParameters</span></span>
<span data-ttu-id="44cb4-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="44cb4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44cb4-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44cb4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44cb4-122">입력</span><span class="sxs-lookup"><span data-stu-id="44cb4-122">INPUTS</span></span>

### <span data-ttu-id="44cb4-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="44cb4-123">System.String</span></span>

## <span data-ttu-id="44cb4-124">출력</span><span class="sxs-lookup"><span data-stu-id="44cb4-124">OUTPUTS</span></span>

### <span data-ttu-id="44cb4-125">AzureApplicationGatewayBackendHttpSettings에 대 한.</span><span class="sxs-lookup"><span data-stu-id="44cb4-125">Microsoft.Azure.Commands.Network.Models.AzureApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="44cb4-126">상속자</span><span class="sxs-lookup"><span data-stu-id="44cb4-126">NOTES</span></span>

## <span data-ttu-id="44cb4-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44cb4-127">RELATED LINKS</span></span>

[<span data-ttu-id="44cb4-128">추가-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="44cb4-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="44cb4-129">새로운 AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="44cb4-129">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="44cb4-130">제거-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="44cb4-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="44cb4-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="44cb4-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

