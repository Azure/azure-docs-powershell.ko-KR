---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/update-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
ms.openlocfilehash: 7acebe247009c95f9d504dc09b2729eeb5aabbbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176585"
---
# <span data-ttu-id="7c2c0-101">Update-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="7c2c0-101">Update-AzADDomainService</span></span>

## <span data-ttu-id="7c2c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c2c0-102">SYNOPSIS</span></span>
<span data-ttu-id="7c2c0-103">도메인 서비스 업데이트 작업을 사용하여 기존 배포를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-103">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="7c2c0-104">업데이트 호출은 PATCH 본문에 나열된 속성만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-104">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="7c2c0-105">구문</span><span class="sxs-lookup"><span data-stu-id="7c2c0-105">SYNTAX</span></span>

### <span data-ttu-id="7c2c0-106">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="7c2c0-106">UpdateExpanded (Default)</span></span>
```
Update-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DomainConfigurationType <String>] [-DomainSecuritySettingNtlmV1 <String>]
 [-DomainSecuritySettingSyncKerberosPassword <String>] [-DomainSecuritySettingSyncNtlmPassword <String>]
 [-DomainSecuritySettingSyncOnPremPassword <String>] [-DomainSecuritySettingTlsV1 <String>]
 [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>] [-LdapSettingExternalAccess <String>]
 [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7c2c0-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7c2c0-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DomainConfigurationType <String>]
 [-DomainSecuritySettingNtlmV1 <String>] [-DomainSecuritySettingSyncKerberosPassword <String>]
 [-DomainSecuritySettingSyncNtlmPassword <String>] [-DomainSecuritySettingSyncOnPremPassword <String>]
 [-DomainSecuritySettingTlsV1 <String>] [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>]
 [-LdapSettingExternalAccess <String>] [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7c2c0-108">설명</span><span class="sxs-lookup"><span data-stu-id="7c2c0-108">DESCRIPTION</span></span>
<span data-ttu-id="7c2c0-109">도메인 서비스 업데이트 작업을 사용하여 기존 배포를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-109">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="7c2c0-110">업데이트 호출은 PATCH 본문에 나열된 속성만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-110">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="7c2c0-111">예제</span><span class="sxs-lookup"><span data-stu-id="7c2c0-111">EXAMPLES</span></span>

### <span data-ttu-id="7c2c0-112">예제 1: ResourceGroupName 및 Name으로 AzADDomainService 업데이트</span><span class="sxs-lookup"><span data-stu-id="7c2c0-112">Example 1: Update AzADDomainService By ResourceGroupName and Name</span></span>
```powershell
PS C:\> $ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="7c2c0-113">ResourceGroupName 및 Name으로 AzADDomainService 업데이트</span><span class="sxs-lookup"><span data-stu-id="7c2c0-113">Update AzADDomainService By ResourceGroupName and Name</span></span>

### <span data-ttu-id="7c2c0-114">예제 2: Inputobject로 AzADDomainService 업데이트</span><span class="sxs-lookup"><span data-stu-id="7c2c0-114">Example 2: Update AzADDomainService By Inputobject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
$ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -InputObject $getAzAddomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="7c2c0-115">Inputobject로 AzADDomainService 업데이트</span><span class="sxs-lookup"><span data-stu-id="7c2c0-115">Update AzADDomainService By Inputobject</span></span>

## <span data-ttu-id="7c2c0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c2c0-116">PARAMETERS</span></span>

### <span data-ttu-id="7c2c0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c2c0-117">-AsJob</span></span>
<span data-ttu-id="7c2c0-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="7c2c0-118">Run the command as a job</span></span>

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

### <span data-ttu-id="7c2c0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c2c0-119">-DefaultProfile</span></span>
<span data-ttu-id="7c2c0-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c2c0-121">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="7c2c0-121">-DomainConfigurationType</span></span>
<span data-ttu-id="7c2c0-122">도메인 구성 유형</span><span class="sxs-lookup"><span data-stu-id="7c2c0-122">Domain Configuration Type</span></span>

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

