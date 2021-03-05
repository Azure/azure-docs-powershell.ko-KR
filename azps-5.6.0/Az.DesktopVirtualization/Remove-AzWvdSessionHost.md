---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: ee8334a233c35c2b834bfb89ddf20152d466367f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966000"
---
# <span data-ttu-id="44568-101">Remove-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="44568-101">Remove-AzWvdSessionHost</span></span>

## <span data-ttu-id="44568-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44568-102">SYNOPSIS</span></span>
<span data-ttu-id="44568-103">SessionHost를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44568-103">Remove a SessionHost.</span></span>

## <span data-ttu-id="44568-104">구문</span><span class="sxs-lookup"><span data-stu-id="44568-104">SYNTAX</span></span>

### <span data-ttu-id="44568-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="44568-105">Delete (Default)</span></span>
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="44568-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="44568-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="44568-107">설명</span><span class="sxs-lookup"><span data-stu-id="44568-107">DESCRIPTION</span></span>
<span data-ttu-id="44568-108">SessionHost를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44568-108">Remove a SessionHost.</span></span>

## <span data-ttu-id="44568-109">예제</span><span class="sxs-lookup"><span data-stu-id="44568-109">EXAMPLES</span></span>

### <span data-ttu-id="44568-110">예제 1: 이름에 의해 Windows Virtual Desktop SessionHost 삭제</span><span class="sxs-lookup"><span data-stu-id="44568-110">Example 1: Delete a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

<span data-ttu-id="44568-111">이 명령은 호스트 풀에서 Windows Virtual Desktop SessionHost를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="44568-111">This command deletes a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="44568-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="44568-112">PARAMETERS</span></span>

### <span data-ttu-id="44568-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44568-113">-DefaultProfile</span></span>
<span data-ttu-id="44568-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44568-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44568-115">-Force</span><span class="sxs-lookup"><span data-stu-id="44568-115">-Force</span></span>
<span data-ttu-id="44568-116">사용자 시전이 있는 경우에도 강제로 sessionHost 지우기를 강제로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="44568-116">Force flag to force sessionHost deletion even when userSession exists.</span></span>

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

### <span data-ttu-id="44568-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="44568-117">-HostPoolName</span></span>
<span data-ttu-id="44568-118">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="44568-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="44568-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44568-119">-InputObject</span></span>
<span data-ttu-id="44568-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="44568-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44568-121">-Name</span><span class="sxs-lookup"><span data-stu-id="44568-121">-Name</span></span>
<span data-ttu-id="44568-122">지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="44568-122">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44568-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44568-123">-PassThru</span></span>
<span data-ttu-id="44568-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="44568-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="44568-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44568-125">-ResourceGroupName</span></span>
<span data-ttu-id="44568-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44568-126">The name of the resource group.</span></span>
<span data-ttu-id="44568-127">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="44568-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="44568-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44568-128">-SubscriptionId</span></span>
<span data-ttu-id="44568-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="44568-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="44568-130">-확인</span><span class="sxs-lookup"><span data-stu-id="44568-130">-Confirm</span></span>
<span data-ttu-id="44568-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="44568-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44568-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44568-132">-WhatIf</span></span>
<span data-ttu-id="44568-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="44568-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44568-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44568-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44568-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44568-135">CommonParameters</span></span>
<span data-ttu-id="44568-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="44568-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44568-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44568-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44568-138">입력</span><span class="sxs-lookup"><span data-stu-id="44568-138">INPUTS</span></span>

### <span data-ttu-id="44568-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="44568-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="44568-140">출력</span><span class="sxs-lookup"><span data-stu-id="44568-140">OUTPUTS</span></span>

### <span data-ttu-id="44568-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="44568-141">System.Boolean</span></span>

## <span data-ttu-id="44568-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="44568-142">NOTES</span></span>

<span data-ttu-id="44568-143">별칭</span><span class="sxs-lookup"><span data-stu-id="44568-143">ALIASES</span></span>

<span data-ttu-id="44568-144">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="44568-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="44568-145">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="44568-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="44568-146">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="44568-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="44568-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="44568-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="44568-148">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="44568-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="44568-149">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="44568-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="44568-150">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="44568-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="44568-151">`[HostPoolName <String>]`: 지정된 리소스 그룹 내의 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="44568-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="44568-152">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="44568-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="44568-153">`[MsixPackageFullName <String>]`: 지정된 호스트풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="44568-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="44568-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44568-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="44568-155">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="44568-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="44568-156">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="44568-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="44568-157">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="44568-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="44568-158">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="44568-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="44568-159">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="44568-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="44568-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44568-160">RELATED LINKS</span></span>

