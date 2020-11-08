---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: b0939a4baa498532a3b519875183e6d1d12945a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213729"
---
# <span data-ttu-id="ad259-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="ad259-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="ad259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad259-102">SYNOPSIS</span></span>
<span data-ttu-id="ad259-103">구성 저장소를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="ad259-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad259-104">SYNTAX</span></span>

### <span data-ttu-id="ad259-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ad259-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ad259-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ad259-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ad259-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ad259-107">DESCRIPTION</span></span>
<span data-ttu-id="ad259-108">구성 저장소를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="ad259-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ad259-109">EXAMPLES</span></span>

### <span data-ttu-id="ad259-110">예제 1: 앱 구성 저장소 제거</span><span class="sxs-lookup"><span data-stu-id="ad259-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="ad259-111">이 명령은 앱 구성 저장소를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="ad259-112">예제 2: 앱 구성 저장소 제거</span><span class="sxs-lookup"><span data-stu-id="ad259-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="ad259-113">이 명령은 앱 구성 저장소를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="ad259-114">변수</span><span class="sxs-lookup"><span data-stu-id="ad259-114">PARAMETERS</span></span>

### <span data-ttu-id="ad259-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad259-115">-AsJob</span></span>
<span data-ttu-id="ad259-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ad259-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ad259-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad259-117">-DefaultProfile</span></span>
<span data-ttu-id="ad259-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad259-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad259-119">-InputObject</span></span>
<span data-ttu-id="ad259-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ad259-121">-이름</span><span class="sxs-lookup"><span data-stu-id="ad259-121">-Name</span></span>
<span data-ttu-id="ad259-122">구성 저장소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="ad259-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ad259-123">-NoWait</span></span>
<span data-ttu-id="ad259-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ad259-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ad259-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad259-125">-PassThru</span></span>
<span data-ttu-id="ad259-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ad259-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad259-127">-ResourceGroupName</span></span>
<span data-ttu-id="ad259-128">컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="ad259-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad259-129">-SubscriptionId</span></span>
<span data-ttu-id="ad259-130">Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="ad259-131">-확인</span><span class="sxs-lookup"><span data-stu-id="ad259-131">-Confirm</span></span>
<span data-ttu-id="ad259-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad259-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad259-133">-WhatIf</span></span>
<span data-ttu-id="ad259-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad259-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad259-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad259-136">CommonParameters</span></span>
<span data-ttu-id="ad259-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad259-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ad259-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad259-139">입력</span><span class="sxs-lookup"><span data-stu-id="ad259-139">INPUTS</span></span>

### <span data-ttu-id="ad259-140">Microsoft. p p. p. p i d.</span><span class="sxs-lookup"><span data-stu-id="ad259-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="ad259-141">출력</span><span class="sxs-lookup"><span data-stu-id="ad259-141">OUTPUTS</span></span>

### <span data-ttu-id="ad259-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ad259-142">System.Boolean</span></span>

## <span data-ttu-id="ad259-143">상속자</span><span class="sxs-lookup"><span data-stu-id="ad259-143">NOTES</span></span>

<span data-ttu-id="ad259-144">별칭과</span><span class="sxs-lookup"><span data-stu-id="ad259-144">ALIASES</span></span>

<span data-ttu-id="ad259-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="ad259-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ad259-146">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ad259-147">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="ad259-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ad259-148">INPUTOBJECT <IAppConfigurationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ad259-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ad259-149">`[ConfigStoreName <String>]`: 구성 저장소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="ad259-150">`[GroupName <String>]`: 비공개 링크 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="ad259-151">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="ad259-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ad259-152">`[PrivateEndpointConnectionName <String>]`: 개인 끝점 연결 이름</span><span class="sxs-lookup"><span data-stu-id="ad259-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="ad259-153">`[ResourceGroupName <String>]`: 컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="ad259-154">`[SubscriptionId <String>]`: Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ad259-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="ad259-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad259-155">RELATED LINKS</span></span>

