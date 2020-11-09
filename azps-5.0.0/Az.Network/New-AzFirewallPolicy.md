---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 17aea8ab38582373420107df87e2b6837a83a1a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309585"
---
# <span data-ttu-id="744f7-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="744f7-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="744f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="744f7-102">SYNOPSIS</span></span>
<span data-ttu-id="744f7-103">새 Azure 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="744f7-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="744f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="744f7-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="744f7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="744f7-105">DESCRIPTION</span></span>
<span data-ttu-id="744f7-106">**새 AzFirewallPolicy** Cmdlet은 Azure 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="744f7-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="744f7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="744f7-107">EXAMPLES</span></span>

### <span data-ttu-id="744f7-108">예제 1:1.</span><span class="sxs-lookup"><span data-stu-id="744f7-108">Example 1: 1.</span></span> <span data-ttu-id="744f7-109">빈 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="744f7-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="744f7-110">이 예제에서는 azure 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="744f7-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="744f7-111">예제 2:2.</span><span class="sxs-lookup"><span data-stu-id="744f7-111">Example 2: 2.</span></span> <span data-ttu-id="744f7-112">ThreatIntel 모드를 사용 하 여 빈 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="744f7-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="744f7-113">이 예제에서는 위협 intel 모드를 사용 하 여 azure 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="744f7-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="744f7-114">예제 3:3.</span><span class="sxs-lookup"><span data-stu-id="744f7-114">Example 3: 3.</span></span> <span data-ttu-id="744f7-115">ThreatIntel 허용 목록를 사용 하 여 빈 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="744f7-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="744f7-116">이 예제에서는 위협 intel 허용 목록을 사용 하 여 azure 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="744f7-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

## <span data-ttu-id="744f7-117">변수</span><span class="sxs-lookup"><span data-stu-id="744f7-117">PARAMETERS</span></span>

### <span data-ttu-id="744f7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="744f7-118">-AsJob</span></span>
<span data-ttu-id="744f7-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="744f7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="744f7-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="744f7-120">-BasePolicy</span></span>
<span data-ttu-id="744f7-121">상속할 기본 정책</span><span class="sxs-lookup"><span data-stu-id="744f7-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="744f7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="744f7-122">-DefaultProfile</span></span>
<span data-ttu-id="744f7-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="744f7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="744f7-124">-Force</span><span class="sxs-lookup"><span data-stu-id="744f7-124">-Force</span></span>
<span data-ttu-id="744f7-125">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="744f7-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="744f7-126">-위치</span><span class="sxs-lookup"><span data-stu-id="744f7-126">-Location</span></span>
<span data-ttu-id="744f7-127">location.</span><span class="sxs-lookup"><span data-stu-id="744f7-127">location.</span></span>

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

### <span data-ttu-id="744f7-128">-이름</span><span class="sxs-lookup"><span data-stu-id="744f7-128">-Name</span></span>
<span data-ttu-id="744f7-129">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="744f7-129">The resource name.</span></span>

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

### <span data-ttu-id="744f7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="744f7-130">-ResourceGroupName</span></span>
<span data-ttu-id="744f7-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="744f7-131">The resource group name.</span></span>

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

### <span data-ttu-id="744f7-132">태그</span><span class="sxs-lookup"><span data-stu-id="744f7-132">-Tag</span></span>
<span data-ttu-id="744f7-133">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="744f7-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="744f7-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="744f7-134">-ThreatIntelMode</span></span>
<span data-ttu-id="744f7-135">위협 인텔리전스의 작동 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="744f7-135">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="744f7-136">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="744f7-136">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="744f7-137">위협 인텔리전스의 허용 목록</span><span class="sxs-lookup"><span data-stu-id="744f7-137">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="744f7-138">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="744f7-138">-DnsSetting</span></span>
<span data-ttu-id="744f7-139">DNS 설정</span><span class="sxs-lookup"><span data-stu-id="744f7-139">The DNS Setting</span></span>

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

### <span data-ttu-id="744f7-140">-확인</span><span class="sxs-lookup"><span data-stu-id="744f7-140">-Confirm</span></span>
<span data-ttu-id="744f7-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="744f7-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="744f7-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="744f7-142">-WhatIf</span></span>
<span data-ttu-id="744f7-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="744f7-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="744f7-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="744f7-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="744f7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="744f7-145">CommonParameters</span></span>
<span data-ttu-id="744f7-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="744f7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="744f7-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="744f7-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="744f7-148">입력</span><span class="sxs-lookup"><span data-stu-id="744f7-148">INPUTS</span></span>

### <span data-ttu-id="744f7-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="744f7-149">System.String</span></span>

### <span data-ttu-id="744f7-150">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="744f7-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="744f7-151">출력</span><span class="sxs-lookup"><span data-stu-id="744f7-151">OUTPUTS</span></span>

### <span data-ttu-id="744f7-152">Microsoft. \* PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="744f7-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="744f7-153">상속자</span><span class="sxs-lookup"><span data-stu-id="744f7-153">NOTES</span></span>

## <span data-ttu-id="744f7-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="744f7-154">RELATED LINKS</span></span>
