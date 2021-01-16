---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
ms.openlocfilehash: fd5dd920863d4bd53257cfe2170e83f53c620096
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357617"
---
# <span data-ttu-id="5742c-101">New-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="5742c-101">New-AzWvdMsixPackage</span></span>

## <span data-ttu-id="5742c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5742c-102">SYNOPSIS</span></span>
<span data-ttu-id="5742c-103">MSIX 패키지를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-103">Create or update a MSIX package.</span></span>

## <span data-ttu-id="5742c-104">구문</span><span class="sxs-lookup"><span data-stu-id="5742c-104">SYNTAX</span></span>

### <span data-ttu-id="5742c-105">CreateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="5742c-105">CreateExpanded (Default)</span></span>
```
New-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-LastUpdated <DateTime>] [-PackageApplication <IMsixPackageApplications[]>]
 [-PackageDependency <IMsixPackageDependencies[]>] [-PackageFamilyName <String>] [-PackageName <String>]
 [-PackageRelativePath <String>] [-Version <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5742c-106">PackageAlias</span><span class="sxs-lookup"><span data-stu-id="5742c-106">PackageAlias</span></span>
```
New-AzWvdMsixPackage -HostPoolName <String> -PackageAlias <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5742c-107">설명</span><span class="sxs-lookup"><span data-stu-id="5742c-107">DESCRIPTION</span></span>
<span data-ttu-id="5742c-108">MSIX 패키지를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-108">Create or update a MSIX package.</span></span>

## <span data-ttu-id="5742c-109">예제</span><span class="sxs-lookup"><span data-stu-id="5742c-109">EXAMPLES</span></span>

### <span data-ttu-id="5742c-110">예제 1: 패키지 별칭을 통해 HostPool에 새 MSIX 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-110">Example 1: Creates New MSIX Package in the HostPool via Package Alias</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
      -PackageAlias packagealias `
      -ImagePath ImagePathURI  `
```

<span data-ttu-id="5742c-111">이 명령은 지정된 이미지 경로의 MSIX 패키지를 HostPool에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-111">This command adds MSIX package from specified image path to HostPool</span></span>

### <span data-ttu-id="5742c-112">예제 2: HostPool에서 새 MSIX 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-112">Example 2: Creates New MSIX Package in the HostPool</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -FullName PackageFullName `
                            -HostPoolName HostPoolName `
                            -ResourceGroupName ResourceGroupName ` 
                            -SubscriptionId SubscriptionId ` 
                            -DisplayName displayname `
                            -ImagePath imageURI ` 
                            -IsActive:$false `
                            -IsRegularRegistration:$false `
                            -LastUpdated datelastupdated `
                            -PackageApplication $apps `
                            -PackageDependency $deps `
                            -PackageFamilyName packagefamilyname `
                            -PackageName packagename `
                            -PackageRelativePath packagerelativepath `
                            -Version packageversion `

Name                              Type
----                              ----
HotPoolName/PackageFullName      Microsoft.DesktopVirtualization/hostpools/msixpackages

```

<span data-ttu-id="5742c-113">이 명령은 지정된 HostPool에 MSIX 패키지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-113">This command adds MSIX Package in the specified HostPool</span></span>

## <span data-ttu-id="5742c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5742c-114">PARAMETERS</span></span>

### <span data-ttu-id="5742c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5742c-115">-DefaultProfile</span></span>
<span data-ttu-id="5742c-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5742c-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5742c-117">-DisplayName</span></span>
<span data-ttu-id="5742c-118">포털에 표시할 사용자 친화적인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-118">User friendly Name to be displayed in the portal.</span></span>

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

### <span data-ttu-id="5742c-119">-FullName</span><span class="sxs-lookup"><span data-stu-id="5742c-119">-FullName</span></span>
<span data-ttu-id="5742c-120">지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="5742c-120">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5742c-121">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="5742c-121">-HostPoolName</span></span>
<span data-ttu-id="5742c-122">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="5742c-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="5742c-123">-ImagePath</span><span class="sxs-lookup"><span data-stu-id="5742c-123">-ImagePath</span></span>
<span data-ttu-id="5742c-124">네트워크 공유의 VHD/CIM 이미지 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-124">VHD/CIM image path on Network Share.</span></span>

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

### <span data-ttu-id="5742c-125">-IsActive</span><span class="sxs-lookup"><span data-stu-id="5742c-125">-IsActive</span></span>
<span data-ttu-id="5742c-126">이 버전의 패키지를 호스트풀에서 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-126">Make this version of the package the active one across the hostpool.</span></span>

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

### <span data-ttu-id="5742c-127">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="5742c-127">-IsRegularRegistration</span></span>
<span data-ttu-id="5742c-128">피드에 패키지를 등록하는 방법을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-128">Specifies how to register Package in feed.</span></span>

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

### <span data-ttu-id="5742c-129">-LastUpdated</span><span class="sxs-lookup"><span data-stu-id="5742c-129">-LastUpdated</span></span>
<span data-ttu-id="5742c-130">날짜 패키지가 마지막으로 업데이트되었습니다. 이 패키지는 appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="5742c-130">Date Package was last updated, found in the appxmanifest.xml.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5742c-131">-PackageAlias</span><span class="sxs-lookup"><span data-stu-id="5742c-131">-PackageAlias</span></span>
<span data-ttu-id="5742c-132">MSIX 이미지 추출에서 패키지 별칭</span><span class="sxs-lookup"><span data-stu-id="5742c-132">Package Alias from extract MSIX Image</span></span>

```yaml
Type: System.String
Parameter Sets: PackageAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5742c-133">-PackageApplication</span><span class="sxs-lookup"><span data-stu-id="5742c-133">-PackageApplication</span></span>
<span data-ttu-id="5742c-134">패키지 애플리케이션 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-134">List of package applications.</span></span>

