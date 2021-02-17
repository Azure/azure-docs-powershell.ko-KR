---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 88c56275bc2687d9693411159551684a9c76f943
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196441"
---
# <span data-ttu-id="99b01-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="99b01-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="99b01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99b01-102">SYNOPSIS</span></span>
<span data-ttu-id="99b01-103">애플리케이션을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-103">Create or update an application.</span></span>

## <span data-ttu-id="99b01-104">구문</span><span class="sxs-lookup"><span data-stu-id="99b01-104">SYNTAX</span></span>

### <span data-ttu-id="99b01-105">CreateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="99b01-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-FilePath <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="99b01-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="99b01-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="99b01-107">설명</span><span class="sxs-lookup"><span data-stu-id="99b01-107">DESCRIPTION</span></span>
<span data-ttu-id="99b01-108">애플리케이션을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-108">Create or update an application.</span></span>

## <span data-ttu-id="99b01-109">예제</span><span class="sxs-lookup"><span data-stu-id="99b01-109">EXAMPLES</span></span>

### <span data-ttu-id="99b01-110">예제 1: Windows Virtual Desktop 애플리케이션 만들기</span><span class="sxs-lookup"><span data-stu-id="99b01-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> New-AzWvdApplication -ResourceGroupName ResourceGroupName `
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

<span data-ttu-id="99b01-111">이 명령은 응용 프로그램 그룹에 Windows Virtual Desktop 애플리케이션을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="99b01-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99b01-112">PARAMETERS</span></span>

### <span data-ttu-id="99b01-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="99b01-113">-AppAlias</span></span>
<span data-ttu-id="99b01-114">시작 메뉴 항목의 앱 별칭</span><span class="sxs-lookup"><span data-stu-id="99b01-114">App Alias from start menu item</span></span>

```yaml
Type: System.String
Parameter Sets: AppAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b01-115">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="99b01-115">-ApplicationType</span></span>
<span data-ttu-id="99b01-116">애플리케이션의 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-116">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b01-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="99b01-117">-CommandLineArgument</span></span>
<span data-ttu-id="99b01-118">애플리케이션에 대한 명령줄 인수입니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-118">Command Line Arguments for Application.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b01-119">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="99b01-119">-CommandLineSetting</span></span>
<span data-ttu-id="99b01-120">이 게시된 애플리케이션을 클라이언트에서 제공하는 명령줄 인수, 게시 시 지정된 명령줄 인수 또는 명령줄 인수를 모두 사용하여 시작될 수 있는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-120">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b01-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b01-121">-DefaultProfile</span></span>
<span data-ttu-id="99b01-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99b01-123">-Description</span><span class="sxs-lookup"><span data-stu-id="99b01-123">-Description</span></span>
<span data-ttu-id="99b01-124">애플리케이션에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-124">Description of Application.</span></span>

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

### <span data-ttu-id="99b01-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="99b01-125">-FilePath</span></span>
<span data-ttu-id="99b01-126">애플리케이션에 대한 실행 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-126">Specifies a path for the executable file for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b01-127">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="99b01-127">-FriendlyName</span></span>
<span data-ttu-id="99b01-128">애플리케이션의 친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-128">Friendly name of Application.</span></span>

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

### <span data-ttu-id="99b01-129">-GroupName</span><span class="sxs-lookup"><span data-stu-id="99b01-129">-GroupName</span></span>
<span data-ttu-id="99b01-130">애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="99b01-130">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b01-131">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="99b01-131">-IconIndex</span></span>
<span data-ttu-id="99b01-132">아이콘의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-132">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b01-133">-IconPath</span><span class="sxs-lookup"><span data-stu-id="99b01-133">-IconPath</span></span>
<span data-ttu-id="99b01-134">아이콘의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-134">Path to icon.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b01-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="99b01-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="99b01-136">MSIX 애플리케이션에 대한 패키지 애플리케이션 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-136">Specifies the package application Id for MSIX applications</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b01-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="99b01-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="99b01-138">MSIX 애플리케이션에 대한 패키지 패밀리 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-138">Specifies the package family name for MSIX applications</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b01-139">-Name</span><span class="sxs-lookup"><span data-stu-id="99b01-139">-Name</span></span>
<span data-ttu-id="99b01-140">지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="99b01-140">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b01-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99b01-141">-ResourceGroupName</span></span>
<span data-ttu-id="99b01-142">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-142">The name of the resource group.</span></span>
<span data-ttu-id="99b01-143">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-143">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b01-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="99b01-144">-ShowInPortal</span></span>
<span data-ttu-id="99b01-145">RD Web Access 서버에서 RemoteApp 프로그램을 표시하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="99b01-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99b01-146">-SubscriptionId</span></span>
<span data-ttu-id="99b01-147">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-147">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b01-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99b01-148">-Confirm</span></span>
<span data-ttu-id="99b01-149">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99b01-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99b01-150">-WhatIf</span></span>
<span data-ttu-id="99b01-151">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="99b01-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99b01-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99b01-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b01-153">CommonParameters</span></span>
<span data-ttu-id="99b01-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="99b01-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b01-155">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="99b01-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b01-156">입력</span><span class="sxs-lookup"><span data-stu-id="99b01-156">INPUTS</span></span>

## <span data-ttu-id="99b01-157">출력</span><span class="sxs-lookup"><span data-stu-id="99b01-157">OUTPUTS</span></span>

### <span data-ttu-id="99b01-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="99b01-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="99b01-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="99b01-159">NOTES</span></span>

<span data-ttu-id="99b01-160">별칭</span><span class="sxs-lookup"><span data-stu-id="99b01-160">ALIASES</span></span>

## <span data-ttu-id="99b01-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99b01-161">RELATED LINKS</span></span>

