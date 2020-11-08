---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: f7bad3a88f4d182407a90a2484daed3d538e3a69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214550"
---
# <span data-ttu-id="d5fc3-101">Remove-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="d5fc3-101">Remove-AzWvdSessionHost</span></span>

## <span data-ttu-id="d5fc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="d5fc3-103">SessionHost를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-103">Remove a SessionHost.</span></span>

## <span data-ttu-id="d5fc3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5fc3-104">SYNTAX</span></span>

### <span data-ttu-id="d5fc3-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d5fc3-105">Delete (Default)</span></span>
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d5fc3-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d5fc3-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d5fc3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d5fc3-107">DESCRIPTION</span></span>
<span data-ttu-id="d5fc3-108">SessionHost를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-108">Remove a SessionHost.</span></span>

## <span data-ttu-id="d5fc3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d5fc3-109">EXAMPLES</span></span>

### <span data-ttu-id="d5fc3-110">예제 1: 이름으로 Windows 가상 데스크톱 SessionHost 삭제</span><span class="sxs-lookup"><span data-stu-id="d5fc3-110">Example 1: Delete a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

<span data-ttu-id="d5fc3-111">이 명령은 호스트 풀에서 Windows 가상 데스크톱 SessionHost를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-111">This command deletes a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="d5fc3-112">변수</span><span class="sxs-lookup"><span data-stu-id="d5fc3-112">PARAMETERS</span></span>

### <span data-ttu-id="d5fc3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5fc3-113">-DefaultProfile</span></span>
<span data-ttu-id="d5fc3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5fc3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d5fc3-115">-Force</span></span>
<span data-ttu-id="d5fc3-116">UserSession이 존재 하는 경우에도 sessionHost를 강제로 삭제 하도록 강제 플래그</span><span class="sxs-lookup"><span data-stu-id="d5fc3-116">Force flag to force sessionHost deletion even when userSession exists.</span></span>

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

### <span data-ttu-id="d5fc3-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="d5fc3-117">-HostPoolName</span></span>
<span data-ttu-id="d5fc3-118">지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="d5fc3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5fc3-119">-InputObject</span></span>
<span data-ttu-id="d5fc3-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d5fc3-121">-이름</span><span class="sxs-lookup"><span data-stu-id="d5fc3-121">-Name</span></span>
<span data-ttu-id="d5fc3-122">지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-122">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="d5fc3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5fc3-123">-PassThru</span></span>
<span data-ttu-id="d5fc3-124">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d5fc3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5fc3-125">-ResourceGroupName</span></span>
<span data-ttu-id="d5fc3-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-126">The name of the resource group.</span></span>
<span data-ttu-id="d5fc3-127">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d5fc3-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5fc3-128">-SubscriptionId</span></span>
<span data-ttu-id="d5fc3-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d5fc3-130">-확인</span><span class="sxs-lookup"><span data-stu-id="d5fc3-130">-Confirm</span></span>
<span data-ttu-id="d5fc3-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5fc3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5fc3-132">-WhatIf</span></span>
<span data-ttu-id="d5fc3-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5fc3-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5fc3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5fc3-135">CommonParameters</span></span>
<span data-ttu-id="d5fc3-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5fc3-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5fc3-138">입력</span><span class="sxs-lookup"><span data-stu-id="d5fc3-138">INPUTS</span></span>

### <span data-ttu-id="d5fc3-139">IDesktopVirtualizationIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="d5fc3-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="d5fc3-140">출력</span><span class="sxs-lookup"><span data-stu-id="d5fc3-140">OUTPUTS</span></span>

### <span data-ttu-id="d5fc3-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="d5fc3-141">System.Boolean</span></span>

## <span data-ttu-id="d5fc3-142">상속자</span><span class="sxs-lookup"><span data-stu-id="d5fc3-142">NOTES</span></span>

<span data-ttu-id="d5fc3-143">별칭과</span><span class="sxs-lookup"><span data-stu-id="d5fc3-143">ALIASES</span></span>

<span data-ttu-id="d5fc3-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d5fc3-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d5fc3-145">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d5fc3-146">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d5fc3-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d5fc3-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d5fc3-148">`[ApplicationGroupName <String>]`: 응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="d5fc3-149">`[ApplicationName <String>]`: 지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="d5fc3-150">`[DesktopName <String>]`: 지정 된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="d5fc3-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="d5fc3-151">`[HostPoolName <String>]`: 지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="d5fc3-152">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="d5fc3-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d5fc3-153">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d5fc3-154">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="d5fc3-155">`[SessionHostName <String>]`: 지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="d5fc3-156">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d5fc3-157">`[UserSessionId <String>]`: 지정 된 세션 호스트 내에 있는 사용자 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5fc3-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="d5fc3-158">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="d5fc3-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="d5fc3-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5fc3-159">RELATED LINKS</span></span>

