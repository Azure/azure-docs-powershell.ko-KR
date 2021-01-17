---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdWorkspace.md
ms.openlocfilehash: 3fa80fc69679346e3462a96340f4af9fc6a251d5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387283"
---
# <span data-ttu-id="47e80-101">Get-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="47e80-101">Get-AzWvdWorkspace</span></span>

## <span data-ttu-id="47e80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47e80-102">SYNOPSIS</span></span>
<span data-ttu-id="47e80-103">작업 영역이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47e80-103">Get a workspace.</span></span>

## <span data-ttu-id="47e80-104">구문</span><span class="sxs-lookup"><span data-stu-id="47e80-104">SYNTAX</span></span>

### <span data-ttu-id="47e80-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="47e80-105">List1 (Default)</span></span>
```
Get-AzWvdWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="47e80-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="47e80-106">Get</span></span>
```
Get-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="47e80-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="47e80-107">GetViaIdentity</span></span>
```
Get-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="47e80-108">목록</span><span class="sxs-lookup"><span data-stu-id="47e80-108">List</span></span>
```
Get-AzWvdWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="47e80-109">설명</span><span class="sxs-lookup"><span data-stu-id="47e80-109">DESCRIPTION</span></span>
<span data-ttu-id="47e80-110">작업 영역이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="47e80-110">Get a workspace.</span></span>

## <span data-ttu-id="47e80-111">예제</span><span class="sxs-lookup"><span data-stu-id="47e80-111">EXAMPLES</span></span>

### <span data-ttu-id="47e80-112">예제 1: 이름으로 Windows Virtual Desktop 작업 영역 다운로드</span><span class="sxs-lookup"><span data-stu-id="47e80-112">Example 1: Get a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName -Name WorkspaceName

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="47e80-113">이 명령은 리소스 그룹에 Windows Virtual Desktop 작업 영역이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="47e80-113">This command gets a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="47e80-114">예제 2: Windows Virtual Desktop 작업 영역 나열</span><span class="sxs-lookup"><span data-stu-id="47e80-114">Example 2: List Windows Virtual Desktop Workspaces</span></span>
```powershell
PS C:\> Get-AzWvdWorkspace -ResourceGroupName ResourceGroupName

Location   Name           Type
--------   ----           ----
eastus     WorkspaceName1 Microsoft.DesktopVirtualization/workspaces
eastus     WorkspaceName2 Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="47e80-115">이 명령은 리소스 그룹에 Windows Virtual Desktop 작업 영역이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="47e80-115">This command lists a Windows Virtual Desktop Workspaces in a Resource Group.</span></span>

## <span data-ttu-id="47e80-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47e80-116">PARAMETERS</span></span>

### <span data-ttu-id="47e80-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e80-117">-DefaultProfile</span></span>
<span data-ttu-id="47e80-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47e80-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47e80-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47e80-119">-InputObject</span></span>
<span data-ttu-id="47e80-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="47e80-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="47e80-121">-Name</span><span class="sxs-lookup"><span data-stu-id="47e80-121">-Name</span></span>
<span data-ttu-id="47e80-122">작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="47e80-122">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47e80-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47e80-123">-ResourceGroupName</span></span>
<span data-ttu-id="47e80-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47e80-124">The name of the resource group.</span></span>
<span data-ttu-id="47e80-125">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="47e80-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="47e80-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47e80-126">-SubscriptionId</span></span>
<span data-ttu-id="47e80-127">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="47e80-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="47e80-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e80-128">CommonParameters</span></span>
<span data-ttu-id="47e80-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="47e80-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e80-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="47e80-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e80-131">입력</span><span class="sxs-lookup"><span data-stu-id="47e80-131">INPUTS</span></span>

### <span data-ttu-id="47e80-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="47e80-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="47e80-133">출력</span><span class="sxs-lookup"><span data-stu-id="47e80-133">OUTPUTS</span></span>

### <span data-ttu-id="47e80-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="47e80-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="47e80-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="47e80-135">NOTES</span></span>

<span data-ttu-id="47e80-136">별칭</span><span class="sxs-lookup"><span data-stu-id="47e80-136">ALIASES</span></span>

<span data-ttu-id="47e80-137">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="47e80-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47e80-138">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="47e80-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47e80-139">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="47e80-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47e80-140">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="47e80-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="47e80-141">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="47e80-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="47e80-142">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="47e80-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="47e80-143">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="47e80-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="47e80-144">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="47e80-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="47e80-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="47e80-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="47e80-146">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="47e80-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="47e80-147">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47e80-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="47e80-148">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="47e80-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="47e80-149">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="47e80-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="47e80-150">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="47e80-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="47e80-151">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="47e80-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="47e80-152">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="47e80-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="47e80-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47e80-153">RELATED LINKS</span></span>

