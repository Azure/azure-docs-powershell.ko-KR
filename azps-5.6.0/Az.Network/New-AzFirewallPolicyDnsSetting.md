---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicydnssetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyDnsSetting.md
ms.openlocfilehash: 35b56e6aafe73c09343fb17d385dd7ab4c705c5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985768"
---
# <span data-ttu-id="ca898-101">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="ca898-101">New-AzFirewallPolicyDnsSetting</span></span>

## <span data-ttu-id="ca898-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca898-102">SYNOPSIS</span></span>
<span data-ttu-id="ca898-103">Azure 방화벽 정책에 대한 새 DNS 설정 생성</span><span class="sxs-lookup"><span data-stu-id="ca898-103">Creates a new DNS Setting for Azure Firewall Policy</span></span>

## <span data-ttu-id="ca898-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca898-104">SYNTAX</span></span>

```
New-AzFirewallPolicyDnsSetting [-EnableProxy] [-Server <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca898-105">설명</span><span class="sxs-lookup"><span data-stu-id="ca898-105">DESCRIPTION</span></span>
<span data-ttu-id="ca898-106">**New-AzFirewallPolicyDnsSetting** cmdlet은 Azure 방화벽 정책에 대한 DNS 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca898-106">The **New-AzFirewallPolicyDnsSetting** cmdlet creates a DNS Setting Object for Azure Firewall Policy</span></span>

## <span data-ttu-id="ca898-107">예제</span><span class="sxs-lookup"><span data-stu-id="ca898-107">EXAMPLES</span></span>

### <span data-ttu-id="ca898-108">1. 빈 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="ca898-108">1. Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy
```

<span data-ttu-id="ca898-109">이 예제에서는 dns 프록시를 사용하도록 설정하는 dns 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca898-109">This example creates a dns Setting object with setting enabling dns proxy.</span></span>

### <span data-ttu-id="ca898-110">2. ThreatIntel 모드로 빈 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="ca898-110">2. Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> $dnsServers = @("10.10.10.1", "20.20.20.2")
PS C:\> New-AzFirewallPolicyDnsSetting -EnableProxy -Server $dnsServers
```

<span data-ttu-id="ca898-111">이 예제에서는 dns 프록시를 사용하도록 설정하고 사용자 지정 dns 서버를 설정하는 dns 설정 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca898-111">This example creates a dns Setting object with setting enabling dns proxy and setting custom dns servers.</span></span>

## <span data-ttu-id="ca898-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ca898-112">PARAMETERS</span></span>

### <span data-ttu-id="ca898-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca898-113">-DefaultProfile</span></span>
<span data-ttu-id="ca898-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca898-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca898-115">-EnableProxy</span><span class="sxs-lookup"><span data-stu-id="ca898-115">-EnableProxy</span></span>
<span data-ttu-id="ca898-116">DNS 프록시를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca898-116">Enable DNS Proxy.</span></span>
<span data-ttu-id="ca898-117">기본적으로 사용하지 않도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca898-117">By default it is disabled.</span></span>

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

### <span data-ttu-id="ca898-118">-Server</span><span class="sxs-lookup"><span data-stu-id="ca898-118">-Server</span></span>
<span data-ttu-id="ca898-119">DNS 서버 목록</span><span class="sxs-lookup"><span data-stu-id="ca898-119">The list of DNS Servers</span></span>

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

### <span data-ttu-id="ca898-120">-확인</span><span class="sxs-lookup"><span data-stu-id="ca898-120">-Confirm</span></span>
<span data-ttu-id="ca898-121">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca898-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca898-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca898-122">-WhatIf</span></span>
<span data-ttu-id="ca898-123">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ca898-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca898-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca898-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca898-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca898-125">CommonParameters</span></span>
<span data-ttu-id="ca898-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca898-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca898-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca898-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca898-128">입력</span><span class="sxs-lookup"><span data-stu-id="ca898-128">INPUTS</span></span>

### <span data-ttu-id="ca898-129">없음</span><span class="sxs-lookup"><span data-stu-id="ca898-129">None</span></span>

## <span data-ttu-id="ca898-130">출력</span><span class="sxs-lookup"><span data-stu-id="ca898-130">OUTPUTS</span></span>

### <span data-ttu-id="ca898-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span><span class="sxs-lookup"><span data-stu-id="ca898-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyDnsSettings</span></span>

## <span data-ttu-id="ca898-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca898-132">NOTES</span></span>

## <span data-ttu-id="ca898-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca898-133">RELATED LINKS</span></span>
