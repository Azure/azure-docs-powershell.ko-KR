---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: a19d1e39fb9ef2e982b569b8c0351d8d1bde1fb2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966176"
---
# <span data-ttu-id="f6070-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="f6070-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="f6070-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6070-102">SYNOPSIS</span></span>
<span data-ttu-id="f6070-103">userSession을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6070-103">Get a userSession.</span></span>

## <span data-ttu-id="f6070-104">구문</span><span class="sxs-lookup"><span data-stu-id="f6070-104">SYNTAX</span></span>

### <span data-ttu-id="f6070-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="f6070-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f6070-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="f6070-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f6070-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f6070-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6070-108">List1</span><span class="sxs-lookup"><span data-stu-id="f6070-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f6070-109">설명</span><span class="sxs-lookup"><span data-stu-id="f6070-109">DESCRIPTION</span></span>
<span data-ttu-id="f6070-110">userSession을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6070-110">Get a userSession.</span></span>

## <span data-ttu-id="f6070-111">예제</span><span class="sxs-lookup"><span data-stu-id="f6070-111">EXAMPLES</span></span>

### <span data-ttu-id="f6070-112">예제 1: 이름에 따라 Windows Virtual Desktop UserSession 다운로드</span><span class="sxs-lookup"><span data-stu-id="f6070-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="f6070-113">이 명령은 세션 호스트에서 Windows Virtual Desktop UserSession을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6070-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="f6070-114">예제 2: Windows Virtual Desktop UserSessions 나열</span><span class="sxs-lookup"><span data-stu-id="f6070-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="f6070-115">이 명령은 세션 호스트에 Windows Virtual Desktop UserSessions를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="f6070-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="f6070-116">예제 3: 호스트 풀에 Windows Virtual Desktop UserSessions 나열</span><span class="sxs-lookup"><span data-stu-id="f6070-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="f6070-117">이 명령은 호스트 풀의 세션 호스트에 Windows Virtual Desktop UserSessions를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="f6070-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="f6070-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f6070-118">PARAMETERS</span></span>

### <span data-ttu-id="f6070-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6070-119">-DefaultProfile</span></span>
<span data-ttu-id="f6070-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6070-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6070-121">-Filter</span><span class="sxs-lookup"><span data-stu-id="f6070-121">-Filter</span></span>
<span data-ttu-id="f6070-122">OData 필터 식입니다.</span><span class="sxs-lookup"><span data-stu-id="f6070-122">OData filter expression.</span></span>
<span data-ttu-id="f6070-123">필터링에 대한 유효한 속성은 userprincipalname 및 sessionstate입니다.</span><span class="sxs-lookup"><span data-stu-id="f6070-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

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

### <span data-ttu-id="f6070-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="f6070-124">-HostPoolName</span></span>
<span data-ttu-id="f6070-125">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="f6070-125">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="f6070-126">-Id</span><span class="sxs-lookup"><span data-stu-id="f6070-126">-Id</span></span>
<span data-ttu-id="f6070-127">지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="f6070-127">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="f6070-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6070-128">-InputObject</span></span>
<span data-ttu-id="f6070-129">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="f6070-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f6070-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6070-130">-ResourceGroupName</span></span>
<span data-ttu-id="f6070-131">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6070-131">The name of the resource group.</span></span>
<span data-ttu-id="f6070-132">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="f6070-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f6070-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="f6070-133">-SessionHostName</span></span>
<span data-ttu-id="f6070-134">지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="f6070-134">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="f6070-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6070-135">-SubscriptionId</span></span>
<span data-ttu-id="f6070-136">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f6070-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f6070-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6070-137">CommonParameters</span></span>
<span data-ttu-id="f6070-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f6070-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6070-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6070-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6070-140">입력</span><span class="sxs-lookup"><span data-stu-id="f6070-140">INPUTS</span></span>

### <span data-ttu-id="f6070-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="f6070-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="f6070-142">출력</span><span class="sxs-lookup"><span data-stu-id="f6070-142">OUTPUTS</span></span>

### <span data-ttu-id="f6070-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IUserSession</span><span class="sxs-lookup"><span data-stu-id="f6070-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IUserSession</span></span>

## <span data-ttu-id="f6070-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f6070-144">NOTES</span></span>

<span data-ttu-id="f6070-145">별칭</span><span class="sxs-lookup"><span data-stu-id="f6070-145">ALIASES</span></span>

<span data-ttu-id="f6070-146">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="f6070-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f6070-147">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f6070-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6070-148">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f6070-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f6070-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f6070-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f6070-150">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="f6070-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="f6070-151">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="f6070-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="f6070-152">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="f6070-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="f6070-153">`[HostPoolName <String>]`: 지정된 리소스 그룹 내의 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="f6070-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="f6070-154">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="f6070-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f6070-155">`[MsixPackageFullName <String>]`: 지정된 호스트풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="f6070-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="f6070-156">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6070-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f6070-157">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="f6070-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="f6070-158">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="f6070-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="f6070-159">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f6070-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f6070-160">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="f6070-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="f6070-161">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="f6070-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="f6070-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6070-162">RELATED LINKS</span></span>

