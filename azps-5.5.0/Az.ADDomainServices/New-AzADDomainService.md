---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/new-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
ms.openlocfilehash: 977621a3f92a8239925494102aed8c672509b222
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176601"
---
# <span data-ttu-id="38474-101">New-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="38474-101">New-AzADDomainService</span></span>

## <span data-ttu-id="38474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38474-102">SYNOPSIS</span></span>
<span data-ttu-id="38474-103">도메인 서비스 만들기 작업은 지정된 매개 변수를 사용하여 새 도메인 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38474-103">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="38474-104">특정 서비스가 이미 있는 경우 패치 가능한 속성이 업데이트되어 변경 불가능한 속성은 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38474-104">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="38474-105">구문</span><span class="sxs-lookup"><span data-stu-id="38474-105">SYNTAX</span></span>

```
New-AzADDomainService -Name <String> -ResourceGroupName <String> -DomainName <String>
 -ReplicaSet <IReplicaSet[]> [-SubscriptionId <String>] [-DomainConfigurationType <String>]
 [-DomainSecuritySettingNtlmV1 <String>] [-DomainSecuritySettingSyncKerberosPassword <String>]
 [-DomainSecuritySettingSyncNtlmPassword <String>] [-DomainSecuritySettingSyncOnPremPassword <String>]
 [-DomainSecuritySettingTlsV1 <String>] [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>]
 [-LdapSettingExternalAccess <String>] [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="38474-106">설명</span><span class="sxs-lookup"><span data-stu-id="38474-106">DESCRIPTION</span></span>
<span data-ttu-id="38474-107">도메인 서비스 만들기 작업은 지정된 매개 변수를 사용하여 새 도메인 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38474-107">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="38474-108">특정 서비스가 이미 있는 경우 패치 가능한 속성이 업데이트되어 변경 불가능한 속성은 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38474-108">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="38474-109">예제</span><span class="sxs-lookup"><span data-stu-id="38474-109">EXAMPLES</span></span>

### <span data-ttu-id="38474-110">예제 1: 새 ADDomainService 만들기</span><span class="sxs-lookup"><span data-stu-id="38474-110">Example 1: Create new ADDomainService</span></span>
```powershell
PS C:\> $replicaSet = New-AzADDomainServiceReplicaSetObject -Location westus -SubnetId /subscriptions/********-****-****-****-**********/resourceGroups/yishitest/providers/Microsoft.Network/virtualNetworks/aadds-vnet/subnets/default
New-AzADDomainService -name youriADdomain -ResourceGroupName youriAddomain -DomainName youriAddomain.com -ReplicaSet $replicaSet -debug

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="38474-111">새 ADDomainService 만들기</span><span class="sxs-lookup"><span data-stu-id="38474-111">Create new ADDomainService</span></span>

## <span data-ttu-id="38474-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38474-112">PARAMETERS</span></span>

### <span data-ttu-id="38474-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38474-113">-AsJob</span></span>
<span data-ttu-id="38474-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="38474-114">Run the command as a job</span></span>

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

