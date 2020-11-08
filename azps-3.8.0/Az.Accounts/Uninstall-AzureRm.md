---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: ee581528810663d09fe724f370b681ff9e20072f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041987"
---
# <span data-ttu-id="ffab7-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="ffab7-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="ffab7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffab7-102">SYNOPSIS</span></span>
<span data-ttu-id="ffab7-103">컴퓨터에서 모든 AzureRm 모듈을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffab7-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="ffab7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ffab7-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ffab7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ffab7-105">DESCRIPTION</span></span>
<span data-ttu-id="ffab7-106">컴퓨터에서 모든 AzureRm 모듈을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffab7-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="ffab7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ffab7-107">EXAMPLES</span></span>

### <span data-ttu-id="ffab7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ffab7-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="ffab7-109">이 명령을 실행 하면 cmdlet이 실행 되는 PowerShell 버전에 대 한 컴퓨터에서 모든 AzureRm 모듈이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffab7-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="ffab7-110">변수</span><span class="sxs-lookup"><span data-stu-id="ffab7-110">PARAMETERS</span></span>

### <span data-ttu-id="ffab7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffab7-111">-DefaultProfile</span></span>
<span data-ttu-id="ffab7-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ffab7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffab7-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ffab7-113">-PassThru</span></span>
<span data-ttu-id="ffab7-114">지정 된 경우 제거한 모듈의 반환 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ffab7-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="ffab7-115">-확인</span><span class="sxs-lookup"><span data-stu-id="ffab7-115">-Confirm</span></span>
<span data-ttu-id="ffab7-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffab7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffab7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffab7-117">-WhatIf</span></span>
<span data-ttu-id="ffab7-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ffab7-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffab7-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffab7-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffab7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffab7-120">CommonParameters</span></span>
<span data-ttu-id="ffab7-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffab7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffab7-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffab7-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffab7-123">입력</span><span class="sxs-lookup"><span data-stu-id="ffab7-123">INPUTS</span></span>

### <span data-ttu-id="ffab7-124">않아야</span><span class="sxs-lookup"><span data-stu-id="ffab7-124">None</span></span>

## <span data-ttu-id="ffab7-125">출력</span><span class="sxs-lookup"><span data-stu-id="ffab7-125">OUTPUTS</span></span>

### <span data-ttu-id="ffab7-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ffab7-126">System.String</span></span>

## <span data-ttu-id="ffab7-127">상속자</span><span class="sxs-lookup"><span data-stu-id="ffab7-127">NOTES</span></span>

## <span data-ttu-id="ffab7-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ffab7-128">RELATED LINKS</span></span>
