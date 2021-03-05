---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 1976c5750b5372cedce8ccf237fe8a444fa1feee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966011"
---
# <span data-ttu-id="ac9fd-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="ac9fd-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="ac9fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac9fd-102">SYNOPSIS</span></span>
<span data-ttu-id="ac9fd-103">사용자에게 메시지를 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-103">Send a message to a user.</span></span>

## <span data-ttu-id="ac9fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="ac9fd-104">SYNTAX</span></span>

### <span data-ttu-id="ac9fd-105">SendExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="ac9fd-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ac9fd-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ac9fd-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac9fd-107">설명</span><span class="sxs-lookup"><span data-stu-id="ac9fd-107">DESCRIPTION</span></span>
<span data-ttu-id="ac9fd-108">사용자에게 메시지를 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-108">Send a message to a user.</span></span>

## <span data-ttu-id="ac9fd-109">예제</span><span class="sxs-lookup"><span data-stu-id="ac9fd-109">EXAMPLES</span></span>

### <span data-ttu-id="ac9fd-110">예제 1: UserSession에 메시지 보내기</span><span class="sxs-lookup"><span data-stu-id="ac9fd-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="ac9fd-111">이 명령은 UserSession에 메시지를 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="ac9fd-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ac9fd-112">PARAMETERS</span></span>

### <span data-ttu-id="ac9fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac9fd-113">-DefaultProfile</span></span>
<span data-ttu-id="ac9fd-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac9fd-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="ac9fd-115">-HostPoolName</span></span>
<span data-ttu-id="ac9fd-116">지정된 리소스 그룹 내의 호스트 풀 이름</span><span class="sxs-lookup"><span data-stu-id="ac9fd-116">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="ac9fd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac9fd-117">-InputObject</span></span>
<span data-ttu-id="ac9fd-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ac9fd-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="ac9fd-119">-MessageBody</span></span>
<span data-ttu-id="ac9fd-120">메시지 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-120">Body of message.</span></span>

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

### <span data-ttu-id="ac9fd-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="ac9fd-121">-MessageTitle</span></span>
<span data-ttu-id="ac9fd-122">메시지 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-122">Title of message.</span></span>

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

### <span data-ttu-id="ac9fd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac9fd-123">-PassThru</span></span>
<span data-ttu-id="ac9fd-124">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ac9fd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac9fd-125">-ResourceGroupName</span></span>
<span data-ttu-id="ac9fd-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-126">The name of the resource group.</span></span>
<span data-ttu-id="ac9fd-127">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ac9fd-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="ac9fd-128">-SessionHostName</span></span>
<span data-ttu-id="ac9fd-129">지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="ac9fd-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="ac9fd-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac9fd-130">-SubscriptionId</span></span>
<span data-ttu-id="ac9fd-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ac9fd-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="ac9fd-132">-UserSessionId</span></span>
<span data-ttu-id="ac9fd-133">지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="ac9fd-133">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="ac9fd-134">-확인</span><span class="sxs-lookup"><span data-stu-id="ac9fd-134">-Confirm</span></span>
<span data-ttu-id="ac9fd-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac9fd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac9fd-136">-WhatIf</span></span>
<span data-ttu-id="ac9fd-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac9fd-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac9fd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac9fd-139">CommonParameters</span></span>
<span data-ttu-id="ac9fd-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac9fd-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac9fd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac9fd-142">입력</span><span class="sxs-lookup"><span data-stu-id="ac9fd-142">INPUTS</span></span>

### <span data-ttu-id="ac9fd-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="ac9fd-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ac9fd-144">출력</span><span class="sxs-lookup"><span data-stu-id="ac9fd-144">OUTPUTS</span></span>

### <span data-ttu-id="ac9fd-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ac9fd-145">System.Boolean</span></span>

## <span data-ttu-id="ac9fd-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ac9fd-146">NOTES</span></span>

<span data-ttu-id="ac9fd-147">별칭</span><span class="sxs-lookup"><span data-stu-id="ac9fd-147">ALIASES</span></span>

<span data-ttu-id="ac9fd-148">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="ac9fd-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ac9fd-149">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac9fd-150">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ac9fd-151">INPUTOBJECT <IDesktopVirtualizationIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ac9fd-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ac9fd-152">`[ApplicationGroupName <String>]`: 애플리케이션 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="ac9fd-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ac9fd-153">`[ApplicationName <String>]`: 지정된 애플리케이션 그룹 내의 애플리케이션 이름</span><span class="sxs-lookup"><span data-stu-id="ac9fd-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ac9fd-154">`[DesktopName <String>]`: 지정된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="ac9fd-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ac9fd-155">`[HostPoolName <String>]`: 지정된 리소스 그룹 내의 호스트 풀의 이름</span><span class="sxs-lookup"><span data-stu-id="ac9fd-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ac9fd-156">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="ac9fd-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ac9fd-157">`[MsixPackageFullName <String>]`: 지정된 호스트풀 내의 MSIX 패키지의 버전별 패키지 전체 이름</span><span class="sxs-lookup"><span data-stu-id="ac9fd-157">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="ac9fd-158">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ac9fd-159">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="ac9fd-160">`[SessionHostName <String>]`: 지정된 호스트 풀 내의 세션 호스트 이름</span><span class="sxs-lookup"><span data-stu-id="ac9fd-160">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ac9fd-161">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ac9fd-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ac9fd-162">`[UserSessionId <String>]`: 지정된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="ac9fd-162">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ac9fd-163">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="ac9fd-163">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ac9fd-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac9fd-164">RELATED LINKS</span></span>

