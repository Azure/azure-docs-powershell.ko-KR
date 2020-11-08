---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 20f3985553a3fc7a993480bdf154a7f8e6776bf6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213735"
---
# <span data-ttu-id="23365-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="23365-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="23365-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23365-102">SYNOPSIS</span></span>
<span data-ttu-id="23365-103">지정 된 매개 변수를 사용 하 여 구성 저장소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23365-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="23365-104">구문과</span><span class="sxs-lookup"><span data-stu-id="23365-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="23365-105">설명은</span><span class="sxs-lookup"><span data-stu-id="23365-105">DESCRIPTION</span></span>
<span data-ttu-id="23365-106">지정 된 매개 변수를 사용 하 여 구성 저장소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23365-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="23365-107">예제의</span><span class="sxs-lookup"><span data-stu-id="23365-107">EXAMPLES</span></span>

### <span data-ttu-id="23365-108">예제 1: 앱 구성 저장소 만들기</span><span class="sxs-lookup"><span data-stu-id="23365-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="23365-109">이 명령은 앱 구성 저장소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23365-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="23365-110">예제 2: IdentityType이 "UserAssigned"으로 설정 된 앱 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="23365-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="23365-111">이 명령은 앱 구성을 만들고 사용자가 할당 한 관리 되는 id를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="23365-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="23365-112">`Update-AzAppConfigurationStore`Nk (cusomer 관리 되는 키)을 사용 하도록 설정 하려면 다음 단계에 대 한 예제를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="23365-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="23365-113">예제 3: IdentityType이 "지정 된 SystemAssigned"으로 설정 된 앱 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="23365-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="23365-114">이 명령은 앱 구성을 만들고 리소스와 연결 된 시스템 할당 관리 id를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="23365-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="23365-115">`Update-AzAppConfigurationStore`Nk (cusomer 관리 되는 키)을 사용 하도록 설정 하려면 다음 단계에 대 한 예제를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="23365-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="23365-116">예제 4: IdentityType이 "SystemAssigned, UserAssigned 됨"으로 설정 된 앱 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="23365-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="23365-117">시스템 할당 관리 id를 사용 하도록 설정 하 고 동시에 사용자에 게 할당 된 id를 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="23365-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="23365-118">`Update-AzAppConfigurationStore`Nk (cusomer 관리 되는 키)을 사용 하도록 설정 하려면 다음 단계에 대 한 예제를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="23365-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="23365-119">변수</span><span class="sxs-lookup"><span data-stu-id="23365-119">PARAMETERS</span></span>

### <span data-ttu-id="23365-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23365-120">-AsJob</span></span>
<span data-ttu-id="23365-121">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="23365-121">Run the command as a job</span></span>

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

### <span data-ttu-id="23365-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23365-122">-DefaultProfile</span></span>
<span data-ttu-id="23365-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23365-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23365-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="23365-124">-IdentityType</span></span>
<span data-ttu-id="23365-125">사용 되는 관리 되는 id의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="23365-125">The type of managed identity used.</span></span>
<span data-ttu-id="23365-126">' SystemAssignedAndUserAssigned ' 형식에는 암시적으로 만들어진 id와 사용자 지정 id 집합이 모두 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="23365-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="23365-127">' 없음 ' 형식은 id를 모두 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="23365-127">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="23365-128">-위치</span><span class="sxs-lookup"><span data-stu-id="23365-128">-Location</span></span>
<span data-ttu-id="23365-129">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="23365-129">The location of the resource.</span></span>
<span data-ttu-id="23365-130">리소스를 만든 후에는 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="23365-130">This cannot be changed after the resource is created.</span></span>

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

### <span data-ttu-id="23365-131">-이름</span><span class="sxs-lookup"><span data-stu-id="23365-131">-Name</span></span>
<span data-ttu-id="23365-132">구성 저장소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23365-132">The name of the configuration store.</span></span>

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

### <span data-ttu-id="23365-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="23365-133">-NoWait</span></span>
<span data-ttu-id="23365-134">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="23365-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="23365-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23365-135">-ResourceGroupName</span></span>
<span data-ttu-id="23365-136">컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23365-136">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="23365-137">-Sku</span><span class="sxs-lookup"><span data-stu-id="23365-137">-Sku</span></span>
<span data-ttu-id="23365-138">구성 저장소의 SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23365-138">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="23365-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23365-139">-SubscriptionId</span></span>
<span data-ttu-id="23365-140">Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="23365-140">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="23365-141">태그</span><span class="sxs-lookup"><span data-stu-id="23365-141">-Tag</span></span>
<span data-ttu-id="23365-142">리소스의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="23365-142">The tags of the resource.</span></span>

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

### <span data-ttu-id="23365-143">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="23365-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="23365-144">리소스와 연결 된 사용자 할당 id의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="23365-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="23365-145">사용자 할당 id 사전 키는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} ' 형식의 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="23365-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="23365-146">-확인</span><span class="sxs-lookup"><span data-stu-id="23365-146">-Confirm</span></span>
<span data-ttu-id="23365-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="23365-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23365-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23365-148">-WhatIf</span></span>
<span data-ttu-id="23365-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="23365-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23365-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23365-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23365-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23365-151">CommonParameters</span></span>
<span data-ttu-id="23365-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="23365-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23365-153">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="23365-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23365-154">입력</span><span class="sxs-lookup"><span data-stu-id="23365-154">INPUTS</span></span>

## <span data-ttu-id="23365-155">출력</span><span class="sxs-lookup"><span data-stu-id="23365-155">OUTPUTS</span></span>

### <span data-ttu-id="23365-156">Api20200601. IConfigurationStore에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="23365-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="23365-157">상속자</span><span class="sxs-lookup"><span data-stu-id="23365-157">NOTES</span></span>

<span data-ttu-id="23365-158">별칭과</span><span class="sxs-lookup"><span data-stu-id="23365-158">ALIASES</span></span>

## <span data-ttu-id="23365-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23365-159">RELATED LINKS</span></span>



[<span data-ttu-id="23365-160">새로운 AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="23365-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

