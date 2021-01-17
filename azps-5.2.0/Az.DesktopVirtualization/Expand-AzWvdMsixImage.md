---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: 417acf03af2bf73d57759841bacc3ed532e8f043
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348158"
---
# <span data-ttu-id="5ed0f-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="5ed0f-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="5ed0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ed0f-102">SYNOPSIS</span></span>
<span data-ttu-id="5ed0f-103">이미지 경로가 제공된 이미지에서 MSIX 패키지를 확장하고 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="5ed0f-104">구문</span><span class="sxs-lookup"><span data-stu-id="5ed0f-104">SYNTAX</span></span>

### <span data-ttu-id="5ed0f-105">ExpandExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="5ed0f-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5ed0f-106">확장</span><span class="sxs-lookup"><span data-stu-id="5ed0f-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5ed0f-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5ed0f-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5ed0f-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5ed0f-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5ed0f-109">설명</span><span class="sxs-lookup"><span data-stu-id="5ed0f-109">DESCRIPTION</span></span>
<span data-ttu-id="5ed0f-110">이미지 경로가 제공된 이미지에서 MSIX 패키지를 확장하고 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="5ed0f-111">예제</span><span class="sxs-lookup"><span data-stu-id="5ed0f-111">EXAMPLES</span></span>

### <span data-ttu-id="5ed0f-112">예제 1: 지정된 이미지 경로를 확장하고 지정된 이미지 경로에 있는 패키지 메타데이터를 AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="5ed0f-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="5ed0f-113">이 명령은 주어진 이미지 경로에 있는 MSIX 패키지의 메타데이터를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="5ed0f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ed0f-114">PARAMETERS</span></span>

### <span data-ttu-id="5ed0f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ed0f-115">-DefaultProfile</span></span>
<span data-ttu-id="5ed0f-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ed0f-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="5ed0f-117">-HostPoolName</span></span>
<span data-ttu-id="5ed0f-118">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="5ed0f-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="5ed0f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ed0f-119">-InputObject</span></span>
<span data-ttu-id="5ed0f-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5ed0f-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="5ed0f-121">-MsixImageUri</span></span>
<span data-ttu-id="5ed0f-122">생성할 MSIX 이미지를 참조하는 URI를 나타내고 MSIXIMAGEURI 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixImageUri
Parameter Sets: Expand, ExpandViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ed0f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ed0f-123">-ResourceGroupName</span></span>
<span data-ttu-id="5ed0f-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-124">The name of the resource group.</span></span>
<span data-ttu-id="5ed0f-125">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5ed0f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ed0f-126">-SubscriptionId</span></span>
<span data-ttu-id="5ed0f-127">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5ed0f-128">-Uri</span><span class="sxs-lookup"><span data-stu-id="5ed0f-128">-Uri</span></span>
<span data-ttu-id="5ed0f-129">이미지에 대한 URI</span><span class="sxs-lookup"><span data-stu-id="5ed0f-129">URI to Image</span></span>

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

### <span data-ttu-id="5ed0f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ed0f-130">-Confirm</span></span>
<span data-ttu-id="5ed0f-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ed0f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ed0f-132">-WhatIf</span></span>
<span data-ttu-id="5ed0f-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5ed0f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ed0f-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ed0f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ed0f-135">CommonParameters</span></span>
<span data-ttu-id="5ed0f-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ed0f-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ed0f-138">입력</span><span class="sxs-lookup"><span data-stu-id="5ed0f-138">INPUTS</span></span>

### <span data-ttu-id="5ed0f-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="5ed0f-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixImageUri</span></span>

### <span data-ttu-id="5ed0f-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="5ed0f-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="5ed0f-141">출력</span><span class="sxs-lookup"><span data-stu-id="5ed0f-141">OUTPUTS</span></span>

### <span data-ttu-id="5ed0f-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="5ed0f-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="5ed0f-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5ed0f-143">NOTES</span></span>

<span data-ttu-id="5ed0f-144">별칭</span><span class="sxs-lookup"><span data-stu-id="5ed0f-144">ALIASES</span></span>

<span data-ttu-id="5ed0f-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="5ed0f-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5ed0f-146">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ed0f-147">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5ed0f-148">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5ed0f-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5ed0f-149">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="5ed0f-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="5ed0f-150">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="5ed0f-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="5ed0f-151">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="5ed0f-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="5ed0f-152">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="5ed0f-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="5ed0f-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="5ed0f-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5ed0f-154">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="5ed0f-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="5ed0f-155">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5ed0f-156">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="5ed0f-157">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="5ed0f-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="5ed0f-158">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5ed0f-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5ed0f-159">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="5ed0f-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="5ed0f-160">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="5ed0f-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="5ed0f-161">MSIXIMAGEURI: MSIX 이미지를 <IMsixImageUri> 참조하는 URI를 나타임</span><span class="sxs-lookup"><span data-stu-id="5ed0f-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="5ed0f-162">`[Uri <String>]`: 이미지에 대한 URI</span><span class="sxs-lookup"><span data-stu-id="5ed0f-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="5ed0f-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ed0f-163">RELATED LINKS</span></span>

