---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: 56122e8d1ae94b6a898c073f2b2f2fb891504789
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387311"
---
# <span data-ttu-id="b8d26-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="b8d26-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="b8d26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8d26-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d26-103">이미지 경로가 제공된 이미지에서 MSIX 패키지를 확장하고 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d26-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="b8d26-104">구문</span><span class="sxs-lookup"><span data-stu-id="b8d26-104">SYNTAX</span></span>

### <span data-ttu-id="b8d26-105">ExpandExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="b8d26-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b8d26-106">확장</span><span class="sxs-lookup"><span data-stu-id="b8d26-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b8d26-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b8d26-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b8d26-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b8d26-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b8d26-109">설명</span><span class="sxs-lookup"><span data-stu-id="b8d26-109">DESCRIPTION</span></span>
<span data-ttu-id="b8d26-110">이미지 경로가 제공된 이미지에서 MSIX 패키지를 확장하고 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d26-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="b8d26-111">예제</span><span class="sxs-lookup"><span data-stu-id="b8d26-111">EXAMPLES</span></span>

### <span data-ttu-id="b8d26-112">예제 1: 지정된 이미지 경로를 확장하고 지정된 이미지 경로에 있는 패키지 메타데이터를 AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="b8d26-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="b8d26-113">이 명령은 주어진 이미지 경로에 있는 MSIX 패키지의 메타데이터를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d26-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="b8d26-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8d26-114">PARAMETERS</span></span>

### <span data-ttu-id="b8d26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d26-115">-DefaultProfile</span></span>
<span data-ttu-id="b8d26-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d26-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8d26-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="b8d26-117">-HostPoolName</span></span>
<span data-ttu-id="b8d26-118">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="b8d26-118">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d26-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8d26-119">-InputObject</span></span>
<span data-ttu-id="b8d26-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b8d26-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: ExpandViaIdentity, ExpandViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d26-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="b8d26-121">-MsixImageUri</span></span>
<span data-ttu-id="b8d26-122">생성할 MSIX 이미지를 참조하는 URI를 나타내고 MSIXIMAGEURI 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8d26-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri
Parameter Sets: Expand, ExpandViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d26-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8d26-123">-ResourceGroupName</span></span>
<span data-ttu-id="b8d26-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d26-124">The name of the resource group.</span></span>
<span data-ttu-id="b8d26-125">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d26-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d26-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8d26-126">-SubscriptionId</span></span>
<span data-ttu-id="b8d26-127">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d26-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d26-128">-Uri</span><span class="sxs-lookup"><span data-stu-id="b8d26-128">-Uri</span></span>
<span data-ttu-id="b8d26-129">이미지에 대한 URI</span><span class="sxs-lookup"><span data-stu-id="b8d26-129">URI to Image</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandExpanded, ExpandViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d26-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8d26-130">-Confirm</span></span>
<span data-ttu-id="b8d26-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8d26-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8d26-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8d26-132">-WhatIf</span></span>
<span data-ttu-id="b8d26-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b8d26-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8d26-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8d26-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8d26-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d26-135">CommonParameters</span></span>
<span data-ttu-id="b8d26-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d26-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d26-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b8d26-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d26-138">입력</span><span class="sxs-lookup"><span data-stu-id="b8d26-138">INPUTS</span></span>

### <span data-ttu-id="b8d26-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="b8d26-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span></span>

### <span data-ttu-id="b8d26-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b8d26-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b8d26-141">출력</span><span class="sxs-lookup"><span data-stu-id="b8d26-141">OUTPUTS</span></span>

### <span data-ttu-id="b8d26-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="b8d26-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="b8d26-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b8d26-143">NOTES</span></span>

<span data-ttu-id="b8d26-144">별칭</span><span class="sxs-lookup"><span data-stu-id="b8d26-144">ALIASES</span></span>

<span data-ttu-id="b8d26-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b8d26-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b8d26-146">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d26-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b8d26-147">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b8d26-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b8d26-148">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b8d26-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b8d26-149">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="b8d26-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b8d26-150">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="b8d26-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b8d26-151">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="b8d26-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b8d26-152">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="b8d26-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b8d26-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="b8d26-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b8d26-154">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="b8d26-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="b8d26-155">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d26-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b8d26-156">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d26-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="b8d26-157">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="b8d26-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b8d26-158">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d26-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b8d26-159">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="b8d26-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b8d26-160">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="b8d26-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="b8d26-161">MSIXIMAGEURI: MSIX 이미지를 <IMsixImageUri> 참조하는 URI를 나타임</span><span class="sxs-lookup"><span data-stu-id="b8d26-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="b8d26-162">`[Uri <String>]`: 이미지에 대한 URI</span><span class="sxs-lookup"><span data-stu-id="b8d26-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="b8d26-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8d26-163">RELATED LINKS</span></span>

