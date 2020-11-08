---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: ab1f338be9d983efceac0045fec96b1a63fb66bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217485"
---
# <span data-ttu-id="8cd86-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="8cd86-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="8cd86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cd86-102">SYNOPSIS</span></span>
<span data-ttu-id="8cd86-103">ApplicationGroup을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="8cd86-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8cd86-104">SYNTAX</span></span>

### <span data-ttu-id="8cd86-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8cd86-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8cd86-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8cd86-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8cd86-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8cd86-107">DESCRIPTION</span></span>
<span data-ttu-id="8cd86-108">ApplicationGroup을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="8cd86-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8cd86-109">EXAMPLES</span></span>

### <span data-ttu-id="8cd86-110">예제 1: 이름별로 Windows 가상 데스크톱 ApplicationGroup 만들기</span><span class="sxs-lookup"><span data-stu-id="8cd86-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="8cd86-111">이 명령은 리소스 그룹에 Windows 가상 데스크톱 ApplicationGroup을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="8cd86-112">변수</span><span class="sxs-lookup"><span data-stu-id="8cd86-112">PARAMETERS</span></span>

### <span data-ttu-id="8cd86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cd86-113">-DefaultProfile</span></span>
<span data-ttu-id="8cd86-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cd86-115">-설명</span><span class="sxs-lookup"><span data-stu-id="8cd86-115">-Description</span></span>
<span data-ttu-id="8cd86-116">ApplicationGroup에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="8cd86-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8cd86-117">-FriendlyName</span></span>
<span data-ttu-id="8cd86-118">ApplicationGroup의 식별 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="8cd86-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cd86-119">-InputObject</span></span>
<span data-ttu-id="8cd86-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cd86-121">-이름</span><span class="sxs-lookup"><span data-stu-id="8cd86-121">-Name</span></span>
<span data-ttu-id="8cd86-122">응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-122">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cd86-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cd86-123">-ResourceGroupName</span></span>
<span data-ttu-id="8cd86-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-124">The name of the resource group.</span></span>
<span data-ttu-id="8cd86-125">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cd86-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8cd86-126">-SubscriptionId</span></span>
<span data-ttu-id="8cd86-127">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cd86-128">태그</span><span class="sxs-lookup"><span data-stu-id="8cd86-128">-Tag</span></span>
<span data-ttu-id="8cd86-129">업데이트할 태그</span><span class="sxs-lookup"><span data-stu-id="8cd86-129">tags to be updated</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cd86-130">-확인</span><span class="sxs-lookup"><span data-stu-id="8cd86-130">-Confirm</span></span>
<span data-ttu-id="8cd86-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cd86-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cd86-132">-WhatIf</span></span>
<span data-ttu-id="8cd86-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cd86-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cd86-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cd86-135">CommonParameters</span></span>
<span data-ttu-id="8cd86-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cd86-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8cd86-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cd86-138">입력</span><span class="sxs-lookup"><span data-stu-id="8cd86-138">INPUTS</span></span>

### <span data-ttu-id="8cd86-139">IDesktopVirtualizationIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="8cd86-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8cd86-140">출력</span><span class="sxs-lookup"><span data-stu-id="8cd86-140">OUTPUTS</span></span>

### <span data-ttu-id="8cd86-141">Api20191210Preview. i i PowerShell. i i m. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="8cd86-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="8cd86-142">상속자</span><span class="sxs-lookup"><span data-stu-id="8cd86-142">NOTES</span></span>

<span data-ttu-id="8cd86-143">별칭과</span><span class="sxs-lookup"><span data-stu-id="8cd86-143">ALIASES</span></span>

<span data-ttu-id="8cd86-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8cd86-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8cd86-145">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8cd86-146">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="8cd86-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8cd86-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8cd86-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8cd86-148">`[ApplicationGroupName <String>]`: 응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8cd86-149">`[ApplicationName <String>]`: 지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8cd86-150">`[DesktopName <String>]`: 지정 된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="8cd86-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8cd86-151">`[HostPoolName <String>]`: 지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8cd86-152">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="8cd86-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8cd86-153">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8cd86-154">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="8cd86-155">`[SessionHostName <String>]`: 지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8cd86-156">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8cd86-157">`[UserSessionId <String>]`: 지정 된 세션 호스트 내에 있는 사용자 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cd86-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8cd86-158">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="8cd86-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="8cd86-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8cd86-159">RELATED LINKS</span></span>

