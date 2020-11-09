---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplication.md
ms.openlocfilehash: e75a9db71a4b20ed87d4e9564597af758af16304
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304856"
---
# <span data-ttu-id="bdf36-101">Get-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="bdf36-101">Get-AzWvdApplication</span></span>

## <span data-ttu-id="bdf36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdf36-102">SYNOPSIS</span></span>
<span data-ttu-id="bdf36-103">응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-103">Get an application.</span></span>

## <span data-ttu-id="bdf36-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bdf36-104">SYNTAX</span></span>

### <span data-ttu-id="bdf36-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="bdf36-105">List (Default)</span></span>
```
Get-AzWvdApplication -GroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bdf36-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="bdf36-106">Get</span></span>
```
Get-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bdf36-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bdf36-107">GetViaIdentity</span></span>
```
Get-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bdf36-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bdf36-108">DESCRIPTION</span></span>
<span data-ttu-id="bdf36-109">응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-109">Get an application.</span></span>

## <span data-ttu-id="bdf36-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bdf36-110">EXAMPLES</span></span>

### <span data-ttu-id="bdf36-111">예제 1: 이름으로 Windows 가상 데스크톱 응용 프로그램 가져오기</span><span class="sxs-lookup"><span data-stu-id="bdf36-111">Example 1: Get a Windows Virtual Desktop Application by name</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName -Name ApplicationName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="bdf36-112">이 명령은 applicaton 그룹의 Windows 가상 데스크톱 응용 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-112">This command gets a Windows Virtual Desktop Application in an applicaton Group.</span></span>

### <span data-ttu-id="bdf36-113">예제 2: Windows 가상 데스크톱 응용 프로그램 나열</span><span class="sxs-lookup"><span data-stu-id="bdf36-113">Example 2: List Windows Virtual Desktop Applications</span></span>
```powershell
PS C:\> Get-AzWvdApplication -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName1 Microsoft.DesktopVirtualization/applicationgroups/applications
ApplicationGroupName/ApplicationName2 Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="bdf36-114">이 명령은 applicaton 그룹의 Windows 가상 데스크톱 응용 프로그램을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-114">This command Lists Windows Virtual Desktop Applications in an applicaton Group.</span></span>

## <span data-ttu-id="bdf36-115">변수</span><span class="sxs-lookup"><span data-stu-id="bdf36-115">PARAMETERS</span></span>

### <span data-ttu-id="bdf36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdf36-116">-DefaultProfile</span></span>
<span data-ttu-id="bdf36-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdf36-118">-GroupName</span><span class="sxs-lookup"><span data-stu-id="bdf36-118">-GroupName</span></span>
<span data-ttu-id="bdf36-119">응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-119">The name of the application group</span></span>

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

### <span data-ttu-id="bdf36-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdf36-120">-InputObject</span></span>
<span data-ttu-id="bdf36-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bdf36-122">-이름</span><span class="sxs-lookup"><span data-stu-id="bdf36-122">-Name</span></span>
<span data-ttu-id="bdf36-123">지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-123">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="bdf36-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdf36-124">-ResourceGroupName</span></span>
<span data-ttu-id="bdf36-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-125">The name of the resource group.</span></span>
<span data-ttu-id="bdf36-126">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bdf36-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bdf36-127">-SubscriptionId</span></span>
<span data-ttu-id="bdf36-128">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bdf36-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdf36-129">CommonParameters</span></span>
<span data-ttu-id="bdf36-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdf36-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bdf36-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdf36-132">입력</span><span class="sxs-lookup"><span data-stu-id="bdf36-132">INPUTS</span></span>

### <span data-ttu-id="bdf36-133">IDesktopVirtualizationIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="bdf36-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="bdf36-134">출력</span><span class="sxs-lookup"><span data-stu-id="bdf36-134">OUTPUTS</span></span>

### <span data-ttu-id="bdf36-135">Api20191210Preview 응용 프로그램에 대 한 Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="bdf36-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="bdf36-136">상속자</span><span class="sxs-lookup"><span data-stu-id="bdf36-136">NOTES</span></span>

<span data-ttu-id="bdf36-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="bdf36-137">ALIASES</span></span>

<span data-ttu-id="bdf36-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="bdf36-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bdf36-139">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bdf36-140">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="bdf36-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bdf36-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="bdf36-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bdf36-142">`[ApplicationGroupName <String>]`: 응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="bdf36-143">`[ApplicationName <String>]`: 지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="bdf36-144">`[DesktopName <String>]`: 지정 된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="bdf36-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="bdf36-145">`[HostPoolName <String>]`: 지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="bdf36-146">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="bdf36-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bdf36-147">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bdf36-148">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="bdf36-149">`[SessionHostName <String>]`: 지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="bdf36-150">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bdf36-151">`[UserSessionId <String>]`: 지정 된 세션 호스트 내에 있는 사용자 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bdf36-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="bdf36-152">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="bdf36-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="bdf36-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bdf36-153">RELATED LINKS</span></span>

