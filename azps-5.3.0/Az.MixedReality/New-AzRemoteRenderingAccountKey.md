---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: be0e79bbc6d1cd9c2a356852e2d9dea83439d25f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492280"
---
# <span data-ttu-id="6f244-101">New-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="6f244-101">New-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="6f244-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f244-102">SYNOPSIS</span></span>
<span data-ttu-id="6f244-103">원격 렌더링 계정의 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="6f244-103">Regenerate key of Remote Rendering Account</span></span>

## <span data-ttu-id="6f244-104">구문</span><span class="sxs-lookup"><span data-stu-id="6f244-104">SYNTAX</span></span>

### <span data-ttu-id="6f244-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f244-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f244-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f244-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f244-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f244-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f244-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f244-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f244-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f244-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f244-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f244-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f244-111">설명</span><span class="sxs-lookup"><span data-stu-id="6f244-111">DESCRIPTION</span></span>
<span data-ttu-id="6f244-112">원격 렌더링 계정의 기본 키 또는 보조 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6f244-112">Regenerate primary key or secondary key of Remote Rendering Account.</span></span>

## <span data-ttu-id="6f244-113">예제</span><span class="sxs-lookup"><span data-stu-id="6f244-113">EXAMPLES</span></span>

### <span data-ttu-id="6f244-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="6f244-114">Example 1</span></span>
```powershell
PS C:\> New-AzRemoteRenderingAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="6f244-115">리소스 그룹 "rg1"에서 원격 렌더링 계정 "example"의 보조 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6f244-115">Regenerate secondary key of Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="6f244-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="6f244-116">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | New-AzRemoteRenderingAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="6f244-117">현재 구독에서 원격 렌더링 계정 "example"의 보조 키를 다시 생성하고 파이핑을 사용하여 리소스 그룹 "rg1"을 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6f244-117">Regenerate secondary key of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="6f244-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f244-118">PARAMETERS</span></span>

### <span data-ttu-id="6f244-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f244-119">-DefaultProfile</span></span>
<span data-ttu-id="6f244-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f244-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6f244-121">-Force</span></span>
<span data-ttu-id="6f244-122">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="6f244-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6f244-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f244-123">-InputObject</span></span>
<span data-ttu-id="6f244-124">사용자 지정 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6f244-124">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6f244-125">-Name</span></span>
<span data-ttu-id="6f244-126">원격 렌더링 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f244-126">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="6f244-127">-Primary</span></span>
<span data-ttu-id="6f244-128">원격 렌더링 계정의 기본 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6f244-128">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f244-129">-ResourceGroupName</span></span>
<span data-ttu-id="6f244-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f244-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f244-131">-ResourceId</span></span>
<span data-ttu-id="6f244-132">원격 렌더링 계정의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6f244-132">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-133">-Secondary</span><span class="sxs-lookup"><span data-stu-id="6f244-133">-Secondary</span></span>
<span data-ttu-id="6f244-134">원격 렌더링 계정의 기본 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6f244-134">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f244-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f244-135">-Confirm</span></span>
<span data-ttu-id="6f244-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f244-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f244-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f244-137">-WhatIf</span></span>
<span data-ttu-id="6f244-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6f244-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f244-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f244-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f244-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f244-140">CommonParameters</span></span>
<span data-ttu-id="6f244-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6f244-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6f244-142">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6f244-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f244-143">입력</span><span class="sxs-lookup"><span data-stu-id="6f244-143">INPUTS</span></span>

### <span data-ttu-id="6f244-144">System.String</span><span class="sxs-lookup"><span data-stu-id="6f244-144">System.String</span></span>

### <span data-ttu-id="6f244-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="6f244-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="6f244-146">출력</span><span class="sxs-lookup"><span data-stu-id="6f244-146">OUTPUTS</span></span>

### <span data-ttu-id="6f244-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6f244-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="6f244-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6f244-148">NOTES</span></span>

## <span data-ttu-id="6f244-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f244-149">RELATED LINKS</span></span>
