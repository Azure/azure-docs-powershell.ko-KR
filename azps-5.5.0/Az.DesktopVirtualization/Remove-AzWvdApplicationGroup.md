---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
ms.openlocfilehash: 59ff3c3bd973e3b2189e7f06cd067eaca42870f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204237"
---
# <span data-ttu-id="0d26b-101">Remove-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="0d26b-101">Remove-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="0d26b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d26b-102">SYNOPSIS</span></span>
<span data-ttu-id="0d26b-103">applicationGroup을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0d26b-103">Remove an applicationGroup.</span></span>

## <span data-ttu-id="0d26b-104">구문</span><span class="sxs-lookup"><span data-stu-id="0d26b-104">SYNTAX</span></span>

### <span data-ttu-id="0d26b-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="0d26b-105">Delete (Default)</span></span>
```
Remove-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0d26b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0d26b-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0d26b-107">설명</span><span class="sxs-lookup"><span data-stu-id="0d26b-107">DESCRIPTION</span></span>
<span data-ttu-id="0d26b-108">applicationGroup을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0d26b-108">Remove an applicationGroup.</span></span>

## <span data-ttu-id="0d26b-109">예제</span><span class="sxs-lookup"><span data-stu-id="0d26b-109">EXAMPLES</span></span>

### <span data-ttu-id="0d26b-110">예제 1: 이름으로 Windows Virtual Desktop ApplicationGroup 삭제</span><span class="sxs-lookup"><span data-stu-id="0d26b-110">Example 1: Delete a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName
```

<span data-ttu-id="0d26b-111">이 명령은 리소스 그룹에서 Windows Virtual Desktop ApplicationGroup을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="0d26b-111">This command deletes a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="0d26b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d26b-112">PARAMETERS</span></span>

### <span data-ttu-id="0d26b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d26b-113">-DefaultProfile</span></span>
<span data-ttu-id="0d26b-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d26b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d26b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d26b-115">-InputObject</span></span>
<span data-ttu-id="0d26b-116">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="0d26b-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d26b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0d26b-117">-Name</span></span>
<span data-ttu-id="0d26b-118">애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="0d26b-118">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d26b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d26b-119">-PassThru</span></span>
<span data-ttu-id="0d26b-120">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0d26b-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0d26b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d26b-121">-ResourceGroupName</span></span>
<span data-ttu-id="0d26b-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d26b-122">The name of the resource group.</span></span>
<span data-ttu-id="0d26b-123">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="0d26b-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d26b-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d26b-124">-SubscriptionId</span></span>
<span data-ttu-id="0d26b-125">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0d26b-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d26b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d26b-126">-Confirm</span></span>
<span data-ttu-id="0d26b-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d26b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d26b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d26b-128">-WhatIf</span></span>
<span data-ttu-id="0d26b-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0d26b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d26b-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d26b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d26b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d26b-131">CommonParameters</span></span>
<span data-ttu-id="0d26b-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0d26b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d26b-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0d26b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d26b-134">입력</span><span class="sxs-lookup"><span data-stu-id="0d26b-134">INPUTS</span></span>

### <span data-ttu-id="0d26b-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="0d26b-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="0d26b-136">출력</span><span class="sxs-lookup"><span data-stu-id="0d26b-136">OUTPUTS</span></span>

### <span data-ttu-id="0d26b-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0d26b-137">System.Boolean</span></span>

## <span data-ttu-id="0d26b-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0d26b-138">NOTES</span></span>

<span data-ttu-id="0d26b-139">별칭</span><span class="sxs-lookup"><span data-stu-id="0d26b-139">ALIASES</span></span>

<span data-ttu-id="0d26b-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="0d26b-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0d26b-141">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0d26b-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0d26b-142">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0d26b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0d26b-143">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0d26b-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0d26b-144">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="0d26b-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="0d26b-145">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="0d26b-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="0d26b-146">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="0d26b-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="0d26b-147">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="0d26b-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="0d26b-148">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="0d26b-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0d26b-149">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="0d26b-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="0d26b-150">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d26b-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0d26b-151">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="0d26b-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="0d26b-152">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="0d26b-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="0d26b-153">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0d26b-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0d26b-154">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="0d26b-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="0d26b-155">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="0d26b-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="0d26b-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d26b-156">RELATED LINKS</span></span>

