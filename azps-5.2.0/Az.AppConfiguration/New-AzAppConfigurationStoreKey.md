---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStoreKey.md
ms.openlocfilehash: 922bc6f596611638c0ea7d27304e6ea3f0d62eeb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322538"
---
# <span data-ttu-id="98e75-101">New-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="98e75-101">New-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="98e75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98e75-102">SYNOPSIS</span></span>
<span data-ttu-id="98e75-103">지정된 구성 저장소에 대한 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="98e75-103">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="98e75-104">구문</span><span class="sxs-lookup"><span data-stu-id="98e75-104">SYNTAX</span></span>

### <span data-ttu-id="98e75-105">RegenerateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="98e75-105">RegenerateExpanded (Default)</span></span>
```
New-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> -Id <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="98e75-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="98e75-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzAppConfigurationStoreKey -InputObject <IAppConfigurationIdentity> -Id <String>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="98e75-107">설명</span><span class="sxs-lookup"><span data-stu-id="98e75-107">DESCRIPTION</span></span>
<span data-ttu-id="98e75-108">지정된 구성 저장소에 대한 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="98e75-108">Regenerates an access key for the specified configuration store.</span></span>

## <span data-ttu-id="98e75-109">예제</span><span class="sxs-lookup"><span data-stu-id="98e75-109">EXAMPLES</span></span>

### <span data-ttu-id="98e75-110">예제 1: 앱 구성 저장소의 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="98e75-110">Example 1: Regenerate key of an app configuration store</span></span>
```powershell
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test -Id $keys[0].id

ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="98e75-111">이 명령은 앱 구성 저장소의 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="98e75-111">This command regenerate key of an app configuration store.</span></span>

### <span data-ttu-id="98e75-112">예제 2: 개체에 따라 앱 구성 저장소의 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="98e75-112">Example 2: Regenerate key of an app configuration store by object</span></span>
```powershell
PS C:\> $app= New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test
PS C:\> $keys= Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test
PS C:\> New-AzAppConfigurationStoreKey -InputObject $app -Id $keys[0].id
ConnectionString                                                                                                                     LastModified        Name      ReadOnly Value
----------------                                                                                                                     ------------        ----      -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=09pv-l0-s0:opFCQMC6+9485xJgN5Ws;Secret=GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY= 5/8/2020 5:47:15 AM Secondary False    GcoE9e9t7GLRNJ910M46IrbHO/Vg0tt4HujRdsaCoTY=
```

<span data-ttu-id="98e75-113">이 명령은 개체에 따라 앱 구성 저장소의 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="98e75-113">This command regenerate key of an app configuration store by object.</span></span>

## <span data-ttu-id="98e75-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98e75-114">PARAMETERS</span></span>

### <span data-ttu-id="98e75-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98e75-115">-DefaultProfile</span></span>
<span data-ttu-id="98e75-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="98e75-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98e75-117">-Id</span><span class="sxs-lookup"><span data-stu-id="98e75-117">-Id</span></span>
<span data-ttu-id="98e75-118">다시 생성할 키의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="98e75-118">The id of the key to regenerate.</span></span>

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

### <span data-ttu-id="98e75-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98e75-119">-InputObject</span></span>
<span data-ttu-id="98e75-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="98e75-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98e75-121">-Name</span><span class="sxs-lookup"><span data-stu-id="98e75-121">-Name</span></span>
<span data-ttu-id="98e75-122">구성 저장소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98e75-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e75-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98e75-123">-ResourceGroupName</span></span>
<span data-ttu-id="98e75-124">컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98e75-124">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e75-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98e75-125">-SubscriptionId</span></span>
<span data-ttu-id="98e75-126">Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="98e75-126">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e75-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98e75-127">-Confirm</span></span>
<span data-ttu-id="98e75-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="98e75-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98e75-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98e75-129">-WhatIf</span></span>
<span data-ttu-id="98e75-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="98e75-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98e75-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98e75-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98e75-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98e75-132">CommonParameters</span></span>
<span data-ttu-id="98e75-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="98e75-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98e75-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="98e75-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98e75-135">입력</span><span class="sxs-lookup"><span data-stu-id="98e75-135">INPUTS</span></span>

### <span data-ttu-id="98e75-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="98e75-136">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="98e75-137">출력</span><span class="sxs-lookup"><span data-stu-id="98e75-137">OUTPUTS</span></span>

### <span data-ttu-id="98e75-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span><span class="sxs-lookup"><span data-stu-id="98e75-138">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="98e75-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="98e75-139">NOTES</span></span>

<span data-ttu-id="98e75-140">별칭</span><span class="sxs-lookup"><span data-stu-id="98e75-140">ALIASES</span></span>

<span data-ttu-id="98e75-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="98e75-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="98e75-142">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="98e75-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="98e75-143">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="98e75-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="98e75-144">INPUTOBJECT: <IAppConfigurationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="98e75-144">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="98e75-145">`[ConfigStoreName <String>]`: 구성 저장소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98e75-145">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="98e75-146">`[GroupName <String>]`: 개인 링크 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98e75-146">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="98e75-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="98e75-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="98e75-148">`[PrivateEndpointConnectionName <String>]`: 개인 엔드포인트 연결 이름</span><span class="sxs-lookup"><span data-stu-id="98e75-148">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="98e75-149">`[ResourceGroupName <String>]`: 컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98e75-149">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="98e75-150">`[SubscriptionId <String>]`: Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="98e75-150">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="98e75-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98e75-151">RELATED LINKS</span></span>

