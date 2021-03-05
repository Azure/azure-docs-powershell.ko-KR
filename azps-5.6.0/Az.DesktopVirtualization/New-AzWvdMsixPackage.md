---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
ms.openlocfilehash: ecb5b1200bacab12f7715600b7fcf60b78b81092
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966144"
---
# <span data-ttu-id="3fabb-101">New-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="3fabb-101">New-AzWvdMsixPackage</span></span>

## <span data-ttu-id="3fabb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fabb-102">SYNOPSIS</span></span>
<span data-ttu-id="3fabb-103">MSIX 패키지를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-103">Create or update a MSIX package.</span></span>

## <span data-ttu-id="3fabb-104">구문</span><span class="sxs-lookup"><span data-stu-id="3fabb-104">SYNTAX</span></span>

### <span data-ttu-id="3fabb-105">CreateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="3fabb-105">CreateExpanded (Default)</span></span>
```
New-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-LastUpdated <DateTime>] [-PackageApplication <IMsixPackageApplications[]>]
 [-PackageDependency <IMsixPackageDependencies[]>] [-PackageFamilyName <String>] [-PackageName <String>]
 [-PackageRelativePath <String>] [-Version <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3fabb-106">PackageAlias</span><span class="sxs-lookup"><span data-stu-id="3fabb-106">PackageAlias</span></span>
```
New-AzWvdMsixPackage -HostPoolName <String> -PackageAlias <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3fabb-107">설명</span><span class="sxs-lookup"><span data-stu-id="3fabb-107">DESCRIPTION</span></span>
<span data-ttu-id="3fabb-108">MSIX 패키지를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-108">Create or update a MSIX package.</span></span>

## <span data-ttu-id="3fabb-109">예제</span><span class="sxs-lookup"><span data-stu-id="3fabb-109">EXAMPLES</span></span>

### <span data-ttu-id="3fabb-110">예제 1: 패키지 별칭을 통해 HostPool에 새 MSIX 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-110">Example 1: Creates New MSIX Package in the HostPool via Package Alias</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
      -PackageAlias packagealias `
      -ImagePath ImagePathURI  `
