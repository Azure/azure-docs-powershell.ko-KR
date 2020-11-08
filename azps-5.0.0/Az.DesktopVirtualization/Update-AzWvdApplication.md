---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 8c2026e7ef8ed5c0eeb1e5a4cb7f605c1a030b9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217488"
---
# <span data-ttu-id="4cff5-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="4cff5-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="4cff5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cff5-102">SYNOPSIS</span></span>
<span data-ttu-id="4cff5-103">응용 프로그램을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-103">Update an application.</span></span>

## <span data-ttu-id="4cff5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4cff5-104">SYNTAX</span></span>

### <span data-ttu-id="4cff5-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4cff5-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-CommandLineSetting <CommandLineSetting>]
 [-Description <String>] [-FilePath <String>] [-FriendlyName <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4cff5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4cff5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4cff5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4cff5-107">DESCRIPTION</span></span>
<span data-ttu-id="4cff5-108">응용 프로그램을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-108">Update an application.</span></span>

## <span data-ttu-id="4cff5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4cff5-109">EXAMPLES</span></span>

### <span data-ttu-id="4cff5-110">예제 1: Windows 가상 데스크톱 응용 프로그램 업데이트</span><span class="sxs-lookup"><span data-stu-id="4cff5-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="4cff5-111">이 명령은 applicaton 그룹의 Windows 가상 데스크톱 응용 프로그램을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="4cff5-112">변수</span><span class="sxs-lookup"><span data-stu-id="4cff5-112">PARAMETERS</span></span>

### <span data-ttu-id="4cff5-113">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="4cff5-113">-CommandLineArgument</span></span>
<span data-ttu-id="4cff5-114">응용 프로그램의 명령줄 인수입니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-114">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="4cff5-115">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="4cff5-115">-CommandLineSetting</span></span>
<span data-ttu-id="4cff5-116">이 게시 된 응용 프로그램을 클라이언트에서 제공 하는 명령줄 인수, 게시 시간에 지정 된 명령줄 인수 또는 명령줄 인수 없이 실행할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-116">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="4cff5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cff5-117">-DefaultProfile</span></span>
<span data-ttu-id="4cff5-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cff5-119">-설명</span><span class="sxs-lookup"><span data-stu-id="4cff5-119">-Description</span></span>
<span data-ttu-id="4cff5-120">응용 프로그램에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-120">Description of Application.</span></span>

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

### <span data-ttu-id="4cff5-121">-FilePath</span><span class="sxs-lookup"><span data-stu-id="4cff5-121">-FilePath</span></span>
<span data-ttu-id="4cff5-122">응용 프로그램의 실행 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-122">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="4cff5-123">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4cff5-123">-FriendlyName</span></span>
<span data-ttu-id="4cff5-124">응용 프로그램의 식별 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-124">Friendly name of Application.</span></span>

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

### <span data-ttu-id="4cff5-125">-GroupName</span><span class="sxs-lookup"><span data-stu-id="4cff5-125">-GroupName</span></span>
<span data-ttu-id="4cff5-126">응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-126">The name of the application group</span></span>

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

### <span data-ttu-id="4cff5-127">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="4cff5-127">-IconIndex</span></span>
<span data-ttu-id="4cff5-128">아이콘의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-128">Index of the icon.</span></span>

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

### <span data-ttu-id="4cff5-129">-IconPath</span><span class="sxs-lookup"><span data-stu-id="4cff5-129">-IconPath</span></span>
<span data-ttu-id="4cff5-130">아이콘 경로</span><span class="sxs-lookup"><span data-stu-id="4cff5-130">Path to icon.</span></span>

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

### <span data-ttu-id="4cff5-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cff5-131">-InputObject</span></span>
<span data-ttu-id="4cff5-132">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-132">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4cff5-133">-이름</span><span class="sxs-lookup"><span data-stu-id="4cff5-133">-Name</span></span>
<span data-ttu-id="4cff5-134">지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-134">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="4cff5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cff5-135">-ResourceGroupName</span></span>
<span data-ttu-id="4cff5-136">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-136">The name of the resource group.</span></span>
<span data-ttu-id="4cff5-137">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4cff5-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="4cff5-138">-ShowInPortal</span></span>
<span data-ttu-id="4cff5-139">RD 웹 액세스 서버에 RemoteApp 프로그램을 표시할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="4cff5-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4cff5-140">-SubscriptionId</span></span>
<span data-ttu-id="4cff5-141">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-141">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4cff5-142">태그</span><span class="sxs-lookup"><span data-stu-id="4cff5-142">-Tag</span></span>
<span data-ttu-id="4cff5-143">업데이트할 태그</span><span class="sxs-lookup"><span data-stu-id="4cff5-143">tags to be updated</span></span>

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

### <span data-ttu-id="4cff5-144">-확인</span><span class="sxs-lookup"><span data-stu-id="4cff5-144">-Confirm</span></span>
<span data-ttu-id="4cff5-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cff5-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cff5-146">-WhatIf</span></span>
<span data-ttu-id="4cff5-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cff5-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cff5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cff5-149">CommonParameters</span></span>
<span data-ttu-id="4cff5-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cff5-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4cff5-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cff5-152">입력</span><span class="sxs-lookup"><span data-stu-id="4cff5-152">INPUTS</span></span>

### <span data-ttu-id="4cff5-153">IDesktopVirtualizationIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="4cff5-153">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4cff5-154">출력</span><span class="sxs-lookup"><span data-stu-id="4cff5-154">OUTPUTS</span></span>

### <span data-ttu-id="4cff5-155">Api20191210Preview 응용 프로그램에 대 한 Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4cff5-155">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="4cff5-156">상속자</span><span class="sxs-lookup"><span data-stu-id="4cff5-156">NOTES</span></span>

<span data-ttu-id="4cff5-157">별칭과</span><span class="sxs-lookup"><span data-stu-id="4cff5-157">ALIASES</span></span>

<span data-ttu-id="4cff5-158">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4cff5-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4cff5-159">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4cff5-160">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="4cff5-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4cff5-161">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4cff5-161">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4cff5-162">`[ApplicationGroupName <String>]`: 응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-162">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4cff5-163">`[ApplicationName <String>]`: 지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-163">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4cff5-164">`[DesktopName <String>]`: 지정 된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="4cff5-164">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4cff5-165">`[HostPoolName <String>]`: 지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-165">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4cff5-166">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="4cff5-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4cff5-167">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4cff5-168">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="4cff5-169">`[SessionHostName <String>]`: 지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-169">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4cff5-170">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4cff5-171">`[UserSessionId <String>]`: 지정 된 세션 호스트 내에 있는 사용자 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cff5-171">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4cff5-172">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="4cff5-172">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4cff5-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cff5-173">RELATED LINKS</span></span>

