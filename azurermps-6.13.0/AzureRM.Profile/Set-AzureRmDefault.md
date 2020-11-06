---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmDefault.md
ms.openlocfilehash: 2836445eabc4b3986a548adf7013ceaa7e75dc4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532380"
---
# <span data-ttu-id="a7542-101">Set-AzureRmDefault</span><span class="sxs-lookup"><span data-stu-id="a7542-101">Set-AzureRmDefault</span></span>

## <span data-ttu-id="a7542-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7542-102">SYNOPSIS</span></span>
<span data-ttu-id="a7542-103">현재 컨텍스트에서 기본값을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7542-103">Sets a default in the current context</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7542-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7542-104">SYNTAX</span></span>

```
Set-AzureRmDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7542-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a7542-105">DESCRIPTION</span></span>
<span data-ttu-id="a7542-106">Set-AzureRmDefault cmdlet은 현재 컨텍스트의 기본값을 추가 하거나 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7542-106">The Set-AzureRmDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="a7542-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a7542-107">EXAMPLES</span></span>

### <span data-ttu-id="a7542-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a7542-108">Example 1</span></span>
```
PS C:\> Set-AzureRmDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="a7542-109">이 명령은 기본 리소스 그룹을 사용자가 지정한 리소스 그룹으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7542-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="a7542-110">변수</span><span class="sxs-lookup"><span data-stu-id="a7542-110">PARAMETERS</span></span>

### <span data-ttu-id="a7542-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7542-111">-DefaultProfile</span></span>
<span data-ttu-id="a7542-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7542-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7542-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a7542-113">-Force</span></span>
<span data-ttu-id="a7542-114">지정 된 기본값이 없는 경우 새 리소스 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="a7542-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="a7542-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7542-115">-ResourceGroupName</span></span>
<span data-ttu-id="a7542-116">기본값으로 설정 되는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7542-116">Name of the resource group being set as default</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7542-117">-범위</span><span class="sxs-lookup"><span data-stu-id="a7542-117">-Scope</span></span>
<span data-ttu-id="a7542-118">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7542-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="a7542-119">-확인</span><span class="sxs-lookup"><span data-stu-id="a7542-119">-Confirm</span></span>
<span data-ttu-id="a7542-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7542-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7542-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7542-121">-WhatIf</span></span>
<span data-ttu-id="a7542-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a7542-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7542-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7542-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7542-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7542-124">CommonParameters</span></span>
<span data-ttu-id="a7542-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7542-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7542-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7542-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7542-127">입력</span><span class="sxs-lookup"><span data-stu-id="a7542-127">INPUTS</span></span>

### <span data-ttu-id="a7542-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a7542-128">System.String</span></span>

## <span data-ttu-id="a7542-129">출력</span><span class="sxs-lookup"><span data-stu-id="a7542-129">OUTPUTS</span></span>

### <span data-ttu-id="a7542-130">Microsoft. Azure. PSResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a7542-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="a7542-131">상속자</span><span class="sxs-lookup"><span data-stu-id="a7542-131">NOTES</span></span>

## <span data-ttu-id="a7542-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7542-132">RELATED LINKS</span></span>
