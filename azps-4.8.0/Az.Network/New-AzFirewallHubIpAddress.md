---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: efb3641f5c2a06ea64eed8d8b92e5e032a0809df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214853"
---
# <span data-ttu-id="0df66-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="0df66-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="0df66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0df66-102">SYNOPSIS</span></span>
<span data-ttu-id="0df66-103">가상 허브의 방화벽에 assoicated Ip 주소</span><span class="sxs-lookup"><span data-stu-id="0df66-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="0df66-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0df66-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0df66-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0df66-105">DESCRIPTION</span></span>
<span data-ttu-id="0df66-106">Ip 주소는 가상 허브의 방화벽으로 assoicated.</span><span class="sxs-lookup"><span data-stu-id="0df66-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="0df66-107">공용 주소와 개인 주소가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-107">These can be public and private addresses</span></span>

## <span data-ttu-id="0df66-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0df66-108">EXAMPLES</span></span>

### <span data-ttu-id="0df66-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="0df66-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="0df66-110">이 예제에서는 공용 Ip 수가 2 개 있는 허브 Ip 주소 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="0df66-111">HubIPAddress 개체는 가상 허브의 방화벽에만 해당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="0df66-112">변수</span><span class="sxs-lookup"><span data-stu-id="0df66-112">PARAMETERS</span></span>

### <span data-ttu-id="0df66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0df66-113">-DefaultProfile</span></span>
<span data-ttu-id="0df66-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0df66-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="0df66-115">-PrivateIPAddress</span></span>
<span data-ttu-id="0df66-116">허브에 연결 된 방화벽의 개인 Ip 주소</span><span class="sxs-lookup"><span data-stu-id="0df66-116">The private Ip Address of the Firewall attached to a Hub</span></span>

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

### <span data-ttu-id="0df66-117">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="0df66-117">-PublicIPs</span></span>
<span data-ttu-id="0df66-118">허브에 연결 된 방화벽의 IP 주소</span><span class="sxs-lookup"><span data-stu-id="0df66-118">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="0df66-119">-확인</span><span class="sxs-lookup"><span data-stu-id="0df66-119">-Confirm</span></span>
<span data-ttu-id="0df66-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0df66-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0df66-121">-WhatIf</span></span>
<span data-ttu-id="0df66-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0df66-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0df66-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0df66-124">CommonParameters</span></span>
<span data-ttu-id="0df66-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0df66-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0df66-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0df66-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0df66-127">입력</span><span class="sxs-lookup"><span data-stu-id="0df66-127">INPUTS</span></span>

### <span data-ttu-id="0df66-128">않아야</span><span class="sxs-lookup"><span data-stu-id="0df66-128">None</span></span>

## <span data-ttu-id="0df66-129">출력</span><span class="sxs-lookup"><span data-stu-id="0df66-129">OUTPUTS</span></span>

### <span data-ttu-id="0df66-130">PSAzureFirewallHubIpAddresses에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0df66-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="0df66-131">상속자</span><span class="sxs-lookup"><span data-stu-id="0df66-131">NOTES</span></span>

## <span data-ttu-id="0df66-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0df66-132">RELATED LINKS</span></span>
