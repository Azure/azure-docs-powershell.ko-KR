---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: eedf639ebf5c25ff9153072a337ea659b41a9e92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212261"
---
# <span data-ttu-id="8a1f2-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="8a1f2-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="8a1f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a1f2-102">SYNOPSIS</span></span>
<span data-ttu-id="8a1f2-103">UserSession을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-103">Get a userSession.</span></span>

## <span data-ttu-id="8a1f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a1f2-104">SYNTAX</span></span>

### <span data-ttu-id="8a1f2-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8a1f2-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a1f2-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="8a1f2-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a1f2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8a1f2-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a1f2-108">List1</span><span class="sxs-lookup"><span data-stu-id="8a1f2-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8a1f2-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8a1f2-109">DESCRIPTION</span></span>
<span data-ttu-id="8a1f2-110">UserSession을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-110">Get a userSession.</span></span>

## <span data-ttu-id="8a1f2-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8a1f2-111">EXAMPLES</span></span>

### <span data-ttu-id="8a1f2-112">예제 1: 이름별로 Windows 가상 데스크톱 UserSession 가져오기</span><span class="sxs-lookup"><span data-stu-id="8a1f2-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="8a1f2-113">이 명령은 세션 호스트에서 Windows 가상 데스크톱 UserSession을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="8a1f2-114">예제 2: Windows 가상 데스크톱 UserSessions 목록 표시</span><span class="sxs-lookup"><span data-stu-id="8a1f2-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="8a1f2-115">이 명령은 세션 호스트에 Windows 가상 데스크톱 UserSessions를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="8a1f2-116">예제 3: 호스트 풀에 Windows 가상 데스크톱 UserSessions 나열</span><span class="sxs-lookup"><span data-stu-id="8a1f2-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="8a1f2-117">이 명령은 호스트 풀의 세션 호스트에 Windows 가상 데스크톱 UserSessions를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="8a1f2-118">변수</span><span class="sxs-lookup"><span data-stu-id="8a1f2-118">PARAMETERS</span></span>

### <span data-ttu-id="8a1f2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a1f2-119">-DefaultProfile</span></span>
<span data-ttu-id="8a1f2-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a1f2-121">-필터</span><span class="sxs-lookup"><span data-stu-id="8a1f2-121">-Filter</span></span>
<span data-ttu-id="8a1f2-122">OData 필터 식입니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-122">OData filter expression.</span></span>
<span data-ttu-id="8a1f2-123">유효한 필터링 속성은 userprincipalname 및 sessionstate입니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1f2-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="8a1f2-124">-HostPoolName</span></span>
<span data-ttu-id="8a1f2-125">지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-125">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1f2-126">-Id</span><span class="sxs-lookup"><span data-stu-id="8a1f2-126">-Id</span></span>
<span data-ttu-id="8a1f2-127">지정 된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="8a1f2-127">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1f2-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a1f2-128">-InputObject</span></span>
<span data-ttu-id="8a1f2-129">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a1f2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a1f2-130">-ResourceGroupName</span></span>
<span data-ttu-id="8a1f2-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-131">The name of the resource group.</span></span>
<span data-ttu-id="8a1f2-132">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-132">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1f2-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="8a1f2-133">-SessionHostName</span></span>
<span data-ttu-id="8a1f2-134">지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-134">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="8a1f2-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a1f2-135">-SubscriptionId</span></span>
<span data-ttu-id="8a1f2-136">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8a1f2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a1f2-137">CommonParameters</span></span>
<span data-ttu-id="8a1f2-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a1f2-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a1f2-140">입력</span><span class="sxs-lookup"><span data-stu-id="8a1f2-140">INPUTS</span></span>

### <span data-ttu-id="8a1f2-141">IDesktopVirtualizationIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="8a1f2-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8a1f2-142">출력</span><span class="sxs-lookup"><span data-stu-id="8a1f2-142">OUTPUTS</span></span>

### <span data-ttu-id="8a1f2-143">Api20191210Preview to. i i m. IUserSession</span><span class="sxs-lookup"><span data-stu-id="8a1f2-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IUserSession</span></span>

## <span data-ttu-id="8a1f2-144">상속자</span><span class="sxs-lookup"><span data-stu-id="8a1f2-144">NOTES</span></span>

<span data-ttu-id="8a1f2-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="8a1f2-145">ALIASES</span></span>

<span data-ttu-id="8a1f2-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8a1f2-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a1f2-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a1f2-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a1f2-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8a1f2-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a1f2-150">`[ApplicationGroupName <String>]`: 응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8a1f2-151">`[ApplicationName <String>]`: 지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8a1f2-152">`[DesktopName <String>]`: 지정 된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="8a1f2-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8a1f2-153">`[HostPoolName <String>]`: 지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8a1f2-154">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="8a1f2-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a1f2-155">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8a1f2-156">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="8a1f2-157">`[SessionHostName <String>]`: 지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8a1f2-158">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8a1f2-159">`[UserSessionId <String>]`: 지정 된 세션 호스트 내에 있는 사용자 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8a1f2-160">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="8a1f2-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="8a1f2-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a1f2-161">RELATED LINKS</span></span>

