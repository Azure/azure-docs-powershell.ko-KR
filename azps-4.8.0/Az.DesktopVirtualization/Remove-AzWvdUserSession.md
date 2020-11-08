---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: da00f15a43b74cbdbc516b86da442f0777775627
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212257"
---
# <span data-ttu-id="15310-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="15310-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="15310-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15310-102">SYNOPSIS</span></span>
<span data-ttu-id="15310-103">UserSession을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="15310-103">Remove a userSession.</span></span>

## <span data-ttu-id="15310-104">구문과</span><span class="sxs-lookup"><span data-stu-id="15310-104">SYNTAX</span></span>

### <span data-ttu-id="15310-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="15310-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="15310-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="15310-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="15310-107">설명은</span><span class="sxs-lookup"><span data-stu-id="15310-107">DESCRIPTION</span></span>
<span data-ttu-id="15310-108">UserSession을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="15310-108">Remove a userSession.</span></span>

## <span data-ttu-id="15310-109">예제의</span><span class="sxs-lookup"><span data-stu-id="15310-109">EXAMPLES</span></span>

### <span data-ttu-id="15310-110">예제 1: 이름으로 Windows 가상 데스크톱 UserSession 삭제</span><span class="sxs-lookup"><span data-stu-id="15310-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="15310-111">이 명령은 세션 호스트에서 Windows 가상 데스크톱 UserSession을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="15310-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="15310-112">변수</span><span class="sxs-lookup"><span data-stu-id="15310-112">PARAMETERS</span></span>

### <span data-ttu-id="15310-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15310-113">-DefaultProfile</span></span>
<span data-ttu-id="15310-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15310-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15310-115">-Force</span><span class="sxs-lookup"><span data-stu-id="15310-115">-Force</span></span>
<span data-ttu-id="15310-116">강제 플래그를 userSession에 로그인 합니다.</span><span class="sxs-lookup"><span data-stu-id="15310-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="15310-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="15310-117">-HostPoolName</span></span>
<span data-ttu-id="15310-118">지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15310-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="15310-119">-Id</span><span class="sxs-lookup"><span data-stu-id="15310-119">-Id</span></span>
<span data-ttu-id="15310-120">지정 된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="15310-120">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="15310-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15310-121">-InputObject</span></span>
<span data-ttu-id="15310-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="15310-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="15310-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15310-123">-PassThru</span></span>
<span data-ttu-id="15310-124">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="15310-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="15310-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15310-125">-ResourceGroupName</span></span>
<span data-ttu-id="15310-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15310-126">The name of the resource group.</span></span>
<span data-ttu-id="15310-127">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="15310-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="15310-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="15310-128">-SessionHostName</span></span>
<span data-ttu-id="15310-129">지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15310-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="15310-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15310-130">-SubscriptionId</span></span>
<span data-ttu-id="15310-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="15310-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="15310-132">-확인</span><span class="sxs-lookup"><span data-stu-id="15310-132">-Confirm</span></span>
<span data-ttu-id="15310-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="15310-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15310-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15310-134">-WhatIf</span></span>
<span data-ttu-id="15310-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="15310-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15310-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15310-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15310-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15310-137">CommonParameters</span></span>
<span data-ttu-id="15310-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="15310-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15310-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="15310-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15310-140">입력</span><span class="sxs-lookup"><span data-stu-id="15310-140">INPUTS</span></span>

### <span data-ttu-id="15310-141">IDesktopVirtualizationIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="15310-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="15310-142">출력</span><span class="sxs-lookup"><span data-stu-id="15310-142">OUTPUTS</span></span>

### <span data-ttu-id="15310-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="15310-143">System.Boolean</span></span>

## <span data-ttu-id="15310-144">상속자</span><span class="sxs-lookup"><span data-stu-id="15310-144">NOTES</span></span>

<span data-ttu-id="15310-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="15310-145">ALIASES</span></span>

<span data-ttu-id="15310-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="15310-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="15310-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="15310-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="15310-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="15310-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="15310-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="15310-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="15310-150">`[ApplicationGroupName <String>]`: 응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15310-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="15310-151">`[ApplicationName <String>]`: 지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15310-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="15310-152">`[DesktopName <String>]`: 지정 된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="15310-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="15310-153">`[HostPoolName <String>]`: 지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15310-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="15310-154">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="15310-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="15310-155">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15310-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="15310-156">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="15310-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="15310-157">`[SessionHostName <String>]`: 지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15310-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="15310-158">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="15310-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="15310-159">`[UserSessionId <String>]`: 지정 된 세션 호스트 내에 있는 사용자 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="15310-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="15310-160">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="15310-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="15310-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15310-161">RELATED LINKS</span></span>

