---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: 61e1eb1f5ae3846ce2f0cf7ad82d17d613d27e0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966203"
---
# <span data-ttu-id="6bf13-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="6bf13-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="6bf13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bf13-102">SYNOPSIS</span></span>
<span data-ttu-id="6bf13-103">사용자 연결을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="6bf13-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="6bf13-104">구문</span><span class="sxs-lookup"><span data-stu-id="6bf13-104">SYNTAX</span></span>

### <span data-ttu-id="6bf13-105">연결 끊기(기본값)</span><span class="sxs-lookup"><span data-stu-id="6bf13-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6bf13-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6bf13-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6bf13-107">설명</span><span class="sxs-lookup"><span data-stu-id="6bf13-107">DESCRIPTION</span></span>
<span data-ttu-id="6bf13-108">사용자 연결을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="6bf13-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="6bf13-109">예제</span><span class="sxs-lookup"><span data-stu-id="6bf13-109">EXAMPLES</span></span>

### <span data-ttu-id="6bf13-110">예제 1: 이름에 따라 Windows Virtual Desktop 사용자 연결 끊기</span><span class="sxs-lookup"><span data-stu-id="6bf13-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="6bf13-111">이 명령은 세션 호스트에서 Windows Virtual Desktop UserSession을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="6bf13-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="6bf13-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6bf13-112">PARAMETERS</span></span>

### <span data-ttu-id="6bf13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bf13-113">-DefaultProfile</span></span>
<span data-ttu-id="6bf13-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6bf13-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bf13-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="6bf13-115">-HostPoolName</span></span>
<span data-ttu-id="6bf13-116">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="6bf13-116">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="6bf13-117">-Id</span><span class="sxs-lookup"><span data-stu-id="6bf13-117">-Id</span></span>
<span data-ttu-id="6bf13-118">지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="6bf13-118">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="6bf13-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bf13-119">-InputObject</span></span>
<span data-ttu-id="6bf13-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="6bf13-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6bf13-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bf13-121">-PassThru</span></span>
<span data-ttu-id="6bf13-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="6bf13-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6bf13-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bf13-123">-ResourceGroupName</span></span>
<span data-ttu-id="6bf13-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6bf13-124">The name of the resource group.</span></span>
<span data-ttu-id="6bf13-125">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="6bf13-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6bf13-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="6bf13-126">-SessionHostName</span></span>
<span data-ttu-id="6bf13-127">지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="6bf13-127">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="6bf13-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6bf13-128">-SubscriptionId</span></span>
<span data-ttu-id="6bf13-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6bf13-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6bf13-130">-확인</span><span class="sxs-lookup"><span data-stu-id="6bf13-130">-Confirm</span></span>
<span data-ttu-id="6bf13-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6bf13-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bf13-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bf13-132">-WhatIf</span></span>
<span data-ttu-id="6bf13-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6bf13-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bf13-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6bf13-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bf13-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bf13-135">CommonParameters</span></span>
<span data-ttu-id="6bf13-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6bf13-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bf13-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bf13-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bf13-138">입력</span><span class="sxs-lookup"><span data-stu-id="6bf13-138">INPUTS</span></span>

### <span data-ttu-id="6bf13-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="6bf13-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="6bf13-140">출력</span><span class="sxs-lookup"><span data-stu-id="6bf13-140">OUTPUTS</span></span>

### <span data-ttu-id="6bf13-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6bf13-141">System.Boolean</span></span>

## <span data-ttu-id="6bf13-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6bf13-142">NOTES</span></span>

<span data-ttu-id="6bf13-143">별칭</span><span class="sxs-lookup"><span data-stu-id="6bf13-143">ALIASES</span></span>

<span data-ttu-id="6bf13-144">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="6bf13-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6bf13-145">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6bf13-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6bf13-146">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6bf13-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6bf13-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6bf13-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6bf13-148">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="6bf13-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="6bf13-149">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="6bf13-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="6bf13-150">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="6bf13-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="6bf13-151">`[HostPoolName <String>]`: 지정된 리소스 그룹 내의 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="6bf13-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="6bf13-152">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="6bf13-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6bf13-153">`[MsixPackageFullName <String>]`: 지정된 호스트풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="6bf13-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="6bf13-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6bf13-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6bf13-155">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="6bf13-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="6bf13-156">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="6bf13-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="6bf13-157">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6bf13-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6bf13-158">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="6bf13-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="6bf13-159">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="6bf13-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="6bf13-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6bf13-160">RELATED LINKS</span></span>

