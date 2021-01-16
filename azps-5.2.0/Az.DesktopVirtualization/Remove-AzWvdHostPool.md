---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
ms.openlocfilehash: 65e7d5870e03d4e2d103254aec7a44835286d5df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338469"
---
# <span data-ttu-id="b5857-101">Remove-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="b5857-101">Remove-AzWvdHostPool</span></span>

## <span data-ttu-id="b5857-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5857-102">SYNOPSIS</span></span>
<span data-ttu-id="b5857-103">호스트 풀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b5857-103">Remove a host pool.</span></span>

## <span data-ttu-id="b5857-104">구문</span><span class="sxs-lookup"><span data-stu-id="b5857-104">SYNTAX</span></span>

### <span data-ttu-id="b5857-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="b5857-105">Delete (Default)</span></span>
```
Remove-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b5857-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b5857-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b5857-107">설명</span><span class="sxs-lookup"><span data-stu-id="b5857-107">DESCRIPTION</span></span>
<span data-ttu-id="b5857-108">호스트 풀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b5857-108">Remove a host pool.</span></span>

## <span data-ttu-id="b5857-109">예제</span><span class="sxs-lookup"><span data-stu-id="b5857-109">EXAMPLES</span></span>

### <span data-ttu-id="b5857-110">예제 1: 이름으로 Windows Virtual Desktop HostPool 삭제</span><span class="sxs-lookup"><span data-stu-id="b5857-110">Example 1: Delete a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Remove-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName
```

<span data-ttu-id="b5857-111">이 명령은 리소스 그룹에서 Windows Virtual Desktop HostPool을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b5857-111">This command deletes a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="b5857-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5857-112">PARAMETERS</span></span>

### <span data-ttu-id="b5857-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5857-113">-DefaultProfile</span></span>
<span data-ttu-id="b5857-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5857-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5857-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b5857-115">-Force</span></span>
<span data-ttu-id="b5857-116">플래그를 강제로 지정하여 sessionHost를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b5857-116">Force flag to delete sessionHost.</span></span>

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

### <span data-ttu-id="b5857-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5857-117">-InputObject</span></span>
<span data-ttu-id="b5857-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b5857-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b5857-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b5857-119">-Name</span></span>
<span data-ttu-id="b5857-120">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="b5857-120">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5857-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5857-121">-PassThru</span></span>
<span data-ttu-id="b5857-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b5857-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b5857-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5857-123">-ResourceGroupName</span></span>
<span data-ttu-id="b5857-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b5857-124">The name of the resource group.</span></span>
<span data-ttu-id="b5857-125">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="b5857-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b5857-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5857-126">-SubscriptionId</span></span>
<span data-ttu-id="b5857-127">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b5857-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b5857-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5857-128">-Confirm</span></span>
<span data-ttu-id="b5857-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5857-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5857-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5857-130">-WhatIf</span></span>
<span data-ttu-id="b5857-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b5857-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5857-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5857-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5857-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5857-133">CommonParameters</span></span>
<span data-ttu-id="b5857-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b5857-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5857-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b5857-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5857-136">입력</span><span class="sxs-lookup"><span data-stu-id="b5857-136">INPUTS</span></span>

### <span data-ttu-id="b5857-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b5857-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b5857-138">출력</span><span class="sxs-lookup"><span data-stu-id="b5857-138">OUTPUTS</span></span>

### <span data-ttu-id="b5857-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b5857-139">System.Boolean</span></span>

## <span data-ttu-id="b5857-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b5857-140">NOTES</span></span>

<span data-ttu-id="b5857-141">별칭</span><span class="sxs-lookup"><span data-stu-id="b5857-141">ALIASES</span></span>

<span data-ttu-id="b5857-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b5857-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b5857-143">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b5857-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b5857-144">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b5857-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b5857-145">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b5857-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b5857-146">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="b5857-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b5857-147">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="b5857-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b5857-148">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="b5857-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b5857-149">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="b5857-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b5857-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="b5857-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b5857-151">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="b5857-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="b5857-152">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b5857-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b5857-153">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="b5857-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="b5857-154">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="b5857-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b5857-155">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b5857-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b5857-156">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="b5857-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b5857-157">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="b5857-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b5857-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5857-158">RELATED LINKS</span></span>

