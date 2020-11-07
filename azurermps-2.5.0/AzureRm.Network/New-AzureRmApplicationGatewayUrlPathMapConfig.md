---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: e43d5277566311fe77ee239d88e55f658aca8b40
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880654"
---
# <span data-ttu-id="938ed-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="938ed-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="938ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="938ed-102">SYNOPSIS</span></span>
<span data-ttu-id="938ed-103">백 엔드 서버 풀에 대 한 URL 경로 매핑의 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="938ed-103">Creates an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="938ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="938ed-104">SYNTAX</span></span>

### <span data-ttu-id="938ed-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="938ed-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="938ed-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="938ed-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="938ed-107">설명은</span><span class="sxs-lookup"><span data-stu-id="938ed-107">DESCRIPTION</span></span>
<span data-ttu-id="938ed-108">**AzureRmApplicationGatewayUrlPathMapConfig** cmdlet은 백 엔드 서버 풀에 대 한 URL 경로 매핑의 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="938ed-108">The **New-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="938ed-109">예제의</span><span class="sxs-lookup"><span data-stu-id="938ed-109">EXAMPLES</span></span>

### <span data-ttu-id="938ed-110">예제 1: 백 엔드 서버 풀에 대 한 URL 경로 매핑 배열 만들기</span><span class="sxs-lookup"><span data-stu-id="938ed-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzureRmApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="938ed-111">이 명령은 백 엔드 서버 풀에 대 한 URL 경로 매핑 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="938ed-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="938ed-112">변수</span><span class="sxs-lookup"><span data-stu-id="938ed-112">PARAMETERS</span></span>

### <span data-ttu-id="938ed-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="938ed-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="938ed-114">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 라우팅할 기본 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="938ed-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="938ed-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="938ed-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="938ed-116">기본 백 엔드 주소 풀 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="938ed-116">Specifies the default backend address pool ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="938ed-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="938ed-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="938ed-118">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 사용할 기본 백 엔드 HTTP 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="938ed-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="938ed-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="938ed-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="938ed-120">기본 백 엔드 HTTP 설정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="938ed-120">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="938ed-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="938ed-121">-DefaultProfile</span></span>
<span data-ttu-id="938ed-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="938ed-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="938ed-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="938ed-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="938ed-124">Application gateway 기본 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="938ed-124">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="938ed-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="938ed-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="938ed-126">응용 프로그램 게이트웨이 기본 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="938ed-126">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="938ed-127">-이름</span><span class="sxs-lookup"><span data-stu-id="938ed-127">-Name</span></span>
<span data-ttu-id="938ed-128">이 cmdlet이 만드는 URL 경로 맵 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="938ed-128">Specifies the URL path map name that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="938ed-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="938ed-129">-PathRules</span></span>
<span data-ttu-id="938ed-130">경로 규칙의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="938ed-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="938ed-131">경로 규칙은 주문에 따라 구분 되며 지정 된 순서 대로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="938ed-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="938ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="938ed-132">CommonParameters</span></span>
<span data-ttu-id="938ed-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="938ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="938ed-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="938ed-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="938ed-135">입력</span><span class="sxs-lookup"><span data-stu-id="938ed-135">INPUTS</span></span>

## <span data-ttu-id="938ed-136">출력</span><span class="sxs-lookup"><span data-stu-id="938ed-136">OUTPUTS</span></span>

### <span data-ttu-id="938ed-137">PSApplicationGatewayUrlPathMap에 대 한.</span><span class="sxs-lookup"><span data-stu-id="938ed-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="938ed-138">상속자</span><span class="sxs-lookup"><span data-stu-id="938ed-138">NOTES</span></span>

## <span data-ttu-id="938ed-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="938ed-139">RELATED LINKS</span></span>

[<span data-ttu-id="938ed-140">추가-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="938ed-140">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="938ed-141">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="938ed-141">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="938ed-142">제거-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="938ed-142">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="938ed-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="938ed-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


