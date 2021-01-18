---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: 016719f32af1af9acdc4543d565f9acc086b05fa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494590"
---
# <span data-ttu-id="75f15-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="75f15-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="75f15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75f15-102">SYNOPSIS</span></span>
<span data-ttu-id="75f15-103">userSession 연결을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="75f15-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="75f15-104">구문</span><span class="sxs-lookup"><span data-stu-id="75f15-104">SYNTAX</span></span>

### <span data-ttu-id="75f15-105">연결 끊기(기본값)</span><span class="sxs-lookup"><span data-stu-id="75f15-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="75f15-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="75f15-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="75f15-107">설명</span><span class="sxs-lookup"><span data-stu-id="75f15-107">DESCRIPTION</span></span>
<span data-ttu-id="75f15-108">userSession 연결을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="75f15-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="75f15-109">예제</span><span class="sxs-lookup"><span data-stu-id="75f15-109">EXAMPLES</span></span>

### <span data-ttu-id="75f15-110">예제 1: 이름에 따라 Windows Virtual Desktop UserSession 연결 끊기</span><span class="sxs-lookup"><span data-stu-id="75f15-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="75f15-111">이 명령은 세션 호스트에서 Windows Virtual Desktop UserSession의 연결을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="75f15-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="75f15-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75f15-112">PARAMETERS</span></span>

### <span data-ttu-id="75f15-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f15-113">-DefaultProfile</span></span>
<span data-ttu-id="75f15-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75f15-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75f15-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="75f15-115">-HostPoolName</span></span>
<span data-ttu-id="75f15-116">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="75f15-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f15-117">-Id</span><span class="sxs-lookup"><span data-stu-id="75f15-117">-Id</span></span>
<span data-ttu-id="75f15-118">지정된 세션 호스트 내의 사용자 세션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75f15-118">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f15-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75f15-119">-InputObject</span></span>
<span data-ttu-id="75f15-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="75f15-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DisconnectViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75f15-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75f15-121">-PassThru</span></span>
<span data-ttu-id="75f15-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="75f15-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f15-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75f15-123">-ResourceGroupName</span></span>
<span data-ttu-id="75f15-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75f15-124">The name of the resource group.</span></span>
<span data-ttu-id="75f15-125">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="75f15-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f15-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="75f15-126">-SessionHostName</span></span>
<span data-ttu-id="75f15-127">지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="75f15-127">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f15-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75f15-128">-SubscriptionId</span></span>
<span data-ttu-id="75f15-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="75f15-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f15-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75f15-130">-Confirm</span></span>
<span data-ttu-id="75f15-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="75f15-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f15-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75f15-132">-WhatIf</span></span>
<span data-ttu-id="75f15-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="75f15-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75f15-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="75f15-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f15-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f15-135">CommonParameters</span></span>
<span data-ttu-id="75f15-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="75f15-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f15-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75f15-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f15-138">입력</span><span class="sxs-lookup"><span data-stu-id="75f15-138">INPUTS</span></span>

### <span data-ttu-id="75f15-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="75f15-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="75f15-140">출력</span><span class="sxs-lookup"><span data-stu-id="75f15-140">OUTPUTS</span></span>

### <span data-ttu-id="75f15-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="75f15-141">System.Boolean</span></span>

## <span data-ttu-id="75f15-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="75f15-142">NOTES</span></span>

<span data-ttu-id="75f15-143">별칭</span><span class="sxs-lookup"><span data-stu-id="75f15-143">ALIASES</span></span>

<span data-ttu-id="75f15-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="75f15-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="75f15-145">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="75f15-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="75f15-146">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="75f15-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="75f15-147">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="75f15-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="75f15-148">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="75f15-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="75f15-149">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="75f15-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="75f15-150">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="75f15-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="75f15-151">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="75f15-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="75f15-152">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="75f15-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="75f15-153">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="75f15-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="75f15-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75f15-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="75f15-155">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="75f15-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="75f15-156">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="75f15-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="75f15-157">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="75f15-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="75f15-158">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="75f15-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="75f15-159">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="75f15-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="75f15-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75f15-160">RELATED LINKS</span></span>

