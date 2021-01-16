---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 20f3985553a3fc7a993480bdf154a7f8e6776bf6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322552"
---
# <span data-ttu-id="4fab9-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="4fab9-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="4fab9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fab9-102">SYNOPSIS</span></span>
<span data-ttu-id="4fab9-103">지정된 매개 변수를 사용하여 구성 저장소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="4fab9-104">구문</span><span class="sxs-lookup"><span data-stu-id="4fab9-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4fab9-105">설명</span><span class="sxs-lookup"><span data-stu-id="4fab9-105">DESCRIPTION</span></span>
<span data-ttu-id="4fab9-106">지정된 매개 변수를 사용하여 구성 저장소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="4fab9-107">예제</span><span class="sxs-lookup"><span data-stu-id="4fab9-107">EXAMPLES</span></span>

### <span data-ttu-id="4fab9-108">예제 1: 앱 구성 저장소 만들기</span><span class="sxs-lookup"><span data-stu-id="4fab9-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4fab9-109">이 명령은 앱 구성 저장소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="4fab9-110">예제 2: IdentityType이 "UserAssigned"로 설정된 앱 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="4fab9-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4fab9-111">이 명령은 앱 구성을 만들고 사용자 할당 관리 ID를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="4fab9-112">CMK(cusomer 관리 키)를 사용하도록 설정하려면 다음 단계의 `Update-AzAppConfigurationStore` 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4fab9-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="4fab9-113">예제 3: IdentityType이 "SystemAssigned"로 설정된 앱 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="4fab9-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4fab9-114">이 명령은 앱 구성을 만들고 리소스와 연결된 시스템 할당 관리 ID를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="4fab9-115">CMK(cusomer 관리 키)를 사용하도록 설정하려면 다음 단계의 `Update-AzAppConfigurationStore` 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4fab9-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="4fab9-116">예제 4: IdentityType이 "SystemAssigned, UserAssigned"로 설정된 앱 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="4fab9-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4fab9-117">시스템 할당 관리 ID를 사용하도록 설정하고 동시에 사용자 할당 ID를 부여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="4fab9-118">CMK(cusomer 관리 키)를 사용하도록 설정하려면 다음 단계의 `Update-AzAppConfigurationStore` 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4fab9-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="4fab9-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fab9-119">PARAMETERS</span></span>

### <span data-ttu-id="4fab9-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fab9-120">-AsJob</span></span>
<span data-ttu-id="4fab9-121">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="4fab9-121">Run the command as a job</span></span>

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

### <span data-ttu-id="4fab9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fab9-122">-DefaultProfile</span></span>
<span data-ttu-id="4fab9-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fab9-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4fab9-124">-IdentityType</span></span>
<span data-ttu-id="4fab9-125">사용되는 관리 ID의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-125">The type of managed identity used.</span></span>
<span data-ttu-id="4fab9-126">'SystemAssignedAndUserAssigned' 형식에는 암시적으로 만든 ID와 사용자 할당 ID 집합이 모두 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="4fab9-127">'없음' 형식은 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-127">The type 'None' will remove any identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fab9-128">-Location</span><span class="sxs-lookup"><span data-stu-id="4fab9-128">-Location</span></span>
<span data-ttu-id="4fab9-129">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-129">The location of the resource.</span></span>
<span data-ttu-id="4fab9-130">리소스를 만든 후 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-130">This cannot be changed after the resource is created.</span></span>

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

### <span data-ttu-id="4fab9-131">-Name</span><span class="sxs-lookup"><span data-stu-id="4fab9-131">-Name</span></span>
<span data-ttu-id="4fab9-132">구성 저장소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-132">The name of the configuration store.</span></span>

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

### <span data-ttu-id="4fab9-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4fab9-133">-NoWait</span></span>
<span data-ttu-id="4fab9-134">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="4fab9-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4fab9-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fab9-135">-ResourceGroupName</span></span>
<span data-ttu-id="4fab9-136">컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-136">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="4fab9-137">-Sku</span><span class="sxs-lookup"><span data-stu-id="4fab9-137">-Sku</span></span>
<span data-ttu-id="4fab9-138">구성 저장소의 SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-138">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="4fab9-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4fab9-139">-SubscriptionId</span></span>
<span data-ttu-id="4fab9-140">Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-140">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="4fab9-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="4fab9-141">-Tag</span></span>
<span data-ttu-id="4fab9-142">리소스의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-142">The tags of the resource.</span></span>

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

### <span data-ttu-id="4fab9-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4fab9-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="4fab9-144">리소스와 연결된 사용자 할당 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="4fab9-145">사용자 할당 ID 사전 키는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}' 형식의 리소스 ID로 설정됩니다. ARM</span><span class="sxs-lookup"><span data-stu-id="4fab9-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="4fab9-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fab9-146">-Confirm</span></span>
<span data-ttu-id="4fab9-147">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fab9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fab9-148">-WhatIf</span></span>
<span data-ttu-id="4fab9-149">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4fab9-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fab9-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fab9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fab9-151">CommonParameters</span></span>
<span data-ttu-id="4fab9-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4fab9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fab9-153">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4fab9-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fab9-154">입력</span><span class="sxs-lookup"><span data-stu-id="4fab9-154">INPUTS</span></span>

## <span data-ttu-id="4fab9-155">출력</span><span class="sxs-lookup"><span data-stu-id="4fab9-155">OUTPUTS</span></span>

### <span data-ttu-id="4fab9-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="4fab9-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="4fab9-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4fab9-157">NOTES</span></span>

<span data-ttu-id="4fab9-158">별칭</span><span class="sxs-lookup"><span data-stu-id="4fab9-158">ALIASES</span></span>

## <span data-ttu-id="4fab9-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fab9-159">RELATED LINKS</span></span>



[<span data-ttu-id="4fab9-160">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4fab9-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

