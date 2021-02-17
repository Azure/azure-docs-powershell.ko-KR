---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 5f2ccffd0b0ba82b215db018ee15f4e495704f15
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180817"
---
# <span data-ttu-id="61a90-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="61a90-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="61a90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61a90-102">SYNOPSIS</span></span>
<span data-ttu-id="61a90-103">애플리케이션 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="61a90-103">Get an application group.</span></span>

## <span data-ttu-id="61a90-104">구문</span><span class="sxs-lookup"><span data-stu-id="61a90-104">SYNTAX</span></span>

### <span data-ttu-id="61a90-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="61a90-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="61a90-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="61a90-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="61a90-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="61a90-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="61a90-108">목록</span><span class="sxs-lookup"><span data-stu-id="61a90-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="61a90-109">설명</span><span class="sxs-lookup"><span data-stu-id="61a90-109">DESCRIPTION</span></span>
<span data-ttu-id="61a90-110">애플리케이션 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="61a90-110">Get an application group.</span></span>

## <span data-ttu-id="61a90-111">예제</span><span class="sxs-lookup"><span data-stu-id="61a90-111">EXAMPLES</span></span>

### <span data-ttu-id="61a90-112">예제 1: 이름으로 Windows Virtual Desktop ApplicationGroup 다운로드</span><span class="sxs-lookup"><span data-stu-id="61a90-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="61a90-113">이 명령은 리소스 그룹에서 Windows Virtual Desktop ApplicationGroup을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="61a90-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="61a90-114">예제 2: Windows Virtual Desktop ApplicationGroups 나열</span><span class="sxs-lookup"><span data-stu-id="61a90-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="61a90-115">이 명령은 리소스 그룹에 Windows Virtual Desktop ApplicationGroups를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="61a90-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="61a90-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61a90-116">PARAMETERS</span></span>

### <span data-ttu-id="61a90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a90-117">-DefaultProfile</span></span>
<span data-ttu-id="61a90-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="61a90-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61a90-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="61a90-119">-Filter</span></span>
<span data-ttu-id="61a90-120">OData 필터 식입니다.</span><span class="sxs-lookup"><span data-stu-id="61a90-120">OData filter expression.</span></span>
<span data-ttu-id="61a90-121">필터링에 유효한 속성은 applicationGroupType입니다.</span><span class="sxs-lookup"><span data-stu-id="61a90-121">Valid properties for filtering are applicationGroupType.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a90-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61a90-122">-InputObject</span></span>
<span data-ttu-id="61a90-123">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="61a90-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="61a90-124">-Name</span><span class="sxs-lookup"><span data-stu-id="61a90-124">-Name</span></span>
<span data-ttu-id="61a90-125">애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="61a90-125">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a90-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61a90-126">-ResourceGroupName</span></span>
<span data-ttu-id="61a90-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61a90-127">The name of the resource group.</span></span>
<span data-ttu-id="61a90-128">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="61a90-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="61a90-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="61a90-129">-SubscriptionId</span></span>
<span data-ttu-id="61a90-130">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="61a90-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="61a90-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a90-131">CommonParameters</span></span>
<span data-ttu-id="61a90-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="61a90-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a90-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61a90-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a90-134">입력</span><span class="sxs-lookup"><span data-stu-id="61a90-134">INPUTS</span></span>

### <span data-ttu-id="61a90-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="61a90-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="61a90-136">출력</span><span class="sxs-lookup"><span data-stu-id="61a90-136">OUTPUTS</span></span>

### <span data-ttu-id="61a90-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="61a90-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="61a90-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="61a90-138">NOTES</span></span>

<span data-ttu-id="61a90-139">별칭</span><span class="sxs-lookup"><span data-stu-id="61a90-139">ALIASES</span></span>

<span data-ttu-id="61a90-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="61a90-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="61a90-141">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="61a90-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="61a90-142">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="61a90-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="61a90-143">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="61a90-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="61a90-144">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="61a90-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="61a90-145">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="61a90-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="61a90-146">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="61a90-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="61a90-147">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="61a90-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="61a90-148">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="61a90-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="61a90-149">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="61a90-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="61a90-150">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61a90-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="61a90-151">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="61a90-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="61a90-152">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="61a90-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="61a90-153">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="61a90-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="61a90-154">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="61a90-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="61a90-155">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="61a90-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="61a90-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61a90-156">RELATED LINKS</span></span>

