---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
ms.openlocfilehash: 45e2c822bc21acfe69296f8d784a3a707dc1797f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180764"
---
# <span data-ttu-id="034cb-101">Remove-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="034cb-101">Remove-AzWvdMsixPackage</span></span>

## <span data-ttu-id="034cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="034cb-102">SYNOPSIS</span></span>
<span data-ttu-id="034cb-103">MSIX 패키지를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="034cb-103">Remove an MSIX Package.</span></span>

## <span data-ttu-id="034cb-104">구문</span><span class="sxs-lookup"><span data-stu-id="034cb-104">SYNTAX</span></span>

### <span data-ttu-id="034cb-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="034cb-105">Delete (Default)</span></span>
```
Remove-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="034cb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="034cb-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="034cb-107">설명</span><span class="sxs-lookup"><span data-stu-id="034cb-107">DESCRIPTION</span></span>
<span data-ttu-id="034cb-108">MSIX 패키지를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="034cb-108">Remove an MSIX Package.</span></span>

## <span data-ttu-id="034cb-109">예제</span><span class="sxs-lookup"><span data-stu-id="034cb-109">EXAMPLES</span></span>

### <span data-ttu-id="034cb-110">예제 1: 패키지 전체 이름으로 MSIX 패키지 삭제</span><span class="sxs-lookup"><span data-stu-id="034cb-110">Example 1: Delete MSIX Package by Package Full Name</span></span>
```powershell
PS C:\> Remove-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName
```

<span data-ttu-id="034cb-111">이 명령은 HostPool에서 MSIX 패키지를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="034cb-111">This command deletes a MSIX Package in a HostPool</span></span>

## <span data-ttu-id="034cb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="034cb-112">PARAMETERS</span></span>

### <span data-ttu-id="034cb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="034cb-113">-DefaultProfile</span></span>
<span data-ttu-id="034cb-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="034cb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="034cb-115">-FullName</span><span class="sxs-lookup"><span data-stu-id="034cb-115">-FullName</span></span>
<span data-ttu-id="034cb-116">지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="034cb-116">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="034cb-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="034cb-117">-HostPoolName</span></span>
<span data-ttu-id="034cb-118">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="034cb-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="034cb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="034cb-119">-InputObject</span></span>
<span data-ttu-id="034cb-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="034cb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="034cb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="034cb-121">-PassThru</span></span>
<span data-ttu-id="034cb-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="034cb-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="034cb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="034cb-123">-ResourceGroupName</span></span>
<span data-ttu-id="034cb-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="034cb-124">The name of the resource group.</span></span>
<span data-ttu-id="034cb-125">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="034cb-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="034cb-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="034cb-126">-SubscriptionId</span></span>
<span data-ttu-id="034cb-127">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="034cb-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="034cb-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="034cb-128">-Confirm</span></span>
<span data-ttu-id="034cb-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="034cb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="034cb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="034cb-130">-WhatIf</span></span>
<span data-ttu-id="034cb-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="034cb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="034cb-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="034cb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="034cb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="034cb-133">CommonParameters</span></span>
<span data-ttu-id="034cb-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="034cb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="034cb-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="034cb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="034cb-136">입력</span><span class="sxs-lookup"><span data-stu-id="034cb-136">INPUTS</span></span>

### <span data-ttu-id="034cb-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="034cb-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="034cb-138">출력</span><span class="sxs-lookup"><span data-stu-id="034cb-138">OUTPUTS</span></span>

### <span data-ttu-id="034cb-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="034cb-139">System.Boolean</span></span>

## <span data-ttu-id="034cb-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="034cb-140">NOTES</span></span>

<span data-ttu-id="034cb-141">별칭</span><span class="sxs-lookup"><span data-stu-id="034cb-141">ALIASES</span></span>

<span data-ttu-id="034cb-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="034cb-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="034cb-143">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="034cb-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="034cb-144">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="034cb-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="034cb-145">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="034cb-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="034cb-146">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="034cb-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="034cb-147">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="034cb-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="034cb-148">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="034cb-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="034cb-149">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="034cb-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="034cb-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="034cb-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="034cb-151">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="034cb-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="034cb-152">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="034cb-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="034cb-153">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="034cb-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="034cb-154">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="034cb-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="034cb-155">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="034cb-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="034cb-156">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="034cb-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="034cb-157">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="034cb-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="034cb-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="034cb-158">RELATED LINKS</span></span>

