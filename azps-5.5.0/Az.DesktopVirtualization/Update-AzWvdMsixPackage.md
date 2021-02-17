---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdMsixPackage.md
ms.openlocfilehash: 8fe887f754c5a5a9f45d38d646a1edd03d1cc006
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186025"
---
# <span data-ttu-id="09a8d-101">Update-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="09a8d-101">Update-AzWvdMsixPackage</span></span>

## <span data-ttu-id="09a8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09a8d-102">SYNOPSIS</span></span>
<span data-ttu-id="09a8d-103">MSIX 패키지를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="09a8d-103">Update an  MSIX Package.</span></span>

## <span data-ttu-id="09a8d-104">구문</span><span class="sxs-lookup"><span data-stu-id="09a8d-104">SYNTAX</span></span>

### <span data-ttu-id="09a8d-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="09a8d-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DisplayName <String>] [-IsActive] [-IsRegularRegistration]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="09a8d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="09a8d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DisplayName <String>] [-IsActive]
 [-IsRegularRegistration] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="09a8d-107">설명</span><span class="sxs-lookup"><span data-stu-id="09a8d-107">DESCRIPTION</span></span>
<span data-ttu-id="09a8d-108">MSIX 패키지를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="09a8d-108">Update an  MSIX Package.</span></span>

## <span data-ttu-id="09a8d-109">예제</span><span class="sxs-lookup"><span data-stu-id="09a8d-109">EXAMPLES</span></span>

### <span data-ttu-id="09a8d-110">예제 1: MSIX 패키지 업데이트</span><span class="sxs-lookup"><span data-stu-id="09a8d-110">Example 1: Update a MSIX Package</span></span> 
```powershell
PS C:\> Update-AzWvdMsixPackage -HostPoolName HostPoolName `
                -ResourceGroupName ResourceGroupName `
                -SubscriptionId SubscriptionId `
                -displayName 'Updated-display-Name' `
                    -IsRegularRegistration:$False `
                -IsActive:$True

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

<span data-ttu-id="09a8d-111">이 명령은 HostPool에서 MSIX 패키지를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="09a8d-111">This command updates a MSIX Package in a HostPool.</span></span>

## <span data-ttu-id="09a8d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09a8d-112">PARAMETERS</span></span>

### <span data-ttu-id="09a8d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09a8d-113">-DefaultProfile</span></span>
<span data-ttu-id="09a8d-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09a8d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09a8d-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="09a8d-115">-DisplayName</span></span>
<span data-ttu-id="09a8d-116">MSIX 패키지의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09a8d-116">Display name for MSIX Package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a8d-117">-FullName</span><span class="sxs-lookup"><span data-stu-id="09a8d-117">-FullName</span></span>
<span data-ttu-id="09a8d-118">지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="09a8d-118">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a8d-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="09a8d-119">-HostPoolName</span></span>
<span data-ttu-id="09a8d-120">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="09a8d-120">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a8d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09a8d-121">-InputObject</span></span>
<span data-ttu-id="09a8d-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="09a8d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09a8d-123">-IsActive</span><span class="sxs-lookup"><span data-stu-id="09a8d-123">-IsActive</span></span>
<span data-ttu-id="09a8d-124">호스트풀에서 활성화될 패키지의 버전을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="09a8d-124">Set a version of the package to be active across hostpool.</span></span>

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

### <span data-ttu-id="09a8d-125">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="09a8d-125">-IsRegularRegistration</span></span>
<span data-ttu-id="09a8d-126">등록 모드를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="09a8d-126">Set Registration mode.</span></span>
<span data-ttu-id="09a8d-127">일반 또는 지연.</span><span class="sxs-lookup"><span data-stu-id="09a8d-127">Regular or Delayed.</span></span>

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

### <span data-ttu-id="09a8d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09a8d-128">-ResourceGroupName</span></span>
<span data-ttu-id="09a8d-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09a8d-129">The name of the resource group.</span></span>
<span data-ttu-id="09a8d-130">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="09a8d-130">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a8d-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09a8d-131">-SubscriptionId</span></span>
<span data-ttu-id="09a8d-132">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="09a8d-132">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a8d-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09a8d-133">-Confirm</span></span>
<span data-ttu-id="09a8d-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="09a8d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09a8d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09a8d-135">-WhatIf</span></span>
<span data-ttu-id="09a8d-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="09a8d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09a8d-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="09a8d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09a8d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09a8d-138">CommonParameters</span></span>
<span data-ttu-id="09a8d-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="09a8d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09a8d-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="09a8d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09a8d-141">입력</span><span class="sxs-lookup"><span data-stu-id="09a8d-141">INPUTS</span></span>

### <span data-ttu-id="09a8d-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="09a8d-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="09a8d-143">출력</span><span class="sxs-lookup"><span data-stu-id="09a8d-143">OUTPUTS</span></span>

### <span data-ttu-id="09a8d-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="09a8d-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="09a8d-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="09a8d-145">NOTES</span></span>

<span data-ttu-id="09a8d-146">별칭</span><span class="sxs-lookup"><span data-stu-id="09a8d-146">ALIASES</span></span>

<span data-ttu-id="09a8d-147">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="09a8d-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="09a8d-148">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="09a8d-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="09a8d-149">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="09a8d-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="09a8d-150">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="09a8d-150">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="09a8d-151">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="09a8d-151">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="09a8d-152">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="09a8d-152">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="09a8d-153">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="09a8d-153">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="09a8d-154">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="09a8d-154">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="09a8d-155">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="09a8d-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="09a8d-156">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="09a8d-156">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="09a8d-157">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09a8d-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="09a8d-158">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="09a8d-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="09a8d-159">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="09a8d-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="09a8d-160">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="09a8d-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="09a8d-161">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="09a8d-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="09a8d-162">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="09a8d-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="09a8d-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09a8d-163">RELATED LINKS</span></span>

