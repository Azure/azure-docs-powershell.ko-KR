---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: 815f7280564d01077de99c4ec9b4003d4996d019
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330933"
---
# <span data-ttu-id="bcbf1-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="bcbf1-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="bcbf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcbf1-102">SYNOPSIS</span></span>
<span data-ttu-id="bcbf1-103">호스트 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bcbf1-103">Get a host pool.</span></span>

## <span data-ttu-id="bcbf1-104">구문</span><span class="sxs-lookup"><span data-stu-id="bcbf1-104">SYNTAX</span></span>

### <span data-ttu-id="bcbf1-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="bcbf1-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bcbf1-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="bcbf1-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bcbf1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bcbf1-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="bcbf1-108">목록</span><span class="sxs-lookup"><span data-stu-id="bcbf1-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bcbf1-109">설명</span><span class="sxs-lookup"><span data-stu-id="bcbf1-109">DESCRIPTION</span></span>
<span data-ttu-id="bcbf1-110">호스트 풀을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bcbf1-110">Get a host pool.</span></span>

## <span data-ttu-id="bcbf1-111">예제</span><span class="sxs-lookup"><span data-stu-id="bcbf1-111">EXAMPLES</span></span>

### <span data-ttu-id="bcbf1-112">예제 1: 이름으로 Windows Virtual Desktop HostPool 다운로드</span><span class="sxs-lookup"><span data-stu-id="bcbf1-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="bcbf1-113">이 명령은 리소스 그룹에서 Windows Virtual Desktop HostPool을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bcbf1-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="bcbf1-114">예제 2: Windows Virtual Desktop HostPools 나열</span><span class="sxs-lookup"><span data-stu-id="bcbf1-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="bcbf1-115">이 명령은 리소스 그룹에 Windows Virtual Desktop HostPools를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="bcbf1-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="bcbf1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcbf1-116">PARAMETERS</span></span>

### <span data-ttu-id="bcbf1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcbf1-117">-DefaultProfile</span></span>
<span data-ttu-id="bcbf1-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bcbf1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcbf1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcbf1-119">-InputObject</span></span>
<span data-ttu-id="bcbf1-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="bcbf1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bcbf1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bcbf1-121">-Name</span></span>
<span data-ttu-id="bcbf1-122">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="bcbf1-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="bcbf1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcbf1-123">-ResourceGroupName</span></span>
<span data-ttu-id="bcbf1-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bcbf1-124">The name of the resource group.</span></span>
<span data-ttu-id="bcbf1-125">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="bcbf1-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bcbf1-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bcbf1-126">-SubscriptionId</span></span>
<span data-ttu-id="bcbf1-127">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bcbf1-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bcbf1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcbf1-128">CommonParameters</span></span>
<span data-ttu-id="bcbf1-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bcbf1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcbf1-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bcbf1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcbf1-131">입력</span><span class="sxs-lookup"><span data-stu-id="bcbf1-131">INPUTS</span></span>

### <span data-ttu-id="bcbf1-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="bcbf1-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="bcbf1-133">출력</span><span class="sxs-lookup"><span data-stu-id="bcbf1-133">OUTPUTS</span></span>

### <span data-ttu-id="bcbf1-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="bcbf1-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IHostPool</span></span>

## <span data-ttu-id="bcbf1-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bcbf1-135">NOTES</span></span>

<span data-ttu-id="bcbf1-136">별칭</span><span class="sxs-lookup"><span data-stu-id="bcbf1-136">ALIASES</span></span>

<span data-ttu-id="bcbf1-137">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="bcbf1-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bcbf1-138">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bcbf1-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bcbf1-139">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bcbf1-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bcbf1-140">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="bcbf1-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bcbf1-141">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="bcbf1-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="bcbf1-142">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="bcbf1-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="bcbf1-143">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="bcbf1-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="bcbf1-144">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="bcbf1-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="bcbf1-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="bcbf1-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bcbf1-146">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="bcbf1-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="bcbf1-147">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bcbf1-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bcbf1-148">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="bcbf1-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="bcbf1-149">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="bcbf1-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="bcbf1-150">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bcbf1-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bcbf1-151">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="bcbf1-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="bcbf1-152">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="bcbf1-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="bcbf1-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bcbf1-153">RELATED LINKS</span></span>

