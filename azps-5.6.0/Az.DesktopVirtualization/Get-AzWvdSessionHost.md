---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 1e7727933f01f1b2fa3196e3c195c25dda5c247b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962016"
---
# <span data-ttu-id="48409-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="48409-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="48409-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48409-102">SYNOPSIS</span></span>
<span data-ttu-id="48409-103">세션 호스트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48409-103">Get a session host.</span></span>

## <span data-ttu-id="48409-104">구문</span><span class="sxs-lookup"><span data-stu-id="48409-104">SYNTAX</span></span>

### <span data-ttu-id="48409-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="48409-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48409-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="48409-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48409-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="48409-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="48409-108">설명</span><span class="sxs-lookup"><span data-stu-id="48409-108">DESCRIPTION</span></span>
<span data-ttu-id="48409-109">세션 호스트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48409-109">Get a session host.</span></span>

## <span data-ttu-id="48409-110">예제</span><span class="sxs-lookup"><span data-stu-id="48409-110">EXAMPLES</span></span>

### <span data-ttu-id="48409-111">예제 1: 이름에 의해 Windows Virtual Desktop SessionHost 다운로드</span><span class="sxs-lookup"><span data-stu-id="48409-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="48409-112">이 명령은 호스트 풀에서 Windows Virtual Desktop SessionHost를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="48409-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="48409-113">예제 2: Windows Virtual Desktop SessionHosts 나열</span><span class="sxs-lookup"><span data-stu-id="48409-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="48409-114">이 명령은 호스트 풀에 Windows Virtual Desktop SessionHosts를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="48409-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="48409-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="48409-115">PARAMETERS</span></span>

### <span data-ttu-id="48409-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48409-116">-DefaultProfile</span></span>
<span data-ttu-id="48409-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="48409-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48409-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="48409-118">-HostPoolName</span></span>
<span data-ttu-id="48409-119">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="48409-119">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48409-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48409-120">-InputObject</span></span>
<span data-ttu-id="48409-121">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="48409-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="48409-122">-Name</span><span class="sxs-lookup"><span data-stu-id="48409-122">-Name</span></span>
<span data-ttu-id="48409-123">지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="48409-123">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48409-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48409-124">-ResourceGroupName</span></span>
<span data-ttu-id="48409-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48409-125">The name of the resource group.</span></span>
<span data-ttu-id="48409-126">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="48409-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48409-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48409-127">-SubscriptionId</span></span>
<span data-ttu-id="48409-128">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="48409-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48409-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48409-129">CommonParameters</span></span>
<span data-ttu-id="48409-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="48409-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48409-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48409-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48409-132">입력</span><span class="sxs-lookup"><span data-stu-id="48409-132">INPUTS</span></span>

### <span data-ttu-id="48409-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="48409-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="48409-134">출력</span><span class="sxs-lookup"><span data-stu-id="48409-134">OUTPUTS</span></span>

### <span data-ttu-id="48409-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span><span class="sxs-lookup"><span data-stu-id="48409-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span></span>

## <span data-ttu-id="48409-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="48409-136">NOTES</span></span>

<span data-ttu-id="48409-137">별칭</span><span class="sxs-lookup"><span data-stu-id="48409-137">ALIASES</span></span>

<span data-ttu-id="48409-138">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="48409-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="48409-139">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="48409-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48409-140">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="48409-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="48409-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="48409-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="48409-142">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="48409-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="48409-143">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="48409-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="48409-144">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="48409-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="48409-145">`[HostPoolName <String>]`: 지정된 리소스 그룹 내의 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="48409-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="48409-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="48409-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="48409-147">`[MsixPackageFullName <String>]`: 지정된 호스트풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="48409-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="48409-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48409-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="48409-149">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="48409-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="48409-150">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="48409-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="48409-151">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="48409-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="48409-152">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="48409-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="48409-153">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="48409-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="48409-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48409-154">RELATED LINKS</span></span>

