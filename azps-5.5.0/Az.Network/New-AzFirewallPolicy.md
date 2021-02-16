---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 0e3a9b99a23715b63eb42c83ba112776272969ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179700"
---
# <span data-ttu-id="57757-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="57757-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="57757-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57757-102">SYNOPSIS</span></span>
<span data-ttu-id="57757-103">새 Azure Firewall 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57757-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="57757-104">구문</span><span class="sxs-lookup"><span data-stu-id="57757-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-IntrusionDetection <PSAzureFirewallPolicyIntrusionDetection>] [-TransportSecurityName <String>]
 [-TransportSecurityKeyVaultSecretId <String>] [-SkuTier <String>] [-UserAssignedIdentityId <String>]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57757-105">설명</span><span class="sxs-lookup"><span data-stu-id="57757-105">DESCRIPTION</span></span>
<span data-ttu-id="57757-106">**New-AzFirewallPolicy** cmdlet은 Azure Firewall 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57757-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="57757-107">예제</span><span class="sxs-lookup"><span data-stu-id="57757-107">EXAMPLES</span></span>

### <span data-ttu-id="57757-108">예제 1: 1.</span><span class="sxs-lookup"><span data-stu-id="57757-108">Example 1: 1.</span></span> <span data-ttu-id="57757-109">빈 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="57757-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="57757-110">이 예제에서는 Azure 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57757-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="57757-111">예제 2: 2.</span><span class="sxs-lookup"><span data-stu-id="57757-111">Example 2: 2.</span></span> <span data-ttu-id="57757-112">ThreatIntel 모드로 빈 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="57757-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="57757-113">이 예제에서는 위협 인텔리전스 모드로 Azure 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57757-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="57757-114">예제 3: 3.</span><span class="sxs-lookup"><span data-stu-id="57757-114">Example 3: 3.</span></span> <span data-ttu-id="57757-115">ThreatIntel Whitelist를 사용하여 빈 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="57757-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="57757-116">이 예제에서는 위협 인텔리전스 허용 목록을 사용하여 Azure 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57757-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

