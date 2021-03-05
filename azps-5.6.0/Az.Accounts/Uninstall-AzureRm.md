---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: 796690bd0a5774e488b978003c48b02eedaac190
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967088"
---
# <span data-ttu-id="49a5b-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="49a5b-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="49a5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="49a5b-103">컴퓨터에서 모든 AzureRm 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="49a5b-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="49a5b-104">구문</span><span class="sxs-lookup"><span data-stu-id="49a5b-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49a5b-105">설명</span><span class="sxs-lookup"><span data-stu-id="49a5b-105">DESCRIPTION</span></span>
<span data-ttu-id="49a5b-106">컴퓨터에서 모든 AzureRm 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="49a5b-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="49a5b-107">예제</span><span class="sxs-lookup"><span data-stu-id="49a5b-107">EXAMPLES</span></span>

### <span data-ttu-id="49a5b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="49a5b-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="49a5b-109">이 명령을 실행하면 cmdlet이 실행되는 PowerShell 버전에 대한 컴퓨터에서 모든 AzureRm 모듈이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="49a5b-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="49a5b-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="49a5b-110">PARAMETERS</span></span>

### <span data-ttu-id="49a5b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a5b-111">-DefaultProfile</span></span>
<span data-ttu-id="49a5b-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49a5b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49a5b-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49a5b-113">-PassThru</span></span>
<span data-ttu-id="49a5b-114">지정된 경우 제거된 모듈 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="49a5b-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="49a5b-115">-확인</span><span class="sxs-lookup"><span data-stu-id="49a5b-115">-Confirm</span></span>
<span data-ttu-id="49a5b-116">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="49a5b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49a5b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49a5b-117">-WhatIf</span></span>
<span data-ttu-id="49a5b-118">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="49a5b-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49a5b-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49a5b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49a5b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a5b-120">CommonParameters</span></span>
<span data-ttu-id="49a5b-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="49a5b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a5b-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49a5b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a5b-123">입력</span><span class="sxs-lookup"><span data-stu-id="49a5b-123">INPUTS</span></span>

### <span data-ttu-id="49a5b-124">없음</span><span class="sxs-lookup"><span data-stu-id="49a5b-124">None</span></span>

## <span data-ttu-id="49a5b-125">출력</span><span class="sxs-lookup"><span data-stu-id="49a5b-125">OUTPUTS</span></span>

### <span data-ttu-id="49a5b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="49a5b-126">System.String</span></span>

## <span data-ttu-id="49a5b-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="49a5b-127">NOTES</span></span>

## <span data-ttu-id="49a5b-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49a5b-128">RELATED LINKS</span></span>
