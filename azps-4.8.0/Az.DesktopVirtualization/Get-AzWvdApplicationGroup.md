---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 1ad8b51a39cdde66728200af28c77f7b094f19c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048321"
---
# <span data-ttu-id="8ff6d-101">Get-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="8ff6d-101">Get-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="8ff6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ff6d-102">SYNOPSIS</span></span>
<span data-ttu-id="8ff6d-103">응용 프로그램 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-103">Get an application group.</span></span>

## <span data-ttu-id="8ff6d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ff6d-104">SYNTAX</span></span>

### <span data-ttu-id="8ff6d-105">List1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8ff6d-105">List1 (Default)</span></span>
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ff6d-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="8ff6d-106">Get</span></span>
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8ff6d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8ff6d-107">GetViaIdentity</span></span>
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ff6d-108">목록</span><span class="sxs-lookup"><span data-stu-id="8ff6d-108">List</span></span>
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8ff6d-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8ff6d-109">DESCRIPTION</span></span>
<span data-ttu-id="8ff6d-110">응용 프로그램 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-110">Get an application group.</span></span>

## <span data-ttu-id="8ff6d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8ff6d-111">EXAMPLES</span></span>

### <span data-ttu-id="8ff6d-112">예제 1: 이름별로 Windows 가상 데스크톱 ApplicationGroup 가져오기</span><span class="sxs-lookup"><span data-stu-id="8ff6d-112">Example 1: Get a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="8ff6d-113">이 명령은 리소스 그룹의 Windows 가상 데스크톱 ApplicationGroup을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-113">This command gets a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="8ff6d-114">예제 2: Windows 가상 데스크톱 ApplicationGroups 그룹 나열</span><span class="sxs-lookup"><span data-stu-id="8ff6d-114">Example 2: List Windows Virtual Desktop ApplicationGroups</span></span>
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="8ff6d-115">이 명령은 리소스 그룹에 Windows 가상 데스크톱 ApplicationGroups를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-115">This command lists a Windows Virtual Desktop ApplicationGroups in a Resource Group.</span></span>

## <span data-ttu-id="8ff6d-116">변수</span><span class="sxs-lookup"><span data-stu-id="8ff6d-116">PARAMETERS</span></span>

### <span data-ttu-id="8ff6d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ff6d-117">-DefaultProfile</span></span>
<span data-ttu-id="8ff6d-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ff6d-119">-필터</span><span class="sxs-lookup"><span data-stu-id="8ff6d-119">-Filter</span></span>
<span data-ttu-id="8ff6d-120">OData 필터 식입니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-120">OData filter expression.</span></span>
<span data-ttu-id="8ff6d-121">필터링에 대 한 유효한 속성은 applicationGroupType입니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-121">Valid properties for filtering are applicationGroupType.</span></span>

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

### <span data-ttu-id="8ff6d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ff6d-122">-InputObject</span></span>
<span data-ttu-id="8ff6d-123">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8ff6d-124">-이름</span><span class="sxs-lookup"><span data-stu-id="8ff6d-124">-Name</span></span>
<span data-ttu-id="8ff6d-125">응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-125">The name of the application group</span></span>

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

### <span data-ttu-id="8ff6d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ff6d-126">-ResourceGroupName</span></span>
<span data-ttu-id="8ff6d-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-127">The name of the resource group.</span></span>
<span data-ttu-id="8ff6d-128">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8ff6d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ff6d-129">-SubscriptionId</span></span>
<span data-ttu-id="8ff6d-130">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8ff6d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ff6d-131">CommonParameters</span></span>
<span data-ttu-id="8ff6d-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ff6d-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ff6d-134">입력</span><span class="sxs-lookup"><span data-stu-id="8ff6d-134">INPUTS</span></span>

### <span data-ttu-id="8ff6d-135">IDesktopVirtualizationIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="8ff6d-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8ff6d-136">출력</span><span class="sxs-lookup"><span data-stu-id="8ff6d-136">OUTPUTS</span></span>

### <span data-ttu-id="8ff6d-137">Api20191210Preview. i i PowerShell. i i m. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="8ff6d-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="8ff6d-138">상속자</span><span class="sxs-lookup"><span data-stu-id="8ff6d-138">NOTES</span></span>

<span data-ttu-id="8ff6d-139">별칭과</span><span class="sxs-lookup"><span data-stu-id="8ff6d-139">ALIASES</span></span>

<span data-ttu-id="8ff6d-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8ff6d-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8ff6d-141">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8ff6d-142">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8ff6d-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8ff6d-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8ff6d-144">`[ApplicationGroupName <String>]`: 응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8ff6d-145">`[ApplicationName <String>]`: 지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8ff6d-146">`[DesktopName <String>]`: 지정 된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="8ff6d-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8ff6d-147">`[HostPoolName <String>]`: 지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8ff6d-148">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="8ff6d-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8ff6d-149">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8ff6d-150">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="8ff6d-151">`[SessionHostName <String>]`: 지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8ff6d-152">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8ff6d-153">`[UserSessionId <String>]`: 지정 된 세션 호스트 내에 있는 사용자 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ff6d-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8ff6d-154">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="8ff6d-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="8ff6d-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ff6d-155">RELATED LINKS</span></span>

