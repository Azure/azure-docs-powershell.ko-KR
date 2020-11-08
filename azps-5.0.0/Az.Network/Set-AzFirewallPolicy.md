---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 3cffe65b1b8e4ba811ee00b7537dc95d9d6dfb72
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226336"
---
# <span data-ttu-id="7c393-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="7c393-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="7c393-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c393-102">SYNOPSIS</span></span>
<span data-ttu-id="7c393-103">수정 된 azure 방화벽 정책 저장</span><span class="sxs-lookup"><span data-stu-id="7c393-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="7c393-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c393-104">SYNTAX</span></span>

### <span data-ttu-id="7c393-105">SetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c393-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c393-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c393-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c393-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c393-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c393-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7c393-108">DESCRIPTION</span></span>
<span data-ttu-id="7c393-109">**AzFirewallPolicy** Cmdlet은 Azure 방화벽 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c393-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="7c393-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7c393-110">EXAMPLES</span></span>

### <span data-ttu-id="7c393-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c393-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="7c393-112">이 예제에서는 새 방화벽 정책 값을 사용 하 여 방화벽 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c393-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="7c393-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="7c393-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="7c393-114">이 예제에서는 새 위협 intel 모드를 사용 하 여 방화벽 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c393-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="7c393-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="7c393-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="7c393-116">이 예제에서는 새 위협으로 방화벽 정책을 설정 합니다. intel 허용 목록</span><span class="sxs-lookup"><span data-stu-id="7c393-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="7c393-117">변수</span><span class="sxs-lookup"><span data-stu-id="7c393-117">PARAMETERS</span></span>

### <span data-ttu-id="7c393-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c393-118">-AsJob</span></span>
<span data-ttu-id="7c393-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7c393-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c393-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="7c393-120">-BasePolicy</span></span>
<span data-ttu-id="7c393-121">상속할 기본 정책</span><span class="sxs-lookup"><span data-stu-id="7c393-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="7c393-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c393-122">-DefaultProfile</span></span>
<span data-ttu-id="7c393-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c393-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c393-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="7c393-124">-DnsSetting</span></span>
<span data-ttu-id="7c393-125">DNS 설정</span><span class="sxs-lookup"><span data-stu-id="7c393-125">The DNS Setting</span></span>

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

### <span data-ttu-id="7c393-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c393-126">-InputObject</span></span>
<span data-ttu-id="7c393-127">AzureFirewall 정책</span><span class="sxs-lookup"><span data-stu-id="7c393-127">The AzureFirewall Policy</span></span>

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

### <span data-ttu-id="7c393-128">-위치</span><span class="sxs-lookup"><span data-stu-id="7c393-128">-Location</span></span>
<span data-ttu-id="7c393-129">location.</span><span class="sxs-lookup"><span data-stu-id="7c393-129">location.</span></span>

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

### <span data-ttu-id="7c393-130">-이름</span><span class="sxs-lookup"><span data-stu-id="7c393-130">-Name</span></span>
<span data-ttu-id="7c393-131">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c393-131">The resource name.</span></span>

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

### <span data-ttu-id="7c393-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c393-132">-ResourceGroupName</span></span>
<span data-ttu-id="7c393-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c393-133">The resource group name.</span></span>

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

### <span data-ttu-id="7c393-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c393-134">-ResourceId</span></span>
<span data-ttu-id="7c393-135">리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="7c393-135">The resource Id.</span></span>

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

### <span data-ttu-id="7c393-136">태그</span><span class="sxs-lookup"><span data-stu-id="7c393-136">-Tag</span></span>
<span data-ttu-id="7c393-137">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="7c393-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7c393-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="7c393-138">-ThreatIntelMode</span></span>
<span data-ttu-id="7c393-139">위협 인텔리전스의 작동 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="7c393-139">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="7c393-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="7c393-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="7c393-141">위협 인텔리전스의 허용 목록</span><span class="sxs-lookup"><span data-stu-id="7c393-141">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="7c393-142">-확인</span><span class="sxs-lookup"><span data-stu-id="7c393-142">-Confirm</span></span>
<span data-ttu-id="7c393-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c393-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c393-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c393-144">-WhatIf</span></span>
<span data-ttu-id="7c393-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c393-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c393-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c393-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c393-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c393-147">CommonParameters</span></span>
<span data-ttu-id="7c393-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c393-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c393-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c393-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c393-150">입력</span><span class="sxs-lookup"><span data-stu-id="7c393-150">INPUTS</span></span>

### <span data-ttu-id="7c393-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7c393-151">System.String</span></span>

### <span data-ttu-id="7c393-152">PSAzureFirewallPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7c393-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="7c393-153">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="7c393-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7c393-154">출력</span><span class="sxs-lookup"><span data-stu-id="7c393-154">OUTPUTS</span></span>

### <span data-ttu-id="7c393-155">Microsoft. \* PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="7c393-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="7c393-156">상속자</span><span class="sxs-lookup"><span data-stu-id="7c393-156">NOTES</span></span>

## <span data-ttu-id="7c393-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c393-157">RELATED LINKS</span></span>
