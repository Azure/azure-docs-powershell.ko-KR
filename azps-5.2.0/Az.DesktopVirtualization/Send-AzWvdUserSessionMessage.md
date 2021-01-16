---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 5b5e5ba314bee8d6260985c65f46d372cce94258
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338426"
---
# <span data-ttu-id="b6bf3-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="b6bf3-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="b6bf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="b6bf3-103">사용자에게 메시지를 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-103">Send a message to a user.</span></span>

## <span data-ttu-id="b6bf3-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6bf3-104">SYNTAX</span></span>

### <span data-ttu-id="b6bf3-105">SendExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="b6bf3-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b6bf3-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b6bf3-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b6bf3-107">설명</span><span class="sxs-lookup"><span data-stu-id="b6bf3-107">DESCRIPTION</span></span>
<span data-ttu-id="b6bf3-108">사용자에게 메시지를 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-108">Send a message to a user.</span></span>

## <span data-ttu-id="b6bf3-109">예제</span><span class="sxs-lookup"><span data-stu-id="b6bf3-109">EXAMPLES</span></span>

### <span data-ttu-id="b6bf3-110">예제 1: UserSession에 메시지 보내기</span><span class="sxs-lookup"><span data-stu-id="b6bf3-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="b6bf3-111">이 명령은 UserSession에 메시지를 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="b6bf3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6bf3-112">PARAMETERS</span></span>

### <span data-ttu-id="b6bf3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6bf3-113">-DefaultProfile</span></span>
<span data-ttu-id="b6bf3-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6bf3-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="b6bf3-115">-HostPoolName</span></span>
<span data-ttu-id="b6bf3-116">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="b6bf3-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6bf3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6bf3-117">-InputObject</span></span>
<span data-ttu-id="b6bf3-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: SendViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6bf3-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="b6bf3-119">-MessageBody</span></span>
<span data-ttu-id="b6bf3-120">메시지 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-120">Body of message.</span></span>

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

### <span data-ttu-id="b6bf3-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="b6bf3-121">-MessageTitle</span></span>
<span data-ttu-id="b6bf3-122">메시지의 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-122">Title of message.</span></span>

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

### <span data-ttu-id="b6bf3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6bf3-123">-PassThru</span></span>
<span data-ttu-id="b6bf3-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b6bf3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6bf3-125">-ResourceGroupName</span></span>
<span data-ttu-id="b6bf3-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-126">The name of the resource group.</span></span>
<span data-ttu-id="b6bf3-127">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6bf3-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="b6bf3-128">-SessionHostName</span></span>
<span data-ttu-id="b6bf3-129">지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="b6bf3-129">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6bf3-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6bf3-130">-SubscriptionId</span></span>
<span data-ttu-id="b6bf3-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6bf3-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="b6bf3-132">-UserSessionId</span></span>
<span data-ttu-id="b6bf3-133">지정된 세션 호스트 내의 사용자 세션 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-133">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6bf3-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6bf3-134">-Confirm</span></span>
<span data-ttu-id="b6bf3-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6bf3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6bf3-136">-WhatIf</span></span>
<span data-ttu-id="b6bf3-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b6bf3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6bf3-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6bf3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6bf3-139">CommonParameters</span></span>
<span data-ttu-id="b6bf3-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6bf3-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6bf3-142">입력</span><span class="sxs-lookup"><span data-stu-id="b6bf3-142">INPUTS</span></span>

### <span data-ttu-id="b6bf3-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b6bf3-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b6bf3-144">출력</span><span class="sxs-lookup"><span data-stu-id="b6bf3-144">OUTPUTS</span></span>

### <span data-ttu-id="b6bf3-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b6bf3-145">System.Boolean</span></span>

## <span data-ttu-id="b6bf3-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6bf3-146">NOTES</span></span>

<span data-ttu-id="b6bf3-147">별칭</span><span class="sxs-lookup"><span data-stu-id="b6bf3-147">ALIASES</span></span>

<span data-ttu-id="b6bf3-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b6bf3-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b6bf3-149">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6bf3-150">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b6bf3-151">INPUTOBJECT: <IDesktopVirtualizationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b6bf3-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b6bf3-152">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="b6bf3-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b6bf3-153">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="b6bf3-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b6bf3-154">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내에서 데스크톱의 이름</span><span class="sxs-lookup"><span data-stu-id="b6bf3-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b6bf3-155">`[HostPoolName <String>]`: 지정된 리소스 그룹 내에서 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="b6bf3-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b6bf3-156">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="b6bf3-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b6bf3-157">`[MsixPackageFullName <String>]`: 지정된 호스트 풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="b6bf3-157">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="b6bf3-158">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b6bf3-159">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="b6bf3-160">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="b6bf3-160">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b6bf3-161">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b6bf3-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b6bf3-162">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="b6bf3-162">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b6bf3-163">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="b6bf3-163">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b6bf3-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6bf3-164">RELATED LINKS</span></span>

