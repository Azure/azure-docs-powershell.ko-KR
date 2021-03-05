---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 8770b9e3b07b677f0f4bd4f59a6c38928421523e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001616"
---
# <span data-ttu-id="dca8c-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="dca8c-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="dca8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dca8c-102">SYNOPSIS</span></span>
<span data-ttu-id="dca8c-103">애플리케이션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-103">Update an application.</span></span>

## <span data-ttu-id="dca8c-104">구문</span><span class="sxs-lookup"><span data-stu-id="dca8c-104">SYNTAX</span></span>

### <span data-ttu-id="dca8c-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="dca8c-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dca8c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dca8c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity>
 [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dca8c-107">설명</span><span class="sxs-lookup"><span data-stu-id="dca8c-107">DESCRIPTION</span></span>
<span data-ttu-id="dca8c-108">애플리케이션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-108">Update an application.</span></span>

## <span data-ttu-id="dca8c-109">예제</span><span class="sxs-lookup"><span data-stu-id="dca8c-109">EXAMPLES</span></span>

### <span data-ttu-id="dca8c-110">예제 1: Windows Virtual Desktop 애플리케이션 업데이트</span><span class="sxs-lookup"><span data-stu-id="dca8c-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> Update-AzWvdApplication -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name ApplicationName `
                             -FilePath 'C:\windows\system32\mspaint.exe' `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `
                             -IconIndex 0 `
                             -IconPath 'C:\windows\system32\mspaint.exe' `
                             -CommandLineSetting 'Allow' `
                             -ShowInPortal:$true

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="dca8c-111">이 명령은 해당 애플리케이션 그룹의 Windows Virtual Desktop 애플리케이션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="dca8c-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="dca8c-112">PARAMETERS</span></span>

### <span data-ttu-id="dca8c-113">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="dca8c-113">-ApplicationType</span></span>
<span data-ttu-id="dca8c-114">애플리케이션의 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-114">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca8c-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="dca8c-115">-CommandLineArgument</span></span>
<span data-ttu-id="dca8c-116">애플리케이션에 대한 명령줄 인수입니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="dca8c-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="dca8c-117">-CommandLineSetting</span></span>
<span data-ttu-id="dca8c-118">이 게시된 애플리케이션을 클라이언트에서 제공하는 명령줄 인수, 게시 시 지정된 명령줄 인수 또는 명령줄 인수가 없는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca8c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca8c-119">-DefaultProfile</span></span>
<span data-ttu-id="dca8c-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dca8c-121">-Description</span><span class="sxs-lookup"><span data-stu-id="dca8c-121">-Description</span></span>
<span data-ttu-id="dca8c-122">애플리케이션에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-122">Description of Application.</span></span>

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

### <span data-ttu-id="dca8c-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="dca8c-123">-FilePath</span></span>
<span data-ttu-id="dca8c-124">애플리케이션에 대한 실행 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="dca8c-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="dca8c-125">-FriendlyName</span></span>
<span data-ttu-id="dca8c-126">애플리케이션의 친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="dca8c-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="dca8c-127">-GroupName</span></span>
<span data-ttu-id="dca8c-128">애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="dca8c-128">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca8c-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="dca8c-129">-IconIndex</span></span>
<span data-ttu-id="dca8c-130">아이콘의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-130">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca8c-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="dca8c-131">-IconPath</span></span>
<span data-ttu-id="dca8c-132">아이콘에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-132">Path to icon.</span></span>

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

### <span data-ttu-id="dca8c-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dca8c-133">-InputObject</span></span>
<span data-ttu-id="dca8c-134">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="dca8c-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dca8c-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="dca8c-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="dca8c-136">MSIX 애플리케이션에 대한 패키지 애플리케이션 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="dca8c-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="dca8c-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="dca8c-138">MSIX 애플리케이션에 대한 패키지 패밀리 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="dca8c-139">-Name</span><span class="sxs-lookup"><span data-stu-id="dca8c-139">-Name</span></span>
<span data-ttu-id="dca8c-140">지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="dca8c-140">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca8c-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dca8c-141">-ResourceGroupName</span></span>
<span data-ttu-id="dca8c-142">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-142">The name of the resource group.</span></span>
<span data-ttu-id="dca8c-143">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dca8c-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="dca8c-144">-ShowInPortal</span></span>
<span data-ttu-id="dca8c-145">RD Web Access 서버에 RemoteApp 프로그램을 표시할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="dca8c-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dca8c-146">-SubscriptionId</span></span>
<span data-ttu-id="dca8c-147">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dca8c-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="dca8c-148">-Tag</span></span>
<span data-ttu-id="dca8c-149">업데이트할 태그</span><span class="sxs-lookup"><span data-stu-id="dca8c-149">tags to be updated</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca8c-150">-확인</span><span class="sxs-lookup"><span data-stu-id="dca8c-150">-Confirm</span></span>
<span data-ttu-id="dca8c-151">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dca8c-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dca8c-152">-WhatIf</span></span>
<span data-ttu-id="dca8c-153">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dca8c-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dca8c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca8c-155">CommonParameters</span></span>
<span data-ttu-id="dca8c-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca8c-157">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dca8c-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca8c-158">입력</span><span class="sxs-lookup"><span data-stu-id="dca8c-158">INPUTS</span></span>

### <span data-ttu-id="dca8c-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="dca8c-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="dca8c-160">출력</span><span class="sxs-lookup"><span data-stu-id="dca8c-160">OUTPUTS</span></span>

### <span data-ttu-id="dca8c-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="dca8c-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="dca8c-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dca8c-162">NOTES</span></span>

<span data-ttu-id="dca8c-163">별칭</span><span class="sxs-lookup"><span data-stu-id="dca8c-163">ALIASES</span></span>

<span data-ttu-id="dca8c-164">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="dca8c-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dca8c-165">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dca8c-166">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dca8c-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dca8c-167">INPUTOBJECT <IDesktopVirtualizationIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="dca8c-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dca8c-168">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="dca8c-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="dca8c-169">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="dca8c-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="dca8c-170">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="dca8c-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="dca8c-171">`[HostPoolName <String>]`: 지정된 리소스 그룹 내의 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="dca8c-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="dca8c-172">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="dca8c-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dca8c-173">`[MsixPackageFullName <String>]`: 지정된 호스트풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="dca8c-173">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="dca8c-174">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-174">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dca8c-175">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-175">The name is case insensitive.</span></span>
  - <span data-ttu-id="dca8c-176">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="dca8c-176">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="dca8c-177">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dca8c-177">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dca8c-178">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="dca8c-178">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="dca8c-179">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="dca8c-179">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="dca8c-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dca8c-180">RELATED LINKS</span></span>

