---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 5aeb8d7ba44f07519ff3cdfdc5e775687bd98260
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369482"
---
# <span data-ttu-id="e1d61-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="e1d61-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="e1d61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1d61-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d61-103">실행 명령 문서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e1d61-103">Get a run command document.</span></span>

## <span data-ttu-id="e1d61-104">구문</span><span class="sxs-lookup"><span data-stu-id="e1d61-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1d61-105">설명</span><span class="sxs-lookup"><span data-stu-id="e1d61-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d61-106">실행 명령 문서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e1d61-106">Get a run command document.</span></span>

## <span data-ttu-id="e1d61-107">예제</span><span class="sxs-lookup"><span data-stu-id="e1d61-107">EXAMPLES</span></span>

### <span data-ttu-id="e1d61-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e1d61-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="e1d61-109">'westus'에서 'RunPowerShellScript'에 대한 특정 실행 명령 문서를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e1d61-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="e1d61-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="e1d61-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="e1d61-111">'westus'에서 사용 가능한 모든 실행 명령을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e1d61-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="e1d61-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1d61-112">PARAMETERS</span></span>

### <span data-ttu-id="e1d61-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="e1d61-113">-CommandId</span></span>
<span data-ttu-id="e1d61-114">명령 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e1d61-114">The command ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d61-115">-DefaultProfile</span></span>
<span data-ttu-id="e1d61-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1d61-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1d61-117">-Location</span><span class="sxs-lookup"><span data-stu-id="e1d61-117">-Location</span></span>
<span data-ttu-id="e1d61-118">실행 명령이 검색되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e1d61-118">The location upon which run commands are queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d61-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d61-119">CommonParameters</span></span>
<span data-ttu-id="e1d61-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e1d61-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d61-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e1d61-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d61-122">입력</span><span class="sxs-lookup"><span data-stu-id="e1d61-122">INPUTS</span></span>

### <span data-ttu-id="e1d61-123">System.String</span><span class="sxs-lookup"><span data-stu-id="e1d61-123">System.String</span></span>

## <span data-ttu-id="e1d61-124">출력</span><span class="sxs-lookup"><span data-stu-id="e1d61-124">OUTPUTS</span></span>

### <span data-ttu-id="e1d61-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="e1d61-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="e1d61-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e1d61-126">NOTES</span></span>

## <span data-ttu-id="e1d61-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1d61-127">RELATED LINKS</span></span>
