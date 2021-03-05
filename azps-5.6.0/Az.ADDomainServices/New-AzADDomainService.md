---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/new-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
ms.openlocfilehash: 61918dd4bce5279a2528e94c4e46fbe1c8813aff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986323"
---
# <span data-ttu-id="326a5-101">New-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="326a5-101">New-AzADDomainService</span></span>

## <span data-ttu-id="326a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="326a5-102">SYNOPSIS</span></span>
<span data-ttu-id="326a5-103">도메인 서비스 만들기 작업은 지정된 매개 변수를 사용하여 새 도메인 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-103">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="326a5-104">특정 서비스가 이미 있는 경우 패치 가능한 속성이 업데이트되어 변경 불가능한 속성은 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-104">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="326a5-105">구문</span><span class="sxs-lookup"><span data-stu-id="326a5-105">SYNTAX</span></span>

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

## <span data-ttu-id="326a5-106">설명</span><span class="sxs-lookup"><span data-stu-id="326a5-106">DESCRIPTION</span></span>
<span data-ttu-id="326a5-107">도메인 서비스 만들기 작업은 지정된 매개 변수를 사용하여 새 도메인 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-107">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="326a5-108">특정 서비스가 이미 있는 경우 패치 가능한 속성이 업데이트되어 변경 불가능한 속성은 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-108">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="326a5-109">예제</span><span class="sxs-lookup"><span data-stu-id="326a5-109">EXAMPLES</span></span>

