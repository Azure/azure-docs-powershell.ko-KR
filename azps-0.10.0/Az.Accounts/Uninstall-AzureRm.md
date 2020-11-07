---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: da9fa6503e76d9af8efbdff84ebbcdd501d8232d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875259"
---
# <span data-ttu-id="943b2-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="943b2-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="943b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="943b2-102">SYNOPSIS</span></span>
<span data-ttu-id="943b2-103">컴퓨터에서 모든 AzureRm 모듈을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="943b2-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="943b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="943b2-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="943b2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="943b2-105">DESCRIPTION</span></span>
<span data-ttu-id="943b2-106">컴퓨터에서 모든 AzureRm 모듈을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="943b2-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="943b2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="943b2-107">EXAMPLES</span></span>

### <span data-ttu-id="943b2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="943b2-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="943b2-109">이 명령을 실행 하면 cmdlet이 실행 되는 PowerShell 버전에 대 한 컴퓨터에서 모든 AzureRm 모듈이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="943b2-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="943b2-110">변수</span><span class="sxs-lookup"><span data-stu-id="943b2-110">PARAMETERS</span></span>

### <span data-ttu-id="943b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="943b2-111">-DefaultProfile</span></span>
<span data-ttu-id="943b2-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="943b2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="943b2-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="943b2-113">-PassThru</span></span>
<span data-ttu-id="943b2-114">지정 된 경우 제거한 모듈의 반환 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="943b2-114">Return list of Modules removed if specified.</span></span>

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

### <span data-ttu-id="943b2-115">-확인</span><span class="sxs-lookup"><span data-stu-id="943b2-115">-Confirm</span></span>
<span data-ttu-id="943b2-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="943b2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="943b2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="943b2-117">-WhatIf</span></span>
<span data-ttu-id="943b2-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="943b2-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="943b2-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="943b2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="943b2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="943b2-120">CommonParameters</span></span>
<span data-ttu-id="943b2-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="943b2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="943b2-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="943b2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="943b2-123">입력</span><span class="sxs-lookup"><span data-stu-id="943b2-123">INPUTS</span></span>

### <span data-ttu-id="943b2-124">않아야</span><span class="sxs-lookup"><span data-stu-id="943b2-124">None</span></span>

## <span data-ttu-id="943b2-125">출력</span><span class="sxs-lookup"><span data-stu-id="943b2-125">OUTPUTS</span></span>

### <span data-ttu-id="943b2-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="943b2-126">System.String</span></span>

## <span data-ttu-id="943b2-127">상속자</span><span class="sxs-lookup"><span data-stu-id="943b2-127">NOTES</span></span>

## <span data-ttu-id="943b2-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="943b2-128">RELATED LINKS</span></span>
