---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: 3d1a822bf545cd111ef3fef19ba380f426a831c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328936"
---
# <span data-ttu-id="f5ae9-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="f5ae9-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="f5ae9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5ae9-102">SYNOPSIS</span></span>
<span data-ttu-id="f5ae9-103">데스크톱을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-103">Update a desktop.</span></span>

## <span data-ttu-id="f5ae9-104">구문</span><span class="sxs-lookup"><span data-stu-id="f5ae9-104">SYNTAX</span></span>

### <span data-ttu-id="f5ae9-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="f5ae9-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f5ae9-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f5ae9-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f5ae9-107">설명</span><span class="sxs-lookup"><span data-stu-id="f5ae9-107">DESCRIPTION</span></span>
<span data-ttu-id="f5ae9-108">데스크톱을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-108">Update a desktop.</span></span>

## <span data-ttu-id="f5ae9-109">예제</span><span class="sxs-lookup"><span data-stu-id="f5ae9-109">EXAMPLES</span></span>

### <span data-ttu-id="f5ae9-110">예제 1: Windows Virtual Desktop 데스크톱 업데이트</span><span class="sxs-lookup"><span data-stu-id="f5ae9-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
```powershell
PS C:\> Update-AzWvdDesktop -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name DesktopName `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="f5ae9-111">이 명령은 응용 프로그램 그룹의 Windows Virtual Desktop 데스크톱을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="f5ae9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5ae9-112">PARAMETERS</span></span>

### <span data-ttu-id="f5ae9-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ae9-113">-ApplicationGroupName</span></span>
<span data-ttu-id="f5ae9-114">애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="f5ae9-114">The name of the application group</span></span>

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

### <span data-ttu-id="f5ae9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5ae9-115">-DefaultProfile</span></span>
<span data-ttu-id="f5ae9-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5ae9-117">-Description</span><span class="sxs-lookup"><span data-stu-id="f5ae9-117">-Description</span></span>
<span data-ttu-id="f5ae9-118">데스크톱에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="f5ae9-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f5ae9-119">-FriendlyName</span></span>
<span data-ttu-id="f5ae9-120">바탕 화면의 친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="f5ae9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5ae9-121">-InputObject</span></span>
<span data-ttu-id="f5ae9-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5ae9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f5ae9-123">-Name</span></span>
<span data-ttu-id="f5ae9-124">지정된 데스크톱 그룹 내의 바탕 화면 이름</span><span class="sxs-lookup"><span data-stu-id="f5ae9-124">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5ae9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5ae9-125">-ResourceGroupName</span></span>
<span data-ttu-id="f5ae9-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-126">The name of the resource group.</span></span>
<span data-ttu-id="f5ae9-127">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f5ae9-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5ae9-128">-SubscriptionId</span></span>
<span data-ttu-id="f5ae9-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f5ae9-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="f5ae9-130">-Tag</span></span>
<span data-ttu-id="f5ae9-131">업데이트할 태그</span><span class="sxs-lookup"><span data-stu-id="f5ae9-131">tags to be updated</span></span>

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

### <span data-ttu-id="f5ae9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5ae9-132">-Confirm</span></span>
<span data-ttu-id="f5ae9-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5ae9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5ae9-134">-WhatIf</span></span>
<span data-ttu-id="f5ae9-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f5ae9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5ae9-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5ae9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5ae9-137">CommonParameters</span></span>
<span data-ttu-id="f5ae9-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5ae9-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5ae9-140">입력</span><span class="sxs-lookup"><span data-stu-id="f5ae9-140">INPUTS</span></span>

### <span data-ttu-id="f5ae9-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="f5ae9-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="f5ae9-142">출력</span><span class="sxs-lookup"><span data-stu-id="f5ae9-142">OUTPUTS</span></span>

### <span data-ttu-id="f5ae9-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="f5ae9-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IDesktop</span></span>

## <span data-ttu-id="f5ae9-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f5ae9-144">NOTES</span></span>

<span data-ttu-id="f5ae9-145">별칭</span><span class="sxs-lookup"><span data-stu-id="f5ae9-145">ALIASES</span></span>

<span data-ttu-id="f5ae9-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="f5ae9-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f5ae9-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f5ae9-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f5ae9-149">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f5ae9-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f5ae9-150">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="f5ae9-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="f5ae9-151">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="f5ae9-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="f5ae9-152">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="f5ae9-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="f5ae9-153">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="f5ae9-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="f5ae9-154">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="f5ae9-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f5ae9-155">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="f5ae9-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="f5ae9-156">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f5ae9-157">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="f5ae9-158">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="f5ae9-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="f5ae9-159">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f5ae9-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f5ae9-160">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="f5ae9-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="f5ae9-161">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="f5ae9-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="f5ae9-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5ae9-162">RELATED LINKS</span></span>

