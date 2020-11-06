---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/rename-azurermcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: aea1fac4450a8625eb3d31e9f951a465344a3bd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530129"
---
# <span data-ttu-id="c5be7-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="c5be7-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="c5be7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5be7-102">SYNOPSIS</span></span>
<span data-ttu-id="c5be7-103">Azure 컨텍스트의 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c5be7-103">Rename an Azure context.</span></span>  <span data-ttu-id="c5be7-104">기본적으로 컨텍스트는 사용자 계정과 구독으로 명명 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5be7-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5be7-105">구문과</span><span class="sxs-lookup"><span data-stu-id="c5be7-105">SYNTAX</span></span>

### <span data-ttu-id="c5be7-106">RenameByInputObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="c5be7-106">RenameByInputObject (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="c5be7-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="c5be7-107">RenameByName</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="c5be7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c5be7-108">DESCRIPTION</span></span>
<span data-ttu-id="c5be7-109">Azure 컨텍스트의 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c5be7-109">Rename an Azure context.</span></span>  <span data-ttu-id="c5be7-110">기본적으로 컨텍스트는 사용자 계정과 구독으로 명명 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5be7-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="c5be7-111">예제의</span><span class="sxs-lookup"><span data-stu-id="c5be7-111">EXAMPLES</span></span>

### <span data-ttu-id="c5be7-112">명명 된 매개 변수를 사용 하 여 컨텍스트 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="c5be7-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="c5be7-113">' user1@contoso.org 12345-6789-2345-3567890 ' 구독을 사용 하 여 ' ' 작업 '에 대 한 컨텍스트의 이름을 ' Work '로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c5be7-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="c5be7-114">이 명령 다음에는 ' AzureRmContext 작업 '을 사용 하 여 컨텍스트를 대상으로 지정할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5be7-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="c5be7-115">탭 완료를 사용 하 여 ' SourceName '에 대 한 값을 tab으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5be7-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="c5be7-116">위치 매개 변수를 사용 하 여 컨텍스트 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="c5be7-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="c5be7-117">"내 컨텍스트" 라는 컨텍스트의 이름을 "Work"로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="c5be7-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="c5be7-118">이 명령 다음에 Select-AzureRmContext 작업을 사용 하 여 컨텍스트를 대상으로 지정할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5be7-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="c5be7-119">변수</span><span class="sxs-lookup"><span data-stu-id="c5be7-119">PARAMETERS</span></span>

### <span data-ttu-id="c5be7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5be7-120">-DefaultProfile</span></span>
<span data-ttu-id="c5be7-121">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c5be7-121">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5be7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c5be7-122">-Force</span></span>
<span data-ttu-id="c5be7-123">대상 컨텍스트가 이미 있는 경우에도 컨텍스트 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="c5be7-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="c5be7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5be7-124">-InputObject</span></span>
<span data-ttu-id="c5be7-125">일반적으로 파이프라인을 통해 전달 되는 컨텍스트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c5be7-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: RenameByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5be7-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5be7-126">-PassThru</span></span>
<span data-ttu-id="c5be7-127">이름을 바꾼 컨텍스트를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5be7-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="c5be7-128">-범위</span><span class="sxs-lookup"><span data-stu-id="c5be7-128">-Scope</span></span>
<span data-ttu-id="c5be7-129">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5be7-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5be7-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="c5be7-130">-SourceName</span></span>
<span data-ttu-id="c5be7-131">컨텍스트 이름</span><span class="sxs-lookup"><span data-stu-id="c5be7-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RenameByName
Aliases:
Accepted values: Default

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5be7-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="c5be7-132">-TargetName</span></span>
<span data-ttu-id="c5be7-133">컨텍스트의 새 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5be7-133">The new name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5be7-134">-확인</span><span class="sxs-lookup"><span data-stu-id="c5be7-134">-Confirm</span></span>
<span data-ttu-id="c5be7-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5be7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5be7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5be7-136">-WhatIf</span></span>
<span data-ttu-id="c5be7-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c5be7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5be7-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5be7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5be7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5be7-139">CommonParameters</span></span>
<span data-ttu-id="c5be7-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5be7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5be7-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5be7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5be7-142">입력</span><span class="sxs-lookup"><span data-stu-id="c5be7-142">INPUTS</span></span>

### <span data-ttu-id="c5be7-143">Microsoft. Azure. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="c5be7-143">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="c5be7-144">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c5be7-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c5be7-145">출력</span><span class="sxs-lookup"><span data-stu-id="c5be7-145">OUTPUTS</span></span>

### <span data-ttu-id="c5be7-146">Microsoft. Azure. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="c5be7-146">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="c5be7-147">상속자</span><span class="sxs-lookup"><span data-stu-id="c5be7-147">NOTES</span></span>

## <span data-ttu-id="c5be7-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5be7-148">RELATED LINKS</span></span>