### <span data-ttu-id="57757-117">예제 4: 4.</span><span class="sxs-lookup"><span data-stu-id="57757-117">Example 4: 4.</span></span> <span data-ttu-id="57757-118">침입 검색, ID 및 전송 보안을 사용하여 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="57757-118">Create policy with intrusion detection, identity and transport security</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride -BypassTraffic $bypass
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/TestRg/providers/Microsoft.ManagedIdentity/userAssignedIdentities/user-assign-identity'
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection -TransportSecurityName tsName -TransportSecurityKeyVaultSecretId "https://<keyvaultname>.vault.azure.net/secrets/cacert"  -UserAssignedIdentityId $userAssignedIdentity
```

<span data-ttu-id="57757-119">이 예제에서는 모드 경고, 사용자 할당 ID 및 전송 보안의 침입 감지를 사용하여 Azure 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57757-119">This example creates an azure firewall policy with a intrusion detection in mode alert, user assigned identity and transport security</span></span>

## <span data-ttu-id="57757-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57757-120">PARAMETERS</span></span>

### <span data-ttu-id="57757-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57757-121">-AsJob</span></span>
<span data-ttu-id="57757-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="57757-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57757-123">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="57757-123">-BasePolicy</span></span>
<span data-ttu-id="57757-124">상속할 기본 정책</span><span class="sxs-lookup"><span data-stu-id="57757-124">The base policy to inherit from</span></span>

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

### <span data-ttu-id="57757-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57757-125">-DefaultProfile</span></span>
<span data-ttu-id="57757-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57757-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57757-127">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="57757-127">-DnsSetting</span></span>
<span data-ttu-id="57757-128">DNS 설정</span><span class="sxs-lookup"><span data-stu-id="57757-128">The DNS Setting</span></span>

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

### <span data-ttu-id="57757-129">-Force</span><span class="sxs-lookup"><span data-stu-id="57757-129">-Force</span></span>
<span data-ttu-id="57757-130">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57757-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="57757-131">-Identity</span><span class="sxs-lookup"><span data-stu-id="57757-131">-Identity</span></span>
<span data-ttu-id="57757-132">방화벽 정책에 할당할 방화벽 정책 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="57757-132">Firewall Policy Identity to be assigned to Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57757-133">-IntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="57757-133">-IntrusionDetection</span></span>
<span data-ttu-id="57757-134">침입 감지 설정</span><span class="sxs-lookup"><span data-stu-id="57757-134">The Intrusion Detection Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetection
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57757-135">-Location</span><span class="sxs-lookup"><span data-stu-id="57757-135">-Location</span></span>
<span data-ttu-id="57757-136">위치.</span><span class="sxs-lookup"><span data-stu-id="57757-136">location.</span></span>

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

### <span data-ttu-id="57757-137">-Name</span><span class="sxs-lookup"><span data-stu-id="57757-137">-Name</span></span>
<span data-ttu-id="57757-138">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57757-138">The resource name.</span></span>

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

### <span data-ttu-id="57757-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57757-139">-ResourceGroupName</span></span>
<span data-ttu-id="57757-140">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57757-140">The resource group name.</span></span>

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

### <span data-ttu-id="57757-141">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="57757-141">-SkuTier</span></span>
<span data-ttu-id="57757-142">방화벽 정책 SKU 계층</span><span class="sxs-lookup"><span data-stu-id="57757-142">Firewall policy sku tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57757-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="57757-143">-Tag</span></span>
<span data-ttu-id="57757-144">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="57757-144">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="57757-145">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="57757-145">-ThreatIntelMode</span></span>
<span data-ttu-id="57757-146">위협 인텔리전스에 대한 작업 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="57757-146">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="57757-147">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="57757-147">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="57757-148">위협 인텔리전스에 대한 화이트리스트</span><span class="sxs-lookup"><span data-stu-id="57757-148">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="57757-149">-TransportSecurityKeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="57757-149">-TransportSecurityKeyVaultSecretId</span></span>
<span data-ttu-id="57757-150">KeyVault에 저장된 (base-64로 인코딩되지 않은 pfx) 'Secret' 또는 'Certificate' 개체의 비밀 ID</span><span class="sxs-lookup"><span data-stu-id="57757-150">Secret Id of (base-64 encoded unencrypted pfx) 'Secret' or 'Certificate' object stored in KeyVault</span></span>

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

### <span data-ttu-id="57757-151">-TransportSecurityName</span><span class="sxs-lookup"><span data-stu-id="57757-151">-TransportSecurityName</span></span>
<span data-ttu-id="57757-152">전송 보안 이름</span><span class="sxs-lookup"><span data-stu-id="57757-152">Transport security name</span></span>

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

### <span data-ttu-id="57757-153">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="57757-153">-UserAssignedIdentityId</span></span>
<span data-ttu-id="57757-154">방화벽 정책에 할당할 사용자 할당 ID의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="57757-154">ResourceId of the user assigned identity to be assigned to Firewall Policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57757-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57757-155">-Confirm</span></span>
<span data-ttu-id="57757-156">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="57757-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57757-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57757-157">-WhatIf</span></span>
<span data-ttu-id="57757-158">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="57757-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57757-159">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57757-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57757-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57757-160">CommonParameters</span></span>
<span data-ttu-id="57757-161">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="57757-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57757-162">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="57757-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57757-163">입력</span><span class="sxs-lookup"><span data-stu-id="57757-163">INPUTS</span></span>

### <span data-ttu-id="57757-164">System.String</span><span class="sxs-lookup"><span data-stu-id="57757-164">System.String</span></span>

### <span data-ttu-id="57757-165">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="57757-165">System.Collections.Hashtable</span></span>

## <span data-ttu-id="57757-166">출력</span><span class="sxs-lookup"><span data-stu-id="57757-166">OUTPUTS</span></span>

### <span data-ttu-id="57757-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="57757-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="57757-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="57757-168">NOTES</span></span>

## <span data-ttu-id="57757-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57757-169">RELATED LINKS</span></span>
