---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
ms.openlocfilehash: c421489490dcd579384b211619180209e9d71f5d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536532"
---
# <span data-ttu-id="7b7ff-101">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="7b7ff-101">Disable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="7b7ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b7ff-102">SYNOPSIS</span></span>
<span data-ttu-id="7b7ff-103">Autosaving Azure 자격 증명을 끄십시오.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="7b7ff-104">다음에 PowerShell 창을 열 때 로그인 정보가 기억나지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b7ff-105">구문과</span><span class="sxs-lookup"><span data-stu-id="7b7ff-105">SYNTAX</span></span>

```
Disable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b7ff-106">설명은</span><span class="sxs-lookup"><span data-stu-id="7b7ff-106">DESCRIPTION</span></span>
<span data-ttu-id="7b7ff-107">Autosaving Azure 자격 증명을 끄십시오.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="7b7ff-108">다음에 PowerShell 창을 열 때 로그인 정보가 기억나지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="7b7ff-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7b7ff-109">EXAMPLES</span></span>

### <span data-ttu-id="7b7ff-110">컨텍스트 autosaving 비활성화</span><span class="sxs-lookup"><span data-stu-id="7b7ff-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzureRmContextAutosave
```

<span data-ttu-id="7b7ff-111">현재 사용자에 대해 자동 저장을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="7b7ff-112">변수</span><span class="sxs-lookup"><span data-stu-id="7b7ff-112">PARAMETERS</span></span>

### <span data-ttu-id="7b7ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b7ff-113">-DefaultProfile</span></span>
<span data-ttu-id="7b7ff-114">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7b7ff-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b7ff-115">-범위</span><span class="sxs-lookup"><span data-stu-id="7b7ff-115">-Scope</span></span>
<span data-ttu-id="7b7ff-116">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="7b7ff-117">-확인</span><span class="sxs-lookup"><span data-stu-id="7b7ff-117">-Confirm</span></span>
<span data-ttu-id="7b7ff-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b7ff-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b7ff-119">-WhatIf</span></span>
<span data-ttu-id="7b7ff-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b7ff-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b7ff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b7ff-122">CommonParameters</span></span>
<span data-ttu-id="7b7ff-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b7ff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b7ff-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b7ff-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b7ff-125">입력</span><span class="sxs-lookup"><span data-stu-id="7b7ff-125">INPUTS</span></span>

### <span data-ttu-id="7b7ff-126">않아야</span><span class="sxs-lookup"><span data-stu-id="7b7ff-126">None</span></span>

## <span data-ttu-id="7b7ff-127">출력</span><span class="sxs-lookup"><span data-stu-id="7b7ff-127">OUTPUTS</span></span>

### <span data-ttu-id="7b7ff-128">Microsoft. Azure. Common. 인증. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="7b7ff-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="7b7ff-129">상속자</span><span class="sxs-lookup"><span data-stu-id="7b7ff-129">NOTES</span></span>

## <span data-ttu-id="7b7ff-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b7ff-130">RELATED LINKS</span></span>
