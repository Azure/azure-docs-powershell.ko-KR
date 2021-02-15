---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 3cffe65b1b8e4ba811ee00b7537dc95d9d6dfb72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189508"
---
# <span data-ttu-id="522a5-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="522a5-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="522a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="522a5-102">SYNOPSIS</span></span>
<span data-ttu-id="522a5-103">수정된 Azure 방화벽 정책을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="522a5-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="522a5-104">구문</span><span class="sxs-lookup"><span data-stu-id="522a5-104">SYNTAX</span></span>

### <span data-ttu-id="522a5-105">SetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="522a5-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="522a5-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="522a5-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="522a5-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="522a5-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="522a5-108">설명</span><span class="sxs-lookup"><span data-stu-id="522a5-108">DESCRIPTION</span></span>
<span data-ttu-id="522a5-109">**Set-AzFirewallPolicy** cmdlet은 Azure Firewall 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="522a5-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="522a5-110">예제</span><span class="sxs-lookup"><span data-stu-id="522a5-110">EXAMPLES</span></span>

### <span data-ttu-id="522a5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="522a5-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="522a5-112">이 예제에서는 새 방화벽 정책 값으로 방화벽 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="522a5-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="522a5-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="522a5-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="522a5-114">이 예제에서는 새 위협 Intel 모드로 방화벽 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="522a5-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="522a5-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="522a5-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="522a5-116">이 예제에서는 새 위협 Intel 허용 목록을 통해 방화벽 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="522a5-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="522a5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="522a5-117">PARAMETERS</span></span>

### <span data-ttu-id="522a5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="522a5-118">-AsJob</span></span>
<span data-ttu-id="522a5-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="522a5-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="522a5-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="522a5-120">-BasePolicy</span></span>
<span data-ttu-id="522a5-121">상속할 기본 정책</span><span class="sxs-lookup"><span data-stu-id="522a5-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="522a5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="522a5-122">-DefaultProfile</span></span>
<span data-ttu-id="522a5-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="522a5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="522a5-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="522a5-124">-DnsSetting</span></span>
<span data-ttu-id="522a5-125">DNS 설정</span><span class="sxs-lookup"><span data-stu-id="522a5-125">The DNS Setting</span></span>

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

### <span data-ttu-id="522a5-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="522a5-126">-InputObject</span></span>
<span data-ttu-id="522a5-127">AzureFirewall 정책</span><span class="sxs-lookup"><span data-stu-id="522a5-127">The AzureFirewall Policy</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="522a5-128">-Location</span><span class="sxs-lookup"><span data-stu-id="522a5-128">-Location</span></span>
<span data-ttu-id="522a5-129">위치.</span><span class="sxs-lookup"><span data-stu-id="522a5-129">location.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="522a5-130">-Name</span><span class="sxs-lookup"><span data-stu-id="522a5-130">-Name</span></span>
<span data-ttu-id="522a5-131">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="522a5-131">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="522a5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="522a5-132">-ResourceGroupName</span></span>
<span data-ttu-id="522a5-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="522a5-133">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="522a5-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="522a5-134">-ResourceId</span></span>
<span data-ttu-id="522a5-135">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="522a5-135">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="522a5-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="522a5-136">-Tag</span></span>
<span data-ttu-id="522a5-137">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="522a5-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="522a5-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="522a5-138">-ThreatIntelMode</span></span>
<span data-ttu-id="522a5-139">위협 인텔리전스에 대한 작업 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="522a5-139">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="522a5-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="522a5-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="522a5-141">위협 인텔리전스에 대한 화이트리스트</span><span class="sxs-lookup"><span data-stu-id="522a5-141">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="522a5-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="522a5-142">-Confirm</span></span>
<span data-ttu-id="522a5-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="522a5-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="522a5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="522a5-144">-WhatIf</span></span>
<span data-ttu-id="522a5-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="522a5-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="522a5-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="522a5-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="522a5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="522a5-147">CommonParameters</span></span>
<span data-ttu-id="522a5-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="522a5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="522a5-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="522a5-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="522a5-150">입력</span><span class="sxs-lookup"><span data-stu-id="522a5-150">INPUTS</span></span>

### <span data-ttu-id="522a5-151">System.String</span><span class="sxs-lookup"><span data-stu-id="522a5-151">System.String</span></span>

### <span data-ttu-id="522a5-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="522a5-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="522a5-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="522a5-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="522a5-154">출력</span><span class="sxs-lookup"><span data-stu-id="522a5-154">OUTPUTS</span></span>

### <span data-ttu-id="522a5-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="522a5-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="522a5-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="522a5-156">NOTES</span></span>

## <span data-ttu-id="522a5-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="522a5-157">RELATED LINKS</span></span>
