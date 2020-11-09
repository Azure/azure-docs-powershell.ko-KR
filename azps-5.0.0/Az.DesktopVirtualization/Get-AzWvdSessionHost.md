---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 94f4c5ad9c401c429c9ef2f2f1c146f83a407196
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304811"
---
# <span data-ttu-id="e30ca-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="e30ca-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="e30ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e30ca-102">SYNOPSIS</span></span>
<span data-ttu-id="e30ca-103">세션 호스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-103">Get a session host.</span></span>

## <span data-ttu-id="e30ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e30ca-104">SYNTAX</span></span>

### <span data-ttu-id="e30ca-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e30ca-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e30ca-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="e30ca-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e30ca-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e30ca-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e30ca-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e30ca-108">DESCRIPTION</span></span>
<span data-ttu-id="e30ca-109">세션 호스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-109">Get a session host.</span></span>

## <span data-ttu-id="e30ca-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e30ca-110">EXAMPLES</span></span>

### <span data-ttu-id="e30ca-111">예제 1: 이름으로 Windows 가상 데스크톱 SessionHost 가져오기</span><span class="sxs-lookup"><span data-stu-id="e30ca-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="e30ca-112">이 명령은 호스트 풀에서 Windows 가상 데스크톱 SessionHost를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="e30ca-113">예제 2: Windows 가상 데스크톱 SessionHosts 목록</span><span class="sxs-lookup"><span data-stu-id="e30ca-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="e30ca-114">이 명령은 호스트 풀에 Windows 가상 데스크톱 SessionHosts를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="e30ca-115">변수</span><span class="sxs-lookup"><span data-stu-id="e30ca-115">PARAMETERS</span></span>

### <span data-ttu-id="e30ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e30ca-116">-DefaultProfile</span></span>
<span data-ttu-id="e30ca-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e30ca-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="e30ca-118">-HostPoolName</span></span>
<span data-ttu-id="e30ca-119">지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-119">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="e30ca-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e30ca-120">-InputObject</span></span>
<span data-ttu-id="e30ca-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e30ca-122">-이름</span><span class="sxs-lookup"><span data-stu-id="e30ca-122">-Name</span></span>
<span data-ttu-id="e30ca-123">지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-123">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="e30ca-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e30ca-124">-ResourceGroupName</span></span>
<span data-ttu-id="e30ca-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-125">The name of the resource group.</span></span>
<span data-ttu-id="e30ca-126">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e30ca-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e30ca-127">-SubscriptionId</span></span>
<span data-ttu-id="e30ca-128">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e30ca-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e30ca-129">CommonParameters</span></span>
<span data-ttu-id="e30ca-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e30ca-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e30ca-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e30ca-132">입력</span><span class="sxs-lookup"><span data-stu-id="e30ca-132">INPUTS</span></span>

### <span data-ttu-id="e30ca-133">IDesktopVirtualizationIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="e30ca-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="e30ca-134">출력</span><span class="sxs-lookup"><span data-stu-id="e30ca-134">OUTPUTS</span></span>

### <span data-ttu-id="e30ca-135">Api20191210Preview. ISessionHost (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e30ca-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="e30ca-136">상속자</span><span class="sxs-lookup"><span data-stu-id="e30ca-136">NOTES</span></span>

<span data-ttu-id="e30ca-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="e30ca-137">ALIASES</span></span>

<span data-ttu-id="e30ca-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e30ca-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e30ca-139">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e30ca-140">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="e30ca-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e30ca-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e30ca-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e30ca-142">`[ApplicationGroupName <String>]`: 응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="e30ca-143">`[ApplicationName <String>]`: 지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="e30ca-144">`[DesktopName <String>]`: 지정 된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="e30ca-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="e30ca-145">`[HostPoolName <String>]`: 지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="e30ca-146">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="e30ca-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e30ca-147">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e30ca-148">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="e30ca-149">`[SessionHostName <String>]`: 지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="e30ca-150">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e30ca-151">`[UserSessionId <String>]`: 지정 된 세션 호스트 내에 있는 사용자 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e30ca-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="e30ca-152">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="e30ca-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="e30ca-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e30ca-153">RELATED LINKS</span></span>

