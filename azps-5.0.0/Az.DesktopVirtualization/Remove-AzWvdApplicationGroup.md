---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
ms.openlocfilehash: 6c885f4962734bf1034256843258f4755a9b3b44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304751"
---
# <span data-ttu-id="477c1-101">Remove-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="477c1-101">Remove-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="477c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="477c1-102">SYNOPSIS</span></span>
<span data-ttu-id="477c1-103">ApplicationGroup을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-103">Remove an applicationGroup.</span></span>

## <span data-ttu-id="477c1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="477c1-104">SYNTAX</span></span>

### <span data-ttu-id="477c1-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="477c1-105">Delete (Default)</span></span>
```
Remove-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="477c1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="477c1-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="477c1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="477c1-107">DESCRIPTION</span></span>
<span data-ttu-id="477c1-108">ApplicationGroup을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-108">Remove an applicationGroup.</span></span>

## <span data-ttu-id="477c1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="477c1-109">EXAMPLES</span></span>

### <span data-ttu-id="477c1-110">예제 1: 이름으로 Windows 가상 데스크톱 ApplicationGroup을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-110">Example 1: Delete a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName
```

<span data-ttu-id="477c1-111">이 명령은 리소스 그룹에서 Windows 가상 데스크톱 ApplicationGroup을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-111">This command deletes a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="477c1-112">변수</span><span class="sxs-lookup"><span data-stu-id="477c1-112">PARAMETERS</span></span>

### <span data-ttu-id="477c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="477c1-113">-DefaultProfile</span></span>
<span data-ttu-id="477c1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="477c1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="477c1-115">-InputObject</span></span>
<span data-ttu-id="477c1-116">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="477c1-117">-이름</span><span class="sxs-lookup"><span data-stu-id="477c1-117">-Name</span></span>
<span data-ttu-id="477c1-118">응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-118">The name of the application group</span></span>

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

### <span data-ttu-id="477c1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="477c1-119">-PassThru</span></span>
<span data-ttu-id="477c1-120">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="477c1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="477c1-121">-ResourceGroupName</span></span>
<span data-ttu-id="477c1-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-122">The name of the resource group.</span></span>
<span data-ttu-id="477c1-123">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="477c1-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="477c1-124">-SubscriptionId</span></span>
<span data-ttu-id="477c1-125">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="477c1-126">-확인</span><span class="sxs-lookup"><span data-stu-id="477c1-126">-Confirm</span></span>
<span data-ttu-id="477c1-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="477c1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="477c1-128">-WhatIf</span></span>
<span data-ttu-id="477c1-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="477c1-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="477c1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="477c1-131">CommonParameters</span></span>
<span data-ttu-id="477c1-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="477c1-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="477c1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="477c1-134">입력</span><span class="sxs-lookup"><span data-stu-id="477c1-134">INPUTS</span></span>

### <span data-ttu-id="477c1-135">IDesktopVirtualizationIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="477c1-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="477c1-136">출력</span><span class="sxs-lookup"><span data-stu-id="477c1-136">OUTPUTS</span></span>

### <span data-ttu-id="477c1-137">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="477c1-137">System.Boolean</span></span>

## <span data-ttu-id="477c1-138">상속자</span><span class="sxs-lookup"><span data-stu-id="477c1-138">NOTES</span></span>

<span data-ttu-id="477c1-139">별칭과</span><span class="sxs-lookup"><span data-stu-id="477c1-139">ALIASES</span></span>

<span data-ttu-id="477c1-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="477c1-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="477c1-141">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="477c1-142">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="477c1-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="477c1-143">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="477c1-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="477c1-144">`[ApplicationGroupName <String>]`: 응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="477c1-145">`[ApplicationName <String>]`: 지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="477c1-146">`[DesktopName <String>]`: 지정 된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="477c1-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="477c1-147">`[HostPoolName <String>]`: 지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="477c1-148">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="477c1-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="477c1-149">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="477c1-150">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="477c1-151">`[SessionHostName <String>]`: 지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="477c1-152">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="477c1-153">`[UserSessionId <String>]`: 지정 된 세션 호스트 내에 있는 사용자 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="477c1-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="477c1-154">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="477c1-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="477c1-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="477c1-155">RELATED LINKS</span></span>

