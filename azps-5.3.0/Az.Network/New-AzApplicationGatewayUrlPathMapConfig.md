---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: cf65e93f1dc2026c0fc973d694fe1f44718df12e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491063"
---
# <span data-ttu-id="13af5-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="13af5-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="13af5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13af5-102">SYNOPSIS</span></span>
<span data-ttu-id="13af5-103">백end 서버 풀에 대한 URL 경로 매핑 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13af5-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="13af5-104">구문</span><span class="sxs-lookup"><span data-stu-id="13af5-104">SYNTAX</span></span>

### <span data-ttu-id="13af5-105">BackendSetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="13af5-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13af5-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="13af5-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13af5-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="13af5-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13af5-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="13af5-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13af5-109">설명</span><span class="sxs-lookup"><span data-stu-id="13af5-109">DESCRIPTION</span></span>
<span data-ttu-id="13af5-110">**New-AzApplicationGatewayUrlPathMapConfig** cmdlet은 백end 서버 풀에 대한 URL 경로 매핑 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13af5-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="13af5-111">예제</span><span class="sxs-lookup"><span data-stu-id="13af5-111">EXAMPLES</span></span>

### <span data-ttu-id="13af5-112">예제 1: 백end 서버 풀에 대한 URL 경로 매핑 배열 만들기</span><span class="sxs-lookup"><span data-stu-id="13af5-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="13af5-113">이 명령은 백end 서버 풀에 대한 URL 경로 매핑 배열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="13af5-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="13af5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13af5-114">PARAMETERS</span></span>

### <span data-ttu-id="13af5-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="13af5-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="13af5-116">*pathRules* 매개 변수에 지정된 규칙이 일치하지 않는 경우 라우팅할 기본 백end 주소 풀을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13af5-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13af5-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="13af5-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="13af5-118">기본 백end 주소 풀 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13af5-118">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13af5-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="13af5-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="13af5-120">*pathRules* 매개 변수에 지정된 규칙이 일치하지 않는 경우 사용할 기본 백end HTTP 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13af5-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13af5-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="13af5-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="13af5-122">기본 백end HTTP 설정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13af5-122">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13af5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13af5-123">-DefaultProfile</span></span>
<span data-ttu-id="13af5-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13af5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13af5-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="13af5-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="13af5-126">Application Gateway 기본 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="13af5-126">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13af5-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="13af5-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="13af5-128">Application Gateway 기본 RedirectConfiguration의 ID</span><span class="sxs-lookup"><span data-stu-id="13af5-128">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13af5-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="13af5-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="13af5-130">Application Gateway 기본 다시 필기 규칙 집합</span><span class="sxs-lookup"><span data-stu-id="13af5-130">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13af5-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="13af5-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="13af5-132">애플리케이션 게이트웨이 기본 다시 덮기 규칙 집합의 ID</span><span class="sxs-lookup"><span data-stu-id="13af5-132">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13af5-133">-Name</span><span class="sxs-lookup"><span data-stu-id="13af5-133">-Name</span></span>
<span data-ttu-id="13af5-134">이 cmdlet에서 만드는 URL 경로 맵 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13af5-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="13af5-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="13af5-135">-PathRules</span></span>
<span data-ttu-id="13af5-136">경로 규칙 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13af5-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="13af5-137">경로 규칙은 순서에 민감하고 지정된 순서대로 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="13af5-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13af5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13af5-138">CommonParameters</span></span>
<span data-ttu-id="13af5-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13af5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13af5-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="13af5-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13af5-141">입력</span><span class="sxs-lookup"><span data-stu-id="13af5-141">INPUTS</span></span>

### <span data-ttu-id="13af5-142">없음</span><span class="sxs-lookup"><span data-stu-id="13af5-142">None</span></span>

## <span data-ttu-id="13af5-143">출력</span><span class="sxs-lookup"><span data-stu-id="13af5-143">OUTPUTS</span></span>

### <span data-ttu-id="13af5-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="13af5-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="13af5-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="13af5-145">NOTES</span></span>

## <span data-ttu-id="13af5-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13af5-146">RELATED LINKS</span></span>

[<span data-ttu-id="13af5-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="13af5-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="13af5-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="13af5-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="13af5-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="13af5-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="13af5-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="13af5-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


