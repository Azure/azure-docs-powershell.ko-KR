---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 9373a154e6bc717c22705961fb5232814ac3d2c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987112"
---
# <span data-ttu-id="a118f-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="a118f-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="a118f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a118f-102">SYNOPSIS</span></span>
<span data-ttu-id="a118f-103">지정된 매개 변수를 사용하여 구성 저장소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="a118f-104">구문</span><span class="sxs-lookup"><span data-stu-id="a118f-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a118f-105">설명</span><span class="sxs-lookup"><span data-stu-id="a118f-105">DESCRIPTION</span></span>
<span data-ttu-id="a118f-106">지정된 매개 변수를 사용하여 구성 저장소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="a118f-107">예제</span><span class="sxs-lookup"><span data-stu-id="a118f-107">EXAMPLES</span></span>

### <span data-ttu-id="a118f-108">예제 1: 앱 구성 저장소 만들기</span><span class="sxs-lookup"><span data-stu-id="a118f-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="a118f-109">이 명령은 앱 구성 저장소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="a118f-110">예제 2: IdentityType이 "UserAssigned"로 설정된 앱 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="a118f-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="a118f-111">이 명령은 앱 구성을 만들고 사용자 할당 관리 ID를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="a118f-112">CMK(cusomer 관리 키)를 사용하도록 설정하는 다음 단계의 `Update-AzAppConfigurationStore` 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a118f-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="a118f-113">예제 3: IdentityType이 "SystemAssigned"로 설정된 앱 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="a118f-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="a118f-114">이 명령은 앱 구성을 만들고 리소스와 연결된 시스템 할당 관리 ID를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="a118f-115">CMK(cusomer 관리 키)를 사용하도록 설정하는 다음 단계의 `Update-AzAppConfigurationStore` 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a118f-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="a118f-116">예제 4: IdentityType이 "SystemAssigned, UserAssigned"로 설정된 앱 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="a118f-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="a118f-117">시스템 할당 관리 ID를 사용하도록 설정하고 동시에 사용자 할당 ID를 부여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="a118f-118">CMK(cusomer 관리 키)를 사용하도록 설정하는 다음 단계의 `Update-AzAppConfigurationStore` 예제를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a118f-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="a118f-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a118f-119">PARAMETERS</span></span>

### <span data-ttu-id="a118f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a118f-120">-AsJob</span></span>
<span data-ttu-id="a118f-121">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-121">Run the command as a job</span></span>

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

### <span data-ttu-id="a118f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a118f-122">-DefaultProfile</span></span>
<span data-ttu-id="a118f-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a118f-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a118f-124">-IdentityType</span></span>
<span data-ttu-id="a118f-125">사용된 관리 ID의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-125">The type of managed identity used.</span></span>
<span data-ttu-id="a118f-126">'SystemAssignedAndUserAssigned' 형식에는 암시적으로 만든 ID와 사용자 할당 ID 집합이 모두 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="a118f-127">'None' 형식은 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-127">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="a118f-128">-Location</span><span class="sxs-lookup"><span data-stu-id="a118f-128">-Location</span></span>
<span data-ttu-id="a118f-129">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-129">The location of the resource.</span></span>
<span data-ttu-id="a118f-130">리소스를 만든 후에 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-130">This cannot be changed after the resource is created.</span></span>

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

### <span data-ttu-id="a118f-131">-Name</span><span class="sxs-lookup"><span data-stu-id="a118f-131">-Name</span></span>
<span data-ttu-id="a118f-132">구성 저장소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-132">The name of the configuration store.</span></span>

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

### <span data-ttu-id="a118f-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a118f-133">-NoWait</span></span>
<span data-ttu-id="a118f-134">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="a118f-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a118f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a118f-135">-ResourceGroupName</span></span>
<span data-ttu-id="a118f-136">컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-136">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="a118f-137">-Sku</span><span class="sxs-lookup"><span data-stu-id="a118f-137">-Sku</span></span>
<span data-ttu-id="a118f-138">구성 저장소의 SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-138">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="a118f-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a118f-139">-SubscriptionId</span></span>
<span data-ttu-id="a118f-140">Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-140">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="a118f-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="a118f-141">-Tag</span></span>
<span data-ttu-id="a118f-142">리소스의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-142">The tags of the resource.</span></span>

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

### <span data-ttu-id="a118f-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a118f-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="a118f-144">리소스와 연결된 사용자 할당 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="a118f-145">사용자 ARM 할당 ID 사전 키는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}' 형식의 리소스 ID로 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="a118f-146">-확인</span><span class="sxs-lookup"><span data-stu-id="a118f-146">-Confirm</span></span>
<span data-ttu-id="a118f-147">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a118f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a118f-148">-WhatIf</span></span>
<span data-ttu-id="a118f-149">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a118f-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a118f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a118f-151">CommonParameters</span></span>
<span data-ttu-id="a118f-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a118f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a118f-153">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a118f-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a118f-154">입력</span><span class="sxs-lookup"><span data-stu-id="a118f-154">INPUTS</span></span>

## <span data-ttu-id="a118f-155">출력</span><span class="sxs-lookup"><span data-stu-id="a118f-155">OUTPUTS</span></span>

### <span data-ttu-id="a118f-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="a118f-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="a118f-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a118f-157">NOTES</span></span>

<span data-ttu-id="a118f-158">별칭</span><span class="sxs-lookup"><span data-stu-id="a118f-158">ALIASES</span></span>

## <span data-ttu-id="a118f-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a118f-159">RELATED LINKS</span></span>



[<span data-ttu-id="a118f-160">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a118f-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

