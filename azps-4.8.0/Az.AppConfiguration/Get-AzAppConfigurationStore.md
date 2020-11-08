---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: 88847cbb128f5545a235eb2c5c02043231ff1078
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047985"
---
# <span data-ttu-id="4cb97-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="4cb97-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="4cb97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cb97-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb97-103">앱 구성 저장소를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cb97-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="4cb97-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4cb97-104">SYNTAX</span></span>

### <span data-ttu-id="4cb97-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4cb97-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4cb97-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="4cb97-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4cb97-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4cb97-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cb97-108">List1</span><span class="sxs-lookup"><span data-stu-id="4cb97-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4cb97-109">설명은</span><span class="sxs-lookup"><span data-stu-id="4cb97-109">DESCRIPTION</span></span>
<span data-ttu-id="4cb97-110">앱 구성 저장소를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cb97-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="4cb97-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4cb97-111">EXAMPLES</span></span>

### <span data-ttu-id="4cb97-112">예제 1: 구독 하는 모든 앱 구성 저장소 나열</span><span class="sxs-lookup"><span data-stu-id="4cb97-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4cb97-113">이 명령은 구독 하는 모든 앱 구성 저장소를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cb97-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="4cb97-114">예제 2: 리소스 그룹 아래에 모든 앱 구성 저장소 나열</span><span class="sxs-lookup"><span data-stu-id="4cb97-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4cb97-115">이 명령은 리소스 그룹 아래에 모든 앱 구성 저장소를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cb97-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="4cb97-116">예제 3: 이름으로 앱 구성 저장소 가져오기</span><span class="sxs-lookup"><span data-stu-id="4cb97-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4cb97-117">이 명령은 이름으로 앱 구성 저장소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4cb97-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="4cb97-118">예제 4: 파이프라인 별로 앱 구성 저장소 가져오기</span><span class="sxs-lookup"><span data-stu-id="4cb97-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="4cb97-119">이 명령은 파이프라인 별로 앱 구성 저장소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4cb97-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="4cb97-120">변수</span><span class="sxs-lookup"><span data-stu-id="4cb97-120">PARAMETERS</span></span>

### <span data-ttu-id="4cb97-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cb97-121">-DefaultProfile</span></span>
<span data-ttu-id="4cb97-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4cb97-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cb97-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cb97-123">-InputObject</span></span>
<span data-ttu-id="4cb97-124">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4cb97-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cb97-125">-이름</span><span class="sxs-lookup"><span data-stu-id="4cb97-125">-Name</span></span>
<span data-ttu-id="4cb97-126">구성 저장소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cb97-126">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb97-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cb97-127">-ResourceGroupName</span></span>
<span data-ttu-id="4cb97-128">컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cb97-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb97-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4cb97-129">-SubscriptionId</span></span>
<span data-ttu-id="4cb97-130">Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4cb97-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb97-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb97-131">CommonParameters</span></span>
<span data-ttu-id="4cb97-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cb97-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb97-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4cb97-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb97-134">입력</span><span class="sxs-lookup"><span data-stu-id="4cb97-134">INPUTS</span></span>

### <span data-ttu-id="4cb97-135">Microsoft. p p. p. p i d.</span><span class="sxs-lookup"><span data-stu-id="4cb97-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="4cb97-136">출력</span><span class="sxs-lookup"><span data-stu-id="4cb97-136">OUTPUTS</span></span>

### <span data-ttu-id="4cb97-137">Api20200601. IConfigurationStore에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4cb97-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="4cb97-138">상속자</span><span class="sxs-lookup"><span data-stu-id="4cb97-138">NOTES</span></span>

<span data-ttu-id="4cb97-139">별칭과</span><span class="sxs-lookup"><span data-stu-id="4cb97-139">ALIASES</span></span>

<span data-ttu-id="4cb97-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4cb97-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4cb97-141">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cb97-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4cb97-142">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="4cb97-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4cb97-143">INPUTOBJECT <IAppConfigurationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4cb97-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4cb97-144">`[ConfigStoreName <String>]`: 구성 저장소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cb97-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="4cb97-145">`[GroupName <String>]`: 비공개 링크 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cb97-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="4cb97-146">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="4cb97-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4cb97-147">`[PrivateEndpointConnectionName <String>]`: 개인 끝점 연결 이름</span><span class="sxs-lookup"><span data-stu-id="4cb97-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="4cb97-148">`[ResourceGroupName <String>]`: 컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cb97-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="4cb97-149">`[SubscriptionId <String>]`: Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4cb97-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="4cb97-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cb97-150">RELATED LINKS</span></span>

