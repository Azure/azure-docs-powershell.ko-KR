---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 17aea8ab38582373420107df87e2b6837a83a1a4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339957"
---
# <span data-ttu-id="e9885-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e9885-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="e9885-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9885-102">SYNOPSIS</span></span>
<span data-ttu-id="e9885-103">새 Azure Firewall 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9885-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="e9885-104">구문</span><span class="sxs-lookup"><span data-stu-id="e9885-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9885-105">설명</span><span class="sxs-lookup"><span data-stu-id="e9885-105">DESCRIPTION</span></span>
<span data-ttu-id="e9885-106">**New-AzFirewallPolicy** cmdlet은 Azure Firewall 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9885-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="e9885-107">예제</span><span class="sxs-lookup"><span data-stu-id="e9885-107">EXAMPLES</span></span>

### <span data-ttu-id="e9885-108">예제 1: 1.</span><span class="sxs-lookup"><span data-stu-id="e9885-108">Example 1: 1.</span></span> <span data-ttu-id="e9885-109">빈 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="e9885-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="e9885-110">이 예제에서는 Azure 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9885-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="e9885-111">예제 2: 2.</span><span class="sxs-lookup"><span data-stu-id="e9885-111">Example 2: 2.</span></span> <span data-ttu-id="e9885-112">ThreatIntel 모드로 빈 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="e9885-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="e9885-113">이 예제에서는 위협 인텔리전스 모드로 Azure 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9885-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="e9885-114">예제 3: 3.</span><span class="sxs-lookup"><span data-stu-id="e9885-114">Example 3: 3.</span></span> <span data-ttu-id="e9885-115">ThreatIntel Whitelist를 사용하여 빈 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="e9885-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="e9885-116">이 예제에서는 위협 인텔리전스 허용 목록을 사용하여 Azure 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e9885-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

## <span data-ttu-id="e9885-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9885-117">PARAMETERS</span></span>

### <span data-ttu-id="e9885-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9885-118">-AsJob</span></span>
<span data-ttu-id="e9885-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e9885-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9885-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="e9885-120">-BasePolicy</span></span>
<span data-ttu-id="e9885-121">상속할 기본 정책</span><span class="sxs-lookup"><span data-stu-id="e9885-121">The base policy to inherit from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9885-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9885-122">-DefaultProfile</span></span>
<span data-ttu-id="e9885-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9885-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9885-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e9885-124">-Force</span></span>
<span data-ttu-id="e9885-125">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9885-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9885-126">-Location</span><span class="sxs-lookup"><span data-stu-id="e9885-126">-Location</span></span>
<span data-ttu-id="e9885-127">위치.</span><span class="sxs-lookup"><span data-stu-id="e9885-127">location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9885-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e9885-128">-Name</span></span>
<span data-ttu-id="e9885-129">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9885-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9885-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9885-130">-ResourceGroupName</span></span>
<span data-ttu-id="e9885-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e9885-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9885-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="e9885-132">-Tag</span></span>
<span data-ttu-id="e9885-133">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e9885-133">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9885-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="e9885-134">-ThreatIntelMode</span></span>
<span data-ttu-id="e9885-135">위협 인텔리전스에 대한 작업 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="e9885-135">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9885-136">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="e9885-136">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="e9885-137">위협 인텔리전스에 대한 화이트리스트</span><span class="sxs-lookup"><span data-stu-id="e9885-137">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallPolicyThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9885-138">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="e9885-138">-DnsSetting</span></span>
<span data-ttu-id="e9885-139">DNS 설정</span><span class="sxs-lookup"><span data-stu-id="e9885-139">The DNS Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyDnsSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9885-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9885-140">-Confirm</span></span>
<span data-ttu-id="e9885-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e9885-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9885-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9885-142">-WhatIf</span></span>
<span data-ttu-id="e9885-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e9885-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9885-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9885-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9885-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9885-145">CommonParameters</span></span>
<span data-ttu-id="e9885-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e9885-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9885-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e9885-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9885-148">입력</span><span class="sxs-lookup"><span data-stu-id="e9885-148">INPUTS</span></span>

### <span data-ttu-id="e9885-149">System.String</span><span class="sxs-lookup"><span data-stu-id="e9885-149">System.String</span></span>

### <span data-ttu-id="e9885-150">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e9885-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e9885-151">출력</span><span class="sxs-lookup"><span data-stu-id="e9885-151">OUTPUTS</span></span>

### <span data-ttu-id="e9885-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="e9885-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="e9885-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e9885-153">NOTES</span></span>

## <span data-ttu-id="e9885-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9885-154">RELATED LINKS</span></span>
