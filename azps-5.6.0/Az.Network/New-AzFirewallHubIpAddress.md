---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: 333e245b77869903b74973a4f851d020d70c0943
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985824"
---
# <span data-ttu-id="c4d83-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="c4d83-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="c4d83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4d83-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d83-103">가상 허브의 방화벽에 대해 분리된 IP 주소</span><span class="sxs-lookup"><span data-stu-id="c4d83-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="c4d83-104">구문</span><span class="sxs-lookup"><span data-stu-id="c4d83-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4d83-105">설명</span><span class="sxs-lookup"><span data-stu-id="c4d83-105">DESCRIPTION</span></span>
<span data-ttu-id="c4d83-106">가상 허브의 방화벽에 대해 분리된 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="c4d83-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="c4d83-107">이러한 주소는 공용 주소 및 개인 주소일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4d83-107">These can be public and private addresses</span></span>

## <span data-ttu-id="c4d83-108">예제</span><span class="sxs-lookup"><span data-stu-id="c4d83-108">EXAMPLES</span></span>

### <span data-ttu-id="c4d83-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="c4d83-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="c4d83-110">이 예제에서는 공용 IP 수가 2개인 Hub IP 주소 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c4d83-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="c4d83-111">HubIPAddress 개체는 가상 허브의 방화벽으로 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4d83-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="c4d83-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c4d83-112">PARAMETERS</span></span>

### <span data-ttu-id="c4d83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4d83-113">-DefaultProfile</span></span>
<span data-ttu-id="c4d83-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4d83-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4d83-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="c4d83-115">-PrivateIPAddress</span></span>
<span data-ttu-id="c4d83-116">Hub에 연결된 방화벽의 개인 IP 주소</span><span class="sxs-lookup"><span data-stu-id="c4d83-116">The private Ip Address of the Firewall attached to a Hub</span></span>

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

### <span data-ttu-id="c4d83-117">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="c4d83-117">-PublicIPs</span></span>
<span data-ttu-id="c4d83-118">허브에 연결된 방화벽의 IP 주소</span><span class="sxs-lookup"><span data-stu-id="c4d83-118">The IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallHubPublicIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4d83-119">-확인</span><span class="sxs-lookup"><span data-stu-id="c4d83-119">-Confirm</span></span>
<span data-ttu-id="c4d83-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4d83-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4d83-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4d83-121">-WhatIf</span></span>
<span data-ttu-id="c4d83-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c4d83-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4d83-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4d83-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4d83-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d83-124">CommonParameters</span></span>
<span data-ttu-id="c4d83-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c4d83-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d83-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4d83-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d83-127">입력</span><span class="sxs-lookup"><span data-stu-id="c4d83-127">INPUTS</span></span>

### <span data-ttu-id="c4d83-128">없음</span><span class="sxs-lookup"><span data-stu-id="c4d83-128">None</span></span>

## <span data-ttu-id="c4d83-129">출력</span><span class="sxs-lookup"><span data-stu-id="c4d83-129">OUTPUTS</span></span>

### <span data-ttu-id="c4d83-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="c4d83-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="c4d83-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c4d83-131">NOTES</span></span>

## <span data-ttu-id="c4d83-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4d83-132">RELATED LINKS</span></span>
