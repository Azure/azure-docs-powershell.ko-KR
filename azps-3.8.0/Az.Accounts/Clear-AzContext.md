---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: 218921922fdd7e4d695a5daeeb30a0e2dd8d1d99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043040"
---
# <span data-ttu-id="322df-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="322df-101">Clear-AzContext</span></span>

## <span data-ttu-id="322df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="322df-102">SYNOPSIS</span></span>
<span data-ttu-id="322df-103">모든 Azure 자격 증명, 계정 및 구독 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="322df-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="322df-104">구문과</span><span class="sxs-lookup"><span data-stu-id="322df-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="322df-105">설명은</span><span class="sxs-lookup"><span data-stu-id="322df-105">DESCRIPTION</span></span>
<span data-ttu-id="322df-106">모든 Azure 자격 증명, 계정 및 구독 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="322df-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="322df-107">예제의</span><span class="sxs-lookup"><span data-stu-id="322df-107">EXAMPLES</span></span>

### <span data-ttu-id="322df-108">전역 컨텍스트 지우기</span><span class="sxs-lookup"><span data-stu-id="322df-108">Clear global context</span></span>
```
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="322df-109">모든 powershell 세션에 대 한 계정, 구독 및 자격 증명 정보를 모두 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="322df-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="322df-110">변수</span><span class="sxs-lookup"><span data-stu-id="322df-110">PARAMETERS</span></span>

### <span data-ttu-id="322df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="322df-111">-DefaultProfile</span></span>
<span data-ttu-id="322df-112">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="322df-112">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="322df-113">-Force</span><span class="sxs-lookup"><span data-stu-id="322df-113">-Force</span></span>
<span data-ttu-id="322df-114">메시지를 표시 하지 않고 전역 범위에서 모든 사용자 및 그룹 삭제</span><span class="sxs-lookup"><span data-stu-id="322df-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="322df-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="322df-115">-PassThru</span></span>
<span data-ttu-id="322df-116">성공 또는 실패를 나타내는 값 반환</span><span class="sxs-lookup"><span data-stu-id="322df-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="322df-117">-범위</span><span class="sxs-lookup"><span data-stu-id="322df-117">-Scope</span></span>
<span data-ttu-id="322df-118">현재 PowerShell 세션 또는 모든 세션에 대해서만 컨텍스트를 지웁니다.</span><span class="sxs-lookup"><span data-stu-id="322df-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="322df-119">-확인</span><span class="sxs-lookup"><span data-stu-id="322df-119">-Confirm</span></span>
<span data-ttu-id="322df-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="322df-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="322df-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="322df-121">-WhatIf</span></span>
<span data-ttu-id="322df-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="322df-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="322df-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="322df-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="322df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="322df-124">CommonParameters</span></span>
<span data-ttu-id="322df-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="322df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="322df-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="322df-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="322df-127">입력</span><span class="sxs-lookup"><span data-stu-id="322df-127">INPUTS</span></span>

### <span data-ttu-id="322df-128">않아야</span><span class="sxs-lookup"><span data-stu-id="322df-128">None</span></span>

## <span data-ttu-id="322df-129">출력</span><span class="sxs-lookup"><span data-stu-id="322df-129">OUTPUTS</span></span>

### <span data-ttu-id="322df-130">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="322df-130">System.Boolean</span></span>

## <span data-ttu-id="322df-131">상속자</span><span class="sxs-lookup"><span data-stu-id="322df-131">NOTES</span></span>

## <span data-ttu-id="322df-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="322df-132">RELATED LINKS</span></span>
