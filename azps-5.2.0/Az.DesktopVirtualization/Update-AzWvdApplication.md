---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 6907967acfd86f151b038e26aa9c33f62db50a5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338409"
---
# <span data-ttu-id="50b9b-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="50b9b-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="50b9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50b9b-102">SYNOPSIS</span></span>
<span data-ttu-id="50b9b-103">애플리케이션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-103">Update an application.</span></span>

## <span data-ttu-id="50b9b-104">구문</span><span class="sxs-lookup"><span data-stu-id="50b9b-104">SYNTAX</span></span>

### <span data-ttu-id="50b9b-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="50b9b-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="50b9b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="50b9b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity>
 [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="50b9b-107">설명</span><span class="sxs-lookup"><span data-stu-id="50b9b-107">DESCRIPTION</span></span>
<span data-ttu-id="50b9b-108">애플리케이션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-108">Update an application.</span></span>

## <span data-ttu-id="50b9b-109">예제</span><span class="sxs-lookup"><span data-stu-id="50b9b-109">EXAMPLES</span></span>

### <span data-ttu-id="50b9b-110">예제 1: Windows Virtual Desktop 애플리케이션 업데이트</span><span class="sxs-lookup"><span data-stu-id="50b9b-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="50b9b-111">이 명령은 응용 프로그램 그룹에서 Windows Virtual Desktop 애플리케이션을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="50b9b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50b9b-112">PARAMETERS</span></span>

### <span data-ttu-id="50b9b-113">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="50b9b-113">-ApplicationType</span></span>
<span data-ttu-id="50b9b-114">애플리케이션의 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-114">Resource Type of Application.</span></span>

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

### <span data-ttu-id="50b9b-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="50b9b-115">-CommandLineArgument</span></span>
<span data-ttu-id="50b9b-116">애플리케이션에 대한 명령줄 인수입니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="50b9b-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="50b9b-117">-CommandLineSetting</span></span>
<span data-ttu-id="50b9b-118">이 게시된 애플리케이션을 클라이언트에서 제공하는 명령줄 인수, 게시 시 지정된 명령줄 인수 또는 명령줄 인수를 모두 사용하여 시작될 수 있는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="50b9b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50b9b-119">-DefaultProfile</span></span>
<span data-ttu-id="50b9b-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50b9b-121">-Description</span><span class="sxs-lookup"><span data-stu-id="50b9b-121">-Description</span></span>
<span data-ttu-id="50b9b-122">애플리케이션에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-122">Description of Application.</span></span>

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

### <span data-ttu-id="50b9b-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="50b9b-123">-FilePath</span></span>
<span data-ttu-id="50b9b-124">애플리케이션에 대한 실행 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="50b9b-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="50b9b-125">-FriendlyName</span></span>
<span data-ttu-id="50b9b-126">애플리케이션의 친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="50b9b-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="50b9b-127">-GroupName</span></span>
<span data-ttu-id="50b9b-128">애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="50b9b-128">The name of the application group</span></span>

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

### <span data-ttu-id="50b9b-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="50b9b-129">-IconIndex</span></span>
<span data-ttu-id="50b9b-130">아이콘의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-130">Index of the icon.</span></span>

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

### <span data-ttu-id="50b9b-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="50b9b-131">-IconPath</span></span>
<span data-ttu-id="50b9b-132">아이콘의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-132">Path to icon.</span></span>

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

### <span data-ttu-id="50b9b-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50b9b-133">-InputObject</span></span>
<span data-ttu-id="50b9b-134">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="50b9b-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="50b9b-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="50b9b-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="50b9b-136">MSIX 애플리케이션에 대한 패키지 애플리케이션 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="50b9b-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="50b9b-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="50b9b-138">MSIX 애플리케이션에 대한 패키지 패밀리 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="50b9b-139">-Name</span><span class="sxs-lookup"><span data-stu-id="50b9b-139">-Name</span></span>
<span data-ttu-id="50b9b-140">지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="50b9b-140">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="50b9b-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50b9b-141">-ResourceGroupName</span></span>
<span data-ttu-id="50b9b-142">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-142">The name of the resource group.</span></span>
<span data-ttu-id="50b9b-143">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="50b9b-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="50b9b-144">-ShowInPortal</span></span>
<span data-ttu-id="50b9b-145">RD Web Access 서버에서 RemoteApp 프로그램을 표시하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="50b9b-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50b9b-146">-SubscriptionId</span></span>
<span data-ttu-id="50b9b-147">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="50b9b-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="50b9b-148">-Tag</span></span>
<span data-ttu-id="50b9b-149">업데이트할 태그</span><span class="sxs-lookup"><span data-stu-id="50b9b-149">tags to be updated</span></span>

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

### <span data-ttu-id="50b9b-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50b9b-150">-Confirm</span></span>
<span data-ttu-id="50b9b-151">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50b9b-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50b9b-152">-WhatIf</span></span>
<span data-ttu-id="50b9b-153">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="50b9b-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50b9b-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50b9b-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50b9b-155">CommonParameters</span></span>
<span data-ttu-id="50b9b-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50b9b-157">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="50b9b-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50b9b-158">입력</span><span class="sxs-lookup"><span data-stu-id="50b9b-158">INPUTS</span></span>

### <span data-ttu-id="50b9b-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="50b9b-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="50b9b-160">출력</span><span class="sxs-lookup"><span data-stu-id="50b9b-160">OUTPUTS</span></span>

### <span data-ttu-id="50b9b-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="50b9b-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplication</span></span>

## <span data-ttu-id="50b9b-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="50b9b-162">NOTES</span></span>

<span data-ttu-id="50b9b-163">별칭</span><span class="sxs-lookup"><span data-stu-id="50b9b-163">ALIASES</span></span>

<span data-ttu-id="50b9b-164">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="50b9b-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="50b9b-165">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="50b9b-166">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="50b9b-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="50b9b-167">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="50b9b-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="50b9b-168">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="50b9b-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="50b9b-169">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="50b9b-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="50b9b-170">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="50b9b-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="50b9b-171">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="50b9b-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="50b9b-172">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="50b9b-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="50b9b-173">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="50b9b-173">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="50b9b-174">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-174">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="50b9b-175">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-175">The name is case insensitive.</span></span>
  - <span data-ttu-id="50b9b-176">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="50b9b-176">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="50b9b-177">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="50b9b-177">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="50b9b-178">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="50b9b-178">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="50b9b-179">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="50b9b-179">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="50b9b-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50b9b-180">RELATED LINKS</span></span>

