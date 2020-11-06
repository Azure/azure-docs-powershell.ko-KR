---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmContext.md
ms.openlocfilehash: 8bc129ddc1b4291ea7b3c9100a964bf5bb1dcee6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537043"
---
# <span data-ttu-id="e1564-101">Remove-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="e1564-101">Remove-AzureRmContext</span></span>

## <span data-ttu-id="e1564-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1564-102">SYNOPSIS</span></span>
<span data-ttu-id="e1564-103">사용 가능한 컨텍스트 집합에서 컨텍스트 제거</span><span class="sxs-lookup"><span data-stu-id="e1564-103">Remove a context from the set of available contexts</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1564-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e1564-104">SYNTAX</span></span>

### <span data-ttu-id="e1564-105">입력 개체 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e1564-105">Input Object (Default)</span></span>
```
Remove-AzureRmContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1564-106">명명 된 컨텍스트</span><span class="sxs-lookup"><span data-stu-id="e1564-106">Named Context</span></span>
```
Remove-AzureRmContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="e1564-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e1564-107">DESCRIPTION</span></span>
<span data-ttu-id="e1564-108">컨텍스트 집합에서 azure 컨텍스트 제거</span><span class="sxs-lookup"><span data-stu-id="e1564-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="e1564-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e1564-109">EXAMPLES</span></span>

### <span data-ttu-id="e1564-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e1564-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmContext -Name Default
```

<span data-ttu-id="e1564-111">Default 라는 컨텍스트 제거</span><span class="sxs-lookup"><span data-stu-id="e1564-111">Remove the context named default</span></span>

## <span data-ttu-id="e1564-112">변수</span><span class="sxs-lookup"><span data-stu-id="e1564-112">PARAMETERS</span></span>

### <span data-ttu-id="e1564-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1564-113">-DefaultProfile</span></span>
<span data-ttu-id="e1564-114">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1564-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1564-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e1564-115">-Force</span></span>
<span data-ttu-id="e1564-116">Defualt 경우에도 컨텍스트 제거</span><span class="sxs-lookup"><span data-stu-id="e1564-116">Remove context even if it is the defualt</span></span>

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

### <span data-ttu-id="e1564-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1564-117">-InputObject</span></span>
<span data-ttu-id="e1564-118">일반적으로 파이프라인을 통해 전달 되는 컨텍스트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e1564-118">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="e1564-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e1564-119">-Name</span></span>
<span data-ttu-id="e1564-120">컨텍스트 이름</span><span class="sxs-lookup"><span data-stu-id="e1564-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: Named Context
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1564-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1564-121">-PassThru</span></span>
<span data-ttu-id="e1564-122">제거 된 컨텍스트 반환</span><span class="sxs-lookup"><span data-stu-id="e1564-122">Return the removed context</span></span>

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

### <span data-ttu-id="e1564-123">-범위</span><span class="sxs-lookup"><span data-stu-id="e1564-123">-Scope</span></span>
<span data-ttu-id="e1564-124">컨텍스트 변경의 범위 (예: wheher 변경 내용이 cusrrent 프로세스 또는이 사용자가 시작한 모든 세션에만 적용 됨)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1564-124">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="e1564-125">-확인</span><span class="sxs-lookup"><span data-stu-id="e1564-125">-Confirm</span></span>
<span data-ttu-id="e1564-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1564-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1564-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1564-127">-WhatIf</span></span>
<span data-ttu-id="e1564-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e1564-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1564-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1564-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1564-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1564-130">CommonParameters</span></span>
<span data-ttu-id="e1564-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1564-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1564-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1564-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1564-133">입력</span><span class="sxs-lookup"><span data-stu-id="e1564-133">INPUTS</span></span>

### <span data-ttu-id="e1564-134">않아야</span><span class="sxs-lookup"><span data-stu-id="e1564-134">None</span></span>

## <span data-ttu-id="e1564-135">출력</span><span class="sxs-lookup"><span data-stu-id="e1564-135">OUTPUTS</span></span>

### <span data-ttu-id="e1564-136">Microsoft. Azure. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="e1564-136">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="e1564-137">상속자</span><span class="sxs-lookup"><span data-stu-id="e1564-137">NOTES</span></span>

## <span data-ttu-id="e1564-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1564-138">RELATED LINKS</span></span>

