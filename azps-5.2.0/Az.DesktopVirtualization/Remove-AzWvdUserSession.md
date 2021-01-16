---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: d460b3e10ccc0e2d37a4e2aeb208d0b9f8006a10
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338421"
---
# <span data-ttu-id="46876-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="46876-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="46876-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46876-102">SYNOPSIS</span></span>
<span data-ttu-id="46876-103">userSession을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="46876-103">Remove a userSession.</span></span>

## <span data-ttu-id="46876-104">구문</span><span class="sxs-lookup"><span data-stu-id="46876-104">SYNTAX</span></span>

### <span data-ttu-id="46876-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="46876-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="46876-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="46876-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="46876-107">설명</span><span class="sxs-lookup"><span data-stu-id="46876-107">DESCRIPTION</span></span>
<span data-ttu-id="46876-108">userSession을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="46876-108">Remove a userSession.</span></span>

## <span data-ttu-id="46876-109">예제</span><span class="sxs-lookup"><span data-stu-id="46876-109">EXAMPLES</span></span>

### <span data-ttu-id="46876-110">예제 1: 이름으로 Windows Virtual Desktop UserSession 삭제</span><span class="sxs-lookup"><span data-stu-id="46876-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="46876-111">이 명령은 세션 호스트에서 Windows Virtual Desktop UserSession을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="46876-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="46876-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46876-112">PARAMETERS</span></span>

### <span data-ttu-id="46876-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46876-113">-DefaultProfile</span></span>
<span data-ttu-id="46876-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46876-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46876-115">-Force</span><span class="sxs-lookup"><span data-stu-id="46876-115">-Force</span></span>
<span data-ttu-id="46876-116">플래그를 강제로 사용자 로그인 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="46876-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="46876-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="46876-117">-HostPoolName</span></span>
<span data-ttu-id="46876-118">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="46876-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="46876-119">-Id</span><span class="sxs-lookup"><span data-stu-id="46876-119">-Id</span></span>
<span data-ttu-id="46876-120">지정된 세션 호스트 내의 사용자 세션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46876-120">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46876-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46876-121">-InputObject</span></span>
<span data-ttu-id="46876-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="46876-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="46876-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46876-123">-PassThru</span></span>
<span data-ttu-id="46876-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="46876-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="46876-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46876-125">-ResourceGroupName</span></span>
<span data-ttu-id="46876-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46876-126">The name of the resource group.</span></span>
<span data-ttu-id="46876-127">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="46876-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="46876-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="46876-128">-SessionHostName</span></span>
<span data-ttu-id="46876-129">지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="46876-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="46876-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46876-130">-SubscriptionId</span></span>
<span data-ttu-id="46876-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="46876-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="46876-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46876-132">-Confirm</span></span>
<span data-ttu-id="46876-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="46876-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46876-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46876-134">-WhatIf</span></span>
<span data-ttu-id="46876-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="46876-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46876-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46876-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46876-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46876-137">CommonParameters</span></span>
<span data-ttu-id="46876-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="46876-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46876-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="46876-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46876-140">입력</span><span class="sxs-lookup"><span data-stu-id="46876-140">INPUTS</span></span>

### <span data-ttu-id="46876-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="46876-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="46876-142">출력</span><span class="sxs-lookup"><span data-stu-id="46876-142">OUTPUTS</span></span>

### <span data-ttu-id="46876-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="46876-143">System.Boolean</span></span>

## <span data-ttu-id="46876-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="46876-144">NOTES</span></span>

<span data-ttu-id="46876-145">별칭</span><span class="sxs-lookup"><span data-stu-id="46876-145">ALIASES</span></span>

<span data-ttu-id="46876-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="46876-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="46876-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="46876-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="46876-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="46876-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="46876-149">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="46876-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="46876-150">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="46876-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="46876-151">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="46876-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="46876-152">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="46876-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="46876-153">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="46876-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="46876-154">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="46876-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="46876-155">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="46876-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="46876-156">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46876-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="46876-157">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="46876-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="46876-158">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="46876-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="46876-159">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="46876-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="46876-160">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="46876-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="46876-161">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="46876-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="46876-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46876-162">RELATED LINKS</span></span>

