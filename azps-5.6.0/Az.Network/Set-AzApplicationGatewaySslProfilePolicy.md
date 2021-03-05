---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 6dff1e78f83c48a103266c39bd9f3462a20b50a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995316"
---
# <span data-ttu-id="b25b4-101">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="b25b4-101">Set-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="b25b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b25b4-102">SYNOPSIS</span></span>
<span data-ttu-id="b25b4-103">애플리케이션 게이트웨이 SSL 프로필의 SSL 정책을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="b25b4-103">Modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="b25b4-104">구문</span><span class="sxs-lookup"><span data-stu-id="b25b4-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DisabledSslProtocols <String[]>] [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b25b4-105">설명</span><span class="sxs-lookup"><span data-stu-id="b25b4-105">DESCRIPTION</span></span>
<span data-ttu-id="b25b4-106">**Set-AzApplicationGatewaySslProfilePolicy** cmdlet은 애플리케이션 게이트웨이 SSL 프로필의 SSL 정책을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="b25b4-106">The **Set-AzApplicationGatewaySslProfilePolicy** cmdlet modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="b25b4-107">예제</span><span class="sxs-lookup"><span data-stu-id="b25b4-107">EXAMPLES</span></span>

### <span data-ttu-id="b25b4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b25b4-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $profile = Set-AzApplicationGatewaySslProfilePolicy -SslProfile $profile -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="b25b4-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b25b4-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="b25b4-110">두 번째 명령은 SslProfile01이라는 ssl 프로필을 $AppGw 변수에 $profile 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b25b4-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="b25b4-111">마지막 명령은 에 저장된 ssl 프로필 개체의 ssl 정책을 $profile.</span><span class="sxs-lookup"><span data-stu-id="b25b4-111">The last command modifies the ssl policy of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="b25b4-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b25b4-112">PARAMETERS</span></span>

### <span data-ttu-id="b25b4-113">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="b25b4-113">-CipherSuite</span></span>
<span data-ttu-id="b25b4-114">애플리케이션 게이트웨이에 지정된 순서대로 사용하도록 설정될 Ssl 암호 제품군</span><span class="sxs-lookup"><span data-stu-id="b25b4-114">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b25b4-115">-DefaultProfile</span></span>
<span data-ttu-id="b25b4-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b25b4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25b4-117">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="b25b4-117">-DisabledSslProtocols</span></span>
<span data-ttu-id="b25b4-118">사용하지 않도록 설정할 SSL 프로토콜 목록</span><span class="sxs-lookup"><span data-stu-id="b25b4-118">List of SSL protocols to be disabled</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25b4-119">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="b25b4-119">-MinProtocolVersion</span></span>
<span data-ttu-id="b25b4-120">애플리케이션 게이트웨이에서 지원할 Ssl 프로토콜의 최소 버전</span><span class="sxs-lookup"><span data-stu-id="b25b4-120">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25b4-121">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="b25b4-121">-PolicyName</span></span>
<span data-ttu-id="b25b4-122">Ssl 미리 정의된 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="b25b4-122">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="b25b4-123">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="b25b4-123">-PolicyType</span></span>
<span data-ttu-id="b25b4-124">Ssl 정책 유형</span><span class="sxs-lookup"><span data-stu-id="b25b4-124">Type of Ssl Policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25b4-125">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="b25b4-125">-SslProfile</span></span>
<span data-ttu-id="b25b4-126">애플리케이션 게이트웨이 SSL 프로필</span><span class="sxs-lookup"><span data-stu-id="b25b4-126">The application gateway SSL profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b25b4-127">-확인</span><span class="sxs-lookup"><span data-stu-id="b25b4-127">-Confirm</span></span>
<span data-ttu-id="b25b4-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b25b4-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25b4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b25b4-129">-WhatIf</span></span>
<span data-ttu-id="b25b4-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b25b4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b25b4-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b25b4-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25b4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b25b4-132">CommonParameters</span></span>
<span data-ttu-id="b25b4-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b25b4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b25b4-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b25b4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b25b4-135">입력</span><span class="sxs-lookup"><span data-stu-id="b25b4-135">INPUTS</span></span>

### <span data-ttu-id="b25b4-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b25b4-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="b25b4-137">출력</span><span class="sxs-lookup"><span data-stu-id="b25b4-137">OUTPUTS</span></span>

### <span data-ttu-id="b25b4-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="b25b4-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="b25b4-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b25b4-139">NOTES</span></span>

## <span data-ttu-id="b25b4-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b25b4-140">RELATED LINKS</span></span>

[<span data-ttu-id="b25b4-141">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="b25b4-141">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="b25b4-142">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="b25b4-142">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="b25b4-143">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="b25b4-143">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="b25b4-144">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="b25b4-144">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)