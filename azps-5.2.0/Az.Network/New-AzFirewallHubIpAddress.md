---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: efb3641f5c2a06ea64eed8d8b92e5e032a0809df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334934"
---
# <span data-ttu-id="bfaef-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="bfaef-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="bfaef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfaef-102">SYNOPSIS</span></span>
<span data-ttu-id="bfaef-103">가상 허브의 방화벽에 연결된 IP 주소</span><span class="sxs-lookup"><span data-stu-id="bfaef-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="bfaef-104">구문</span><span class="sxs-lookup"><span data-stu-id="bfaef-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfaef-105">설명</span><span class="sxs-lookup"><span data-stu-id="bfaef-105">DESCRIPTION</span></span>
<span data-ttu-id="bfaef-106">가상 허브의 방화벽에 연결된 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="bfaef-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="bfaef-107">이러한 주소는 공용 및 개인 주소일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bfaef-107">These can be public and private addresses</span></span>

## <span data-ttu-id="bfaef-108">예제</span><span class="sxs-lookup"><span data-stu-id="bfaef-108">EXAMPLES</span></span>

### <span data-ttu-id="bfaef-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="bfaef-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="bfaef-110">이 예제에서는 공용 IP가 2개인 허브 IP 주소 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfaef-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="bfaef-111">HubIPAddress 개체는 가상 허브의 방화벽에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="bfaef-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="bfaef-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfaef-112">PARAMETERS</span></span>

### <span data-ttu-id="bfaef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfaef-113">-DefaultProfile</span></span>
<span data-ttu-id="bfaef-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bfaef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfaef-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="bfaef-115">-PrivateIPAddress</span></span>
<span data-ttu-id="bfaef-116">허브에 연결된 방화벽의 개인 IP 주소</span><span class="sxs-lookup"><span data-stu-id="bfaef-116">The private Ip Address of the Firewall attached to a Hub</span></span>

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

### <span data-ttu-id="bfaef-117">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="bfaef-117">-PublicIPs</span></span>
<span data-ttu-id="bfaef-118">허브에 연결된 방화벽의 IP 주소</span><span class="sxs-lookup"><span data-stu-id="bfaef-118">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="bfaef-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfaef-119">-Confirm</span></span>
<span data-ttu-id="bfaef-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bfaef-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfaef-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfaef-121">-WhatIf</span></span>
<span data-ttu-id="bfaef-122">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bfaef-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bfaef-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bfaef-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfaef-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfaef-124">CommonParameters</span></span>
<span data-ttu-id="bfaef-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bfaef-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfaef-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bfaef-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfaef-127">입력</span><span class="sxs-lookup"><span data-stu-id="bfaef-127">INPUTS</span></span>

### <span data-ttu-id="bfaef-128">없음</span><span class="sxs-lookup"><span data-stu-id="bfaef-128">None</span></span>

## <span data-ttu-id="bfaef-129">출력</span><span class="sxs-lookup"><span data-stu-id="bfaef-129">OUTPUTS</span></span>

### <span data-ttu-id="bfaef-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="bfaef-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="bfaef-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bfaef-131">NOTES</span></span>

## <span data-ttu-id="bfaef-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfaef-132">RELATED LINKS</span></span>
