---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 2e4179019f74a8fd85b5f0ea3471bc586864172a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214837"
---
# <span data-ttu-id="ab4ca-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="ab4ca-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="ab4ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab4ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ab4ca-103">Azure 방화벽 정책에 대 한 새 DNS 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab4ca-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="ab4ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ab4ca-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-ProxyNotRequiredForNetworkRule] [-Server <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab4ca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ab4ca-105">DESCRIPTION</span></span>
<span data-ttu-id="ab4ca-106">**AzFirewallPolicyDnsSetting** Cmdlet은 Azure 방화벽 정책에 대 한 DNS 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab4ca-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="ab4ca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ab4ca-107">EXAMPLES</span></span>

### <span data-ttu-id="ab4ca-108">1. 빈 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="ab4ca-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="ab4ca-109">이 예제에서는 dns 프록시를 사용 하도록 설정 하 여 dns 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab4ca-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="ab4ca-110">2. ThreatIntel 모드를 사용 하 여 빈 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="ab4ca-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```
<span data-ttu-id="ab4ca-111">이 예제에서는 dns 프록시를 사용 하도록 설정 하 고 사용자 지정 dns 서버를 설정 하 여 dns 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ab4ca-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="ab4ca-112">변수</span><span class="sxs-lookup"><span data-stu-id="ab4ca-112">PARAMETERS</span></span>

### <span data-ttu-id="ab4ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab4ca-113">-DefaultProfile</span></span>
<span data-ttu-id="ab4ca-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab4ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab4ca-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="ab4ca-115">-EnableProxy</span></span>
<span data-ttu-id="ab4ca-116">DNS 프록시를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab4ca-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="ab4ca-117">기본적으로 사용 하지 않도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ab4ca-117">By default it is disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab4ca-118">-ProxyNotRequiredForNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ab4ca-118">-ProxyNotRequiredForNetworkRule</span></span>
<span data-ttu-id="ab4ca-119">네트워크 규칙 내에서 Fqdn에 대 한 DNS 프록시 기능이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab4ca-119">Requires DNS Proxy functionality for FQDNs within Network Rules.</span></span>
<span data-ttu-id="ab4ca-120">기본적으로 true입니다.</span><span class="sxs-lookup"><span data-stu-id="ab4ca-120">By default it is true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab4ca-121">-서버</span><span class="sxs-lookup"><span data-stu-id="ab4ca-121">-Server</span></span>
<span data-ttu-id="ab4ca-122">DNS 서버 목록</span><span class="sxs-lookup"><span data-stu-id="ab4ca-122">The list of DNS Servers</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab4ca-123">-확인</span><span class="sxs-lookup"><span data-stu-id="ab4ca-123">-Confirm</span></span>
<span data-ttu-id="ab4ca-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab4ca-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab4ca-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab4ca-125">-WhatIf</span></span>
<span data-ttu-id="ab4ca-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ab4ca-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab4ca-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ab4ca-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab4ca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab4ca-128">CommonParameters</span></span>
<span data-ttu-id="ab4ca-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ab4ca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab4ca-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ab4ca-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab4ca-131">입력</span><span class="sxs-lookup"><span data-stu-id="ab4ca-131">INPUTS</span></span>

### <span data-ttu-id="ab4ca-132">않아야</span><span class="sxs-lookup"><span data-stu-id="ab4ca-132">None</span></span>

## <span data-ttu-id="ab4ca-133">출력</span><span class="sxs-lookup"><span data-stu-id="ab4ca-133">OUTPUTS</span></span>

### <span data-ttu-id="ab4ca-134">PSAzureFirewallPolicyDnsSettings에 대 한.</span><span class="sxs-lookup"><span data-stu-id="ab4ca-134">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="ab4ca-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ab4ca-135">NOTES</span></span>

## <span data-ttu-id="ab4ca-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab4ca-136">RELATED LINKS</span></span>
