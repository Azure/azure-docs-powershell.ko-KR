---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: de52995d5cda17e332c137966f58b349d64c01f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492068"
---
# <span data-ttu-id="e46f9-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="e46f9-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="e46f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e46f9-102">SYNOPSIS</span></span>
<span data-ttu-id="e46f9-103">데스크톱을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e46f9-103">Get a desktop.</span></span>

## <span data-ttu-id="e46f9-104">구문</span><span class="sxs-lookup"><span data-stu-id="e46f9-104">SYNTAX</span></span>

### <span data-ttu-id="e46f9-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="e46f9-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e46f9-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="e46f9-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e46f9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e46f9-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e46f9-108">설명</span><span class="sxs-lookup"><span data-stu-id="e46f9-108">DESCRIPTION</span></span>
<span data-ttu-id="e46f9-109">데스크톱을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e46f9-109">Get a desktop.</span></span>

## <span data-ttu-id="e46f9-110">예제</span><span class="sxs-lookup"><span data-stu-id="e46f9-110">EXAMPLES</span></span>

### <span data-ttu-id="e46f9-111">예제 1: 이름으로 Windows Virtual Desktop 데스크톱 다운로드</span><span class="sxs-lookup"><span data-stu-id="e46f9-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="e46f9-112">이 명령은 응용 프로그램 그룹에서 Windows Virtual Desktop 데스크톱을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e46f9-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="e46f9-113">예제 2: Windows Virtual Desktop 데스크톱 나열</span><span class="sxs-lookup"><span data-stu-id="e46f9-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="e46f9-114">이 명령은 응용 프로그램 그룹의 Virtual Desktops를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e46f9-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="e46f9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e46f9-115">PARAMETERS</span></span>

### <span data-ttu-id="e46f9-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="e46f9-116">-ApplicationGroupName</span></span>
<span data-ttu-id="e46f9-117">애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="e46f9-117">The name of the application group</span></span>

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

### <span data-ttu-id="e46f9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e46f9-118">-DefaultProfile</span></span>
<span data-ttu-id="e46f9-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e46f9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e46f9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e46f9-120">-InputObject</span></span>
<span data-ttu-id="e46f9-121">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="e46f9-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e46f9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e46f9-122">-Name</span></span>
<span data-ttu-id="e46f9-123">지정된 데스크톱 그룹 내의 바탕 화면 이름</span><span class="sxs-lookup"><span data-stu-id="e46f9-123">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e46f9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e46f9-124">-ResourceGroupName</span></span>
<span data-ttu-id="e46f9-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e46f9-125">The name of the resource group.</span></span>
<span data-ttu-id="e46f9-126">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="e46f9-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e46f9-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e46f9-127">-SubscriptionId</span></span>
<span data-ttu-id="e46f9-128">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e46f9-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e46f9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e46f9-129">CommonParameters</span></span>
<span data-ttu-id="e46f9-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e46f9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e46f9-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e46f9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e46f9-132">입력</span><span class="sxs-lookup"><span data-stu-id="e46f9-132">INPUTS</span></span>

### <span data-ttu-id="e46f9-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="e46f9-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="e46f9-134">출력</span><span class="sxs-lookup"><span data-stu-id="e46f9-134">OUTPUTS</span></span>

### <span data-ttu-id="e46f9-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span><span class="sxs-lookup"><span data-stu-id="e46f9-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktop</span></span>

### <span data-ttu-id="e46f9-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span><span class="sxs-lookup"><span data-stu-id="e46f9-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IDesktopList</span></span>

## <span data-ttu-id="e46f9-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e46f9-137">NOTES</span></span>

<span data-ttu-id="e46f9-138">별칭</span><span class="sxs-lookup"><span data-stu-id="e46f9-138">ALIASES</span></span>

<span data-ttu-id="e46f9-139">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e46f9-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e46f9-140">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e46f9-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e46f9-141">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e46f9-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e46f9-142">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e46f9-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e46f9-143">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="e46f9-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="e46f9-144">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="e46f9-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="e46f9-145">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="e46f9-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="e46f9-146">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="e46f9-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="e46f9-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="e46f9-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e46f9-148">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="e46f9-148">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="e46f9-149">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e46f9-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e46f9-150">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="e46f9-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="e46f9-151">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="e46f9-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="e46f9-152">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e46f9-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e46f9-153">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="e46f9-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="e46f9-154">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="e46f9-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="e46f9-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e46f9-155">RELATED LINKS</span></span>