<span data-ttu-id="5742c-135">생성을 위해 PACKAGEAPPLICATION 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="5742c-135">To construct, see NOTES section for PACKAGEAPPLICATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackageApplications[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5742c-136">-PackageDependency</span><span class="sxs-lookup"><span data-stu-id="5742c-136">-PackageDependency</span></span>
<span data-ttu-id="5742c-137">패키지 종속성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-137">List of package dependencies.</span></span>

<span data-ttu-id="5742c-138">생성을 위해 PACKAGEDEPENDENCY 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="5742c-138">To construct, see NOTES section for PACKAGEDEPENDENCY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackageDependencies[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5742c-139">-PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="5742c-139">-PackageFamilyName</span></span>
<span data-ttu-id="5742c-140">패키지 패밀리 이름은 appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="5742c-140">Package Family Name from appxmanifest.xml.</span></span>
<span data-ttu-id="5742c-141">패키지 이름 및 게시자 이름을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-141">Contains Package Name and Publisher name.</span></span>

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

### <span data-ttu-id="5742c-142">-PackageName</span><span class="sxs-lookup"><span data-stu-id="5742c-142">-PackageName</span></span>
<span data-ttu-id="5742c-143">패키지 이름의 appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="5742c-143">Package Name from appxmanifest.xml.</span></span>

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

### <span data-ttu-id="5742c-144">-PackageRelativePath</span><span class="sxs-lookup"><span data-stu-id="5742c-144">-PackageRelativePath</span></span>
<span data-ttu-id="5742c-145">이미지 내부의 패키지에 대한 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-145">Relative Path to the package inside the image.</span></span>

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

### <span data-ttu-id="5742c-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5742c-146">-ResourceGroupName</span></span>
<span data-ttu-id="5742c-147">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-147">The name of the resource group.</span></span>
<span data-ttu-id="5742c-148">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-148">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5742c-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5742c-149">-SubscriptionId</span></span>
<span data-ttu-id="5742c-150">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-150">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5742c-151">-Version</span><span class="sxs-lookup"><span data-stu-id="5742c-151">-Version</span></span>
<span data-ttu-id="5742c-152">패키지 버전은 appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="5742c-152">Package Version found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="5742c-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5742c-153">-Confirm</span></span>
<span data-ttu-id="5742c-154">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5742c-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5742c-155">-WhatIf</span></span>
<span data-ttu-id="5742c-156">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5742c-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5742c-157">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5742c-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5742c-158">CommonParameters</span></span>
<span data-ttu-id="5742c-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5742c-160">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5742c-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5742c-161">입력</span><span class="sxs-lookup"><span data-stu-id="5742c-161">INPUTS</span></span>

## <span data-ttu-id="5742c-162">출력</span><span class="sxs-lookup"><span data-stu-id="5742c-162">OUTPUTS</span></span>

### <span data-ttu-id="5742c-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="5742c-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span></span>

## <span data-ttu-id="5742c-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5742c-164">NOTES</span></span>

<span data-ttu-id="5742c-165">별칭</span><span class="sxs-lookup"><span data-stu-id="5742c-165">ALIASES</span></span>

<span data-ttu-id="5742c-166">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="5742c-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5742c-167">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5742c-168">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5742c-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5742c-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: 패키지 애플리케이션 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: List of package applications.</span></span> 
  - <span data-ttu-id="5742c-170">`[AppId <String>]`: 패키지 애플리케이션 ID로, appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="5742c-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="5742c-171">`[AppUserModelId <String>]`: 패키지 애플리케이션을 활성화하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-171">`[AppUserModelId <String>]`: Used to activate Package Application.</span></span> <span data-ttu-id="5742c-172">패키지 이름 및 ApplicationID로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-172">Consists of Package Name and ApplicationID.</span></span> <span data-ttu-id="5742c-173">다음 appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="5742c-173">Found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="5742c-174">`[Description <String>]`: 패키지 애플리케이션에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-174">`[Description <String>]`: Description of Package Application.</span></span>
  - <span data-ttu-id="5742c-175">`[FriendlyName <String>]`: 사용자 친화적인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-175">`[FriendlyName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="5742c-176">`[IconImageName <String>]`: 사용자 친화적인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-176">`[IconImageName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="5742c-177">`[RawIcon <Byte[]>]`: 아이콘은 바이트 배열인 64비트 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-177">`[RawIcon <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>
  - <span data-ttu-id="5742c-178">`[RawPng <Byte[]>]`: 아이콘은 바이트 배열인 64비트 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-178">`[RawPng <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>

<span data-ttu-id="5742c-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: 패키지 종속성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span></span> 
  - <span data-ttu-id="5742c-180">`[DependencyName <String>]`: 패키지 종속성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-180">`[DependencyName <String>]`: Name of package dependency.</span></span>
  - <span data-ttu-id="5742c-181">`[MinVersion <String>]`: 종속성 버전이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-181">`[MinVersion <String>]`: Dependency version required.</span></span>
  - <span data-ttu-id="5742c-182">`[Publisher <String>]`: 종속성 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5742c-182">`[Publisher <String>]`: Name of dependency publisher.</span></span>

## <span data-ttu-id="5742c-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5742c-183">RELATED LINKS</span></span>
