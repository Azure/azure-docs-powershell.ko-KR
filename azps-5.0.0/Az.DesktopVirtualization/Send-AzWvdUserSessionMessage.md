---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 047ede26246c31b17fbeb49fca4353b2cb17594c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304718"
---
# <span data-ttu-id="53f53-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="53f53-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="53f53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53f53-102">SYNOPSIS</span></span>
<span data-ttu-id="53f53-103">사용자에 게 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-103">Send a message to a user.</span></span>

## <span data-ttu-id="53f53-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53f53-104">SYNTAX</span></span>

### <span data-ttu-id="53f53-105">SendExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="53f53-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="53f53-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="53f53-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="53f53-107">설명은</span><span class="sxs-lookup"><span data-stu-id="53f53-107">DESCRIPTION</span></span>
<span data-ttu-id="53f53-108">사용자에 게 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-108">Send a message to a user.</span></span>

## <span data-ttu-id="53f53-109">예제의</span><span class="sxs-lookup"><span data-stu-id="53f53-109">EXAMPLES</span></span>

### <span data-ttu-id="53f53-110">예제 1: UserSession에 메시지 보내기</span><span class="sxs-lookup"><span data-stu-id="53f53-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="53f53-111">이 명령은 UserSession에 메시지를 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="53f53-112">변수</span><span class="sxs-lookup"><span data-stu-id="53f53-112">PARAMETERS</span></span>

### <span data-ttu-id="53f53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f53-113">-DefaultProfile</span></span>
<span data-ttu-id="53f53-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53f53-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="53f53-115">-HostPoolName</span></span>
<span data-ttu-id="53f53-116">지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-116">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="53f53-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53f53-117">-InputObject</span></span>
<span data-ttu-id="53f53-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="53f53-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="53f53-119">-MessageBody</span></span>
<span data-ttu-id="53f53-120">메시지 본문</span><span class="sxs-lookup"><span data-stu-id="53f53-120">Body of message.</span></span>

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

### <span data-ttu-id="53f53-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="53f53-121">-MessageTitle</span></span>
<span data-ttu-id="53f53-122">메시지의 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-122">Title of message.</span></span>

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

### <span data-ttu-id="53f53-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53f53-123">-PassThru</span></span>
<span data-ttu-id="53f53-124">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="53f53-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53f53-125">-ResourceGroupName</span></span>
<span data-ttu-id="53f53-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-126">The name of the resource group.</span></span>
<span data-ttu-id="53f53-127">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="53f53-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="53f53-128">-SessionHostName</span></span>
<span data-ttu-id="53f53-129">지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="53f53-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="53f53-130">-SubscriptionId</span></span>
<span data-ttu-id="53f53-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="53f53-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="53f53-132">-UserSessionId</span></span>
<span data-ttu-id="53f53-133">지정 된 세션 호스트 내의 사용자 세션 이름</span><span class="sxs-lookup"><span data-stu-id="53f53-133">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="53f53-134">-확인</span><span class="sxs-lookup"><span data-stu-id="53f53-134">-Confirm</span></span>
<span data-ttu-id="53f53-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53f53-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53f53-136">-WhatIf</span></span>
<span data-ttu-id="53f53-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53f53-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53f53-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f53-139">CommonParameters</span></span>
<span data-ttu-id="53f53-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f53-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="53f53-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f53-142">입력</span><span class="sxs-lookup"><span data-stu-id="53f53-142">INPUTS</span></span>

### <span data-ttu-id="53f53-143">IDesktopVirtualizationIdentity (Microsoft. PowerShell.)</span><span class="sxs-lookup"><span data-stu-id="53f53-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="53f53-144">출력</span><span class="sxs-lookup"><span data-stu-id="53f53-144">OUTPUTS</span></span>

### <span data-ttu-id="53f53-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="53f53-145">System.Boolean</span></span>

## <span data-ttu-id="53f53-146">상속자</span><span class="sxs-lookup"><span data-stu-id="53f53-146">NOTES</span></span>

<span data-ttu-id="53f53-147">별칭과</span><span class="sxs-lookup"><span data-stu-id="53f53-147">ALIASES</span></span>

<span data-ttu-id="53f53-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="53f53-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="53f53-149">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="53f53-150">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="53f53-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="53f53-151">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="53f53-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="53f53-152">`[ApplicationGroupName <String>]`: 응용 프로그램 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="53f53-153">`[ApplicationName <String>]`: 지정 된 응용 프로그램 그룹 내 응용 프로그램의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="53f53-154">`[DesktopName <String>]`: 지정 된 데스크톱 그룹 내의 데스크톱 이름</span><span class="sxs-lookup"><span data-stu-id="53f53-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="53f53-155">`[HostPoolName <String>]`: 지정 된 리소스 그룹 내에 있는 호스트 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="53f53-156">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="53f53-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="53f53-157">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="53f53-158">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="53f53-159">`[SessionHostName <String>]`: 지정 된 호스트 풀 내에 있는 세션 호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-159">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="53f53-160">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="53f53-161">`[UserSessionId <String>]`: 지정 된 세션 호스트 내에 있는 사용자 세션의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="53f53-161">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="53f53-162">`[WorkspaceName <String>]`: 작업 영역의 이름</span><span class="sxs-lookup"><span data-stu-id="53f53-162">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="53f53-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53f53-163">RELATED LINKS</span></span>

