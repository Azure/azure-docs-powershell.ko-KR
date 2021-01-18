---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: b03fe0c62a446c9ed54c9330708f29737e18bd59
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493059"
---
# <span data-ttu-id="2b00f-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="2b00f-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="2b00f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b00f-102">SYNOPSIS</span></span>
<span data-ttu-id="2b00f-103">applicationGroup을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2b00f-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="2b00f-104">구문</span><span class="sxs-lookup"><span data-stu-id="2b00f-104">SYNTAX</span></span>

### <span data-ttu-id="2b00f-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="2b00f-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2b00f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2b00f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="2b00f-107">설명</span><span class="sxs-lookup"><span data-stu-id="2b00f-107">DESCRIPTION</span></span>
<span data-ttu-id="2b00f-108">applicationGroup을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2b00f-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="2b00f-109">예제</span><span class="sxs-lookup"><span data-stu-id="2b00f-109">EXAMPLES</span></span>

### <span data-ttu-id="2b00f-110">예제 1: 이름으로 Windows Virtual Desktop ApplicationGroup 만들기</span><span class="sxs-lookup"><span data-stu-id="2b00f-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="2b00f-111">이 명령은 리소스 그룹에 Windows Virtual Desktop ApplicationGroup을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b00f-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="2b00f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b00f-112">PARAMETERS</span></span>

### <span data-ttu-id="2b00f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b00f-113">-DefaultProfile</span></span>
<span data-ttu-id="2b00f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b00f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b00f-115">-Description</span><span class="sxs-lookup"><span data-stu-id="2b00f-115">-Description</span></span>
<span data-ttu-id="2b00f-116">ApplicationGroup에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="2b00f-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="2b00f-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2b00f-117">-FriendlyName</span></span>
<span data-ttu-id="2b00f-118">ApplicationGroup의 친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b00f-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="2b00f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b00f-119">-InputObject</span></span>
<span data-ttu-id="2b00f-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="2b00f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2b00f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2b00f-121">-Name</span></span>
<span data-ttu-id="2b00f-122">애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="2b00f-122">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b00f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b00f-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b00f-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b00f-124">The name of the resource group.</span></span>
<span data-ttu-id="2b00f-125">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="2b00f-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2b00f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b00f-126">-SubscriptionId</span></span>
<span data-ttu-id="2b00f-127">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2b00f-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2b00f-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b00f-128">-Tag</span></span>
<span data-ttu-id="2b00f-129">업데이트할 태그</span><span class="sxs-lookup"><span data-stu-id="2b00f-129">tags to be updated</span></span>

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

### <span data-ttu-id="2b00f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b00f-130">-Confirm</span></span>
<span data-ttu-id="2b00f-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b00f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b00f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b00f-132">-WhatIf</span></span>
<span data-ttu-id="2b00f-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2b00f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b00f-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b00f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b00f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b00f-135">CommonParameters</span></span>
<span data-ttu-id="2b00f-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2b00f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b00f-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2b00f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b00f-138">입력</span><span class="sxs-lookup"><span data-stu-id="2b00f-138">INPUTS</span></span>

### <span data-ttu-id="2b00f-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="2b00f-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="2b00f-140">출력</span><span class="sxs-lookup"><span data-stu-id="2b00f-140">OUTPUTS</span></span>

### <span data-ttu-id="2b00f-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="2b00f-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="2b00f-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2b00f-142">NOTES</span></span>

<span data-ttu-id="2b00f-143">별칭</span><span class="sxs-lookup"><span data-stu-id="2b00f-143">ALIASES</span></span>

<span data-ttu-id="2b00f-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="2b00f-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2b00f-145">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2b00f-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2b00f-146">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2b00f-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2b00f-147">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2b00f-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2b00f-148">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="2b00f-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="2b00f-149">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="2b00f-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="2b00f-150">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="2b00f-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="2b00f-151">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="2b00f-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="2b00f-152">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="2b00f-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2b00f-153">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="2b00f-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="2b00f-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b00f-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2b00f-155">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="2b00f-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="2b00f-156">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="2b00f-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="2b00f-157">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2b00f-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2b00f-158">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="2b00f-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="2b00f-159">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="2b00f-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="2b00f-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b00f-160">RELATED LINKS</span></span>

