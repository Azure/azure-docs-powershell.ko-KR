---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188345"
---
# <span data-ttu-id="8c263-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="8c263-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="8c263-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c263-102">SYNOPSIS</span></span>
<span data-ttu-id="8c263-103">이미지 사용자 지정 단위를 설명</span><span class="sxs-lookup"><span data-stu-id="8c263-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="8c263-104">구문</span><span class="sxs-lookup"><span data-stu-id="8c263-104">SYNTAX</span></span>

### <span data-ttu-id="8c263-105">ShellCustomizer(기본값)</span><span class="sxs-lookup"><span data-stu-id="8c263-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="8c263-106">FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="8c263-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="8c263-107">PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="8c263-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c263-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="8c263-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="8c263-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="8c263-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="8c263-110">설명</span><span class="sxs-lookup"><span data-stu-id="8c263-110">DESCRIPTION</span></span>
<span data-ttu-id="8c263-111">이미지 사용자 지정 단위를 설명</span><span class="sxs-lookup"><span data-stu-id="8c263-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="8c263-112">예제</span><span class="sxs-lookup"><span data-stu-id="8c263-112">EXAMPLES</span></span>

### <span data-ttu-id="8c263-113">예제 1: Windows 업데이트 사용자 지정자 만들기</span><span class="sxs-lookup"><span data-stu-id="8c263-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="8c263-114">이 명령은 Windows 업데이트 사용자 지정 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="8c263-115">예제 2: 파일 사용자 지정자 만들기</span><span class="sxs-lookup"><span data-stu-id="8c263-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="8c263-116">이 명령은 파일 사용자 지정 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="8c263-117">예제 3: PowerShell 사용자 지정자 만들기</span><span class="sxs-lookup"><span data-stu-id="8c263-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="8c263-118">이 명령은 PowerShell 사용자 지정 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="8c263-119">예제 4: 다시 시작 사용자 지정자 만들기</span><span class="sxs-lookup"><span data-stu-id="8c263-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="8c263-120">이 명령은 다시 시작 사용자 지정 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="8c263-121">예제 5: 셸 사용자 지정자 만들기</span><span class="sxs-lookup"><span data-stu-id="8c263-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="8c263-122">이 명령은 셸 사용자 지정 프로그램을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="8c263-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c263-123">PARAMETERS</span></span>

### <span data-ttu-id="8c263-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="8c263-124">-CustomizerName</span></span>
<span data-ttu-id="8c263-125">이 사용자 지정 단계의 작동에 대한 컨텍스트를 제공하는 친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-125">Friendly Name to provide context on what this customization step does.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-126">-Destination</span><span class="sxs-lookup"><span data-stu-id="8c263-126">-Destination</span></span>
<span data-ttu-id="8c263-127">파일(sourceUri에서)이 VM에 업로드될 파일의 절대 경로(이미 생성된 중첩된 디렉터리 구조)입니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-128">-FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="8c263-128">-FileCustomizer</span></span>
<span data-ttu-id="8c263-129">VM(Linux, Windows)에 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="8c263-130">Packer 파일 프로비전자에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-130">Corresponds to Packer file provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="8c263-131">-Filter</span></span>
<span data-ttu-id="8c263-132">적용할 업데이트를 선택할 필터 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="8c263-133">기본값을 사용할 빈 배열을 생략하거나 지정합니다(필터 없음).</span><span class="sxs-lookup"><span data-stu-id="8c263-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="8c263-134">이 필드의 예제 및 자세한 설명은 위의 링크를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8c263-134">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-135">-Inline</span><span class="sxs-lookup"><span data-stu-id="8c263-135">-Inline</span></span>
<span data-ttu-id="8c263-136">실행할 셸 명령의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-136">Array of shell commands to execute.</span></span>

