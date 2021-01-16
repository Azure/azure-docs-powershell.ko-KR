---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: b0939a4baa498532a3b519875183e6d1d12945a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322517"
---
# <span data-ttu-id="664e7-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="664e7-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="664e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="664e7-102">SYNOPSIS</span></span>
<span data-ttu-id="664e7-103">구성 저장소를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="664e7-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="664e7-104">구문</span><span class="sxs-lookup"><span data-stu-id="664e7-104">SYNTAX</span></span>

### <span data-ttu-id="664e7-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="664e7-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="664e7-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="664e7-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="664e7-107">설명</span><span class="sxs-lookup"><span data-stu-id="664e7-107">DESCRIPTION</span></span>
<span data-ttu-id="664e7-108">구성 저장소를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="664e7-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="664e7-109">예제</span><span class="sxs-lookup"><span data-stu-id="664e7-109">EXAMPLES</span></span>

### <span data-ttu-id="664e7-110">예제 1: 앱 구성 저장소 제거</span><span class="sxs-lookup"><span data-stu-id="664e7-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="664e7-111">이 명령은 앱 구성 저장소를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="664e7-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="664e7-112">예제 2: 앱 구성 저장소 제거</span><span class="sxs-lookup"><span data-stu-id="664e7-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="664e7-113">이 명령은 앱 구성 저장소를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="664e7-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="664e7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="664e7-114">PARAMETERS</span></span>

### <span data-ttu-id="664e7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="664e7-115">-AsJob</span></span>
<span data-ttu-id="664e7-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="664e7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="664e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="664e7-117">-DefaultProfile</span></span>
<span data-ttu-id="664e7-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="664e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="664e7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="664e7-119">-InputObject</span></span>
<span data-ttu-id="664e7-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="664e7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="664e7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="664e7-121">-Name</span></span>
<span data-ttu-id="664e7-122">구성 저장소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="664e7-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="664e7-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="664e7-123">-NoWait</span></span>
<span data-ttu-id="664e7-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="664e7-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="664e7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="664e7-125">-PassThru</span></span>
<span data-ttu-id="664e7-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="664e7-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="664e7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="664e7-127">-ResourceGroupName</span></span>
<span data-ttu-id="664e7-128">컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="664e7-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="664e7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="664e7-129">-SubscriptionId</span></span>
<span data-ttu-id="664e7-130">Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="664e7-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="664e7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="664e7-131">-Confirm</span></span>
<span data-ttu-id="664e7-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="664e7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="664e7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="664e7-133">-WhatIf</span></span>
<span data-ttu-id="664e7-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="664e7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="664e7-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="664e7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="664e7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="664e7-136">CommonParameters</span></span>
<span data-ttu-id="664e7-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="664e7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="664e7-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="664e7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="664e7-139">입력</span><span class="sxs-lookup"><span data-stu-id="664e7-139">INPUTS</span></span>

### <span data-ttu-id="664e7-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="664e7-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="664e7-141">출력</span><span class="sxs-lookup"><span data-stu-id="664e7-141">OUTPUTS</span></span>

### <span data-ttu-id="664e7-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="664e7-142">System.Boolean</span></span>

## <span data-ttu-id="664e7-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="664e7-143">NOTES</span></span>

<span data-ttu-id="664e7-144">별칭</span><span class="sxs-lookup"><span data-stu-id="664e7-144">ALIASES</span></span>

<span data-ttu-id="664e7-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="664e7-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="664e7-146">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="664e7-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="664e7-147">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="664e7-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="664e7-148">INPUTOBJECT: <IAppConfigurationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="664e7-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="664e7-149">`[ConfigStoreName <String>]`: 구성 저장소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="664e7-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="664e7-150">`[GroupName <String>]`: 개인 링크 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="664e7-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="664e7-151">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="664e7-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="664e7-152">`[PrivateEndpointConnectionName <String>]`: 개인 엔드포인트 연결 이름</span><span class="sxs-lookup"><span data-stu-id="664e7-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="664e7-153">`[ResourceGroupName <String>]`: 컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="664e7-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="664e7-154">`[SubscriptionId <String>]`: Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="664e7-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="664e7-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="664e7-155">RELATED LINKS</span></span>

