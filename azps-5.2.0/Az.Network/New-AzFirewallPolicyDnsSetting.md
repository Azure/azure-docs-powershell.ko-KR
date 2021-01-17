---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 137c12a8de58c5daa8fbd3f997aa6fd8f3e04caa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361523"
---
# <span data-ttu-id="352e6-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="352e6-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="352e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="352e6-102">SYNOPSIS</span></span>
<span data-ttu-id="352e6-103">Azure Firewall 정책에 대한 새 DNS 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="352e6-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="352e6-104">구문</span><span class="sxs-lookup"><span data-stu-id="352e6-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-Server <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="352e6-105">설명</span><span class="sxs-lookup"><span data-stu-id="352e6-105">DESCRIPTION</span></span>
<span data-ttu-id="352e6-106">**New-AzFirewallPolicyDnsSetting** cmdlet은 Azure Firewall 정책에 대한 DNS 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="352e6-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="352e6-107">예제</span><span class="sxs-lookup"><span data-stu-id="352e6-107">EXAMPLES</span></span>

### <span data-ttu-id="352e6-108">1. 빈 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="352e6-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="352e6-109">이 예제에서는 DNS 프록시를 사용하도록 설정하여 dns 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="352e6-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="352e6-110">2. ThreatIntel 모드로 빈 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="352e6-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```

<span data-ttu-id="352e6-111">이 예제에서는 DNS 프록시를 사용하도록 설정하고 사용자 지정 DNS 서버를 설정하는 DNS 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="352e6-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="352e6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="352e6-112">PARAMETERS</span></span>

### <span data-ttu-id="352e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="352e6-113">-DefaultProfile</span></span>
<span data-ttu-id="352e6-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="352e6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="352e6-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="352e6-115">-EnableProxy</span></span>
<span data-ttu-id="352e6-116">DNS 프록시를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="352e6-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="352e6-117">기본적으로 사용하지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="352e6-117">By default it is disabled.</span></span>

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

### <span data-ttu-id="352e6-118">-Server</span><span class="sxs-lookup"><span data-stu-id="352e6-118">-Server</span></span>
<span data-ttu-id="352e6-119">DNS 서버 목록</span><span class="sxs-lookup"><span data-stu-id="352e6-119">The list of DNS Servers</span></span>

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

### <span data-ttu-id="352e6-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="352e6-120">-Confirm</span></span>
<span data-ttu-id="352e6-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="352e6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="352e6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="352e6-122">-WhatIf</span></span>
<span data-ttu-id="352e6-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="352e6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="352e6-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="352e6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="352e6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="352e6-125">CommonParameters</span></span>
<span data-ttu-id="352e6-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="352e6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="352e6-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="352e6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="352e6-128">입력</span><span class="sxs-lookup"><span data-stu-id="352e6-128">INPUTS</span></span>

### <span data-ttu-id="352e6-129">없음</span><span class="sxs-lookup"><span data-stu-id="352e6-129">None</span></span>

## <span data-ttu-id="352e6-130">출력</span><span class="sxs-lookup"><span data-stu-id="352e6-130">OUTPUTS</span></span>

### <span data-ttu-id="352e6-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="352e6-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="352e6-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="352e6-132">NOTES</span></span>

## <span data-ttu-id="352e6-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="352e6-133">RELATED LINKS</span></span>