### <span data-ttu-id="38474-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38474-115">-DefaultProfile</span></span>
<span data-ttu-id="38474-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38474-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-117">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="38474-117">-DomainConfigurationType</span></span>
<span data-ttu-id="38474-118">도메인 구성 유형</span><span class="sxs-lookup"><span data-stu-id="38474-118">Domain Configuration Type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-119">-DomainName</span><span class="sxs-lookup"><span data-stu-id="38474-119">-DomainName</span></span>
<span data-ttu-id="38474-120">사용자가 Domain Services를 배포할 Azure 도메인의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38474-120">The name of the Azure domain that the user would like to deploy Domain Services to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-121">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="38474-121">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="38474-122">NtlmV1을 사용하도록 설정하거나 사용하지 않도록 설정할지 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="38474-122">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-123">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="38474-123">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="38474-124">SyncKerberosPasswords의 사용 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="38474-124">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-125">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="38474-125">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="38474-126">SyncNtlmPasswords의 사용 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="38474-126">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-127">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="38474-127">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="38474-128">SyncOnPremPasswords의 사용 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="38474-128">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-129">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="38474-129">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="38474-130">TlsV1을 사용하도록 설정하거나 사용하지 않도록 설정할지 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="38474-130">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-131">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="38474-131">-FilteredSync</span></span>
<span data-ttu-id="38474-132">그룹 기반 필터링된 동기화를 켜는 활성화 또는 사용 안 하여 플래그</span><span class="sxs-lookup"><span data-stu-id="38474-132">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-133">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="38474-133">-ForestTrust</span></span>
<span data-ttu-id="38474-134">구성할 리소스 포리스트에 대한 설정 목록은 FORESTTRUST 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="38474-134">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IForestTrust[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-135">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="38474-135">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="38474-136">인터넷을 통해 LDAP 액세스를 보호할지 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="38474-136">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-137">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="38474-137">-LdapSettingLdaps</span></span>
<span data-ttu-id="38474-138">보안 LDAP를 사용하도록 설정하거나 사용하지 않도록 설정할지 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="38474-138">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-139">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="38474-139">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="38474-140">보안 LDAP를 구성하는 데 필요한 인증서입니다.</span><span class="sxs-lookup"><span data-stu-id="38474-140">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="38474-141">여기에 전달된 매개 변수는 인증서 pfx 파일의 base64로 인코딩된 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="38474-141">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-142">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="38474-142">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="38474-143">제공된 보안 LDAP 인증서 pfx 파일의 암호를 해독하는 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="38474-143">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-144">-Name</span><span class="sxs-lookup"><span data-stu-id="38474-144">-Name</span></span>
<span data-ttu-id="38474-145">도메인 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38474-145">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-146">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="38474-146">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="38474-147">추가 받는 사람 목록</span><span class="sxs-lookup"><span data-stu-id="38474-147">The list of additional recipients</span></span>

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

### <span data-ttu-id="38474-148">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="38474-148">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="38474-149">도메인 컨트롤러 관리자에게 알림을 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="38474-149">Should domain controller admins be notified</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-150">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="38474-150">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="38474-151">전역 관리자에게 알림을 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="38474-151">Should global admins be notified</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-152">-NoWait</span><span class="sxs-lookup"><span data-stu-id="38474-152">-NoWait</span></span>
<span data-ttu-id="38474-153">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="38474-153">Run the command asynchronously</span></span>

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

### <span data-ttu-id="38474-154">-ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="38474-154">-ReplicaSet</span></span>
<span data-ttu-id="38474-155">생성할 ReplicaSets 목록은 REPLICASET 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="38474-155">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IReplicaSet[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-156">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="38474-156">-ResourceForest</span></span>
<span data-ttu-id="38474-157">리소스 포리스트</span><span class="sxs-lookup"><span data-stu-id="38474-157">Resource Forest</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38474-158">-ResourceGroupName</span></span>
<span data-ttu-id="38474-159">사용자의 구독 내에서 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38474-159">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="38474-160">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="38474-160">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="38474-161">-Sku</span></span>
<span data-ttu-id="38474-162">SKU 유형</span><span class="sxs-lookup"><span data-stu-id="38474-162">Sku Type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-163">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38474-163">-SubscriptionId</span></span>
<span data-ttu-id="38474-164">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="38474-164">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="38474-165">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="38474-165">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="38474-166">-Tag</span></span>
<span data-ttu-id="38474-167">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="38474-167">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38474-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38474-168">-Confirm</span></span>
<span data-ttu-id="38474-169">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="38474-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38474-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38474-170">-WhatIf</span></span>
<span data-ttu-id="38474-171">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="38474-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38474-172">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38474-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38474-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38474-173">CommonParameters</span></span>
<span data-ttu-id="38474-174">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="38474-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38474-175">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38474-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38474-176">입력</span><span class="sxs-lookup"><span data-stu-id="38474-176">INPUTS</span></span>

## <span data-ttu-id="38474-177">출력</span><span class="sxs-lookup"><span data-stu-id="38474-177">OUTPUTS</span></span>

### <span data-ttu-id="38474-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="38474-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="38474-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="38474-179">NOTES</span></span>

<span data-ttu-id="38474-180">별칭</span><span class="sxs-lookup"><span data-stu-id="38474-180">ALIASES</span></span>

<span data-ttu-id="38474-181">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="38474-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="38474-182">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="38474-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="38474-183">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="38474-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="38474-184">FORESTTRUST <IForestTrust[]>: 리소스 포리스트에 대한 설정 목록</span><span class="sxs-lookup"><span data-stu-id="38474-184">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="38474-185">`[FriendlyName <String>]`: 이름</span><span class="sxs-lookup"><span data-stu-id="38474-185">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="38474-186">`[RemoteDnsIP <String>]`: 원격 Dns IP</span><span class="sxs-lookup"><span data-stu-id="38474-186">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="38474-187">`[TrustDirection <String>]`: 트러스트 방향</span><span class="sxs-lookup"><span data-stu-id="38474-187">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="38474-188">`[TrustPassword <String>]`: 암호 신뢰</span><span class="sxs-lookup"><span data-stu-id="38474-188">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="38474-189">`[TrustedDomainFqdn <String>]`: 신뢰할 수 있는 도메인 FQDN</span><span class="sxs-lookup"><span data-stu-id="38474-189">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="38474-190">REPLICASET <IReplicaSet[]>: ReplicaSets 목록</span><span class="sxs-lookup"><span data-stu-id="38474-190">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="38474-191">`[Location <String>]`: 가상 네트워크 위치</span><span class="sxs-lookup"><span data-stu-id="38474-191">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="38474-192">`[SubnetId <String>]`: Domain Services를 배포할 가상 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38474-192">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="38474-193">Domain Services가 배포될 서브넷의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="38474-193">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="38474-194">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="38474-194">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="38474-195">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38474-195">RELATED LINKS</span></span>

