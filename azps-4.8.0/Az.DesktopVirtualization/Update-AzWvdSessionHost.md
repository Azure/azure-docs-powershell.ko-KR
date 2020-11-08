---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: ec80e3382c401f9d64fb469c58a074ed47719ee9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056376"
---
# <span data-ttu-id="1ce35-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="1ce35-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="1ce35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ce35-102">SYNOPSIS</span></span>
<span data-ttu-id="1ce35-103">세션 호스트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-103">Update a session host.</span></span>

## <span data-ttu-id="1ce35-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1ce35-104">SYNTAX</span></span>

### <span data-ttu-id="1ce35-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1ce35-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1ce35-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1ce35-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1ce35-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1ce35-107">DESCRIPTION</span></span>
<span data-ttu-id="1ce35-108">세션 호스트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-108">Update a session host.</span></span>

## <span data-ttu-id="1ce35-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1ce35-109">EXAMPLES</span></span>

### <span data-ttu-id="1ce35-110">예제 1: 이름으로 Windows 가상 데스크톱 SessionHost 업데이트</span><span class="sxs-lookup"><span data-stu-id="1ce35-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="1ce35-111">이 명령은 호스트 풀에서 Windows 가상 데스크톱 SessionHost를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="1ce35-112">변수</span><span class="sxs-lookup"><span data-stu-id="1ce35-112">PARAMETERS</span></span>

### <span data-ttu-id="1ce35-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="1ce35-113">-AllowNewSession</span></span>
<span data-ttu-id="1ce35-114">새 세션을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-114">Allow a new session.</span></span>

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

### <span data-ttu-id="1ce35-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="1ce35-115">-AssignedUser</span></span>
<span data-ttu-id="1ce35-116">SessionHost에 할당 된 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="1ce35-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ce35-117">-DefaultProfile</span></span>
<span data-ttu-id="1ce35-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ce35-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="1ce35-119">-HostPoolName</span></span>
<span data-ttu-id="1ce35-120">지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="1ce35-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ce35-121">-InputObject</span></span>
<span data-ttu-id="1ce35-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1ce35-123">-이름</span><span class="sxs-lookup"><span data-stu-id="1ce35-123">-Name</span></span>
<span data-ttu-id="1ce35-124">지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-124">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ce35-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ce35-125">-ResourceGroupName</span></span>
<span data-ttu-id="1ce35-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-126">The name of the resource group.</span></span>
<span data-ttu-id="1ce35-127">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1ce35-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ce35-128">-SubscriptionId</span></span>
<span data-ttu-id="1ce35-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1ce35-130">-확인</span><span class="sxs-lookup"><span data-stu-id="1ce35-130">-Confirm</span></span>
<span data-ttu-id="1ce35-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ce35-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ce35-132">-WhatIf</span></span>
<span data-ttu-id="1ce35-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ce35-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ce35-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ce35-135">CommonParameters</span></span>
<span data-ttu-id="1ce35-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ce35-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1ce35-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ce35-138">입력</span><span class="sxs-lookup"><span data-stu-id="1ce35-138">INPUTS</span></span>

### <span data-ttu-id="1ce35-139">IDesktopVirtualizationIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="1ce35-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="1ce35-140">출력</span><span class="sxs-lookup"><span data-stu-id="1ce35-140">OUTPUTS</span></span>

### <span data-ttu-id="1ce35-141">Api20191210Preview. ISessionHost (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ce35-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="1ce35-142">상속자</span><span class="sxs-lookup"><span data-stu-id="1ce35-142">NOTES</span></span>

<span data-ttu-id="1ce35-143">별칭과</span><span class="sxs-lookup"><span data-stu-id="1ce35-143">ALIASES</span></span>

<span data-ttu-id="1ce35-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1ce35-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1ce35-145">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1ce35-146">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="1ce35-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1ce35-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1ce35-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1ce35-148">`[ApplicationGroupName <String>]`: 응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="1ce35-149">`[ApplicationName <String>]`: 지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="1ce35-150">`[DesktopName <String>]`: 지정 된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="1ce35-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="1ce35-151">`[HostPoolName <String>]`: 지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="1ce35-152">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="1ce35-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1ce35-153">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1ce35-154">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="1ce35-155">`[SessionHostName <String>]`: 지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="1ce35-156">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1ce35-157">`[UserSessionId <String>]`: 지정 된 세션 호스트 내에 있는 사용자 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ce35-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="1ce35-158">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="1ce35-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="1ce35-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ce35-159">RELATED LINKS</span></span>

