---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: ee581528810663d09fe724f370b681ff9e20072f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342597"
---
# <span data-ttu-id="2698d-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="2698d-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="2698d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2698d-102">SYNOPSIS</span></span>
<span data-ttu-id="2698d-103">컴퓨터에서 모든 AzureRm 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2698d-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="2698d-104">구문</span><span class="sxs-lookup"><span data-stu-id="2698d-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2698d-105">설명</span><span class="sxs-lookup"><span data-stu-id="2698d-105">DESCRIPTION</span></span>
<span data-ttu-id="2698d-106">컴퓨터에서 모든 AzureRm 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2698d-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="2698d-107">예제</span><span class="sxs-lookup"><span data-stu-id="2698d-107">EXAMPLES</span></span>

### <span data-ttu-id="2698d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2698d-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="2698d-109">이 명령을 실행하면 cmdlet이 실행되는 PowerShell 버전에 대한 컴퓨터에서 모든 AzureRm 모듈이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="2698d-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="2698d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2698d-110">PARAMETERS</span></span>

### <span data-ttu-id="2698d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2698d-111">-DefaultProfile</span></span>
<span data-ttu-id="2698d-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2698d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2698d-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2698d-113">-PassThru</span></span>
<span data-ttu-id="2698d-114">지정된 경우 제거된 모듈 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2698d-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="2698d-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2698d-115">-Confirm</span></span>
<span data-ttu-id="2698d-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2698d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2698d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2698d-117">-WhatIf</span></span>
<span data-ttu-id="2698d-118">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2698d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2698d-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2698d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2698d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2698d-120">CommonParameters</span></span>
<span data-ttu-id="2698d-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2698d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2698d-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2698d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2698d-123">입력</span><span class="sxs-lookup"><span data-stu-id="2698d-123">INPUTS</span></span>

### <span data-ttu-id="2698d-124">없음</span><span class="sxs-lookup"><span data-stu-id="2698d-124">None</span></span>

## <span data-ttu-id="2698d-125">출력</span><span class="sxs-lookup"><span data-stu-id="2698d-125">OUTPUTS</span></span>

### <span data-ttu-id="2698d-126">System.String</span><span class="sxs-lookup"><span data-stu-id="2698d-126">System.String</span></span>

## <span data-ttu-id="2698d-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2698d-127">NOTES</span></span>

## <span data-ttu-id="2698d-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2698d-128">RELATED LINKS</span></span>
