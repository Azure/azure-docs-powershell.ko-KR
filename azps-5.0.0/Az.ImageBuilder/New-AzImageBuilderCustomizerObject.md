---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304028"
---
# <span data-ttu-id="8d921-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="8d921-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="8d921-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d921-102">SYNOPSIS</span></span>
<span data-ttu-id="8d921-103">이미지 사용자 지정 단위를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="8d921-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d921-104">SYNTAX</span></span>

### <span data-ttu-id="8d921-105">ShellCustomizer 지정자 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8d921-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="8d921-106">FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="8d921-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="8d921-107">PowerShellCustomizer 지정자</span><span class="sxs-lookup"><span data-stu-id="8d921-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="8d921-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="8d921-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="8d921-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="8d921-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="8d921-110">설명은</span><span class="sxs-lookup"><span data-stu-id="8d921-110">DESCRIPTION</span></span>
<span data-ttu-id="8d921-111">이미지 사용자 지정 단위를 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="8d921-112">예제의</span><span class="sxs-lookup"><span data-stu-id="8d921-112">EXAMPLES</span></span>

### <span data-ttu-id="8d921-113">예제 1: windows 업데이트 사용자 지정자 만들기</span><span class="sxs-lookup"><span data-stu-id="8d921-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="8d921-114">이 명령은 windows 업데이트 사용자 지정자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="8d921-115">예제 2: 파일 사용자 지정자 만들기</span><span class="sxs-lookup"><span data-stu-id="8d921-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="8d921-116">이 명령은 파일 사용자 지정자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="8d921-117">예제 3: powershell 사용자 지정자 만들기</span><span class="sxs-lookup"><span data-stu-id="8d921-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="8d921-118">이 명령은 powershell 사용자 지정자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="8d921-119">예제 4: 다시 시작 사용자 지정자 만들기</span><span class="sxs-lookup"><span data-stu-id="8d921-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="8d921-120">이 명령은 다시 시작 사용자 지정자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="8d921-121">예제 5: 셸 사용자 지정자 만들기</span><span class="sxs-lookup"><span data-stu-id="8d921-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="8d921-122">이 명령은 shell 사용자 지정자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="8d921-123">변수</span><span class="sxs-lookup"><span data-stu-id="8d921-123">PARAMETERS</span></span>

### <span data-ttu-id="8d921-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="8d921-124">-CustomizerName</span></span>
<span data-ttu-id="8d921-125">이 사용자 지정 단계의 역할에 대 한 컨텍스트를 제공 하는 친근 한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-125">Friendly Name to provide context on what this customization step does.</span></span>

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

### <span data-ttu-id="8d921-126">-대상</span><span class="sxs-lookup"><span data-stu-id="8d921-126">-Destination</span></span>
<span data-ttu-id="8d921-127">VM에서 파일이 원본 Uri에서 업로드 되는 파일 (중첩 된 디렉터리 구조가 이미 만들어짐)에 대 한 절대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

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

### <span data-ttu-id="8d921-128">-FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="8d921-128">-FileCustomizer</span></span>
<span data-ttu-id="8d921-129">Vm (Linux, Windows)에 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="8d921-130">팩 Er 파일 provisioner에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-130">Corresponds to Packer file provisioner.</span></span>

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

### <span data-ttu-id="8d921-131">-필터</span><span class="sxs-lookup"><span data-stu-id="8d921-131">-Filter</span></span>
<span data-ttu-id="8d921-132">적용할 업데이트를 선택 하는 필터의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="8d921-133">기본 (필터 없음)을 사용 하려면 생략 하거나 빈 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="8d921-134">이 필드에 대 한 자세한 설명과 예제는 위의 링크를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d921-134">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="8d921-135">-인라인</span><span class="sxs-lookup"><span data-stu-id="8d921-135">-Inline</span></span>
<span data-ttu-id="8d921-136">실행할 셸 명령의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-136">Array of shell commands to execute.</span></span>

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

### <span data-ttu-id="8d921-137">-PowerShellCustomizer 지정자</span><span class="sxs-lookup"><span data-stu-id="8d921-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="8d921-138">VM (Windows)에서 지정 된 PowerShell을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="8d921-139">이는 팩 Er powershell provisioner에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="8d921-140">' ScriptUri ' 또는 ' inline ' 중 하나만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="8d921-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="8d921-141">-RestartCheckCommand</span></span>
<span data-ttu-id="8d921-142">명령-다시 시작이 성공 했는지 확인 하려면 [기본값: ' ']을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-142">Command to check if restart succeeded [Default: ''].</span></span>

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

### <span data-ttu-id="8d921-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="8d921-143">-RestartCommand</span></span>
<span data-ttu-id="8d921-144">다시 시작을 실행 하는 명령 [기본값: ' 종료/r/f/t 0/c 팩 er 다시 시작 ']</span><span class="sxs-lookup"><span data-stu-id="8d921-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

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