### <span data-ttu-id="7c2c0-123">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="7c2c0-123">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="7c2c0-124">NtlmV1을 사용하도록 설정하거나 사용하지 않도록 설정할지 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-124">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="7c2c0-125">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="7c2c0-125">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="7c2c0-126">SyncKerberosPasswords의 사용 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-126">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="7c2c0-127">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="7c2c0-127">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="7c2c0-128">SyncNtlmPasswords의 사용 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-128">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="7c2c0-129">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="7c2c0-129">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="7c2c0-130">SyncOnPremPasswords의 사용 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-130">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="7c2c0-131">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="7c2c0-131">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="7c2c0-132">TlsV1을 사용하도록 설정하거나 사용하지 않도록 설정할지 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-132">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="7c2c0-133">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="7c2c0-133">-FilteredSync</span></span>
<span data-ttu-id="7c2c0-134">그룹 기반 필터링된 동기화를 켜는 활성화 또는 사용 안 하여 플래그</span><span class="sxs-lookup"><span data-stu-id="7c2c0-134">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="7c2c0-135">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="7c2c0-135">-ForestTrust</span></span>
<span data-ttu-id="7c2c0-136">구성할 리소스 포리스트에 대한 설정 목록은 FORESTTRUST 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-136">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

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

### <span data-ttu-id="7c2c0-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c2c0-137">-InputObject</span></span>
<span data-ttu-id="7c2c0-138">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-138">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c2c0-139">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="7c2c0-139">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="7c2c0-140">인터넷을 통해 LDAP 액세스를 보호할지 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-140">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="7c2c0-141">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="7c2c0-141">-LdapSettingLdaps</span></span>
<span data-ttu-id="7c2c0-142">보안 LDAP를 사용하도록 설정하거나 사용하지 않도록 설정할지 여부를 결정하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-142">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="7c2c0-143">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="7c2c0-143">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="7c2c0-144">보안 LDAP를 구성하는 데 필요한 인증서입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-144">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="7c2c0-145">여기에 전달된 매개 변수는 인증서 pfx 파일의 base64로 인코딩된 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-145">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="7c2c0-146">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="7c2c0-146">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="7c2c0-147">제공된 보안 LDAP 인증서 pfx 파일의 암호를 해독하는 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-147">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

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

### <span data-ttu-id="7c2c0-148">-Name</span><span class="sxs-lookup"><span data-stu-id="7c2c0-148">-Name</span></span>
<span data-ttu-id="7c2c0-149">도메인 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-149">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c2c0-150">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="7c2c0-150">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="7c2c0-151">추가 받는 사람 목록</span><span class="sxs-lookup"><span data-stu-id="7c2c0-151">The list of additional recipients</span></span>

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

### <span data-ttu-id="7c2c0-152">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="7c2c0-152">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="7c2c0-153">도메인 컨트롤러 관리자에게 알림을 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-153">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="7c2c0-154">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="7c2c0-154">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="7c2c0-155">전역 관리자에게 알림을 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-155">Should global admins be notified</span></span>

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

### <span data-ttu-id="7c2c0-156">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7c2c0-156">-NoWait</span></span>
<span data-ttu-id="7c2c0-157">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="7c2c0-157">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7c2c0-158">-ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="7c2c0-158">-ReplicaSet</span></span>
<span data-ttu-id="7c2c0-159">생성할 ReplicaSets 목록은 REPLICASET 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-159">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IReplicaSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c2c0-160">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="7c2c0-160">-ResourceForest</span></span>
<span data-ttu-id="7c2c0-161">리소스 포리스트</span><span class="sxs-lookup"><span data-stu-id="7c2c0-161">Resource Forest</span></span>

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

### <span data-ttu-id="7c2c0-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c2c0-162">-ResourceGroupName</span></span>
<span data-ttu-id="7c2c0-163">사용자의 구독 내에서 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-163">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="7c2c0-164">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-164">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c2c0-165">-Sku</span><span class="sxs-lookup"><span data-stu-id="7c2c0-165">-Sku</span></span>
<span data-ttu-id="7c2c0-166">SKU 유형</span><span class="sxs-lookup"><span data-stu-id="7c2c0-166">Sku Type</span></span>

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