```

<span data-ttu-id="3fabb-111">이 명령은 지정된 이미지 경로에서 HostPool에 MSIX 패키지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-111">This command adds MSIX package from specified image path to HostPool</span></span>

### <span data-ttu-id="3fabb-112">예제 2: HostPool에서 새 MSIX 패키지를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-112">Example 2: Creates New MSIX Package in the HostPool</span></span>
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

<span data-ttu-id="3fabb-113">이 명령은 지정된 HostPool에 MSIX 패키지를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-113">This command adds MSIX Package in the specified HostPool</span></span>

## <span data-ttu-id="3fabb-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3fabb-114">PARAMETERS</span></span>

### <span data-ttu-id="3fabb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fabb-115">-DefaultProfile</span></span>
<span data-ttu-id="3fabb-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fabb-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3fabb-117">-DisplayName</span></span>
<span data-ttu-id="3fabb-118">포털에 표시할 사용자 친화적인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-118">User friendly Name to be displayed in the portal.</span></span>

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

### <span data-ttu-id="3fabb-119">-FullName</span><span class="sxs-lookup"><span data-stu-id="3fabb-119">-FullName</span></span>
<span data-ttu-id="3fabb-120">지정된 호스트풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="3fabb-120">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="3fabb-121">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="3fabb-121">-HostPoolName</span></span>
<span data-ttu-id="3fabb-122">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="3fabb-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="3fabb-123">-ImagePath</span><span class="sxs-lookup"><span data-stu-id="3fabb-123">-ImagePath</span></span>
<span data-ttu-id="3fabb-124">네트워크 공유의 VHD/CIM 이미지 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-124">VHD/CIM image path on Network Share.</span></span>

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

### <span data-ttu-id="3fabb-125">-IsActive</span><span class="sxs-lookup"><span data-stu-id="3fabb-125">-IsActive</span></span>
<span data-ttu-id="3fabb-126">호스트풀에서 이 버전의 패키지를 활성 패키지로 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-126">Make this version of the package the active one across the hostpool.</span></span>

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

### <span data-ttu-id="3fabb-127">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="3fabb-127">-IsRegularRegistration</span></span>
<span data-ttu-id="3fabb-128">피드에 패키지를 등록하는 방법을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-128">Specifies how to register Package in feed.</span></span>

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

### <span data-ttu-id="3fabb-129">-LastUpdated</span><span class="sxs-lookup"><span data-stu-id="3fabb-129">-LastUpdated</span></span>
<span data-ttu-id="3fabb-130">날짜 패키지가 마지막으로 업데이트되었습니다. 이 패키지는 appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="3fabb-130">Date Package was last updated, found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="3fabb-131">-PackageAlias</span><span class="sxs-lookup"><span data-stu-id="3fabb-131">-PackageAlias</span></span>
<span data-ttu-id="3fabb-132">MSIX 이미지 추출에서 별칭 패키지</span><span class="sxs-lookup"><span data-stu-id="3fabb-132">Package Alias from extract MSIX Image</span></span>

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

### <span data-ttu-id="3fabb-133">-PackageApplication</span><span class="sxs-lookup"><span data-stu-id="3fabb-133">-PackageApplication</span></span>
<span data-ttu-id="3fabb-134">패키지 애플리케이션 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-134">List of package applications.</span></span>

<span data-ttu-id="3fabb-135">생성을 위해 PACKAGEAPPLICATION 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="3fabb-135">To construct, see NOTES section for PACKAGEAPPLICATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackageApplications[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fabb-136">-PackageDependency</span><span class="sxs-lookup"><span data-stu-id="3fabb-136">-PackageDependency</span></span>
<span data-ttu-id="3fabb-137">패키지 종속성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-137">List of package dependencies.</span></span>

<span data-ttu-id="3fabb-138">생성을 위해 PACKAGEDEPENDENCY 속성에 대한 메모 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="3fabb-138">To construct, see NOTES section for PACKAGEDEPENDENCY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackageDependencies[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fabb-139">-PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="3fabb-139">-PackageFamilyName</span></span>
<span data-ttu-id="3fabb-140">패키지 패밀리 이름을 appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="3fabb-140">Package Family Name from appxmanifest.xml.</span></span>
<span data-ttu-id="3fabb-141">패키지 이름 및 게시자 이름이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-141">Contains Package Name and Publisher name.</span></span>

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

### <span data-ttu-id="3fabb-142">-PackageName</span><span class="sxs-lookup"><span data-stu-id="3fabb-142">-PackageName</span></span>
<span data-ttu-id="3fabb-143">패키지 이름에서 appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="3fabb-143">Package Name from appxmanifest.xml.</span></span>

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

### <span data-ttu-id="3fabb-144">-PackageRelativePath</span><span class="sxs-lookup"><span data-stu-id="3fabb-144">-PackageRelativePath</span></span>
<span data-ttu-id="3fabb-145">이미지 내부의 패키지에 대한 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-145">Relative Path to the package inside the image.</span></span>

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

### <span data-ttu-id="3fabb-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fabb-146">-ResourceGroupName</span></span>
<span data-ttu-id="3fabb-147">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-147">The name of the resource group.</span></span>
<span data-ttu-id="3fabb-148">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-148">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3fabb-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3fabb-149">-SubscriptionId</span></span>
<span data-ttu-id="3fabb-150">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-150">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3fabb-151">-Version</span><span class="sxs-lookup"><span data-stu-id="3fabb-151">-Version</span></span>
<span data-ttu-id="3fabb-152">패키지 버전은 appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="3fabb-152">Package Version found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="3fabb-153">-확인</span><span class="sxs-lookup"><span data-stu-id="3fabb-153">-Confirm</span></span>
<span data-ttu-id="3fabb-154">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fabb-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fabb-155">-WhatIf</span></span>
<span data-ttu-id="3fabb-156">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fabb-157">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fabb-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fabb-158">CommonParameters</span></span>
<span data-ttu-id="3fabb-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fabb-160">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fabb-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fabb-161">입력</span><span class="sxs-lookup"><span data-stu-id="3fabb-161">INPUTS</span></span>

## <span data-ttu-id="3fabb-162">출력</span><span class="sxs-lookup"><span data-stu-id="3fabb-162">OUTPUTS</span></span>

### <span data-ttu-id="3fabb-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="3fabb-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="3fabb-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3fabb-164">NOTES</span></span>

<span data-ttu-id="3fabb-165">별칭</span><span class="sxs-lookup"><span data-stu-id="3fabb-165">ALIASES</span></span>

<span data-ttu-id="3fabb-166">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="3fabb-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3fabb-167">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3fabb-168">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3fabb-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3fabb-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: 패키지 애플리케이션 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: List of package applications.</span></span> 
  - <span data-ttu-id="3fabb-170">`[AppId <String>]`: 패키지 애플리케이션 id( appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="3fabb-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="3fabb-171">`[AppUserModelId <String>]`: 패키지 애플리케이션을 활성화하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-171">`[AppUserModelId <String>]`: Used to activate Package Application.</span></span> <span data-ttu-id="3fabb-172">패키지 이름 및 ApplicationID로 구성됩니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-172">Consists of Package Name and ApplicationID.</span></span> <span data-ttu-id="3fabb-173">에서 appxmanifest.xml.</span><span class="sxs-lookup"><span data-stu-id="3fabb-173">Found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="3fabb-174">`[Description <String>]`: 패키지 애플리케이션에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-174">`[Description <String>]`: Description of Package Application.</span></span>
  - <span data-ttu-id="3fabb-175">`[FriendlyName <String>]`: 사용자 친화적인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-175">`[FriendlyName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="3fabb-176">`[IconImageName <String>]`: 사용자 친화적인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-176">`[IconImageName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="3fabb-177">`[RawIcon <Byte[]>]`: 64비트 문자열을 바이트 배열로 아이콘합니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-177">`[RawIcon <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>
  - <span data-ttu-id="3fabb-178">`[RawPng <Byte[]>]`: 64비트 문자열을 바이트 배열로 아이콘합니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-178">`[RawPng <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>

<span data-ttu-id="3fabb-179">PACKAGEDEPENDENCY <PackageDependencies[]>: 패키지 종속성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span></span> 
  - <span data-ttu-id="3fabb-180">`[DependencyName <String>]`: 패키지 종속성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-180">`[DependencyName <String>]`: Name of package dependency.</span></span>
  - <span data-ttu-id="3fabb-181">`[MinVersion <String>]`: 종속성 버전이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-181">`[MinVersion <String>]`: Dependency version required.</span></span>
  - <span data-ttu-id="3fabb-182">`[Publisher <String>]`: 종속성 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3fabb-182">`[Publisher <String>]`: Name of dependency publisher.</span></span>

## <span data-ttu-id="3fabb-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3fabb-183">RELATED LINKS</span></span>

