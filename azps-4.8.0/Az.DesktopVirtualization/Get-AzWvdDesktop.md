---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdDesktop.md
ms.openlocfilehash: 72075a00cab24d9e7ac82814b2f1e644d90d74c9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056389"
---
# <span data-ttu-id="7fb92-101">Get-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="7fb92-101">Get-AzWvdDesktop</span></span>

## <span data-ttu-id="7fb92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fb92-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb92-103">데스크톱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-103">Get a desktop.</span></span>

## <span data-ttu-id="7fb92-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7fb92-104">SYNTAX</span></span>

### <span data-ttu-id="7fb92-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="7fb92-105">List (Default)</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7fb92-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="7fb92-106">Get</span></span>
```
Get-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7fb92-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7fb92-107">GetViaIdentity</span></span>
```
Get-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fb92-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7fb92-108">DESCRIPTION</span></span>
<span data-ttu-id="7fb92-109">데스크톱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-109">Get a desktop.</span></span>

## <span data-ttu-id="7fb92-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7fb92-110">EXAMPLES</span></span>

### <span data-ttu-id="7fb92-111">예제 1: 이름별로 Windows 가상 데스크톱 데스크톱 가져오기</span><span class="sxs-lookup"><span data-stu-id="7fb92-111">Example 1: Get a Windows Virtual Desktop Desktop by name</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name DesktopName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="7fb92-112">이 명령은 applicaton 그룹의 Windows 가상 데스크톱 데스크톱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-112">This command gets a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

### <span data-ttu-id="7fb92-113">예제 2: Windows 가상 데스크톱 데스크톱 나열</span><span class="sxs-lookup"><span data-stu-id="7fb92-113">Example 2: List Windows Virtual Desktop Desktops</span></span>
```powershell
PS C:\> Get-AzWvdDesktop -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="7fb92-114">이 명령은 applicaton 그룹의 가상 데스크톱 데스크톱을 listsWindows 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-114">This command listsWindows Virtual Desktop Desktops in an applicaton Group.</span></span>

## <span data-ttu-id="7fb92-115">변수</span><span class="sxs-lookup"><span data-stu-id="7fb92-115">PARAMETERS</span></span>

### <span data-ttu-id="7fb92-116">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="7fb92-116">-ApplicationGroupName</span></span>
<span data-ttu-id="7fb92-117">응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-117">The name of the application group</span></span>

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

### <span data-ttu-id="7fb92-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb92-118">-DefaultProfile</span></span>
<span data-ttu-id="7fb92-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fb92-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fb92-120">-InputObject</span></span>
<span data-ttu-id="7fb92-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7fb92-122">-이름</span><span class="sxs-lookup"><span data-stu-id="7fb92-122">-Name</span></span>
<span data-ttu-id="7fb92-123">지정 된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="7fb92-123">The name of the desktop within the specified desktop group</span></span>

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

### <span data-ttu-id="7fb92-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fb92-124">-ResourceGroupName</span></span>
<span data-ttu-id="7fb92-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-125">The name of the resource group.</span></span>
<span data-ttu-id="7fb92-126">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7fb92-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7fb92-127">-SubscriptionId</span></span>
<span data-ttu-id="7fb92-128">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7fb92-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb92-129">CommonParameters</span></span>
<span data-ttu-id="7fb92-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb92-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7fb92-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb92-132">입력</span><span class="sxs-lookup"><span data-stu-id="7fb92-132">INPUTS</span></span>

### <span data-ttu-id="7fb92-133">IDesktopVirtualizationIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="7fb92-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="7fb92-134">출력</span><span class="sxs-lookup"><span data-stu-id="7fb92-134">OUTPUTS</span></span>

### <span data-ttu-id="7fb92-135">Microsoft Api20191210Preview. i i m. IDesktop</span><span class="sxs-lookup"><span data-stu-id="7fb92-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

### <span data-ttu-id="7fb92-136">Api20191210Preview. IDesktopList에 대 한 Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7fb92-136">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktopList</span></span>

## <span data-ttu-id="7fb92-137">상속자</span><span class="sxs-lookup"><span data-stu-id="7fb92-137">NOTES</span></span>

<span data-ttu-id="7fb92-138">별칭과</span><span class="sxs-lookup"><span data-stu-id="7fb92-138">ALIASES</span></span>

<span data-ttu-id="7fb92-139">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="7fb92-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7fb92-140">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7fb92-141">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="7fb92-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7fb92-142">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7fb92-142">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7fb92-143">`[ApplicationGroupName <String>]`: 응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-143">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="7fb92-144">`[ApplicationName <String>]`: 지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-144">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="7fb92-145">`[DesktopName <String>]`: 지정 된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="7fb92-145">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="7fb92-146">`[HostPoolName <String>]`: 지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-146">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="7fb92-147">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="7fb92-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7fb92-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7fb92-149">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="7fb92-150">`[SessionHostName <String>]`: 지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="7fb92-151">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7fb92-152">`[UserSessionId <String>]`: 지정 된 세션 호스트 내에 있는 사용자 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb92-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="7fb92-153">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="7fb92-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="7fb92-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7fb92-154">RELATED LINKS</span></span>