### <span data-ttu-id="8d921-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="8d921-145">-RestartCustomizer</span></span>
<span data-ttu-id="8d921-146">VM을 재부팅 하 고 다시 온라인 상태가 될 때까지 기다립니다 (Windows).</span><span class="sxs-lookup"><span data-stu-id="8d921-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="8d921-147">팩 Er windows-provisioner 다시 시작에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-147">Corresponds to Packer windows-restart provisioner.</span></span>

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

### <span data-ttu-id="8d921-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="8d921-148">-RestartTimeout</span></span>
<span data-ttu-id="8d921-149">시간 제한을 다시 시작 합니다 (예: ' 5m ' (5 분) 또는 ' 2h ' (2 시간) [기본값: ' 5m ']의 크기와 단위 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

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

### <span data-ttu-id="8d921-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="8d921-150">-RunElevated</span></span>
<span data-ttu-id="8d921-151">지정 된 경우 PowerShell 스크립트는 관리자 권한으로 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

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

### <span data-ttu-id="8d921-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="8d921-152">-ScriptUri</span></span>
<span data-ttu-id="8d921-153">사용자 지정 하기 위해 실행할 셸 스크립트의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="8d921-154">이는 github 링크, Azure Storage 용 SAS URI 등 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="8d921-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="8d921-155">-SearchCriterion</span></span>
<span data-ttu-id="8d921-156">업데이트를 검색 하는 조건입니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-156">Criteria to search updates.</span></span>
<span data-ttu-id="8d921-157">기본 (모두 검색)을 사용 하도록 빈 문자열을 생략 하거나 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="8d921-158">이 필드에 대 한 자세한 설명과 예제는 위의 링크를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d921-158">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="8d921-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="8d921-159">-Sha256Checksum</span></span>
<span data-ttu-id="8d921-160">ScriptUri 필드에 제공 된 셸 스크립트의 SHA256 체크섬입니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

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

### <span data-ttu-id="8d921-161">-ShellCustomizer 지정자</span><span class="sxs-lookup"><span data-stu-id="8d921-161">-ShellCustomizer</span></span>
<span data-ttu-id="8d921-162">사용자 지정 단계 (Linux) 중에 셸 스크립트를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="8d921-163">이는 팩 Er shell provisioner에 해당 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="8d921-164">' ScriptUri ' 또는 ' inline ' 중 하나만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="8d921-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="8d921-165">-SourceUri</span></span>
<span data-ttu-id="8d921-166">VM을 사용자 지정 하기 위해 업로드할 파일의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="8d921-167">이는 github 링크, Azure Storage 용 SAS URI 등 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="8d921-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="8d921-168">-UpdateLimit</span></span>
<span data-ttu-id="8d921-169">한 번에 적용할 최대 업데이트 수</span><span class="sxs-lookup"><span data-stu-id="8d921-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="8d921-170">0을 생략 하거나 지정 하 여 기본값 (1000)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-170">Omit or specify 0 to use the default (1000).</span></span>

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

### <span data-ttu-id="8d921-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="8d921-171">-ValidExitCode</span></span>
<span data-ttu-id="8d921-172">PowerShell 스크립트에 대 한 유효한 종료 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="8d921-173">[기본값: 0].</span><span class="sxs-lookup"><span data-stu-id="8d921-173">[Default: 0].</span></span>

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

### <span data-ttu-id="8d921-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="8d921-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="8d921-175">Windows 업데이트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-175">Installs Windows Updates.</span></span>
<span data-ttu-id="8d921-176">이 (가) 팩 Er (Provisioner) 업데이트에 해당 https://github.com/rgl/packer-provisioner-windows-update) 합니다 (.</span><span class="sxs-lookup"><span data-stu-id="8d921-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

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

### <span data-ttu-id="8d921-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d921-177">CommonParameters</span></span>
<span data-ttu-id="8d921-178">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d921-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d921-179">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d921-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d921-180">입력</span><span class="sxs-lookup"><span data-stu-id="8d921-180">INPUTS</span></span>

## <span data-ttu-id="8d921-181">출력</span><span class="sxs-lookup"><span data-stu-id="8d921-181">OUTPUTS</span></span>

### <span data-ttu-id="8d921-182">Api20200214. IImageTemplateCustomizer에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8d921-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="8d921-183">상속자</span><span class="sxs-lookup"><span data-stu-id="8d921-183">NOTES</span></span>

<span data-ttu-id="8d921-184">별칭과</span><span class="sxs-lookup"><span data-stu-id="8d921-184">ALIASES</span></span>

## <span data-ttu-id="8d921-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d921-185">RELATED LINKS</span></span>

