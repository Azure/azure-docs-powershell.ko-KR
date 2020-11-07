---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: d2e495b58e68232bf20bd309d06207cd45cd427e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698222"
---
# <span data-ttu-id="54248-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="54248-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="54248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54248-102">SYNOPSIS</span></span>
<span data-ttu-id="54248-103">컴퓨터에서 모든 AzureRm 모듈을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="54248-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="54248-104">구문과</span><span class="sxs-lookup"><span data-stu-id="54248-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54248-105">설명은</span><span class="sxs-lookup"><span data-stu-id="54248-105">DESCRIPTION</span></span>
<span data-ttu-id="54248-106">컴퓨터에서 모든 AzureRm 모듈을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="54248-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="54248-107">예제의</span><span class="sxs-lookup"><span data-stu-id="54248-107">EXAMPLES</span></span>

### <span data-ttu-id="54248-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="54248-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="54248-109">이 명령을 실행 하면 cmdlet이 실행 되는 PowerShell 버전에 대 한 컴퓨터에서 모든 AzureRm 모듈이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="54248-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="54248-110">변수</span><span class="sxs-lookup"><span data-stu-id="54248-110">PARAMETERS</span></span>

### <span data-ttu-id="54248-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54248-111">-DefaultProfile</span></span>
<span data-ttu-id="54248-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="54248-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54248-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54248-113">-PassThru</span></span>
<span data-ttu-id="54248-114">지정 된 경우 제거한 모듈의 반환 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="54248-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="54248-115">-확인</span><span class="sxs-lookup"><span data-stu-id="54248-115">-Confirm</span></span>
<span data-ttu-id="54248-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="54248-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54248-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54248-117">-WhatIf</span></span>
<span data-ttu-id="54248-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="54248-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54248-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="54248-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54248-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54248-120">CommonParameters</span></span>
<span data-ttu-id="54248-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="54248-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54248-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54248-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54248-123">입력</span><span class="sxs-lookup"><span data-stu-id="54248-123">INPUTS</span></span>

### <span data-ttu-id="54248-124">않아야</span><span class="sxs-lookup"><span data-stu-id="54248-124">None</span></span>

## <span data-ttu-id="54248-125">출력</span><span class="sxs-lookup"><span data-stu-id="54248-125">OUTPUTS</span></span>

### <span data-ttu-id="54248-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="54248-126">System.String</span></span>

## <span data-ttu-id="54248-127">상속자</span><span class="sxs-lookup"><span data-stu-id="54248-127">NOTES</span></span>

## <span data-ttu-id="54248-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="54248-128">RELATED LINKS</span></span>
