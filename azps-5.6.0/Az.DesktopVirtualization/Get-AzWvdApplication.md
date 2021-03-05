---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: b7aa21b07726140f8f6514fe8d7b6dc9a4b191dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962059"
---
# <span data-ttu-id="1ca97-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="1ca97-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="1ca97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ca97-102">SYNOPSIS</span></span>
<span data-ttu-id="1ca97-103">애플리케이션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1ca97-103">Get an application.</span></span>

## <span data-ttu-id="1ca97-104">구문</span><span class="sxs-lookup"><span data-stu-id="1ca97-104">SYNTAX</span></span>

### <span data-ttu-id="1ca97-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="1ca97-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1ca97-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="1ca97-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1ca97-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1ca97-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ca97-108">설명</span><span class="sxs-lookup"><span data-stu-id="1ca97-108">DESCRIPTION</span></span>
<span data-ttu-id="1ca97-109">애플리케이션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1ca97-109">Get an application.</span></span>

## <span data-ttu-id="1ca97-110">예제</span><span class="sxs-lookup"><span data-stu-id="1ca97-110">EXAMPLES</span></span>

### <span data-ttu-id="1ca97-111">예제 1: 이름에 따라 Windows Virtual Desktop 애플리케이션을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="1ca97-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="1ca97-112">이 명령은 해당 애플리케이션 그룹에서 Windows Virtual Desktop Application을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1ca97-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="1ca97-113">예제 2: Windows Virtual Desktop 애플리케이션 나열</span><span class="sxs-lookup"><span data-stu-id="1ca97-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="1ca97-114">이 명령은 해당 애플리케이션 그룹에 Windows Virtual Desktop 애플리케이션을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="1ca97-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="1ca97-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1ca97-115">PARAMETERS</span></span>

### <span data-ttu-id="1ca97-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ca97-116">-DefaultProfile</span></span>
<span data-ttu-id="1ca97-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ca97-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ca97-118">-GroupName</span><span class="sxs-lookup"><span data-stu-id="1ca97-118">-GroupName</span></span>
<span data-ttu-id="1ca97-119">애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="1ca97-119">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ca97-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ca97-120">-InputObject</span></span>
<span data-ttu-id="1ca97-121">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="1ca97-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1ca97-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1ca97-122">-Name</span></span>
<span data-ttu-id="1ca97-123">지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="1ca97-123">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ca97-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ca97-124">-ResourceGroupName</span></span>
<span data-ttu-id="1ca97-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ca97-125">The name of the resource group.</span></span>
<span data-ttu-id="1ca97-126">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="1ca97-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1ca97-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ca97-127">-SubscriptionId</span></span>
<span data-ttu-id="1ca97-128">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1ca97-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1ca97-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ca97-129">CommonParameters</span></span>
<span data-ttu-id="1ca97-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1ca97-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ca97-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ca97-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ca97-132">입력</span><span class="sxs-lookup"><span data-stu-id="1ca97-132">INPUTS</span></span>

### <span data-ttu-id="1ca97-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="1ca97-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="1ca97-134">출력</span><span class="sxs-lookup"><span data-stu-id="1ca97-134">OUTPUTS</span></span>

### <span data-ttu-id="1ca97-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="1ca97-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="1ca97-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1ca97-136">NOTES</span></span>

<span data-ttu-id="1ca97-137">별칭</span><span class="sxs-lookup"><span data-stu-id="1ca97-137">ALIASES</span></span>

<span data-ttu-id="1ca97-138">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1ca97-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1ca97-139">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1ca97-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1ca97-140">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1ca97-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1ca97-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1ca97-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1ca97-142">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="1ca97-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="1ca97-143">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="1ca97-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="1ca97-144">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="1ca97-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="1ca97-145">`[HostPoolName <String>]`: 지정된 리소스 그룹 내의 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="1ca97-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="1ca97-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="1ca97-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1ca97-147">`[MsixPackageFullName <String>]`: 지정된 호스트풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="1ca97-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="1ca97-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1ca97-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1ca97-149">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="1ca97-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="1ca97-150">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="1ca97-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="1ca97-151">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1ca97-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1ca97-152">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="1ca97-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="1ca97-153">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="1ca97-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="1ca97-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ca97-154">RELATED LINKS</span></span>