### <span data-ttu-id="7c2c0-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c2c0-167">-SubscriptionId</span></span>
<span data-ttu-id="7c2c0-168">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-168">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7c2c0-169">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-169">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c2c0-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="7c2c0-170">-Tag</span></span>
<span data-ttu-id="7c2c0-171">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="7c2c0-171">Resource tags</span></span>

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

### <span data-ttu-id="7c2c0-172">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c2c0-172">-Confirm</span></span>
<span data-ttu-id="7c2c0-173">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c2c0-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c2c0-174">-WhatIf</span></span>
<span data-ttu-id="7c2c0-175">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7c2c0-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c2c0-176">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c2c0-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c2c0-177">CommonParameters</span></span>
<span data-ttu-id="7c2c0-178">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c2c0-179">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c2c0-180">입력</span><span class="sxs-lookup"><span data-stu-id="7c2c0-180">INPUTS</span></span>

### <span data-ttu-id="7c2c0-181">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="7c2c0-181">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="7c2c0-182">출력</span><span class="sxs-lookup"><span data-stu-id="7c2c0-182">OUTPUTS</span></span>

### <span data-ttu-id="7c2c0-183">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="7c2c0-183">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="7c2c0-184">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7c2c0-184">NOTES</span></span>

<span data-ttu-id="7c2c0-185">별칭</span><span class="sxs-lookup"><span data-stu-id="7c2c0-185">ALIASES</span></span>

<span data-ttu-id="7c2c0-186">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="7c2c0-186">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7c2c0-187">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-187">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7c2c0-188">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-188">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7c2c0-189">FORESTTRUST <IForestTrust[]>: 리소스 포리스트에 대한 설정 목록</span><span class="sxs-lookup"><span data-stu-id="7c2c0-189">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="7c2c0-190">`[FriendlyName <String>]`: 이름</span><span class="sxs-lookup"><span data-stu-id="7c2c0-190">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="7c2c0-191">`[RemoteDnsIP <String>]`: 원격 Dns IP</span><span class="sxs-lookup"><span data-stu-id="7c2c0-191">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="7c2c0-192">`[TrustDirection <String>]`: 트러스트 방향</span><span class="sxs-lookup"><span data-stu-id="7c2c0-192">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="7c2c0-193">`[TrustPassword <String>]`: 암호 신뢰</span><span class="sxs-lookup"><span data-stu-id="7c2c0-193">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="7c2c0-194">`[TrustedDomainFqdn <String>]`: 신뢰할 수 있는 도메인 FQDN</span><span class="sxs-lookup"><span data-stu-id="7c2c0-194">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="7c2c0-195">INPUTOBJECT: <IAdDomainServicesIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7c2c0-195">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7c2c0-196">`[DomainServiceName <String>]`: 도메인 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-196">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="7c2c0-197">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="7c2c0-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7c2c0-198">`[ResourceGroupName <String>]`: 사용자의 구독 내에서 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-198">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="7c2c0-199">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-199">The name is case insensitive.</span></span>
  - <span data-ttu-id="7c2c0-200">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-200">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="7c2c0-201">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-201">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="7c2c0-202">REPLICASET <IReplicaSet[]>: ReplicaSets 목록</span><span class="sxs-lookup"><span data-stu-id="7c2c0-202">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="7c2c0-203">`[Location <String>]`: 가상 네트워크 위치</span><span class="sxs-lookup"><span data-stu-id="7c2c0-203">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="7c2c0-204">`[SubnetId <String>]`: Domain Services를 배포할 가상 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-204">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="7c2c0-205">Domain Services가 배포될 서브넷의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-205">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="7c2c0-206">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="7c2c0-206">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="7c2c0-207">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c2c0-207">RELATED LINKS</span></span>

