---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Rename-AzureRmContext.md
ms.openlocfilehash: 9c9c0c3c52f610c0bb2c0198e9995cf2804b2b24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711518"
---
# <span data-ttu-id="4ec05-101">Rename-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="4ec05-101">Rename-AzureRmContext</span></span>

## <span data-ttu-id="4ec05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ec05-102">SYNOPSIS</span></span>
<span data-ttu-id="4ec05-103">Azure 컨텍스트의 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="4ec05-103">Rename an Azure context.</span></span>  <span data-ttu-id="4ec05-104">기본적으로 컨텍스트는 사용자 계정과 구독으로 명명 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ec05-104">By default contexts are named by user account and subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ec05-105">구문과</span><span class="sxs-lookup"><span data-stu-id="4ec05-105">SYNTAX</span></span>

### <span data-ttu-id="4ec05-106">입력 개체 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4ec05-106">Input Object (Default)</span></span>
```
Rename-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="4ec05-107">컨텍스트 이름</span><span class="sxs-lookup"><span data-stu-id="4ec05-107">Context Name</span></span>
```
Rename-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="4ec05-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4ec05-108">DESCRIPTION</span></span>
<span data-ttu-id="4ec05-109">Azure 컨텍스트의 이름을 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="4ec05-109">Rename an Azure context.</span></span>  <span data-ttu-id="4ec05-110">기본적으로 컨텍스트는 사용자 계정과 구독으로 명명 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ec05-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="4ec05-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4ec05-111">EXAMPLES</span></span>

### <span data-ttu-id="4ec05-112">명명 된 매개 변수를 사용 하 여 컨텍스트 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="4ec05-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzureRmContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="4ec05-113">' user1@contoso.org 12345-6789-2345-3567890 ' 구독을 사용 하 여 ' ' 작업 '에 대 한 컨텍스트의 이름을 ' Work '로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="4ec05-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="4ec05-114">이 명령 다음에는 ' AzureRmContext 작업 '을 사용 하 여 컨텍스트를 대상으로 지정할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ec05-114">After this command, you will be able to target the context using 'Select-AzureRmContext Work'.</span></span>  <span data-ttu-id="4ec05-115">탭 완료를 사용 하 여 ' SourceName '에 대 한 값을 tab으로 이동할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ec05-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="4ec05-116">위치 매개 변수를 사용 하 여 컨텍스트 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="4ec05-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzureRmContext "My context" "Work"
```

<span data-ttu-id="4ec05-117">"내 컨텍스트" 라는 컨텍스트의 이름을 "Work"로 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="4ec05-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="4ec05-118">이 명령 다음에 Select-AzureRmContext 작업을 사용 하 여 컨텍스트를 대상으로 지정할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ec05-118">After this command, you will be able to target the context using Select-AzureRmContext Work</span></span>

## <span data-ttu-id="4ec05-119">변수</span><span class="sxs-lookup"><span data-stu-id="4ec05-119">PARAMETERS</span></span>

### <span data-ttu-id="4ec05-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ec05-120">-DefaultProfile</span></span>
<span data-ttu-id="4ec05-121">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4ec05-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ec05-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4ec05-122">-Force</span></span>
<span data-ttu-id="4ec05-123">대상 컨텍스트가 이미 있는 경우에도 컨텍스트 이름 바꾸기</span><span class="sxs-lookup"><span data-stu-id="4ec05-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="4ec05-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ec05-124">-InputObject</span></span>
<span data-ttu-id="4ec05-125">일반적으로 파이프라인을 통해 전달 되는 컨텍스트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec05-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Input Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ec05-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ec05-126">-PassThru</span></span>
<span data-ttu-id="4ec05-127">이름을 바꾼 컨텍스트를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ec05-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="4ec05-128">-범위</span><span class="sxs-lookup"><span data-stu-id="4ec05-128">-Scope</span></span>
<span data-ttu-id="4ec05-129">컨텍스트 변경의 범위 (예: wheher 변경 내용이 cusrrent 프로세스 또는이 사용자가 시작한 모든 세션에만 적용 됨)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ec05-129">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="4ec05-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="4ec05-130">-SourceName</span></span>
<span data-ttu-id="4ec05-131">컨텍스트 이름</span><span class="sxs-lookup"><span data-stu-id="4ec05-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Context Name
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ec05-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="4ec05-132">-TargetName</span></span>
<span data-ttu-id="4ec05-133">컨텍스트의 새 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ec05-133">The new name of the context</span></span>

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

### <span data-ttu-id="4ec05-134">-확인</span><span class="sxs-lookup"><span data-stu-id="4ec05-134">-Confirm</span></span>
<span data-ttu-id="4ec05-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ec05-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ec05-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ec05-136">-WhatIf</span></span>
<span data-ttu-id="4ec05-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4ec05-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ec05-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ec05-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ec05-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ec05-139">CommonParameters</span></span>
<span data-ttu-id="4ec05-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ec05-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ec05-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ec05-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ec05-142">입력</span><span class="sxs-lookup"><span data-stu-id="4ec05-142">INPUTS</span></span>

### <span data-ttu-id="4ec05-143">않아야</span><span class="sxs-lookup"><span data-stu-id="4ec05-143">None</span></span>

## <span data-ttu-id="4ec05-144">출력</span><span class="sxs-lookup"><span data-stu-id="4ec05-144">OUTPUTS</span></span>

### <span data-ttu-id="4ec05-145">Microsoft. Azure. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="4ec05-145">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="4ec05-146">상속자</span><span class="sxs-lookup"><span data-stu-id="4ec05-146">NOTES</span></span>

## <span data-ttu-id="4ec05-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ec05-147">RELATED LINKS</span></span>