```yaml
Type: System.String[]
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-137">-PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="8c263-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="8c263-138">VM(Windows)에서 지정된 PowerShell을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="8c263-139">Packer PowerShell 프로비전에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="8c263-140">정확히 'scriptUri' 또는 'inline' 중 하나를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PowerShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="8c263-141">-RestartCheckCommand</span></span>
<span data-ttu-id="8c263-142">다시 시작이 성공하는지 확인하려면 명령합니다[기본값: ''].</span><span class="sxs-lookup"><span data-stu-id="8c263-142">Command to check if restart succeeded [Default: ''].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="8c263-143">-RestartCommand</span></span>
<span data-ttu-id="8c263-144">다시 시작을 실행하는 명령 [기본값: 'shutdown /r /f /t 0 /c packer restart']</span><span class="sxs-lookup"><span data-stu-id="8c263-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="8c263-145">-RestartCustomizer</span></span>
<span data-ttu-id="8c263-146">VM을 다시 부팅하고 다시 온라인(Windows)으로 돌아올 때까지 기다릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="8c263-147">Packer windows-restart 프로비전에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-147">Corresponds to Packer windows-restart provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestartCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="8c263-148">-RestartTimeout</span></span>
<span data-ttu-id="8c263-149">크기 및 단위 문자열로 지정된 시간 제한을 다시 시작합니다(예: '5m'(5분) 또는 '2h'(2시간) [기본값: '5m'].</span><span class="sxs-lookup"><span data-stu-id="8c263-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="8c263-150">-RunElevated</span></span>
<span data-ttu-id="8c263-151">지정된 경우 PowerShell 스크립트는 상승된 권한으로 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="8c263-152">-ScriptUri</span></span>
<span data-ttu-id="8c263-153">사용자 지정을 위해 실행할 셸 스크립트의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="8c263-154">Github 링크, Azure Storage에 대한 SAS URI 등이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="8c263-155">-SearchCriterion</span></span>
<span data-ttu-id="8c263-156">업데이트를 검색하는 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-156">Criteria to search updates.</span></span>
<span data-ttu-id="8c263-157">기본값을 사용하기 위해 빈 문자열을 생략하거나 지정합니다(모두 검색).</span><span class="sxs-lookup"><span data-stu-id="8c263-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="8c263-158">이 필드의 예제 및 자세한 설명은 위의 링크를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8c263-158">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="8c263-159">-Sha256Checksum</span></span>
<span data-ttu-id="8c263-160">scriptUri 필드에 제공된 셸 스크립트의 SHA256 체크um입니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer, PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-161">-ShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="8c263-161">-ShellCustomizer</span></span>
<span data-ttu-id="8c263-162">사용자 지정 단계(Linux) 중에 셸 스크립트를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="8c263-163">Packer 셸 프로비전에 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="8c263-164">정확히 'scriptUri' 또는 'inline' 중 하나를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="8c263-165">-SourceUri</span></span>
<span data-ttu-id="8c263-166">VM을 사용자 지정하기 위해 업로드할 파일의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="8c263-167">Github 링크, Azure Storage에 대한 SAS URI 등이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="8c263-168">-UpdateLimit</span></span>
<span data-ttu-id="8c263-169">한 때 적용할 최대 업데이트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="8c263-170">기본값을 사용하기 위해 0을 생략하거나 지정합니다(1000).</span><span class="sxs-lookup"><span data-stu-id="8c263-170">Omit or specify 0 to use the default (1000).</span></span>

```yaml
Type: System.Int32
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="8c263-171">-ValidExitCode</span></span>
<span data-ttu-id="8c263-172">PowerShell 스크립트에 대한 유효한 종료 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="8c263-173">[기본값: 0].</span><span class="sxs-lookup"><span data-stu-id="8c263-173">[Default: 0].</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="8c263-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="8c263-175">Windows 업데이트를 설치합니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-175">Installs Windows Updates.</span></span>
<span data-ttu-id="8c263-176">Packer Windows Update https://github.com/rgl/packer-provisioner-windows-update) Provisioner(.</span><span class="sxs-lookup"><span data-stu-id="8c263-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c263-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c263-177">CommonParameters</span></span>
<span data-ttu-id="8c263-178">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8c263-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c263-179">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8c263-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c263-180">입력</span><span class="sxs-lookup"><span data-stu-id="8c263-180">INPUTS</span></span>

## <span data-ttu-id="8c263-181">출력</span><span class="sxs-lookup"><span data-stu-id="8c263-181">OUTPUTS</span></span>

### <span data-ttu-id="8c263-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span><span class="sxs-lookup"><span data-stu-id="8c263-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="8c263-183">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8c263-183">NOTES</span></span>

<span data-ttu-id="8c263-184">별칭</span><span class="sxs-lookup"><span data-stu-id="8c263-184">ALIASES</span></span>

## <span data-ttu-id="8c263-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c263-185">RELATED LINKS</span></span>

