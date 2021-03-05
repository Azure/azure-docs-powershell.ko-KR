---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 88a89a17adc7a05e75865121d2133f723e534fcc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960299"
---
# <span data-ttu-id="a248f-101">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="a248f-101">Remove-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="a248f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a248f-102">SYNOPSIS</span></span>
<span data-ttu-id="a248f-103">Azure 애플리케이션 게이트웨이 SSL 프로필에서 SSL 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a248f-103">Removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="a248f-104">구문</span><span class="sxs-lookup"><span data-stu-id="a248f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a248f-105">설명</span><span class="sxs-lookup"><span data-stu-id="a248f-105">DESCRIPTION</span></span>
<span data-ttu-id="a248f-106">Remove-AzApplicationGatewaySslProfilePolicy cmdlet은 Azure 애플리케이션 게이트웨이 SSL 프로필에서 SSL 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a248f-106">The Remove-AzApplicationGatewaySslProfilePolicy cmdlet removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="a248f-107">예제</span><span class="sxs-lookup"><span data-stu-id="a248f-107">EXAMPLES</span></span>

### <span data-ttu-id="a248f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a248f-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> $profile = Remove-AzApplicationGatewaySslProfilePolicy -SslProfile $profile
```

<span data-ttu-id="a248f-109">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a248f-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="a248f-110">두 번째 명령은 프로필01이라는 SSL 프로필을 $AppGw 변수에 $profile 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a248f-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="a248f-111">마지막 명령은 에 저장된 ssl 프로필의 ssl 정책을 $profile.</span><span class="sxs-lookup"><span data-stu-id="a248f-111">The last command removes the ssl policy of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="a248f-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a248f-112">PARAMETERS</span></span>

### <span data-ttu-id="a248f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a248f-113">-DefaultProfile</span></span>
<span data-ttu-id="a248f-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a248f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a248f-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="a248f-115">-SslProfile</span></span>
<span data-ttu-id="a248f-116">ApplicationGateway SSL 프로필</span><span class="sxs-lookup"><span data-stu-id="a248f-116">The applicationGateway SSL profile</span></span>

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

### <span data-ttu-id="a248f-117">-확인</span><span class="sxs-lookup"><span data-stu-id="a248f-117">-Confirm</span></span>
<span data-ttu-id="a248f-118">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a248f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a248f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a248f-119">-WhatIf</span></span>
<span data-ttu-id="a248f-120">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a248f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a248f-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a248f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a248f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a248f-122">CommonParameters</span></span>
<span data-ttu-id="a248f-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a248f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a248f-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a248f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a248f-125">입력</span><span class="sxs-lookup"><span data-stu-id="a248f-125">INPUTS</span></span>

### <span data-ttu-id="a248f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="a248f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="a248f-127">출력</span><span class="sxs-lookup"><span data-stu-id="a248f-127">OUTPUTS</span></span>

### <span data-ttu-id="a248f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="a248f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="a248f-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a248f-129">NOTES</span></span>

## <span data-ttu-id="a248f-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a248f-130">RELATED LINKS</span></span>

[<span data-ttu-id="a248f-131">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="a248f-131">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="a248f-132">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="a248f-132">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="a248f-133">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="a248f-133">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="a248f-134">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="a248f-134">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)