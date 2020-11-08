---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: e04d13b96f36b96b2ae1c22f6f6e5b3c50b338f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212794"
---
# <span data-ttu-id="6db69-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="6db69-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="6db69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6db69-102">SYNOPSIS</span></span>
<span data-ttu-id="6db69-103">호스트 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-103">Get a host pool.</span></span>

## <span data-ttu-id="6db69-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6db69-104">SYNTAX</span></span>

### <span data-ttu-id="6db69-105">List1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6db69-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6db69-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="6db69-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6db69-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6db69-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6db69-108">목록</span><span class="sxs-lookup"><span data-stu-id="6db69-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6db69-109">설명은</span><span class="sxs-lookup"><span data-stu-id="6db69-109">DESCRIPTION</span></span>
<span data-ttu-id="6db69-110">호스트 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-110">Get a host pool.</span></span>

## <span data-ttu-id="6db69-111">예제의</span><span class="sxs-lookup"><span data-stu-id="6db69-111">EXAMPLES</span></span>

### <span data-ttu-id="6db69-112">예제 1: 이름으로 Windows 가상 데스크톱 호스트 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="6db69-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="6db69-113">이 명령은 리소스 그룹의 Windows 가상 데스크톱 호스트 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="6db69-114">예제 2: List Windows 가상 데스크톱 호스트 풀</span><span class="sxs-lookup"><span data-stu-id="6db69-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="6db69-115">이 명령은 리소스 그룹에 Windows 가상 데스크톱 호스트 풀을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="6db69-116">변수</span><span class="sxs-lookup"><span data-stu-id="6db69-116">PARAMETERS</span></span>

### <span data-ttu-id="6db69-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db69-117">-DefaultProfile</span></span>
<span data-ttu-id="6db69-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6db69-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6db69-119">-InputObject</span></span>
<span data-ttu-id="6db69-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6db69-121">-이름</span><span class="sxs-lookup"><span data-stu-id="6db69-121">-Name</span></span>
<span data-ttu-id="6db69-122">지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-122">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6db69-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6db69-123">-ResourceGroupName</span></span>
<span data-ttu-id="6db69-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-124">The name of the resource group.</span></span>
<span data-ttu-id="6db69-125">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6db69-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6db69-126">-SubscriptionId</span></span>
<span data-ttu-id="6db69-127">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6db69-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db69-128">CommonParameters</span></span>
<span data-ttu-id="6db69-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db69-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6db69-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db69-131">입력</span><span class="sxs-lookup"><span data-stu-id="6db69-131">INPUTS</span></span>

### <span data-ttu-id="6db69-132">IDesktopVirtualizationIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="6db69-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="6db69-133">출력</span><span class="sxs-lookup"><span data-stu-id="6db69-133">OUTPUTS</span></span>

### <span data-ttu-id="6db69-134">Api20191210Preview. IHostPool에 대 한 Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6db69-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="6db69-135">상속자</span><span class="sxs-lookup"><span data-stu-id="6db69-135">NOTES</span></span>

<span data-ttu-id="6db69-136">별칭과</span><span class="sxs-lookup"><span data-stu-id="6db69-136">ALIASES</span></span>

<span data-ttu-id="6db69-137">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="6db69-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6db69-138">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6db69-139">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="6db69-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6db69-140">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6db69-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6db69-141">`[ApplicationGroupName <String>]`: 응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="6db69-142">`[ApplicationName <String>]`: 지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="6db69-143">`[DesktopName <String>]`: 지정 된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="6db69-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="6db69-144">`[HostPoolName <String>]`: 지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="6db69-145">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="6db69-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6db69-146">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6db69-147">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-147">The name is case insensitive.</span></span>
  - <span data-ttu-id="6db69-148">`[SessionHostName <String>]`: 지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-148">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="6db69-149">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6db69-150">`[UserSessionId <String>]`: 지정 된 세션 호스트 내에 있는 사용자 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6db69-150">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="6db69-151">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="6db69-151">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="6db69-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6db69-152">RELATED LINKS</span></span>

