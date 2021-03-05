---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 7c338f49191071bfa48214e65f79e196a75650eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973680"
---
# <span data-ttu-id="bfff9-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfff9-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="bfff9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfff9-102">SYNOPSIS</span></span>
<span data-ttu-id="bfff9-103">애플리케이션 게이트웨이에 대한 개인 링크 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfff9-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="bfff9-104">구문</span><span class="sxs-lookup"><span data-stu-id="bfff9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfff9-105">설명</span><span class="sxs-lookup"><span data-stu-id="bfff9-105">DESCRIPTION</span></span>
<span data-ttu-id="bfff9-106">**New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 PrivateLink 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfff9-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="bfff9-107">개인 링크 기능을 사용하도록 설정하려면 개인 링크 구성을 프런트 엔드 IP 구성에 연결해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfff9-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="bfff9-108">하나의 개인 링크 구성은 애플리케이션 게이트웨이에서 하나의 프런트 엔드 IP 구성에만 연결될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bfff9-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="bfff9-109">예제</span><span class="sxs-lookup"><span data-stu-id="bfff9-109">EXAMPLES</span></span>

### <span data-ttu-id="bfff9-110">예제 1: 단일 IP 구성을 사용하여 개인 링크 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="bfff9-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="bfff9-111">이 명령은 'privateLinkConfig01'이라는 PrivateLink 구성을 만들고 결과를 $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="bfff9-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="bfff9-112">예제 2: 여러 IP 구성을 사용하여 개인 링크 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="bfff9-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="bfff9-113">이 명령은 두 개의 ipConfigurations를 사용하여 'privateLinkConfig01'이라는 PrivateLink 구성을 만들고 결과를 2개의 ipConfigurations라는 변수에 $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="bfff9-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="bfff9-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bfff9-114">PARAMETERS</span></span>

### <span data-ttu-id="bfff9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfff9-115">-DefaultProfile</span></span>
<span data-ttu-id="bfff9-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bfff9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfff9-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfff9-117">-IpConfiguration</span></span>
<span data-ttu-id="bfff9-118">ipConfiguration 목록</span><span class="sxs-lookup"><span data-stu-id="bfff9-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfff9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bfff9-119">-Name</span></span>
<span data-ttu-id="bfff9-120">privateLink 구성의 이름</span><span class="sxs-lookup"><span data-stu-id="bfff9-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="bfff9-121">-확인</span><span class="sxs-lookup"><span data-stu-id="bfff9-121">-Confirm</span></span>
<span data-ttu-id="bfff9-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bfff9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfff9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfff9-123">-WhatIf</span></span>
<span data-ttu-id="bfff9-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bfff9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfff9-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bfff9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfff9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfff9-126">CommonParameters</span></span>
<span data-ttu-id="bfff9-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bfff9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfff9-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfff9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfff9-129">입력</span><span class="sxs-lookup"><span data-stu-id="bfff9-129">INPUTS</span></span>

### <span data-ttu-id="bfff9-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="bfff9-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="bfff9-131">출력</span><span class="sxs-lookup"><span data-stu-id="bfff9-131">OUTPUTS</span></span>

### <span data-ttu-id="bfff9-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfff9-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="bfff9-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bfff9-133">NOTES</span></span>

## <span data-ttu-id="bfff9-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfff9-134">RELATED LINKS</span></span>

[<span data-ttu-id="bfff9-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfff9-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="bfff9-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfff9-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="bfff9-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfff9-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="bfff9-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfff9-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
