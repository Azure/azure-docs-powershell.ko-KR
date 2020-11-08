---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 7a78404c8dde734f756792b85d27d712b5c5ed69
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214554"
---
# <span data-ttu-id="fb74f-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="fb74f-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="fb74f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb74f-102">SYNOPSIS</span></span>
<span data-ttu-id="fb74f-103">응용 프로그램을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-103">Create or update an application.</span></span>

## <span data-ttu-id="fb74f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb74f-104">SYNTAX</span></span>

### <span data-ttu-id="fb74f-105">CreateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="fb74f-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-FilePath <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fb74f-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="fb74f-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fb74f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fb74f-107">DESCRIPTION</span></span>
<span data-ttu-id="fb74f-108">응용 프로그램을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-108">Create or update an application.</span></span>

## <span data-ttu-id="fb74f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fb74f-109">EXAMPLES</span></span>

### <span data-ttu-id="fb74f-110">예제 1: Windows 가상 데스크톱 응용 프로그램 만들기</span><span class="sxs-lookup"><span data-stu-id="fb74f-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="fb74f-111">이 명령은 applicaton 그룹에 Windows 가상 데스크톱 응용 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="fb74f-112">변수</span><span class="sxs-lookup"><span data-stu-id="fb74f-112">PARAMETERS</span></span>

### <span data-ttu-id="fb74f-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="fb74f-113">-AppAlias</span></span>
<span data-ttu-id="fb74f-114">시작 메뉴 항목의 앱 별칭</span><span class="sxs-lookup"><span data-stu-id="fb74f-114">App Alias from start menu item</span></span>

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

### <span data-ttu-id="fb74f-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="fb74f-115">-CommandLineArgument</span></span>
<span data-ttu-id="fb74f-116">응용 프로그램의 명령줄 인수입니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="fb74f-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="fb74f-117">-CommandLineSetting</span></span>
<span data-ttu-id="fb74f-118">이 게시 된 응용 프로그램을 클라이언트에서 제공 하는 명령줄 인수, 게시 시간에 지정 된 명령줄 인수 또는 명령줄 인수 없이 실행할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="fb74f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb74f-119">-DefaultProfile</span></span>
<span data-ttu-id="fb74f-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb74f-121">-설명</span><span class="sxs-lookup"><span data-stu-id="fb74f-121">-Description</span></span>
<span data-ttu-id="fb74f-122">응용 프로그램에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-122">Description of Application.</span></span>

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

### <span data-ttu-id="fb74f-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="fb74f-123">-FilePath</span></span>
<span data-ttu-id="fb74f-124">응용 프로그램의 실행 파일에 대 한 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="fb74f-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="fb74f-125">-FriendlyName</span></span>
<span data-ttu-id="fb74f-126">응용 프로그램의 식별 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="fb74f-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="fb74f-127">-GroupName</span></span>
<span data-ttu-id="fb74f-128">응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-128">The name of the application group</span></span>

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

### <span data-ttu-id="fb74f-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="fb74f-129">-IconIndex</span></span>
<span data-ttu-id="fb74f-130">아이콘의 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-130">Index of the icon.</span></span>

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

### <span data-ttu-id="fb74f-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="fb74f-131">-IconPath</span></span>
<span data-ttu-id="fb74f-132">아이콘 경로</span><span class="sxs-lookup"><span data-stu-id="fb74f-132">Path to icon.</span></span>

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

### <span data-ttu-id="fb74f-133">-이름</span><span class="sxs-lookup"><span data-stu-id="fb74f-133">-Name</span></span>
<span data-ttu-id="fb74f-134">지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-134">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="fb74f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb74f-135">-ResourceGroupName</span></span>
<span data-ttu-id="fb74f-136">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-136">The name of the resource group.</span></span>
<span data-ttu-id="fb74f-137">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fb74f-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="fb74f-138">-ShowInPortal</span></span>
<span data-ttu-id="fb74f-139">RD 웹 액세스 서버에 RemoteApp 프로그램을 표시할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="fb74f-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fb74f-140">-SubscriptionId</span></span>
<span data-ttu-id="fb74f-141">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-141">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fb74f-142">-확인</span><span class="sxs-lookup"><span data-stu-id="fb74f-142">-Confirm</span></span>
<span data-ttu-id="fb74f-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb74f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb74f-144">-WhatIf</span></span>
<span data-ttu-id="fb74f-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb74f-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb74f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb74f-147">CommonParameters</span></span>
<span data-ttu-id="fb74f-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb74f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb74f-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fb74f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb74f-150">입력</span><span class="sxs-lookup"><span data-stu-id="fb74f-150">INPUTS</span></span>

## <span data-ttu-id="fb74f-151">출력</span><span class="sxs-lookup"><span data-stu-id="fb74f-151">OUTPUTS</span></span>

### <span data-ttu-id="fb74f-152">Api20191210Preview 응용 프로그램에 대 한 Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fb74f-152">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="fb74f-153">상속자</span><span class="sxs-lookup"><span data-stu-id="fb74f-153">NOTES</span></span>

<span data-ttu-id="fb74f-154">별칭과</span><span class="sxs-lookup"><span data-stu-id="fb74f-154">ALIASES</span></span>

## <span data-ttu-id="fb74f-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb74f-155">RELATED LINKS</span></span>

