---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
ms.openlocfilehash: 420a73dc1890db1b26cff5ca5289dc030666b038
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304733"
---
# <span data-ttu-id="1bd26-101">Remove-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="1bd26-101">Remove-AzWvdWorkspace</span></span>

## <span data-ttu-id="1bd26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bd26-102">SYNOPSIS</span></span>
<span data-ttu-id="1bd26-103">작업 영역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-103">Remove a workspace.</span></span>

## <span data-ttu-id="1bd26-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1bd26-104">SYNTAX</span></span>

### <span data-ttu-id="1bd26-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1bd26-105">Delete (Default)</span></span>
```
Remove-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1bd26-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1bd26-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1bd26-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1bd26-107">DESCRIPTION</span></span>
<span data-ttu-id="1bd26-108">작업 영역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-108">Remove a workspace.</span></span>

## <span data-ttu-id="1bd26-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1bd26-109">EXAMPLES</span></span>

### <span data-ttu-id="1bd26-110">예제 1: Windows 가상 데스크톱 Worksapce 이름으로 삭제</span><span class="sxs-lookup"><span data-stu-id="1bd26-110">Example 1: Delete a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> Remove-AzWvdWorksapce -ResourceGroupName ResourceGroupName -Name WorkspaceName
```

<span data-ttu-id="1bd26-111">이 명령은 리소스 그룹에서 Windows 가상 데스크톱 작업 영역을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-111">This command deletes a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="1bd26-112">변수</span><span class="sxs-lookup"><span data-stu-id="1bd26-112">PARAMETERS</span></span>

### <span data-ttu-id="1bd26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bd26-113">-DefaultProfile</span></span>
<span data-ttu-id="1bd26-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bd26-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bd26-115">-InputObject</span></span>
<span data-ttu-id="1bd26-116">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1bd26-117">-이름</span><span class="sxs-lookup"><span data-stu-id="1bd26-117">-Name</span></span>
<span data-ttu-id="1bd26-118">작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="1bd26-118">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bd26-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bd26-119">-PassThru</span></span>
<span data-ttu-id="1bd26-120">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1bd26-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bd26-121">-ResourceGroupName</span></span>
<span data-ttu-id="1bd26-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-122">The name of the resource group.</span></span>
<span data-ttu-id="1bd26-123">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1bd26-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1bd26-124">-SubscriptionId</span></span>
<span data-ttu-id="1bd26-125">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1bd26-126">-확인</span><span class="sxs-lookup"><span data-stu-id="1bd26-126">-Confirm</span></span>
<span data-ttu-id="1bd26-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bd26-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bd26-128">-WhatIf</span></span>
<span data-ttu-id="1bd26-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bd26-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bd26-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bd26-131">CommonParameters</span></span>
<span data-ttu-id="1bd26-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bd26-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1bd26-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bd26-134">입력</span><span class="sxs-lookup"><span data-stu-id="1bd26-134">INPUTS</span></span>

### <span data-ttu-id="1bd26-135">IDesktopVirtualizationIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="1bd26-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="1bd26-136">출력</span><span class="sxs-lookup"><span data-stu-id="1bd26-136">OUTPUTS</span></span>

### <span data-ttu-id="1bd26-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1bd26-137">System.Boolean</span></span>

## <span data-ttu-id="1bd26-138">상속자</span><span class="sxs-lookup"><span data-stu-id="1bd26-138">NOTES</span></span>

<span data-ttu-id="1bd26-139">별칭과</span><span class="sxs-lookup"><span data-stu-id="1bd26-139">ALIASES</span></span>

<span data-ttu-id="1bd26-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1bd26-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1bd26-141">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1bd26-142">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="1bd26-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1bd26-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1bd26-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1bd26-144">`[ApplicationGroupName <String>]`: 응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="1bd26-145">`[ApplicationName <String>]`: 지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="1bd26-146">`[DesktopName <String>]`: 지정 된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="1bd26-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="1bd26-147">`[HostPoolName <String>]`: 지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="1bd26-148">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="1bd26-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1bd26-149">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1bd26-150">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="1bd26-151">`[SessionHostName <String>]`: 지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="1bd26-152">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1bd26-153">`[UserSessionId <String>]`: 지정 된 세션 호스트 내에 있는 사용자 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1bd26-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="1bd26-154">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="1bd26-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="1bd26-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1bd26-155">RELATED LINKS</span></span>

