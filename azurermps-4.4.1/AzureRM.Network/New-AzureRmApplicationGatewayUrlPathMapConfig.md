---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 5c3a59b497208c761ffcf7a24bc12b5ab2c50f27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530008"
---
# <span data-ttu-id="2984c-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2984c-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="2984c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2984c-102">SYNOPSIS</span></span>
<span data-ttu-id="2984c-103">백 엔드 서버 풀에 대 한 URL 경로 매핑의 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2984c-103">Creates an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2984c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2984c-104">SYNTAX</span></span>

### <span data-ttu-id="2984c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2984c-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2984c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2984c-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2984c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2984c-107">DESCRIPTION</span></span>
<span data-ttu-id="2984c-108">**AzureRmApplicationGatewayUrlPathMapConfig** cmdlet은 백 엔드 서버 풀에 대 한 URL 경로 매핑의 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2984c-108">The **New-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="2984c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2984c-109">EXAMPLES</span></span>

### <span data-ttu-id="2984c-110">예제 1: 백 엔드 서버 풀에 대 한 URL 경로 매핑 배열 만들기</span><span class="sxs-lookup"><span data-stu-id="2984c-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzureRmApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="2984c-111">이 명령은 백 엔드 서버 풀에 대 한 URL 경로 매핑 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2984c-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="2984c-112">변수</span><span class="sxs-lookup"><span data-stu-id="2984c-112">PARAMETERS</span></span>

### <span data-ttu-id="2984c-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2984c-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="2984c-114">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 라우팅할 기본 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2984c-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2984c-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2984c-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="2984c-116">기본 백 엔드 주소 풀 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2984c-116">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2984c-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2984c-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="2984c-118">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 사용할 기본 백 엔드 HTTP 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2984c-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2984c-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="2984c-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="2984c-120">기본 백 엔드 HTTP 설정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2984c-120">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2984c-121">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2984c-121">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="2984c-122">Application gateway 기본 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2984c-122">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2984c-123">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2984c-123">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="2984c-124">응용 프로그램 게이트웨이 기본 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2984c-124">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2984c-125">-이름</span><span class="sxs-lookup"><span data-stu-id="2984c-125">-Name</span></span>
<span data-ttu-id="2984c-126">이 cmdlet이 만드는 URL 경로 맵 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2984c-126">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2984c-127">-PathRules</span><span class="sxs-lookup"><span data-stu-id="2984c-127">-PathRules</span></span>
<span data-ttu-id="2984c-128">경로 규칙의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2984c-128">Specifies a list of path rules.</span></span>
<span data-ttu-id="2984c-129">경로 규칙은 주문에 따라 구분 되며 지정 된 순서 대로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2984c-129">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2984c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2984c-130">-DefaultProfile</span></span>
<span data-ttu-id="2984c-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2984c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2984c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2984c-132">CommonParameters</span></span>
<span data-ttu-id="2984c-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2984c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2984c-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2984c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2984c-135">입력</span><span class="sxs-lookup"><span data-stu-id="2984c-135">INPUTS</span></span>

## <span data-ttu-id="2984c-136">출력</span><span class="sxs-lookup"><span data-stu-id="2984c-136">OUTPUTS</span></span>

### <span data-ttu-id="2984c-137">PSApplicationGatewayUrlPathMap에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2984c-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="2984c-138">상속자</span><span class="sxs-lookup"><span data-stu-id="2984c-138">NOTES</span></span>

## <span data-ttu-id="2984c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2984c-139">RELATED LINKS</span></span>

[<span data-ttu-id="2984c-140">추가-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2984c-140">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2984c-141">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2984c-141">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2984c-142">제거-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2984c-142">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2984c-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2984c-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