### <span data-ttu-id="326a5-110">예제 1: 새 ADDomainService 만들기</span><span class="sxs-lookup"><span data-stu-id="326a5-110">Example 1: Create new ADDomainService</span></span>
```powershell
PS C:\> $replicaSet = New-AzADDomainServiceReplicaSetObject -Location westus -SubnetId /subscriptions/********-****-****-****-**********/resourceGroups/yishitest/providers/Microsoft.Network/virtualNetworks/aadds-vnet/subnets/default
New-AzADDomainService -name youriADdomain -ResourceGroupName youriAddomain -DomainName youriAddomain.com -ReplicaSet $replicaSet -debug

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="326a5-111">새 ADDomainService 만들기</span><span class="sxs-lookup"><span data-stu-id="326a5-111">Create new ADDomainService</span></span>

## <span data-ttu-id="326a5-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="326a5-112">PARAMETERS</span></span>

### <span data-ttu-id="326a5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="326a5-113">-AsJob</span></span>
<span data-ttu-id="326a5-114">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-114">Run the command as a job</span></span>

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

### <span data-ttu-id="326a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="326a5-115">-DefaultProfile</span></span>
<span data-ttu-id="326a5-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="326a5-117">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="326a5-117">-DomainConfigurationType</span></span>
<span data-ttu-id="326a5-118">도메인 구성 유형</span><span class="sxs-lookup"><span data-stu-id="326a5-118">Domain Configuration Type</span></span>

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

### <span data-ttu-id="326a5-119">-DomainName</span><span class="sxs-lookup"><span data-stu-id="326a5-119">-DomainName</span></span>
<span data-ttu-id="326a5-120">도메인 서비스를 배포할 Azure 도메인의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-120">The name of the Azure domain that the user would like to deploy Domain Services to.</span></span>

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

### <span data-ttu-id="326a5-121">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="326a5-121">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="326a5-122">NtlmV1을 사용하도록 설정하거나 사용하지 않도록 설정하는지 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-122">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="326a5-123">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="326a5-123">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="326a5-124">SyncKerberosPasswords를 사용하도록 설정하거나 사용하지 않도록 설정하는지 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-124">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="326a5-125">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="326a5-125">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="326a5-126">SyncNtlmPasswords를 사용하도록 설정하거나 사용하지 않도록 설정하는지 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-126">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="326a5-127">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="326a5-127">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="326a5-128">SyncOnPremPasswords를 사용하도록 설정하거나 사용하지 않도록 설정하는지 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-128">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="326a5-129">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="326a5-129">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="326a5-130">TlsV1을 사용하도록 설정하거나 사용하지 않도록 설정하는지 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-130">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="326a5-131">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="326a5-131">-FilteredSync</span></span>
<span data-ttu-id="326a5-132">그룹 기반 필터링된 동기화를 사용하도록 설정하거나 사용하지 않도록 설정한 플래그</span><span class="sxs-lookup"><span data-stu-id="326a5-132">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="326a5-133">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="326a5-133">-ForestTrust</span></span>
<span data-ttu-id="326a5-134">리소스 포리스트를 구성하기 위한 설정 목록은 FORESTTRUST 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="326a5-134">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

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

### <span data-ttu-id="326a5-135">-LdapSettingExternalAccesss</span><span class="sxs-lookup"><span data-stu-id="326a5-135">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="326a5-136">인터넷을 통해 LDAP 액세스 보호를 사용하도록 설정하거나 사용하지 않도록 설정하는지 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-136">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="326a5-137">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="326a5-137">-LdapSettingLdaps</span></span>
<span data-ttu-id="326a5-138">보안 LDAP를 사용하도록 설정하거나 사용하지 않도록 설정하는지 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-138">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="326a5-139">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="326a5-139">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="326a5-140">보안 LDAP를 구성하는 데 필요한 인증서입니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-140">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="326a5-141">여기서 전달된 매개 변수는 인증서 pfx 파일의 base64encoded 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-141">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="326a5-142">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="326a5-142">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="326a5-143">제공된 보안 LDAP 인증서 pfx 파일을 해독하는 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-143">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

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

### <span data-ttu-id="326a5-144">-Name</span><span class="sxs-lookup"><span data-stu-id="326a5-144">-Name</span></span>
<span data-ttu-id="326a5-145">도메인 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-145">The name of the domain service.</span></span>

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

### <span data-ttu-id="326a5-146">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="326a5-146">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="326a5-147">추가 받는 사람 목록</span><span class="sxs-lookup"><span data-stu-id="326a5-147">The list of additional recipients</span></span>

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

### <span data-ttu-id="326a5-148">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="326a5-148">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="326a5-149">도메인 컨트롤러 관리자에게 알림을 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-149">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="326a5-150">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="326a5-150">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="326a5-151">전역 관리자에게 알림을 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-151">Should global admins be notified</span></span>

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

### <span data-ttu-id="326a5-152">-NoWait</span><span class="sxs-lookup"><span data-stu-id="326a5-152">-NoWait</span></span>
<span data-ttu-id="326a5-153">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="326a5-153">Run the command asynchronously</span></span>

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

### <span data-ttu-id="326a5-154">-복제본 세트</span><span class="sxs-lookup"><span data-stu-id="326a5-154">-ReplicaSet</span></span>
<span data-ttu-id="326a5-155">복제본 집합을 만들 목록은 복제본 세트 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="326a5-155">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

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

### <span data-ttu-id="326a5-156">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="326a5-156">-ResourceForest</span></span>
<span data-ttu-id="326a5-157">리소스 포리스트</span><span class="sxs-lookup"><span data-stu-id="326a5-157">Resource Forest</span></span>

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

### <span data-ttu-id="326a5-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="326a5-158">-ResourceGroupName</span></span>
<span data-ttu-id="326a5-159">사용자의 구독 내의 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-159">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="326a5-160">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-160">The name is case insensitive.</span></span>

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

### <span data-ttu-id="326a5-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="326a5-161">-Sku</span></span>
<span data-ttu-id="326a5-162">Sku 유형</span><span class="sxs-lookup"><span data-stu-id="326a5-162">Sku Type</span></span>

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

### <span data-ttu-id="326a5-163">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="326a5-163">-SubscriptionId</span></span>
<span data-ttu-id="326a5-164">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-164">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="326a5-165">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-165">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="326a5-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="326a5-166">-Tag</span></span>
<span data-ttu-id="326a5-167">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="326a5-167">Resource tags</span></span>

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

### <span data-ttu-id="326a5-168">-확인</span><span class="sxs-lookup"><span data-stu-id="326a5-168">-Confirm</span></span>
<span data-ttu-id="326a5-169">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="326a5-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="326a5-170">-WhatIf</span></span>
<span data-ttu-id="326a5-171">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="326a5-172">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="326a5-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="326a5-173">CommonParameters</span></span>
<span data-ttu-id="326a5-174">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="326a5-175">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="326a5-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="326a5-176">입력</span><span class="sxs-lookup"><span data-stu-id="326a5-176">INPUTS</span></span>

## <span data-ttu-id="326a5-177">출력</span><span class="sxs-lookup"><span data-stu-id="326a5-177">OUTPUTS</span></span>

### <span data-ttu-id="326a5-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="326a5-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="326a5-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="326a5-179">NOTES</span></span>

<span data-ttu-id="326a5-180">별칭</span><span class="sxs-lookup"><span data-stu-id="326a5-180">ALIASES</span></span>

<span data-ttu-id="326a5-181">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="326a5-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="326a5-182">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="326a5-183">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="326a5-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="326a5-184">FORESTTRUST <IForestTrust[]>: 리소스 포리스트에 대한 설정 목록</span><span class="sxs-lookup"><span data-stu-id="326a5-184">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="326a5-185">`[FriendlyName <String>]`: 친숙한 이름</span><span class="sxs-lookup"><span data-stu-id="326a5-185">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="326a5-186">`[RemoteDnsIP <String>]`: 원격 Dns ips</span><span class="sxs-lookup"><span data-stu-id="326a5-186">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="326a5-187">`[TrustDirection <String>]`: 신뢰 방향</span><span class="sxs-lookup"><span data-stu-id="326a5-187">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="326a5-188">`[TrustPassword <String>]`: 암호 신뢰</span><span class="sxs-lookup"><span data-stu-id="326a5-188">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="326a5-189">`[TrustedDomainFqdn <String>]`: 신뢰할 수 있는 도메인 FQDN</span><span class="sxs-lookup"><span data-stu-id="326a5-189">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="326a5-190">복제본 <IReplicaSet[]>: 복제본 세트 목록</span><span class="sxs-lookup"><span data-stu-id="326a5-190">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="326a5-191">`[Location <String>]`: 가상 네트워크 위치</span><span class="sxs-lookup"><span data-stu-id="326a5-191">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="326a5-192">`[SubnetId <String>]`: Domain Services가 배포할 가상 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-192">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="326a5-193">Domain Services가 배포할 서브넷의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="326a5-193">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="326a5-194">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="326a5-194">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="326a5-195">관련 링크</span><span class="sxs-lookup"><span data-stu-id="326a5-195">RELATED LINKS</span></span>

